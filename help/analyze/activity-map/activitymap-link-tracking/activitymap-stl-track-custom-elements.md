---
title: Verwenden Sie die tl()-Methode mit Activity Map
description: Mit der Methode tl() können Sie benutzerdefinierte Elemente verfolgen und das Überlagerungsrendering für dynamische Inhalte konfigurieren.
feature: Activity Map
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 43%

---


# Verwenden Sie die `tl()`-Methode mit Activity Map

Mit der `tl()`-Methode können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalte konfigurieren.

## Benutzerdefinierte Elemente verfolgen

Durch Verwendung der [`tl()`-Methode](/help/implement/vars/functions/tl-method.md) als Bestandteil des Activity Map-Moduls AppMeasurement können Sie alle Objekte verfolgen, auf die geklickt wird, selbst Objekte, die keine Anker-Tags oder Bildelemente sind. Mit `tl()` können Sie alle benutzerspezifischen Elemente verfolgen, die nicht zum Laden der Seite führen.

In der `tl()`-Methode wird der Parameter `linkName`, der aktuell zum Identifizieren der Exitlinks, benutzerdefinierten Links usw. dient, jetzt auch zum Identifizieren der Link-ID für die Activity Map-Variable verwendet.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

Wenn Sie also `tl()` verwenden, um Ihre benutzerdefinierten Elemente zu verfolgen, wird die Link-ID aus dem Wert gezogen, der als dritter Parameter (Linkname) in der `tl()`-Methode übergeben wird. Sie wird nicht dem Standard-Linktracking-Algorithmus entnommen, der zur [Standardverfolgung](activitymap-link-tracking-methodology.md) in Activity Map verwendet wird.

## Überlagerungsrendering für dynamischen Inhalt

Wenn die `tl()`-Methode direkt vom On-Click-Ereignis des HTML-Elements aufgerufen wird, kann Activity Map beim Laden der Webseite eine Überlagerung für dieses Element anzeigen. Beispiel: 

```html
<a href="javascript:" onclick="s.tl(this,'o','Example custom link');">Example link text</a>
```

Wenn der Webseite nach dem ersten Laden Inhalt hinzugefügt wird, so wird die `tl()`-Methode indirekt aufgerufen und es können keine Überlagerungen für diesen neuen Inhalt angezeigt werden, es sei denn, er wird explizit aktiviert oder angeklickt. Dann wird ein neuer Link-Erfassungsprozess von Activity Map ausgelöst.

Wenn die `tl()`-Methode nicht direkt vom onclick-Ereignis eines HTML-Elements aufgerufen wird, kann Activity Map die Überlagerung erst anzeigen, nachdem der Benutzer auf dieses Element geklickt hat. Im folgenden Beispiel wird die `tl()`-Methode indirekt aufgerufen:

```html
<a href="javascript:" onclick="someFn(event);">Example link text</a>
<script>function someFn (event)
{
  s.tl(event.srcElement,'o','Example custom link');
}
</script>
```

Die beste Möglichkeit zum Überlagern dynamischer Inhaltslinks besteht darin, dass eine benutzerdefinierte `ActivityMap.link`-Funktion eingerichtet ist, um dieselbe Funktion aufzurufen, deren Rückgabewert an `tl()` übergeben wird. Beispiel:

```js
var originalLinkFunction = s.ActivityMap.link;
s.ActivityMap.link = function(element,linkName)
{
    // if this is a s.tl call, just return string passed
    return linkName ||      
    // this is ActivityMap reporting time
    makeLinkName(element) ||
    // our custom function didn't return anything, so just return the default ActivityMap Link
    originalLinkFunction(element,linkName);
};
```

```html
<button type="button" onclick="s.tl(this,'o',makeLinkName(this)">Add To Cart</button>
```

Hier haben wir die Funktion `ActivityMap.link` überschrieben, um bei einem Aufruf eines von drei Dingen auszuführen:

1. Wenn `linkName` übergeben wird, wurde dies von `tl()` aufgerufen, also geben Sie einfach zurück, was `tl()` als `linkName` weitergegeben wurde.
2. Wenn Activity Map zur Berichte-Zeit aufgerufen wird, wird ein `linkName` nie übergeben. Rufen Sie daher `makeLinkName()` mit dem Link-Element auf. Dies ist der entscheidende Schritt hier - der `makeLinkName(element)`-Aufruf sollte mit dem 3. Argument des `tl()`-Aufrufs im `<button>`-Tag identisch sein. Das bedeutet, dass beim Aufruf von `tl()` die von `makeLinkName()` zurückgegebene Zeichenfolge verfolgt wird. Beim Activity Map von Berichten zu den Links auf der Seite wird der gleiche Aufruf verwendet, um einen Link zu erstellen.
3. Als endgültige Lösung wird der ursprüngliche Rückgabewert der Standard-Activity Map-Link-Funktion zurückzugeben. Wenn Sie diesen Verweis so umschließen, dass er im Standardfall aufgerufen wird, müssen Sie nur benutzerdefinierten Code für `makeLinkName()` überschreiben und keinen Link-Rückgabewert für alle Links auf der Seite erstellen.
