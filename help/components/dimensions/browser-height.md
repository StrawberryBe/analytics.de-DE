---
title: Browser-Höhe – zusammengefasst
description: Die Höhe des Browser-Fensters in Pixel.
feature: Dimensions
exl-id: bdfd2ef5-c200-4d6e-b478-3917fca66227
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 100%

---

# Browser-Höhe

Die Dimension „Browser-Höhe – zusammengefasst“ gibt die Höhe des Browser-Fensters an, klassifiziert in Gruppen von 100 Pixel. Diese Dimension ist nützlich, wenn Sie verstehen möchten, wo sich die Kante auf Ihrer Site für Besucher befindet. Wenn Sie wissen, wo die Kante ist, können Sie Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von der Bildschirmhöhe. Die Browser-Höhe ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmhöhe die Höhe des gesamten Monitors in Pixel darstellt. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```javascript
"Browser height: " + window.innerHeight + " pixels\nScreen height: " + screen.height + " pixels";
```

Die Browser-Höhe ist immer kleiner oder gleich der Bildschirmhöhe, da die Browser-Höhe keine Browser-Navigation oder -Ränder enthält.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`bh` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `window.innerHeight` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `bh` beim ersten Treffer jedes Besuchs einbeziehen.

Adobe behält die Browser-Höhe für einen Besuch bei. Wenn die Browser-Höhe während des Besuchs angepasst wird, wird die Anpassung nicht aufgezeichnet.

## Dimensionselemente

Zu den Dimensionselementen gehören alle erfassten Browser-Höhen, klassifiziert in Gruppen von 100 Pixel. Wenn die Browser-Höhe eines Treffers beispielsweise `720` beträgt, wird sie im Dimensionselement `700 to 799` gruppiert.
