---
description: Zeigt den Zeitraum an, den Besucher auf der Seite verbringen.
title: Besuchszeit pro Seite
topic: Reports
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Besuchszeit pro Seite

Adobe Analytics bietet mehrere Möglichkeiten, die in Analytics-Berichten verbrachte Zeit zu bestimmen. In den meisten Fällen wird die Besuchszeit anhand der folgenden Schritte berechnet:

1. Sehen Sie sich für einen bestimmten Treffer den Wert für Zeitstempel und Dimension an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des nächsten Treffers im Besuch.
3. Die Zeit, die zwischen diesen beiden Treffern verstrichen ist, zählt zur Besuchszeit für diese Seite.

Beachten Sie beim Anzeigen von Besuchszeit-Dimensionsdaten Folgendes:

* Bei der Besuchszeit werden Zuordnung und Gültigkeit berücksichtigt.
* Sowohl Seitenansichten als auch Linktracking-Treffertypen werden bei der Berechnung der Besuchszeitdaten berücksichtigt.
* Die Besuchszeit wird beim letzten Treffer des Besuchs nicht gemessen, da keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit vorliegt.
* Absprünge können die Besuchszeit nicht messen, da der Besuch aus einem einzelnen Treffer besteht.

Die auf der Seite verbrachte Zeit misst die verstrichene Zeit zwischen Treffern in einem Besuch. Es gibt separate Dimensionen zwischen **präzise** und **zusammengefasst**.

* **Präzise:** Jeder Dimensionswert entspricht einer anderen Anzahl von Sekunden, die zwischen zwei Treffern verbracht wird.
* **Zusammengefasst:** Jeder Dimensionswert entspricht einem vordefinierten Container:
   * Weniger als 15 Sekunden
   * 15–29 Sekunden
   * 1–3 Minuten
   * 3–5 Minuten
   * 5–10 Minuten
   * 10–15 Minuten
   * 15–20 Minuten
   * 20–30 Minuten
   * Mehr als 30 Minuten

Diese Dimension basiert auf Treffern, die bei Verwendung als Aufschlüsselung aussagekräftigere Daten liefern können. Vergleichen Sie diese Dimension mit der [Zeit pro Besuch](reports-time-spent-per-visit.md), die einer besuchsbasierten Dimension entspricht.

![Besuchszeit](/help/components/c-variables/c-metrics/assets/time-spent1.png)
