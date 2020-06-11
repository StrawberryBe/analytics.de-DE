---
title: Browserbreite - Zusammengefasst
description: Die Breite des Browserfensters in Pixel.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Browserbreite

Die Dimension &quot;Browserbreite - Zusammengefasst&quot;zeigt die Breite des Browserfensters, die in Gruppen von 100 Pixeln klassifiziert ist. Diese Dimension ist nützlich, wenn Sie wissen möchten, wie breit Besucher Ihren Inhalt sehen. Wenn Sie wissen, wie breit Ihre Inhalte normalerweise angezeigt werden, können Sie die Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von der Bildschirmbreite. Die Browserbreite ist die Anzahl der Pixel im sichtbaren Browserbereich, während die Bildschirmbreite die Breite des gesamten Monitors in Pixel darstellt. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```javascript
"Browser width: " + window.innerWidth + " pixels\nScreen width: " + screen.width + " pixels";
```

Die Browserbreite ist immer kleiner als oder gleich der Bildschirmbreite, da die Browserbreite keine Bildlaufleisten oder Ränder enthält.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`bw` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `window.innerWidth` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `bw` für die Zeichenfolge beim ersten Treffer jedes Besuchs einbeziehen.

Adobe behält die Browserbreite bei einem Besuch bei. Wenn die Browserbreite während des Besuchs angepasst wird, wird die Anpassung nicht aufgezeichnet.

## Dimensionswerte

Dimensionswerte umfassen alle erfassten Browserbreiten, die in Gruppen von 100 Pixeln eingeteilt werden. Wenn die Browserbreite eines Treffers beispielsweise `1280`ist, wird er im Dimensionswert gruppiert `1200 to 1299`.
