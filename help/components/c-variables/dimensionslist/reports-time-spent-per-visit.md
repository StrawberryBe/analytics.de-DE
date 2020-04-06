---
description: 'null'
title: Zeit pro Besuch
topic: Reports
uuid: 76441e36-b7fe-4cf3-8d72-c51d558afa13
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Zeit pro Besuch

Adobe Analytics bietet mehrere Möglichkeiten, die in Analytics-Berichten verbrachte Zeit zu bestimmen. In den meisten Fällen wird die Besuchszeit anhand der folgenden Schritte berechnet:

1. Betrachten Sie bei einem bestimmten Besuch den Zeitstempel des ersten Treffers.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des letzten Treffers des Besuchs.
3. Die Zeit, die zwischen diesen beiden Treffern verstrichen ist, entspricht der Besuchszeit.

Beachten Sie beim Anzeigen von Besuchszeit-Dimensionsdaten Folgendes:

* Sowohl Seitenansichten als auch Linktracking-Treffertypen werden bei der Berechnung der Besuchszeitdaten berücksichtigt.
* Die Besuchszeit wird beim letzten Treffer des Besuchs nicht gemessen, da keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit vorliegt.
* Absprünge können die Besuchszeit nicht messen, da der Besuch aus einem einzelnen Treffer besteht.

Die Zeit pro Besuch misst die gesamte verstrichene Zeit eines Besuchs. Es gibt separate Dimensionen zwischen **präzise** und **zusammengefasst**.

* **Präzise:** Jeder Dimensionswert entspricht einer anderen Anzahl von Sekunden, die einen Besuch ergeben.
* **Zusammengefasst:** Jeder Dimensionswert entspricht einem vordefinierten Container:
   * Weniger als 1 Minute
   * 1–5 Minuten
   * 5–10 Minuten
   * 30–60 Minuten
   * 1–2 Stunden
   * 2–5 Stunden
   * 5–10 Stunden
   * 10–15 Stunden
   * 15+ Stunden

>[!NOTE] [Besuche](../c-metrics/metrics-visit.md) enden in der Regel nach 12 Stunden Aktivität. Besuche können jedoch 12 Stunden überschreiten, wenn Treffer mit Zeitstempel oder Datenquellen verwendet werden.

Diese Dimension basiert auf Besuchen. Vergleichen Sie diese Dimension mit der [Besuchszeit pro Seite](reports-time-spent-on-page.md), die einer trefferbasierten Dimension entspricht.
