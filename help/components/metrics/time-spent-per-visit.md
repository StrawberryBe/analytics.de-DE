---
title: Zeit pro Besuch (Metriken)
description: Die Zeit, die pro Besuch für das Dimensionselement verbracht wurde.
feature: Dimensions
exl-id: f241eb2d-7e22-47ee-ade8-8aeb7b2b9694
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Zeit pro Besuch (Sekunden)

*Auf dieser Hilfeseite wird beschrieben, wie „Zeit pro Besuch“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Zeit pro Besuch](../dimensions/time-spent-per-visit.md).*

Die Metrik „Zeit pro Besuch (Sekunden)“ gibt die durchschnittliche Zeit an, die Besucher während jedes Besuchs mit einem bestimmten Dimensionselement interagieren.

1. Diese Metrik ist aufgrund ihrer unterschiedlichen Verarbeitungsarchitektur nicht in Data Warehouse verfügbar.
2. Berechnung dieser Metrik
3. Diese Metrik verwendet die Formel [`[Total seconds spent]`](total-seconds-spent.md) `divided by (`[`[Visits]`](visits.md) `minus` [`[Bounces]`](bounces.md)`)`.

Vergleich mit der durchschnittlichen Besuchszeit pro Site

>Diese Metrik und die [Durchschnittliche Besuchszeit pro Site](average-time-on-site.md) sind ähnlich, weisen jedoch einige wesentliche Unterschiede auf. Beide Metriken verwenden „Gesamtbesuchszeit in Sekunden“ als Zähler. „Durchschnittliche Besuchszeit pro Site“ verwendet jedoch die Sequenzen, die ein Dimensionselement enthalten, als Nenner. „Zeit pro Besuch“ verwendet die Anzahl der Besuche als Nenner.
>
>Aus diesem Grund geben diese Metriken ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber auf einer Trefferebene.

Prozentsätze über 100 %[](time-spent-on-page.md)

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die Zeit pro Besuch der gesamten Dimension und der Zähler ist die Zeit pro Besuch des Dimensionselements. Wenn die Zeit pro Besuch der gesamten Dimension kürzer ist als die Zeit pro Besuch eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die Zeit pro Besuch angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.[](../metrics/time-spent-per-visit.md)

## Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](time-spent.md).

These dimensions work out of the box for all implementations. If a report suite contains data, these dimensions work.

## Dimension items

Multiple dimensions exist for time spent per visit:

* **Time spent per visit - bucketed**: The amount of time is bucketed. Dimension items range from `"Less than 1 minute"` to `"More than 15 hours"`. Visits typically don&#39;t last longer than 12 hours; however, visits can exceed 12 hours if using timestamped hits or data sources.
* **Time spent per visit - granular**: Each number of seconds is a unique dimension item. This dimension is not available in Reports &amp; Analytics or Data Warehouse.

See [Time spent overview](../metrics/time-spent.md) for more general information on time spent.
