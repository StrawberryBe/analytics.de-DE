---
title: Browserhöhe - Zusammengefasst
description: Die Höhe des Browser-Fensters in Pixel.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Browserhöhe

Die Dimension &quot;Browserhöhe - Zusammengefasst&quot;zeigt die Höhe des Browser-Fensters, die in Gruppen von 100 Pixeln klassifiziert ist. Diese Dimension ist nützlich, wenn Sie verstehen möchten, wo sich die Kante auf Ihrer Site für Besucher befindet. Wenn Sie wissen, wo Ihre Kante ist, können Sie Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von der Bildschirmhöhe. Die Browserhöhe ist die Anzahl der Pixel im sichtbaren Browserbereich, während die Bildschirmhöhe die Höhe des gesamten Monitors in Pixel darstellt. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```javascript
"Browser height: " + window.innerHeight + " pixels\nScreen height: " + screen.height + " pixels";
```

Die Browserhöhe ist immer kleiner oder gleich der Bildschirmhöhe, da die Browserhöhe keine Browsernavigation oder -ränder enthält.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`bh` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `window.innerHeight` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `bh` für die Zeichenfolge beim ersten Treffer jedes Besuchs einbeziehen.

Adobe behält die Browserhöhe für einen Besuch bei. Wenn die Browserhöhe während des Besuchs angepasst wird, wird die Anpassung nicht aufgezeichnet.

## Dimensionswerte

Dimensionswerte umfassen alle erfassten Browserhöhen, die in Gruppen von 100 Pixeln klassifiziert sind. Wenn die Browserhöhe eines Treffers beispielsweise `720`beträgt, wird er im Dimensionswert gruppiert `700 to 799`.
