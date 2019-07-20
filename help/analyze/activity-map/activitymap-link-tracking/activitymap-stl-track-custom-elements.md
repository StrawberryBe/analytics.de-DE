---
description: Mit der Funktion s.tl() können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalt konfigurieren.
seo-description: Mit der Funktion s.tl() können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalt konfigurieren.
seo-title: Verwenden der Funktion s. tl ()
solution: Analytics
title: Verwenden der Funktion s. tl ()
topic: Activity Map
uuid: 59 e 062 af -6 a 1 c -46 ff -9 c 3 b -6 cf 7 a 0453711
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Verwenden der Funktion s. tl ()

Mit der Funktion s.tl() können Sie benutzerdefinierte Elemente verfolgen und Überlagerungsrendering für dynamischen Inhalt konfigurieren.

## Tracking custom elements {#section_5D6688DFFFC241718249A9A0C632E465}

Durch Verwendung der [Funktion s.tl()](https://marketing.adobe.com/resources/help/en_US/sc/implement/function_tl.html) als Bestandteil des Activity Map-Moduls AppMeasurement können Sie alle Objekte verfolgen, auf die geklickt wird, sogar Objekte, die keine Anker-Tags oder Bildelemente sind. Mit s.tl können Sie benutzerdefinierte Elemente verfolgen, die nicht zum Laden einer Seite führen.

In der Funktion s.tl wird der Parameter linkName, der aktuell zum Identifizieren der Exitlinks, benutzerdefinierten Links usw. dient, jetzt auch zum Identifizieren der Link-ID für die Activity Map-Variable verwendet.

```
s.tl(this,linkType, 
<b>linkName</b>,variableOverrides,doneAction)
```

Anders gesagt, wenn Sie s.tl zur Verfolgung Ihrer spezifischen Elemente verwenden, wird die Link-ID dem Wert entnommen, der als dritter Parameter (linkName) in der Funktion s.tl übergeben wird. Sie wird nicht dem Standard-Linktracking-Algorithmus entnommen, der zur [Standardverfolgung](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md) in Activity Map verwendet wird.

## Overlay rendering for dynamic content {#section_FD24B61A732149C7B58BA957DD84A5E7}

Wenn die Funktion s.tl() direkt vom onclick-Ereignis des HTML-Elements aufgerufen wird, kann Activity Map eine Überlagerung für dieses Element anzeigen, sobald die Webseite geladen ist. Beispiel:

```
<div onclick="s.tl(this,'o','some link name')">Text to click on</a>
```

Wenn der Webseite nach dem ersten Laden Inhalt hinzugefügt wird, so wird die Funktion s.tl indirekt aufgerufen und es können keine Überlagerungen für diesen neuen Inhalt angezeigt werden, es sei denn, er wird explizit aktiviert oder angeklickt. Dann wird ein neuer Linkerfassungsprozess von Activity Map ausgelöst.

Wenn die Funktion s.tl() nicht direkt vom onclick-Ereignis eines HTML-Elements aufgerufen wird, kann Activity Map die Überlagerung erst anzeigen, nachdem der Benutzer auf dieses Element geklickt hat. In dem folgenden Beispiel wurde die Funktion s.tl() indirekt aufgerufen:

```
<div onclick="someFn(event)"></div> 
 <script>function someFn (event) 
 {    
 s.tl(event.srcElement,'o','some link name'); 
 } 
 </script>
```

Die beste Methode, wie mit Activity Map dynamische Inhaltslinks überlagert werden können, ist die Einrichtung einer benutzerdefinierten ActivityMap.link-Funktion, um dieselbe Funktion aufzurufen, deren Rückgabewert an s.tl übergeben wird. Beispiel:

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
1. Dies wird von Activity Map zur Berichtszeit aufgerufen, weshalb linkName nie übergeben wird und makeLinkName() mit dem Linkelement aufgerufen werden kann. This is the crucial step here - the “makeLinkName(element)” call should be the same at the s.tl call’s 3rd argument in the `<button>` tag. Deshalb verfolgen wird beim Aufruf von s.tl die Zeichenkette, die von makeLinkName zurückgegeben wird. Wenn Activity Map Berichte für die Links auf der Seite erstellt, wird derselbe Aufruf zur Erstellung eines Links verwendet.
1. Als endgültige Lösung wird der ursprüngliche Rückgabewert der Standard-Activity Map-Link-Funktion zurückzugeben. Durch dieses Verfahren müssen Sie nur makeLinkName überschreiben bzw. benutzerdefinierten Code dafür schreiben, und nicht einen Link-Rückgabewert für alle Links auf der Seite erstellen.
