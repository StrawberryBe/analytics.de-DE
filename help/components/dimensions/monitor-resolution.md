---
title: Bildschirmauflösung
description: Die Auflösung des Bildschirms des Besuchers in Pixel.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 1%

---


# Bildschirmauflösung

Die Dimension &quot;Bildschirmauflösung&quot;zeigt die Höhe und Breite der aktiven Anzeige in Pixel an. Diese Dimension ist nützlich, wenn Sie wissen möchten, wo sich die Kante auf Ihrer Site für Besucher befindet oder wie breit Besucher ihr Browserfenster gestalten können. Wenn Sie wissen, wo Ihre Kante ist, können Sie Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von Browserhöhe und -breite. Die Browserhöhe/-breite ist die Anzahl der Pixel im sichtbaren Browserbereich, während die Bildschirmauflösung die Anzahl der Pixel des gesamten Monitors ist. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "\nBrowser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

Browserdimensionen sind immer kleiner als die Monitorauflösung, da Browser-Dimensionen keine Browsernavigation oder -ränder enthalten.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`s` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der JavaScript-Variablen `screen.width` und `screen.height` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. beim Starten der Adobe Experience Platform), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `s` für die Zeichenfolge in Bildanforderungen einschließen.

## Dimensionselemente

Dimensionselemente umfassen alle erfassten Monitorauflösungen. Zu den Beispielwerten gehören `1920 x 1080`, `1366 x 768`und `1280 x 720`.
