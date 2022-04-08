---
title: Minute
description: Die Minute, in der die Metrik aufgetreten ist.
feature: Dimensions
exl-id: 63f13083-321f-4fd8-9352-e413e1ebf168
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '145'
ht-degree: 100%

---

# Minute

Die Dimension „Minute“ zeigt die Minute an, in der eine bestimmte Metrik aufgetreten ist (abgerundet). Das erste Dimensionselement ist die erste Minute im Datumsbereich und das letzte Dimensionselement die letzte Minute im Datumsbereich. Diese Dimension ist für Trend-Berichte hilfreich, da sie es Ihnen ermöglicht, Metriken im Zeitverlauf anzuzeigen. Angesichts der Granularität dieser Dimension empfiehlt Adobe, den Datumsbereich des Berichte auf ein oder zwei Tage zu begrenzen.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Die Dimensionelemente enthalten eine bestimmte Minute innerhalb des Datumsbereichs eines Berichts und deren Datum. Sie sind als `HH:MM YYYY-MM-DD` formatiert. Dimensionselemente, die mit `00:00` beginnen, entsprechen Mitternacht an diesem Tag, während Werte, die mit `23:59` beginnen, 23:59 Uhr an diesem Tag entsprechen.
