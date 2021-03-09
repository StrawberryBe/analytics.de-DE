---
title: 'Erläuterung der Metrik „Seitenansichten“ | Adobe Analytics '
description: Erfahren Sie, wie die Metrik „Seitenansichten“ in Adobe Analytics funktioniert, und lernen Sie den Unterschied zwischen Seitenansichten und Seitenbesuchen kennen.
translation-type: ht
source-git-commit: c588087b949093152435967f62e43758e9e86208
workflow-type: ht
source-wordcount: '176'
ht-degree: 100%

---


# Weitere Informationen zu Seitenansichten mit Adobe Analytics

Die Metrik „Seitenansichten“ gibt an, wie oft ein bestimmtes Dimensionselement auf einer Seite festgelegt oder beibehalten wurde. Es handelt sich dabei um eine der häufigsten und grundlegendsten Metriken in Berichten.

## Berechnung dieser Metrik

Diese Metrik zählt alle Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) in einer Report Suite. Bei Dimensionen sind auch Treffer enthalten, bei denen ein Dimensionselement definiert oder beibehalten wird. Sie enthält keine Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Vergleich mit ähnlichen Metriken

* **Seitenansichten im Vergleich zu [Besuche](visits.md)**: „Seitenansichten“ zählt, wie oft eine Seite angezeigt wird. „Besuche“ zählt die Anzahl der Sitzungen für Besucher. Ein Besuch besteht aus einer oder mehreren Seiten.
* **Seitenansichten im Vergleich zu [Seitenereignisse](page-events.md)**: „Seitenansichten“ zählt die Anzahl der Seitenansicht-Tracking-Aufrufe (`t()`) und schließt Linktracking-Aufrufe (`tl()`) aus. „Seitenereignisse“ im Gegensatz dazu zählt die Anzahl der Linktracking-Aufrufe und schließt Seitenansichten aus.