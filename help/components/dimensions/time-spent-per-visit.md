---
title: Zeit pro Besuch (Dimensionen)
description: Die Gesamtdauer des Besuchs.
feature: Dimensions
exl-id: f241eb2d-7e22-47ee-ade8-8aeb7b2b9694
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 98%

---

# Zeit pro Besuch

*Auf dieser Hilfeseite wird beschrieben, wie „Zeit pro Besuch“ in ihren jeweiligen Dimensionen funktioniert. Weitere Informationen finden Sie unter der Metrik [Zeit pro Besuch](../metrics/time-spent-per-visit.md).*

Die Dimensionen „Zeit pro Besuch“ geben die Zeit an, die ein Besucher für den gesamten Besuch aufgewendet hat. Zur Berechnung werden die folgenden Schritte verwendet:

1. Sehen Sie sich den Zeitstempel des ersten Treffers des Besuchs an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des letzten Treffers des Besuchs.
3. Die Zeit, die zwischen diesen beiden Treffern verstrichen ist, zählt zur Besuchszeit.

Diese Dimensionen sind nützlich, wenn Sie verstehen möchten, wie lange Besucher mit Ihrer Site im Allgemeinen interagieren.

>[!TIP]
>
>Die Besuchszeit erfordert mindestens zwei Treffer bei einem Besuch, um die Zeit zu messen. Besuche, die aus einem einzelnen Treffer bestehen, werden nicht in dieser Dimension angezeigt.

Diese Dimension basiert auf Besuchen, d. h., der Wert gilt für jeden Treffer innerhalb des Besuchs und ändert sich nicht. Vergleichen Sie diese Dimension mit der [Besuchszeit pro Seite](time-spent-on-page.md), die einer trefferbasierten Dimension entspricht.

Diese Dimension bezieht sich auf die Metriken [Durchschnittliche Besuchszeit pro Site](../metrics/average-time-on-site.md) und [Zeit pro Besuch](../metrics/time-spent-per-visit.md).

## Füllen dieser Dimension mit Daten

Diese Dimensionen sind bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktionieren diese Dimensionen.

## Dimensionselemente

Für die Zeit pro Besuch gibt es mehrere Dimensionen:

* **Zeit pro Besuch – zusammengefasst**: Die Zeitdauer wird zusammengefasst. Dimensionselemente reichen von `"Less than 1 minute"` bis `"More than 15 hours"`. Besuche dauern in der Regel nicht länger als 12 Stunden. Besuche können jedoch 12 Stunden überschreiten, wenn Treffer mit Zeitstempel oder Datenquellen verwendet werden.
* **Zeit pro Besuch – präzise**: Jede Anzahl von Sekunden ist ein eindeutiges Dimensionselement. Diese Dimension steht in Reports &amp; Analytics oder Data Warehouse nicht zur Verfügung.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](../metrics/time-spent.md).
