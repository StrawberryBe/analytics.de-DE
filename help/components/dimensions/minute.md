---
title: Minute
description: Die Minute, in der die Metrik aufgetreten ist.
translation-type: tm+mt
source-git-commit: 2c262e5345c39a71a6a54062c607273528294b24
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# Minute

Die Dimension &quot;Minute&quot;berichtet, in welchem Moment eine bestimmte Metrik aufgetreten ist (abgerundet). Der erste Dimensionswert ist die erste Minute im Datumsbereich und der letzte Dimensionswert die letzte Minute im Datumsbereich. Diese Dimension ist für Trendberichte nützlich, da sie Ihnen die Anzeige von Metriken im Zeitverlauf ermöglicht. Angesichts der Granularität dieser Dimension empfiehlt Adobe, den Datumsbereich des Berichte auf ein oder zwei Tage zu begrenzen.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionswerte

Dimensionswerte beinhalten eine bestimmte Minute innerhalb des Datumsbereichs eines Berichts neben dem Datum. Es ist formatiert wie `HH:MM YYYY-MM-DD`. Dimensionswerte, die an diesem Tag mit `00:00` Gleichung zu Mitternacht beginnen, während Werte, die mit 23:59 für diesen Tag beginnen, `23:59` gleich sind.
