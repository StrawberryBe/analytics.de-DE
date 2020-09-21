---
title: Einzelseitenbesuche
description: Eine Markierung, die angibt, dass der Besuch aus einer einzelnen Seite bestand.
translation-type: ht
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: ht
source-wordcount: '143'
ht-degree: 100%

---


# Einzelseitenbesuche

*Auf dieser Hilfeseite wird beschrieben, wie „Einzelseitenbesuche“ als Dimension funktioniert. Weitere Informationen finden Sie unter der Metrik [Einzelseitenbesuche](../metrics/single-page-visits.md).*

Die Dimension „Einzelseitenbesuche“ gibt die Anzahl der Besuche an, die aus einem einzigen eindeutigen Dimensionselement für [Seite](page.md) bestanden. Es handelt sich um die Dimension, die der Metrik [Einzelseitenbesuche](../metrics/single-page-visits.md) entspricht.

Diese Dimension wird am häufigsten als Komponente in der [Segmentierung](../segmentation/seg-home.md) verwendet. Sie wird normalerweise nicht als Dimension in Berichten verwendet.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Das einzige Dimensionselement ist `"Enabled"`. Wenn ein Besuch aus einer Einzelseite besteht, wird der Treffer auf diesen Wert gesetzt. Alle anderen Treffer werden in diesem Bericht ausgelassen.
