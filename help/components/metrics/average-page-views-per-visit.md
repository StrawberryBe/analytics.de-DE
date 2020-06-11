---
title: Durchschnittliche Ansichten pro Besuch
description: Die durchschnittliche Häufigkeit, mit der ein bestimmter Dimensionswert bei einem Besuch angezeigt wurde.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---


# Durchschnittliche Ansichten pro Besuch

Die Dimension &quot;Durchschnittliche Ansichten pro Besuch&quot;zeigt an, wie viele Ansichten im Durchschnitt zu Ihrer gewünschten Dimension auftraten. Bei zeitbasierten Dimensionen können Sie sehen, wie die durchschnittliche Anzahl von Ansichten innerhalb eines Besuchs im Zeitverlauf tendiert. Diese Metrik ist hilfreich, wenn Sie wissen möchten, wie oft Dimensionswerte bei einem Besuch angezeigt werden.

>[TIPP] Verwenden Sie diese Metrik neben einer anderen Metrik (z. B. [Besuche](visits.md)), um bessere Einblicke zu erhalten. Wenn Sie diese Metrik selbst verwenden, erhalten Sie Dimensionswerte, die abweichende Ansichten pro Besuch enthalten. Dies ist in der Regel nicht wertvoll.

## Berechnung dieser Metrik

Diese Metrik wird mit der Formel berechnet [`Page views`](page-views.md)` divided by `[`Visits`](visits.md).

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die durchschnittliche Ansicht der Seite pro Besuch der gesamten Dimension, und der Zähler ist die durchschnittliche Ansicht des Dimensionswerts pro Besuch. Wenn die durchschnittliche Ansicht der Seite pro Besuch der gesamten Dimension unter der durchschnittlichen Ansicht der Seite pro Besuch eines bestimmten Dimensionswerts liegt, werden Prozentsätze über 100 % angezeigt. Die Sortierung von Rangberichten nach dieser Metrik zeigt abweichende durchschnittliche Seitenwerte pro Besuch an, was normalerweise nicht wertvoll ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie [Besuche](visits.md)zu sortieren.