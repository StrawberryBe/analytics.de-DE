---
description: Mit der s.tl()-Methode können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalte konfigurieren.
title: s.tl()-Methode verwenden
topic: Activity map
uuid: 59e062af-6a1c-46ff-9c3b-6cf7a0453711
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 100%

---


# `tl()`-Methode verwenden

Mit der `tl()`-Methode können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalte konfigurieren.

## Benutzerdefinierte Elemente verfolgen {#section_5D6688DFFFC241718249A9A0C632E465}

Durch Verwendung der [`tl()`-Methode](/help/implement/vars/functions/tl-method.md) als Bestandteil des Activity Map-Moduls AppMeasurement können Sie alle Objekte verfolgen, auf die geklickt wird, selbst Objekte, die keine Anker-Tags oder Bildelemente sind. Mit s.tl können Sie benutzerdefinierte Elemente verfolgen, die nicht zum Laden einer Seite führen.

In der `tl()`-Methode wird der Parameter `linkName`, der aktuell zum Identifizieren der Exitlinks, benutzerdefinierten Links usw. dient, jetzt auch zum Identifizieren der Link-ID für die Activity Map-Variable verwendet.

```js
s.tl(this,linkType,linkName,variableOverrides)
```

Mit anderen Worten, wenn Sie `s.tl()` zur Verfolgung Ihrer benutzerdefinierten Elemente verwenden, wird die Link-ID dem Wert entnommen, der als dritter Parameter (linkName) in der `s.tl()`-Methode übergeben wird. Sie wird nicht dem Standard-Linktracking-Algorithmus entnommen, der zur [Standardverfolgung](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md) in Activity Map verwendet wird.

## Überlagerungsrendering für dynamischen Inhalt {#section_FD24B61A732149C7B58BA957DD84A5E7}

Wenn die Funktion s.tl() direkt vom onclick-Ereignis des HTML-Elements aufgerufen wird, kann Activity Map eine Überlagerung für dieses Element anzeigen, sobald die Webseite geladen ist. Beispiel:

```html
<div onclick="s.tl(this,'o','Example custom link')">Example link text</a>
```

Wenn der Webseite nach dem ersten Laden Inhalt hinzugefügt wird, so wird die `tl()`-Methode indirekt aufgerufen und es können keine Überlagerungen für diesen neuen Inhalt angezeigt werden, es sei denn, er wird explizit aktiviert oder angeklickt. Dann wird ein neuer Link-Erfassungsprozess von Activity Map ausgelöst.

Wenn die `tl()`-Methode nicht direkt vom onclick-Ereignis eines HTML-Elements aufgerufen wird, kann Activity Map die Überlagerung erst anzeigen, nachdem der Benutzer auf dieses Element geklickt hat. Im folgenden Beispiel wird die `tl()`-Methode indirekt aufgerufen:

```html
<div onclick="someFn(event)"></div>
<script>function someFn (event)
{
  s.tl(event.srcElement,'o','Example custom link');
}
</script>
```

Die beste Möglichkeit für Activity Map, dynamische Inhalts-Links zu überlagern, besteht darin, eine benutzerdefinierte ActivityMap.link-Funktion einzurichten, um dieselbe Funktion aufzurufen, deren Rückgabewert an `s.tl` übergeben wird. Beispiel:

```js
var originalLinkFunction = s.ActivityMap.link;
s.ActivityMap.link = function(element,linkName) {
    return linkName ||      // if this is a s.tl call, just return string passed
        makeLinkName(element) || // this is ActivityMap reporting time
        originalLinkFunction(element,linkName); // our custom function didn't return anything, so just return the default ActivityMap Link
};
```

```html
<button type="button" onclick="s.tl(this,'o',makeLinkName(this)">Add To Cart</button>
```

Wir haben die ActivityMap.link-Funktion überschrieben, damit sie eine der drei Aktionen bewirkt, wenn sie aufgerufen wird:

1. Wenn linkName übergeben wird, wird dieser von s.tl() aufgerufen, es wird also nur zurückgegeben, was s.tl als linkName übergeben hat.
2. Dies wird von Activity Map zur Berichtszeit aufgerufen, weshalb linkName nie übergeben wird und makeLinkName() mit dem Linkelement aufgerufen werden kann. Dieser Schritt hier ist ausschlaggebend: Der „makeLinkName(element)“-Aufruf sollte derselbe sein wie das dritte Argument beim s.tl-Aufruf im `<button>`-Tag. Deshalb verfolgen wird beim Aufruf von s.tl die Zeichenkette, die von makeLinkName zurückgegeben wird. Wenn Activity Map Berichte für die Links auf der Seite erstellt, wird derselbe Aufruf zur Erstellung eines Links verwendet.
3. Als endgültige Lösung wird der ursprüngliche Rückgabewert der Standard-Activity Map-Link-Funktion zurückzugeben. Durch dieses Verfahren müssen Sie nur makeLinkName überschreiben bzw. benutzerdefinierten Code dafür schreiben, und nicht einen Link-Rückgabewert für alle Links auf der Seite erstellen.
