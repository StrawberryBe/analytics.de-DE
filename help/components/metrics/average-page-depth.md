---
title: Durchschnittliche Klicktiefe
description: Gibt an, bei wie vielen Seiten die Dimension im Durchschnitt vorhanden ist.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 59%

---


# Durchschnittliche Klicktiefe

Die Metrik &quot;Durchschnittliche Seitentiefe&quot;zeigt an, wie weit sich das Dimensionselement bei einem bestimmten Besuch befindet. Ihre Startseite würde z. B. in der Regel eine kleinere durchschnittliche Klicktiefe aufweisen als Ihre Kaufbestätigungsseite, die normalerweise später in einem Besuch aufgerufen wird. Diese Metrik ist hilfreich, wenn Sie verstehen möchten, wie viele Seiten eines Dimensionselements sich im Durchschnitt befinden. Mithilfe dieser Informationen können Sie bestimmte Seiten für neue Besucher optimieren, wenn die Seite im Durchschnitt eine niedrige Klicktiefe aufweist.

>[TIPP] Verwenden Sie diese Metrik zusammen mit einer anderen Metrik (z. B. [Besuche](visits.md)), um bessere Einblicke zu erhalten. Wenn Sie diese Metrik selbst verwenden, erhalten Sie Dimensionselemente mit abweichenden Seitentiefen, was normalerweise nicht wertvoll ist.

## Berechnung dieser Metrik

Die erste Seite eines Besuchs hat eine Klicktiefe von `0`. Die nächste Seite hat eine Klicktiefe von 1, usw. bis zum Ende des Besuchs. Diese Metrik erhöht sich nur bei Seitenansicht- ([`t()`](/help/implement/vars/functions/t-method.md)) und nicht bei Linktracking-Aufrufen ([`tl()`](/help/implement/vars/functions/tl-method.md)).

Fügen Sie für ein bestimmtes Dimensionselement alle Seitentiefe für dieses Dimensionselement hinzu und teilen Sie es durch Besuche. Die resultierende Zahl ist die durchschnittliche Klicktiefe, gerundet auf die nächste Ganzzahl. Dimension items with an average page depth of `0` means it was frequently on the first page of the visit.

Betrachten Sie beispielsweise den folgenden Besuch:

```text
Page1 > Page2 > Page2 > Page3 > Page4 > Page2
```

If we wanted average page depth for the dimension item `Page2`, it would be calculated as follows:

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

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die durchschnittliche Seitentiefe der gesamten Dimension und der Zähler ist die durchschnittliche Seitentiefe des Dimensionselements. Wenn die durchschnittliche Seitentiefe der gesamten Dimension unter der durchschnittlichen Seitentiefe eines Dimensionselements liegt, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die durchschnittliche Klicktiefe angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.