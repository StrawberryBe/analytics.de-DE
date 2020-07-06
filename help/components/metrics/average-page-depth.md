---
title: Durchschnittliche Seitentiefe
description: Wie viele Seiten im Durchschnitt die Dimension vorhanden ist.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---


# Durchschnittliche Seitentiefe

Die Metrik &quot;Durchschnittliche Seitentiefe&quot;zeigt an, wie weit sich der Dimensionswert bei einem bestimmten Besuch befindet. Ihre Startseite würde z. B. in der Regel eine kleinere durchschnittliche Seitentiefe anzeigen als Ihre Kaufbestätigungsseite, die normalerweise bei einem Besuch weiter oben auftaucht. Diese Metrik ist hilfreich, wenn Sie verstehen möchten, wie viele Seiten in einem bestimmten Dimensionswert sich im Durchschnitt befinden. Mithilfe dieser Informationen können Sie bestimmte Seiten für neue Besucher optimieren, wenn die Seite im Durchschnitt eine niedrige Seitentiefe aufweist.

>[TIPP] Verwenden Sie diese Metrik neben einer anderen Metrik (z. B. [Besuche](visits.md)), um bessere Einblicke zu erhalten. Wenn Sie diese Metrik selbst verwenden, erhalten Sie Dimensionswerte mit abweichenden Seitentiefen, was normalerweise nicht wertvoll ist.

## Berechnung dieser Metrik

Die erste Seite eines Besuchs hat eine Seitentiefe von `0`. Die nächste Seite hat eine Seitentiefe von 1 und erhöht jede Ansicht bis zum Ende des Besuchs. Diese Metrik erhöht sich nur bei Seitenaufrufen ([`t()`](/help/implement/vars/functions/t-method.md)) und nicht bei Linktracking-Aufrufen ([`tl()`](/help/implement/vars/functions/tl-method.md)).

Fügen Sie für einen bestimmten Dimensionswert alle Seitentiefe für diesen Dimensionswert hinzu und teilen Sie ihn durch Besuche. Die resultierende Zahl ist die durchschnittliche Seitentiefe, gerundet auf die nächste Ganzzahl. Dimensionswerte mit einer durchschnittlichen Seitentiefe `0` bedeutet, dass sie häufig auf der ersten Seite des Besuchs vorkamen.

Betrachten Sie zum Beispiel den folgenden Beispielbesuch:

```text
Page1 > Page2 > Page2 > Page3 > Page4 > Page2
```

Wenn die durchschnittliche Seitentiefe für den Dimensionswert `Page2`gewünscht würde, würde sie wie folgt berechnet:

```text
If 'Count repeat instances' is enabled:
(1 + 2 + 5) / 3 = 2.67, rounded up to 3

If 'Count repeat instances' is disabled:
(1 + 4) / 2 = 2.5, rounded up to 3
```

>[!TIP]
>
>Wenn Sie die durchschnittliche Seitentiefe mit einer Dezimalstelle anzeigen möchten, erstellen Sie eine berechnete Metrik mit dieser Metrik als einziges Element in der Formel. Erhöhen Sie die Dezimalstellen in der berechneten Metrik auf die gewünschte Dezimalstelle.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die durchschnittliche Seitentiefe der gesamten Dimension und der Zähler ist die durchschnittliche Seitentiefe des Dimensionswerts. Wenn die durchschnittliche Seitentiefe der gesamten Dimension unter der durchschnittlichen Seitentiefe eines bestimmten Dimensionswerts liegt, werden Prozentsätze über 100 % angezeigt. Die Sortierung von Rangberichten nach dieser Metrik zeigt abweichende durchschnittliche Seitentiefenwerte an, was normalerweise nicht wertvoll ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie [Besuche](visits.md)zu sortieren.