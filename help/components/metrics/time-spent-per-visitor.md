---
title: Zeit pro Besucher (Sekunden)
description: null
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 6%

---


# Zeit pro Besucher (Sekunden)

Die Metrik &quot;Besuchszeit pro Besucher (Sekunden)&quot;zeigt die durchschnittliche Zeit an, die Besucher während der gesamten Lebensdauer eines Besuchers mit einem bestimmten Dimensionselement interagieren.

Diese Metrik ist aufgrund ihrer unterschiedlichen Verarbeitungsarchitektur nicht in Data warehouse verfügbar.

## Berechnung dieser Metrik

Diese Metrik verwendet die Formel [`Total seconds spent`](total-seconds-spent.md) `divided by` [`Unique visitors`](unique-visitors.md).

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die gesamte Besuchszeit der Dimension pro Besucher und der Zähler ist die Besuchszeit des Dimensionselements pro Besucher. Wenn die gesamte Besuchszeit der Dimension pro Besucher niedriger ist als die Besuchszeit eines bestimmten Dimensionselements pro Besucher, werden Prozentsätze über 100 % angezeigt. Die Sortierung von Rangberichten nach dieser Metrik zeigt die anormale Besuchszeit pro Besucher an, was normalerweise nicht wertvoll ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie [Besuche](visits.md)zu sortieren.

Allgemeine Informationen zur Besuchszeit finden Sie unter Übersicht über die [Besuchszeit](time-spent.md) .
