---
title: Durchschnittliche Klicktiefe
description: Gibt an, bei wie vielen Seiten die Dimension im Durchschnitt vorhanden ist.
translation-type: tm+mt
source-git-commit: 226bbce18750825d459056ac2a87549614eb3c2c
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 96%

---


# Durchschnittliche Klicktiefe

Die Metrik „Durchschnittliche Klicktiefe“ gibt an, wie weit sich das Dimensionselement innerhalb eines bestimmten Besuchs befindet. Ihre Startseite würde z. B. in der Regel eine kleinere durchschnittliche Klicktiefe aufweisen als Ihre Kaufbestätigungsseite, die normalerweise später in einem Besuch aufgerufen wird. Diese Metrik ist hilfreich, wenn Sie verstehen möchten, wie viele Seiten innerhalb eines Besuchs sich ein bestimmtes Dimensionselement im Durchschnitt befindet. Mithilfe dieser Informationen können Sie bestimmte Seiten für neue Besucher optimieren, wenn die Seite im Durchschnitt eine niedrige Klicktiefe aufweist.

>[!TIP]
>
>Use this metric alongside another metric (such as [Visits](visits.md)) to obtain better insights. Wenn Sie diese Metrik allein verwenden, erhalten Sie Dimensionselemente mit anomalen Klicktiefen, was normalerweise nicht nützlich ist.

## Berechnung dieser Metrik

Die erste Seite eines Besuchs hat eine Klicktiefe von `0`. Die nächste Seite hat eine Klicktiefe von 1, usw. bis zum Ende des Besuchs. Diese Metrik erhöht sich nur bei Seitenansicht- ([`t()`](/help/implement/vars/functions/t-method.md)) und nicht bei Linktracking-Aufrufen ([`tl()`](/help/implement/vars/functions/tl-method.md)).

Fügen Sie für ein bestimmtes Dimensionselement alle Klicktiefen für dieses Dimensionselement hinzu und teilen Sie es durch Besuche. Die resultierende Zahl ist die durchschnittliche Klicktiefe, gerundet auf die nächste Ganzzahl. Wenn Dimensionselemente eine durchschnittlichen Klicktiefe von `0` haben, bedeutet das, dass sie auf der ersten Seite des Besuchs vorkamen.

Betrachten Sie beispielsweise den folgenden Besuch:

```text
Page1 > Page2 > Page2 > Page3 > Page4 > Page2
```

Wenn Sie die durchschnittliche Klicktiefe für das Dimensionselement `Page2` wünschen, würde diese wie folgt berechnet:

```text
If 'Count repeat instances' is enabled:
(1 + 2 + 5) / 3 = 2.67, rounded up to 3

If 'Count repeat instances' is disabled:
(1 + 4) / 2 = 2.5, rounded up to 3
```

>[!TIP]
>
>Wenn Sie die durchschnittliche Klicktiefe mit einer Dezimalstelle anzeigen möchten, erstellen Sie eine berechnete Metrik mit dieser Metrik als einziges Element in der Formel. Erhöhen Sie die Dezimalstellen in der berechneten Metrik auf die gewünschte Dezimalstelle.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die durchschnittliche Klicktiefe der gesamten Dimension und der Zähler die durchschnittliche Klicktiefe des Dimensionselements. Wenn die durchschnittliche Klicktiefe der gesamten Dimension kleiner ist als die durchschnittliche Klicktiefe eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die durchschnittliche Klicktiefe angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.