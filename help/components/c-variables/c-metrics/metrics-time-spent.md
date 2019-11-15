---
description: Adobe Analytics bietet verschiedene Metriken und Dimensionen zur Besuchszeit. Erfahren Sie mehr über die Funktionsweise und die Berechnung solcher Metriken.
solution: Analytics
title: Besuchszeit
topic: Metrics
translation-type: tm+mt
source-git-commit: 6c57780d0ecf65669c1a5306dde267f6e48f1cc4

---


# Besuchszeitmetriken

Adobe Analytics bietet mehrere Möglichkeiten, die in Analytics-Berichten verbrachte Zeit zu bestimmen. In den meisten Fällen wird die Besuchszeit anhand der folgenden Schritte berechnet:

1. Sehen Sie sich für einen bestimmten Treffer den Wert für Zeitstempel und Dimension an.
1. Vergleichen Sie diesen Treffer mit dem Zeitstempel des nächsten Treffers im Besuch.
1. Die Zeit, die zwischen diesen beiden Treffern verstrichen ist, trägt zur Besuchszeit für diesen Dimensionswert bei.

Beachten Sie beim Anzeigen von Besuchszeitmetriken Folgendes:

* Die Besuchszeit berücksichtigt Zuordnung und Ablauf.
* Sowohl Seitenansichten als auch die Linktracking-Treffertypen werden bei der Berechnung der Besuchszeitdaten berücksichtigt.
* Die Besuchszeit wird beim letzten Treffer des Besuchs nicht gemessen, da keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit vorliegt.
* Absprünge können die Besuchszeit nicht messen, da der Besuch aus einem einzelnen Treffer besteht.

## Gesamtbesuchszeit in Sekunden

Die Gesamtdauer, die alle Besucher mit einem Dimensionswert interagierten, gemessen in Sekunden.

## Zeit pro Besuch (Sekunden)

Die durchschnittliche Zeit, die Besucher bei einem Besuch mit einem Dimensionswert interagieren. Die ungefähre Berechnung ist `Total seconds spent / (Visits - Bounces)`die.

## Besuchszeit pro Besucher (Sekunden)

Die durchschnittliche Zeit, die Besucher während der gesamten Lebensdauer des Besuchers mit einem Dimensionswert interagieren. Die ungefähre Berechnung ist `Total seconds spent / (Unique Visitors - Bounces)`die.

## Durchschnittliche Besuchszeit pro Site (Sekunden)

Die durchschnittliche auf Ihrer Site verbrachte Zeit, die normalerweise mit einer Datumsdimension gepaart wird. Obwohl diese Metrik in der Regel die Besuchszeit im Zeitverlauf anzeigt, kann sie auch mit Dimensionen als Alternative zur Besuchszeit pro Besuch verwendet werden. Die ungefähre Berechnung ist `Total seconds spent / (Sequences - Bounces)`die. Sequenzen sind eine Reihe von Treffern, bei denen sich der Dimensionswert nicht geändert hat.

> [!NOTE] Die Besuchszeit pro Besuch und die durchschnittliche Besuchszeit pro Site sind ähnliche Metriken. Der Unterschied zwischen diesen beiden Metriken ist ihr Nenner. Besuchszeit pro Besuch verwendet `visits - bounces`wird, während die durchschnittliche Besuchszeit pro Site verwendet `sequences - bounces`. Auf Besuchsebene erscheinen diese Metriken ähnlich, können jedoch auf Trefferebene einige Unterschiede aufweisen.

## Durchschnittliche Besuchszeit pro Seite

Nur in ReportBuilder verfügbar. In den meisten Fällen verwenden Sie stattdessen die Zeit pro Besuch.
