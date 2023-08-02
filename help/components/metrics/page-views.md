---
title: Seitenansichten
description: Die Häufigkeit, mit der ein Dimensionselement in Adobe Analytics festgelegt oder beibehalten wurde.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 60a630c9934d613aa69523bdb87b92165a135eb9
workflow-type: ht
source-wordcount: '197'
ht-degree: 100%

---

# Seitenansichten

Die Metrik **[!UICONTROL Seitenansichten]** zeigt an, wie oft ein bestimmtes Dimensionselement (Dimensionswert) auf einer Seite definiert oder beibehalten wurde (d. h. wann es abläuft). Es handelt sich dabei um eine der häufigsten und grundlegendsten Metriken in Berichten.

Beispiel: Die Dimension [!UICONTROL Wochentage] enthält die folgenden Dimensionselemente: Sonntag, Montag, Dienstag, Mittwoch, Donnerstag, Freitag und Samstag.

## Berechnung dieser Metrik

Diese Metrik zählt alle Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) in einer Report Suite. Bei Dimensionen sind auch Treffer enthalten, bei denen ein Dimensionselement definiert oder beibehalten wird. Sie enthält keine Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) oder Daten aus der Zusammenfassung von [Datenquellen](/help/import/data-sources/overview.md).

## Vergleich mit ähnlichen Metriken

* **Seitenansichten im Vergleich zu [Besuchen](visits.md)**: „Seitenansichten“ zählt, wie oft eine Seite angezeigt wird. „Besuche“ zählt die Anzahl der Sitzungen für Besucher. Ein Besuch kann aus einer oder mehreren Seitenansichten bestehen.
* **Seitenansichten im Vergleich zu [Seitenereignissen](page-events.md)**: „Seitenansichten“ zählt die Anzahl der Seitenansicht-Tracking-Aufrufe (`t()`) und schließt Linktracking-Aufrufe (`tl()`) aus. Seitenereignisse sind das Gegenteil. Sie zählen die Anzahl der Linktracking-Aufrufe und schließen Seitenansicht-Tracking-Aufrufe aus.
