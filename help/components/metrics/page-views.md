---
title: Seitenansichten
description: Die Häufigkeit, mit der eine Seite angezeigt wurde.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---


# Seitenansichten

Die Metrik &quot;Seitenpositionen&quot;zeigt an, wie oft ein bestimmtes Dimensionselement auf einer Ansicht festgelegt oder beibehalten wurde. Es handelt sich dabei um eine der häufigsten und grundlegendsten Metriken in Berichten.

## Berechnung dieser Metrik

Diese Metrik zählt alle Seitenverfolgungsaufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) in einer Report Suite. Bei Dimensionen sind auch Treffer enthalten, bei denen ein Dimensionselement definiert oder beibehalten wird. Es enthält keine Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Vergleichen mit ähnlichen Metriken

* **Seiten-Ansichten vs.[Besuche](visits.md)**: Seitenansichten zählen, wie oft eine Ansicht angezeigt wird. Besuche zählen die Anzahl der Sitzungen für Besucher. Ein Besuch besteht aus einer oder mehreren Seiten.
* **Seiten-Ansichten im Vergleich zu[Seiten-Ereignissen](page-events.md)**: Seitenaufrufe zählen die Anzahl der Ansichten-Verfolgungsaufrufe (`t()`) und schließen Linkverfolgungsaufrufe (`tl()`) aus. Das Gegenteil ist der Fall bei den Ereignissen der Seite. Es zählt die Anzahl der Linkverfolgungsaufrufe und schließt Seitenaufrufe aus.