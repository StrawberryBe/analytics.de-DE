---
title: Einzelseitenbesuche (Dimensionen)
description: Eine Markierung, die angibt, dass der Besuch aus einer einzelnen Seite bestand.
feature: Dimensions
exl-id: f7b58941-add4-4e7b-8645-a64280fd9dcb
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 97%

---

# Einzelseitenbesuche

*Auf dieser Hilfeseite wird beschrieben, wie „Einzelseitenbesuche“ als Dimension funktioniert. Weitere Informationen finden Sie unter der Metrik [Einzelseitenbesuche](../metrics/single-page-visits.md).*

Die Dimension „Einzelseitenbesuche“ gibt die Anzahl der Besuche an, die aus einem einzigen eindeutigen Dimensionselement für [Seite](page.md) bestanden. Es handelt sich um die Dimension, die der Metrik [Einzelseitenbesuche](../metrics/single-page-visits.md) entspricht.

Diese Dimension wird am häufigsten als Komponente in der [Segmentierung](../segmentation/seg-home.md) verwendet. Sie wird normalerweise nicht als Dimension in Berichten verwendet.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Das einzige Dimensionselement ist `"Enabled"`. Wenn ein Besuch aus einer Einzelseite besteht, wird der Treffer auf diesen Wert gesetzt. Alle anderen Treffer werden in diesem Bericht ausgelassen.
