---
description: Mit der Funktion s.tl() können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalt konfigurieren.
seo-description: Mit der Funktion s.tl() können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalt konfigurieren.
seo-title: s.tl()-Funktion verwenden
solution: Analytics
title: s.tl()-Funktion verwenden
topic: Activity Map
uuid: 59e062af-6a1c-46ff-9c3b-6cf7a0453711
translation-type: tm+mt
source-git-commit: 36637b76b8026fbf87ad48adcfa47386c530e732

---


# s.tl()-Funktion verwenden

Mit der Funktion s.tl() können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalt konfigurieren.

## Tracking custom elements {#section_5D6688DFFFC241718249A9A0C632E465}

Using the [s.tl() function](https://marketing.adobe.com/resources/help/en_US/sc/implement/function_tl.html) as part of the [!DNL Activity Map] AppMeasurement module lets you track any object that is clicked on, even objects that are not anchor tags or image elements. Mit s.tl können Sie benutzerdefinierte Elemente verfolgen, die nicht zum Laden einer Seite führen.

In der Funktion s.tl wird der Parameter linkName, der aktuell zum Identifizieren der Exitlinks, benutzerdefinierten Links usw. dient, is now also used to identify the Link ID for the [!DNL Activity Map] variable.

```
s.tl(this,linkType, 
<b>linkName</b>,variableOverrides,doneAction)
```

Anders gesagt, wenn Sie s.tl zur Verfolgung Ihrer spezifischen Elemente verwenden, wird die Link-ID dem Wert entnommen, der als dritter Parameter (linkName) in der Funktion s.tl übergeben wird. It is not pulled from the standard link tracking algorithm that is used for [default tracking](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md) in [!DNL Activity Map].

## Overlay rendering for dynamic content {#section_FD24B61A732149C7B58BA957DD84A5E7}

When the s.tl() function is called directly from the HTML element’s on-click event, [!DNL Activity Map] can display an overlay for that element when the web page is loaded. Beispiel:

```
<div onclick="s.tl(this,'o','some link name')">Text to click on</a>
```

Wenn der Webseite nach dem ersten Laden Inhalt hinzugefügt wird, so wird die Funktion s.tl indirekt aufgerufen und es können keine Überlagerungen für diesen neuen Inhalt angezeigt werden, es sei denn, er wird explizit aktiviert oder angeklickt. Then a new link collection process is triggered from [!DNL Activity Map].

When the s.tl() function is not called directly from the HTML element’s on-click event, [!DNL Activity Map] can only display overlay once that element has been clicked by the user. In dem folgenden Beispiel wurde die Funktion s.tl() indirekt aufgerufen:

```
<div onclick="someFn(event)"></div> 
 <script>function someFn (event) 
 {    
 s.tl(event.srcElement,'o','some link name'); 
 } 
 </script>
```

The best way for [!DNL Activity Map] to overlay dynamic content links is to have a customized ActivityMap.link function set up to call the same function whose return value is passed to s.tl. Beispiel:

```
var originalLinkFunction = s.ActivityMap.link; 
s.ActivityMap.link = function(element,linkName){ 
    return linkName ||      // if this is a s.tl call, just return string passed 
        makeLinkName(element) || // this is ActivityMap reporting time 
        originalLinkFunction(element,linkName); // our custom function didn't return anything, so just return the default ActivityMap Link 
};
```

```
<button type=”button” onclick=”s.tl(this,’o’,makeLinkName(this)”>Add To Cart</button>
```

Wir haben die ActivityMap.link-Funktion überschrieben, damit sie eine der drei Aktionen bewirkt, wenn sie aufgerufen wird:

1. Wenn linkName übergeben wird, wird dieser von s.tl() aufgerufen, es wird also nur zurückgegeben, was s.tl als linkName übergeben hat.
1. This is called by [!DNL Activity Map] at reporting time, so a linkName is never passed, and so call makeLinkName() with the link element. This is the crucial step here - the “makeLinkName(element)” call should be the same at the s.tl call’s 3rd argument in the `<button>` tag. Deshalb verfolgen wird beim Aufruf von s.tl die Zeichenkette, die von makeLinkName zurückgegeben wird. When [!DNL Activity Map] reports on the links on the page, is uses the same call to make a link.
1. Als endgültige Lösung wird der ursprüngliche Rückgabewert der Standard-Activity Map-Link-Funktion zurückzugeben. Durch dieses Verfahren müssen Sie nur makeLinkName überschreiben bzw. benutzerdefinierten Code dafür schreiben, und nicht einen Link-Rückgabewert für alle Links auf der Seite erstellen.
