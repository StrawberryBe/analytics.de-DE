---
title: Einzelseitenbesuche
description: Eine Flag, die angibt, dass der Besuch aus einer einzelnen Seite bestand.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Einzelseitenbesuche

*Auf dieser Hilfeseite wird beschrieben, wie &quot;Einzelseitenbesuche&quot;als Dimension funktioniert. Weitere Informationen finden Sie in der Metrik[Einzelseitenbesuche](../metrics/single-page-visits.md).*

Die Dimension &quot;Einzelseitenbesuche&quot;zeigt die Anzahl der Besuche an, die aus einem einzigen Dimensionselement der [Seite](page.md) bestand. Es ist die Dimensionform der Metrik [Einzelseitenbesuche](../metrics/single-page-visits.md) .

Diese Dimension wird am häufigsten als Komponente in der [Segmentierung](../c-segmentation/seg-home.md)verwendet. Es wird normalerweise nicht als Dimension in Berichten verwendet.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Das einzige Dimensionselement ist `"Enabled"`. Wenn ein Besuch aus einer einzelnen Seite besteht, wird der Treffer auf diesen Wert gesetzt. Alle anderen Treffer werden in diesem Bericht ausgelassen.
