---
title: Durchschnittliche Seitenansichten pro Besuch
description: Die durchschnittliche Häufigkeit, mit der ein bestimmtes Dimensionselement bei einem Besuch angezeigt wurde.
translation-type: tm+mt
source-git-commit: 226bbce18750825d459056ac2a87549614eb3c2c
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 93%

---


# Durchschnittliche Seitenansichten pro Besuch

Die Dimension „Durchschnittliche Seitenansichten pro Besuch“ gibt an, wie viele Seitenansichten durchschnittlich in Ihrer gewünschten Dimension aufgetreten sind. Bei zeitbasierten Dimensionen können Sie sehen, wie sich die durchschnittliche Anzahl der Seitenansichten innerhalb eines Besuchs im Zeitverlauf entwickelt. Diese Metrik ist hilfreich, wenn Sie wissen möchten, wie häufig Dimensionselemente bei einem Besuch angezeigt werden.

>[!TIP]
>
>Verwenden Sie diese Metrik zusammen mit einer anderen Metrik (z. B. [Besuche](visits.md)), um bessere Einblicke zu erhalten. Wenn Sie diese Metrik allein verwenden, erhalten Sie Dimensionselemente mit anomalen Seitenansichten pro Besuch, was normalerweise nicht nützlich ist.

## Berechnung dieser Metrik

Diese Metrik wird mit der Formel [`Page views`](page-views.md)` divided by `[`Visits`](visits.md) berechnet.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Im Nenner sind die durchschnittlichen Seitenansichten pro Besuch der gesamten Dimension und im Zähler die durchschnittlichen Seitenansichten pro Besuch des Dimensionselements. Wenn die durchschnittlichen Seitenansichten pro Besuch der gesamten Dimension geringer sind als die durchschnittlichen Seitenansichten pro Besuch eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für durchschnittlichen Seitenansichten pro Besuch angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.