---
title: Browser-Breite – zusammengefasst
description: Die Breite des Browser-Fensters in Pixel.
feature: Dimensions
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 93%

---

# Browser-Breite

Die &quot;Browser-Breite - zusammengefasst&quot; [Dimension](overview.md) zeigt die Breite des Browser-Fensters, klassifiziert in Gruppen von 100 Pixel. Diese Dimension ist nützlich, wenn Sie wissen möchten, wie breit Besuchern Ihr Inhalt angezeigt wird. Wenn Sie wissen, wie breit Ihr Inhalt normalerweise angezeigt wird, können Sie den Inhalt für die Anzeige optimieren.

Diese Dimension unterscheidet sich von der Bildschirmbreite. Die Browser-Breite ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmbreite die Breite des gesamten Monitors in Pixel darstellt. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```javascript
"Browser width: " + window.innerWidth + " pixels\nScreen width: " + screen.width + " pixels";
```

Die Browser-Breite ist immer kleiner als oder gleich der Bildschirmbreite, da die Browser-Breite keine Bildlaufleisten oder Ränder enthält.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`bw` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `window.innerWidth` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `bw` beim ersten Treffer jedes Besuchs einbeziehen.

Adobe behält die Browser-Breite für einen Besuch bei. Wenn die Browser-Breite während des Besuchs angepasst wird, wird die Anpassung nicht aufgezeichnet.

## Dimensionselemente

Zu den Dimensionselementen gehören alle erfassten Browser-Breiten, klassifiziert in Gruppen von 100 Pixel. Wenn die Browser-Breite eines Treffers beispielsweise `1280` beträgt, wird sie im Dimensionselement `1200 to 1299` gruppiert.
