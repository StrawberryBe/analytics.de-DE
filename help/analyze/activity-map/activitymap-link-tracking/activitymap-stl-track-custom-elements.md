---
title: Verwenden der tl()-Methode mit Activity Map
description: Mit der tl()-Methode können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalt konfigurieren.
feature: Activity Map
role: User, Admin
exl-id: e4e32de7-0e46-413a-abc9-9707e273903d
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 43%

---

# Verwenden der `tl()`-Methode mit Activity Map

Mit der `tl()`-Methode können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalte konfigurieren.

## Benutzerdefinierte Elemente verfolgen

Durch Verwendung der [`tl()`-Methode](/help/implement/vars/functions/tl-method.md) als Bestandteil des Activity Map-Moduls AppMeasurement können Sie alle Objekte verfolgen, auf die geklickt wird, selbst Objekte, die keine Anker-Tags oder Bildelemente sind. Mit `tl()` können Sie alle benutzerdefinierten Elemente verfolgen, die nicht zum Laden einer Seite führen.

In der `tl()`-Methode wird der Parameter `linkName`, der aktuell zum Identifizieren der Exitlinks, benutzerdefinierten Links usw. dient, jetzt auch zum Identifizieren der Link-ID für die Activity Map-Variable verwendet.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

Mit anderen Worten: Wenn Sie `tl()` verwenden, um Ihre benutzerdefinierten Elemente zu verfolgen, wird die Link-ID aus dem Wert abgerufen, der als dritter Parameter (Linkname) in der `tl()`-Methode übergeben wird. Sie wird nicht dem Standard-Linktracking-Algorithmus entnommen, der zur [Standardverfolgung](activitymap-link-tracking-methodology.md) in Activity Map verwendet wird.

## Überlagerungsrendering für dynamischen Inhalt

Wenn die `tl()`-Methode direkt vom onclick-Ereignis des HTML-Elements aufgerufen wird, kann Activity Map beim Laden der Webseite eine Überlagerung für dieses Element anzeigen. Beispiel:

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

Die beste Möglichkeit für Activity Map, dynamische Inhaltslinks zu überlagern, besteht darin, eine benutzerdefinierte Funktion `ActivityMap.link` einzurichten, um dieselbe Funktion aufzurufen, deren Rückgabewert an `tl()` übergeben wird. Beispiel:

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

Hier haben wir die `ActivityMap.link`-Funktion überschrieben, um eine der drei folgenden Aktionen auszuführen:

1. Wenn `linkName` übergeben wird, wurde dies von `tl()` aufgerufen. Geben Sie also einfach das zurück, was `tl()` als `linkName` übergeben wurde.
2. Wenn das Activity Map zum Zeitpunkt der Berichterstellung aufgerufen wird, wird kein `linkName` übergeben. Rufen Sie daher `makeLinkName()` mit dem Link-Element auf. Dies ist der entscheidende Schritt hier - der `makeLinkName(element)`-Aufruf sollte mit dem dritten Argument des `tl()`-Aufrufs im Tag `<button>` übereinstimmen. Wenn `tl()` aufgerufen wird, verfolgen wir also die von `makeLinkName()` zurückgegebene Zeichenfolge. Wenn Activity Map über die Links auf der Seite berichtet, verwendet es denselben Aufruf, um einen Link zu erstellen.
3. Als endgültige Lösung wird der ursprüngliche Rückgabewert der Standard-Activity Map-Link-Funktion zurückzugeben. Wenn Sie diese Referenz so pflegen, dass im Standardfall aufgerufen wird, müssen Sie nur benutzerdefinierten Code für `makeLinkName()` überschreiben oder schreiben und keinen Link-Rückgabewert für alle Links auf der Seite erstellen.
