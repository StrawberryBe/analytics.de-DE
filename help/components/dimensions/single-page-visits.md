---
title: Einzelseitenbesuche
description: Eine Flag, die angibt, dass der Besuch aus einer einzelnen Seite bestand.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Einzelseitenbesuche

*Auf dieser Hilfeseite wird beschrieben, wie &quot;Einzelseitenbesuche&quot;als Dimension funktioniert. Weitere Informationen finden Sie in der Metrik[Einzelseitenbesuche](../metrics/single-page-visits.md).*

Die Dimension &quot;Einzelseitenbesuche&quot;zeigt die Anzahl der Besuche an, die aus einem einzigen eindeutigen [Seitendimensionswert](page.md) bestand. Es ist die Dimensionform der Metrik [Einzelseitenbesuche](../metrics/single-page-visits.md) .

Diese Dimension wird am häufigsten als Komponente in der [Segmentierung](../c-segmentation/seg-home.md)verwendet. Es wird normalerweise nicht als Dimension in Berichten verwendet.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionswerte

Der einzige Dimensionswert ist `"Enabled"`. Wenn ein Besuch aus einer einzelnen Seite besteht, wird der Treffer auf diesen Wert gesetzt. Alle anderen Treffer werden in diesem Bericht ausgelassen.
