---
title: Besuchszeit pro Seite
description: Die Zeit, die ein Besucher auf der Seite verbracht hat.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 13%

---


# Besuchszeit pro Seite

Die Dimension &quot;Besuchszeit pro Seite&quot;zeichnet die Zeit auf, die ein Besucher auf der Seite verbracht hat. Zur Berechnung werden die folgenden Schritte verwendet:

1. Sehen Sie sich für einen bestimmten Treffer den Zeitstempel an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des nächsten Treffers im Besuch. Sowohl die Ansicht als auch die Linktracking-Treffer werden gezählt.
3. Die Zeit, die zwischen diesen beiden Treffern verstrichen ist, trägt zur Besuchszeit bei.

Diese Dimension ist nützlich, wenn Sie verstehen möchten, wie lange Besucher mit einer bestimmten Metrik auf Ihrer Site interagieren.

>[!TIP]
>
>Die Besuchszeit wird nicht für den letzten Treffer des Besuchs gemessen, da es keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit gibt. Dieses Konzept gilt auch für Besuche, die aus einem einzelnen Treffer (einem Absprung) bestehen.

Diese Dimension basiert auf Treffern, d. h., der Wert ist bei jedem Treffer unterschiedlich. Vergleichen Sie diese Dimension mit der [Zeit pro Besuch](time-spent-per-visit.md), die einer besuchsbasierten Dimension entspricht. Höhere Besuchszeit bedeutet, dass ein Besucher länger auf einer Seite bleibt (Treffer).

![Besuchszeit pro Seite](../metrics/assets/time-spent2.png)

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionswerte

Für die auf der Seite verbrachte Zeit gibt es mehrere Dimensionen:

* **Besuchszeit pro Seite - Zusammengefasst**: Die Zeitdauer ist festgeschrieben. Dimensionswerte reichen von `"Less than 15 seconds"` bis `"More than 30 minutes"`. Die Ansichten zwischen den Seiten dauern in der Regel nicht länger als 30 Minuten. Bei Verwendung von Treffern mit Zeitstempel oder Datenquellen kann die Ansicht zwischen den Seiten jedoch 30 Minuten überschreiten.
* **Besuchszeit pro Seite - granular**: Jede Anzahl von Sekunden ist ein eindeutiger Dimensionswert.

Allgemeine Informationen zur Besuchszeit finden Sie unter Übersicht über die [Besuchszeit](../metrics/time-spent.md) .
