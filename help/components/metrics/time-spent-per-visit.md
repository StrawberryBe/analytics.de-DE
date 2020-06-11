---
title: Zeit pro Besuch
description: Die Zeit, die pro Besuch für den Dimensionswert verbracht wurde.
translation-type: tm+mt
source-git-commit: 5282ad3f6fdd2853979cbfb2707cc07a698f63a7
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 3%

---


# Zeit pro Besuch (Sekunden)

*Auf dieser Hilfeseite wird beschrieben, wie &quot;Zeit pro Besuch&quot;als Metrik funktioniert. Weitere Informationen finden Sie unter[Besuchszeit](../dimensions/time-spent-per-visit.md)pro Besuch.*

Die Metrik &quot;Zeit pro Besuch (Sekunden)&quot;zeigt die durchschnittliche Zeit an, die Besucher während jedes Besuchs mit einem bestimmten Dimensionswert interagieren.

Diese Metrik ist aufgrund ihrer unterschiedlichen Verarbeitungsarchitektur nicht in Data Warehouse verfügbar.

## Berechnung dieser Metrik

Diese Metrik verwendet die Formel [`Total seconds spent`](total-seconds-spent.md) ( `divided by`[`Visits`](visits.md) `minus` [`Bounces`](bounces.md)).

## Vergleich mit der durchschnittlichen Besuchszeit auf der Site

Diese Metrik und die [durchschnittliche Besuchszeit auf der Site](average-time-on-site.md) sind ähnlich, weisen jedoch einige wesentliche Unterschiede auf. Beide Metriken verwenden &quot;Gesamtdauer in Sekunden&quot;als Zähler. &quot;Durchschnittliche Besuchszeit pro Site&quot;verwendet jedoch die Sequenzen, die ein Dimensionselement als Nenner enthalten. Die Besuchszeit pro Besuch dient als Nenner.

Daher liefern diese Metriken ähnliche Ergebnisse auf Besuchsebene, unterscheiden sich jedoch auf Trefferebene.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die gesamte Zeit, die die Dimension pro Besuch verbringt, und der Zähler ist die Zeit, die der Dimensionswert pro Besuch verbringt. Wenn die gesamte Besuchszeit der Dimension unter der Besuchszeit pro Besuch liegt, werden Prozentsätze über 100 % angezeigt. Die Sortierung von Rangberichten nach dieser Metrik zeigt die Anomalie-Besuchszeit pro Besuch an, was normalerweise nicht wertvoll ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie [Besuche](visits.md)zu sortieren.

Allgemeine Informationen zur Besuchszeit finden Sie unter Übersicht über die [Besuchszeit](time-spent.md) .
