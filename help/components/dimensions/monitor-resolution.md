---
title: Bildschirmauflösung
description: Die Auflösung des Bildschirms des Besuchers in Pixeln.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '239'
ht-degree: 100%

---


# Bildschirmauflösung

Die Dimension „Bildschirmauflösung“ zeigt die Höhe und Breite der aktiven Anzeige in Pixeln an. Diese Dimension ist nützlich, wenn Sie wissen möchten, wo sich die Kante auf Ihrer Site für Besucher befindet oder wie breit Besucher ihr Browser-Fenster gestalten können. Wenn Sie wissen, wo die Kante ist, können Sie Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von der Höhe und Breite des Browsers. Die Browserhöhe/-breite ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmauflösung die Anzahl der Pixel des gesamten Monitors ist. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "\nBrowser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

Browserdimensionen sind immer kleiner als die Bildschirmauflösung, da Browser-Dimensionen keine Browsernavigation oder Rahmen enthalten.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`s` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `screen.width` und `screen.height` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `s` bei allen Bildanforderungen einbeziehen.

## Dimensionselemente

Die Dimensionselemente umfassen alle erfassten Monitorauflösungen. Zu den Beispielwerten gehören `1920 x 1080`, `1366 x 768` und `1280 x 720`.
