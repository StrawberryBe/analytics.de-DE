---
title: Bildschirmauflösung
description: Die Auflösung des Bildschirms des Besuchers in Pixeln.
feature: Dimensions
exl-id: 6bae65eb-4546-4d07-877d-6e257fbe6cfa
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '240'
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

Diese Dimension ruft Daten aus der [`s` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `screen.width` und `screen.height` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `s` bei allen Bildanforderungen einbeziehen.

## Dimensionselemente

Die Dimensionselemente umfassen alle erfassten Monitorauflösungen. Zu den Beispielwerten gehören `1920 x 1080`, `1366 x 768` und `1280 x 720`.
