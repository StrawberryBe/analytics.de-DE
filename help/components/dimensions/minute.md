---
title: Minute
description: Die Minute, in der die Metrik aufgetreten ist.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# Minute

Die Dimension &quot;Minute&quot;berichtet, in welchem Moment eine bestimmte Metrik aufgetreten ist (abgerundet). Das erste Dimensionselement ist die erste Minute im Datumsbereich und das letzte Dimensionselement die letzte Minute im Datumsbereich. Diese Dimension ist für Trendberichte nützlich, da sie Ihnen die Anzeige von Metriken im Zeitverlauf ermöglicht. Angesichts der Granularität dieser Dimension empfiehlt Adobe, den Datumsbereich des Berichte auf ein oder zwei Tage zu begrenzen.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Dimensionselemente enthalten eine bestimmte Minute innerhalb des Datumsbereichs eines Berichts neben dem Datum. Es ist formatiert wie `HH:MM YYYY-MM-DD`. Dimensionselemente, die an diesem Tag mit `00:00` Gleichheit zu Mitternacht beginnen, während Werte, die mit 23:59 für diesen Tag beginnen, `23:59` gleich sind.
