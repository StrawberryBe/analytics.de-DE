---
title: Seitenansichten
description: Die Häufigkeit, mit der ein Dimensionselement in Adobe Analytics festgelegt oder beibehalten wurde.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 1be9a8ceb03f8102a0799f4518db35c1e8cd7b14
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 33%

---

# Seitenansichten

Die Metrik „Seitenansichten“ gibt an, wie oft ein bestimmtes Dimensionselement auf einer Seite festgelegt oder beibehalten wurde. Es handelt sich dabei um eine der häufigsten und grundlegendsten Metriken in Berichten.

## Berechnung dieser Metrik

Diese Metrik zählt alle Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) in einer Report Suite. Bei Dimensionen sind auch Treffer enthalten, bei denen ein Dimensionselement definiert oder beibehalten wird. Sie enthält keine Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) oder Daten aus der Zusammenfassung [Datenquellen](/help/import/data-sources/overview.md).

## Vergleich mit ähnlichen Metriken

* **Seitenansichten vs. [Besuche](visits.md)**: Seitenansichten zählen, wie oft eine Seite angezeigt wird. Besuche zählen die Anzahl der Sitzungen für Besucher. Ein Besuch besteht aus einem oder mehreren Seitenansichten.
* **Seitenansichten vs. [Seitenereignisse](page-events.md)**: Seitenansichten zählen die Anzahl der Seitenansichts-Tracking-Aufrufe (`t()`) und schließt Linktracking-Aufrufe (`tl()`). Seitenereignisse sind das Gegenteil; sie zählen die Anzahl der Linktracking-Aufrufe und schließen Seitenansicht-Tracking-Aufrufe aus.
