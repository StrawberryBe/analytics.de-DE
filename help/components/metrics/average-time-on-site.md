---
title: Durchschnittliche Zeit auf der Site
description: Der durchschnittliche Zeitraum, in dem ein bestimmtes Dimensionselement zwischen Treffern vorhanden war.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 1%

---


# Durchschnittliche Zeit auf der Site

Die Metrik &quot;Durchschnittliche Besuchszeit pro Site&quot;zeigt die Zeit an, die zwischen den Treffern für ein bestimmtes Dimensionselement verstrichen ist. Diese Metrik ist hilfreich, wenn Sie die durchschnittliche Besuchszeit für bestimmte Dimensionselemente sehen möchten. Sie können diese Metrik auch im Laufe der Zeit als Trend verfolgen, um zu sehen, wie sich die Gesamtbesuchszeit ändert. Diese Metrik wird im `HH:MM:SS` Format angezeigt.

Diese Metrik bezieht sich auf die Dimension [Besuchszeit pro Besuch](../dimensions/time-spent-per-visit.md) .

## Berechnung dieser Metrik

Nehmen Sie für ein bestimmtes Dimensionselement den Zeitstempel jedes Treffers ein, bei dem dieses Dimensionselement vorhanden ist. Vergleichen Sie ihn mit dem Zeitstempel des nächsten Treffers im Besuch. Wenn der Treffer keinen nachfolgenden Treffer aufweist, nehmen Sie ihn nicht in diese Metrik auf. Teilen Sie alle für das Dimensionselement aufgewendeten Zeiträume durch die Anzahl der &quot;Sequenzen&quot;für dieses Dimensionselement. Eine &quot;Sequenz&quot;ist, wenn ein Dimensionselement bei einem oder mehreren aufeinander folgenden Treffern gleich ist. Diese Zahl ist die in Berichten angezeigte Metrik.

Betrachten Sie zum Beispiel den folgenden Besuch:

| `Timestamp` | `Page` |
| --- | --- |
| `12:03:00` | `Home page` |
| `12:04:20` | `Product page A` |
| `12:05:30` | `Product page A` |
| `12:07:00` | `Product page B` |
| `12:07:40` | `Product page A` |
| `12:08:10` | `Checkout` |
| `12:10:00` | `Purchase` |
| `12:25:00` | `Home page` |
| `12:25:40` | `Product page A` |


Wenn Sie die durchschnittliche Besuchszeit pro Site für das Dimensionselement benötigen `Product page A`, nehmen Sie zunächst die Zeit, die zwischen den Treffern für diese Dimension verstrichen wurde:

* **12:04:20 - 12:05:30** - 1 Minute 10 Sekunden
* **12:05:30 - 12:07:00** - 1 Minute 30 Sekunden
* **12:07:40 - 12:08:10** - 30 Sekunden
* **12:25:40 - ?** - Nicht eingeschlossen

Die Gesamtbesuchszeit `Product page A` beträgt `00:03:10`. Bei diesem Besuch gab es zwei Sequenzen: die erste Sequenz für die beiden aufeinander folgenden Werte und die zweite vor dem Checkout. Der letzte Treffer des Besuchs ist keine Sequenz, da kein Endzeitstempel vorhanden ist.

Die durchschnittliche Besuchszeit pro Site `Product page A` ist `00:01:35`.

## Durchschnittliche auf der Site verbrachte Zeit (Sekunden)

Die Metrik &quot;Durchschnittliche Besuchszeit pro Site (Sekunden)&quot;zeigt dieselben Daten als Ganzzahl und nicht als `HH:MM:SS` Format an. Diese Metrik ist als Komponente in berechneten Metriken am wertvollsten.

## Aufschlüsselungssummen stimmen nicht mit dem übergeordneten Zeilenelement überein

Die Metrik &quot;Durchschnittliche Besuchszeit pro Site&quot;verwendet nicht unterbrochene Sequenzen einer bestimmten Dimension. Die Aufschlüsselungsdimension ist bei der Berechnung dieser Sequenzen nicht von der übergeordneten Dimension abhängig. Betrachten Sie zum Beispiel den folgenden Besuch:

| `Timestamp` | `Page name` | `Site section` |
| --- | --- | --- |
| `12:00:00` | `Home` | `Foxes` |
| `12:00:30` | `Product` | `Foxes` |
| `12:02:10` | `Home` | `Foxes` |
| `12:02:20` | `(None; exit link click)` | `(None; exit link click)` |

Für die Berechnung der durchschnittlichen Besuchszeit pro Site für den Dimensionselement `Home` wird die folgende Berechnung verwendet:

```text
(30 + 10) / 2 = 20 seconds average time on site
```

Wenn Sie eine Aufschlüsselung unter Verwendung der Dimension &quot; [Site-Abschnitte](../dimensions/site-section.md) &quot;vorgenommen haben, wird die folgende Berechnung verwendet:

```text
(30 + 10) / 1 = 40 seconds average time on site
```

Da es in der Aufschlüsselungsdimension eine einzelne Sequenz gab, wird ein anderer Nenner verwendet als die übergeordnete Dimension. Diese Metriken liefern in der Regel ähnliche Ergebnisse auf Besuchsebene, können jedoch auf Trefferebene unterschiedlich sein.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die durchschnittliche Zeit der gesamten Dimension auf der Site, und der Zähler ist die durchschnittliche Zeit des Dimensionselements auf der Site. Wenn die durchschnittliche Besuchszeit der gesamten Dimension auf der Site unter der durchschnittlichen Besuchszeit eines Dimensionselements liegt, werden Prozentsätze über 100 % angezeigt. Die Sortierung von Rangberichten nach dieser Metrik zeigt die abweichende durchschnittliche Besuchszeit auf der Site an, was normalerweise nicht wertvoll ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie [Besuche](visits.md)zu sortieren.

Allgemeine Informationen zur Besuchszeit finden Sie unter Übersicht über die [Besuchszeit](time-spent.md) .
