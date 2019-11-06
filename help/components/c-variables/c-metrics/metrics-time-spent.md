---
description: Adobe Analytics bietet verschiedene Metriken und Dimensionen zur Besuchszeit. Erfahren Sie mehr über die Funktionsweise und die Berechnung solcher Metriken.
solution: Analytics
title: Besuchszeit
topic: Metriken
translation-type: tm+mt
source-git-commit: ee9a6462138fe3483ca8a4ba042cb4eb39536031

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

Die durchschnittliche Besuchszeit auf Ihrer Site mit dem angegebenen Dimensionswert. Diese Metrik wird in der Regel mit einer Datumsdimension gepaart, um die über einen bestimmten Zeitraum verbrachte Zeit anzuzeigen. Die ungefähre Berechnung ist `Total seconds spent / (Sequences - Bounces)`die. Sequenzen sind eine Reihe von Treffern, bei denen sich der Dimensionswert nicht geändert hat. In den meisten Fällen verwenden Sie stattdessen die Zeit pro Besuch.

## Durchschnittliche Besuchszeit pro Seite

Nur in ReportBuilder verfügbar. In den meisten Fällen verwenden Sie stattdessen die Zeit pro Besuch.
