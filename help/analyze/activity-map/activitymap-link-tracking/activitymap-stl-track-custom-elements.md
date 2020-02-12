---
description: Mit der Methode s.tl() können Sie benutzerdefinierte Elemente verfolgen und das Überlagerungsrendering für dynamische Inhalte konfigurieren.
title: Verwenden der Methode s.tl()
topic: Activity map
uuid: 59e062af-6a1c-46ff-9c3b-6cf7a0453711
translation-type: tm+mt
source-git-commit: 290526ecc1b040f93d0734a5deaf2d79ab1bde10

---


# Use the `tl` method

You can use the `tl` method to track custom elements and to configure overlay rendering for dynamic content.

## Verfolgen von benutzerdefinierten Elementen {#section_5D6688DFFFC241718249A9A0C632E465}

Using the [`tl` method](/help/implement/vars/functions/tl-method.md) as part of the Activity Map AppMeasurement module lets you track any object that is clicked on, even objects that are not anchor tags or image elements. Mit s.tl können Sie benutzerdefinierte Elemente verfolgen, die nicht zum Laden einer Seite führen.

In the `tl` method, the `linkName` parameter that is currently used to identify the exit links, custom links, etc. jetzt auch zum Identifizieren der Link-ID für die Activity Map-Variable verwendet.

```js
s.tl(this,linkType,linkName,variableOverrides)
```

In other words, if you use `s.tl` to track your custom elements, the link ID is pulled from the value passed as the third parameter (linkName) in the `s.tl` method. Sie wird nicht dem Standard-Linktracking-Algorithmus entnommen, der zur [Standardverfolgung](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md) in Activity Map verwendet wird.

## Überlagerungsrendering für dynamischen Inhalt {#section_FD24B61A732149C7B58BA957DD84A5E7}

Wenn die Funktion s.tl() direkt vom onclick-Ereignis des HTML-Elements aufgerufen wird, kann Activity Map eine Überlagerung für dieses Element anzeigen, sobald die Webseite geladen ist. Beispiel:

```html
<div onclick="s.tl(this,'o','Example custom link')">Example link text</a>
```

Whenever any web page content is added to the page after the initial page load, the `tl` method is called indirectly and we cannot display overlays for that new content unless it is expressly activated/clicked. Dann wird ein neuer Linkerfassungsprozess von Activity Map ausgelöst.

When the `tl` method is not called directly from the HTML element&#39;s on-click event, Activity Map can only display overlay once that element has been clicked by the user. Here is an example where the `tl` method is called indirectly:

```html
<div onclick="someFn(event)"></div>
<script>function someFn (event)
{
  s.tl(event.srcElement,'o','Example custom link');
}
</script>
```

The best way for Activity Map to overlay dynamic content links is to have a customized ActivityMap.link function set up to call the same function whose return value is passed to `s.tl`. Beispiel:

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
