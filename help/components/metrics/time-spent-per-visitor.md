---
title: Besuchsdauer pro Besucher (Sekunden)
description: null
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '153'
ht-degree: 100%

---


# Besuchsdauer pro Besucher (Sekunden)

Die Metrik „Besuchsdauer pro Besucher (Sekunden)“ gibt die durchschnittliche Zeit an, die Besucher während der gesamten Lebensdauer eines Besuchers mit einem bestimmten Dimensionselement interagieren.

Diese Metrik ist aufgrund ihrer unterschiedlichen Verarbeitungsarchitektur nicht in Data Warehouse verfügbar.

## Berechnung dieser Metrik

Diese Metrik verwendet die Formel [`Total seconds spent`](total-seconds-spent.md) `divided by` [`Unique visitors`](unique-visitors.md).

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die Besuchsdauer pro Besucher der gesamten Dimension und der Zähler ist die Besuchsdauer pro Besucher des Dimensionselements. Wenn die Besuchsdauer pro Besucher der gesamten Dimension kürzer ist als die Besuchsdauer pro Besucher eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die Besuchszeit pro Besucher angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](time-spent.md).
