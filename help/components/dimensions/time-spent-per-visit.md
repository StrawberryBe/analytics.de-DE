---
title: Zeit pro Besuch
description: Die Gesamtdauer des Besuchs.
translation-type: tm+mt
source-git-commit: 52e00470df0f0c6bff84b26c1548e64ff5114fb8
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---


# Zeit pro Besuch

*Auf dieser Hilfeseite wird beschrieben, wie &quot;Zeit pro Besuch&quot;als ihre jeweiligen Dimensionen funktioniert. Weitere Informationen finden Sie in der Metrik[Besuchszeit](../metrics/time-spent-per-visit.md)pro Besuch.*

Die Dimensionen &quot;Besuchszeit pro Besuch&quot;zeichnen die Zeit auf, die ein Besucher während des gesamten Besuchs verbracht hat. Zur Berechnung werden die folgenden Schritte verwendet:

1. Sehen Sie sich den Zeitstempel des ersten Treffers des Besuchs an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des letzten Treffers des Besuchs.
3. Die Zeit, die zwischen diesen beiden Treffern verstrichen ist, trägt zur Besuchszeit bei.

Diese Dimensionen sind wertvoll, wenn Sie verstehen möchten, wie lange Besucher mit Ihrer Site im Allgemeinen interagieren.

>[!TIP] Die Besuchszeit erfordert mindestens zwei Treffer bei einem Besuch, um die Zeit zu messen. Besuche, die aus einem einzelnen Treffer bestehen, werden nicht in dieser Dimension angezeigt.

Diese Dimension basiert auf Besuchen, d. h., der Wert gilt für jeden Treffer innerhalb des Besuchs und ändert sich nicht. Vergleichen Sie diese Dimension mit der [Besuchszeit pro Seite](time-spent-on-page.md), die einer trefferbasierten Dimension entspricht.

Diese Dimension bezieht sich auf die Metriken [Durchschnittliche Besuchszeit pro Site](../metrics/average-time-on-site.md) und [Besuchszeit](../metrics/time-spent-per-visit.md) .

## Diese Dimension mit Daten füllen

Diese Dimensionen funktionieren bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktionieren diese Dimensionen.

## Dimensionswerte

Für die Zeit pro Besuch sind mehrere Dimensionen vorhanden:

* **Besuchszeit pro Besuch - Zusammengefasst**: Die Zeitdauer ist festgeschrieben. Dimensionswerte reichen von `"Less than 1 minute"` bis `"More than 15 hours"`. Besuche dauern in der Regel nicht länger als 12 Stunden; Besuche können jedoch 12 Stunden überschreiten, wenn Treffer mit Zeitstempel oder Datenquellen verwendet werden.
* **Besuchszeit pro Besuch - granular**: Jede Anzahl von Sekunden ist ein eindeutiger Dimensionswert. Diese Dimension ist in Reports &amp; Analysen oder Data Warehouse nicht verfügbar.

Allgemeine Informationen zur Besuchszeit finden Sie unter Übersicht über die [Besuchszeit](../metrics/time-spent.md) .
