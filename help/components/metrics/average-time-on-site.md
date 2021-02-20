---
title: Durchschnittliche Besuchszeit pro Site
description: Die durchschnittliche Zeitspanne, in der ein bestimmtes Dimensionselement zwischen Treffern existierte.
translation-type: tm+mt
source-git-commit: ec93137d0b5334e312fe0ec42953457243117d4a
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 94%

---


# Durchschnittliche Besuchszeit pro Site

Die Metrik „Durchschnittliche Besuchszeit pro Site“ gibt die Zeit an, die zwischen den Treffern für ein bestimmtes Dimensionselement verstrichen ist. Diese Metrik ist hilfreich, wenn Sie die durchschnittliche Besuchszeit für bestimmte Dimensionselemente anzeigen möchten. Sie können diese Metrik auch im Zeitverlauf als Trend verfolgen, um zu sehen, wie sich die Gesamtbesuchszeit ändert. Diese Metrik wird im `HH:MM:SS`-Format angezeigt.

Diese Metrik bezieht sich auf die Dimension [Besuchszeit pro Besuch](../dimensions/time-spent-per-visit.md).

## Berechnung dieser Metrik

Nehmen Sie für ein gegebenes Dimensionselement den Zeitstempel jedes Treffers, bei dem dieses Dimensionselement existiert. Vergleichen Sie ihn mit dem Zeitstempel des nächsten Treffers im Besuch. Wenn der Treffer keinen nachfolgenden Treffer aufweist, nehmen Sie ihn nicht in diese Metrik auf. Teilen Sie von der gesamten für das Dimensionselement aufgewendeten Zeit alle durch die Anzahl der „Sequenzen“ für dieses Dimensionselement. Eine „Sequenz“ liegt vor, wenn ein Dimensionselement für einen oder mehrere aufeinander folgende Treffer dasselbe ist. Diese resultierende Zahl ist die in Berichten angezeigte Metrik.

Betrachten Sie beispielsweise den folgenden Besuch:

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


Wenn Sie die durchschnittliche Besuchszeit pro Site für das Dimensionselement `Product page A` wünschen, nehmen Sie zunächst die Zeit, die zwischen den Treffern für diese Dimension verstrichen ist:

* **12:04:20–12:05:30** – 1 Minute 10 Sekunden
* **12:05:30–12:07:00** – 1 Minute 30 Sekunden
* **12:07:40–12:08:10** – 30 Sekunden
* **12:25:40–?** - Nicht eingeschlossen

Die Gesamtbesuchszeit für `Product page A` beträgt `00:03:10`. Bei diesem Besuch gab es zwei Sequenzen: die erste Sequenz für die beiden aufeinander folgenden Werte und die zweite vor dem Checkout. Der letzte Treffer des Besuchs ist keine Sequenz, da es keinen Endzeitstempel gibt.

Die durchschnittliche Besuchszeit pro Site für `Product page A` ist `00:01:35`.

>[!NOTE]
>
>Diese Metrik zeigt den Wert `"Invalid"` an, wenn das Dimensionselement nur Treffer enthält, die zuletzt bei einem Besuch auftraten. Für diese Metrik ist ein nachfolgender Treffer erforderlich, um die Besuchszeit zu verfolgen.

## Durchschnittliche Besuchszeit pro Site (Sekunden)

Die Metrik „Durchschnittliche Besuchszeit pro Site (Sekunden)“ gibt dieselben Daten als Ganzzahl und nicht im `HH:MM:SS`-Format an. Diese Metrik ist als Komponente in berechneten Metriken am nützlichsten.

## Aufschlüsselungssummen stimmen nicht mit dem übergeordneten Zeileneintrag überein

Die Metrik „Durchschnittliche Besuchszeit pro Site“ verwendet ununterbrochene Sequenzen einer bestimmten Dimension. Die Aufschlüsselungsdimension hängt bei der Berechnung dieser Sequenzen nicht von der übergeordneten Dimension ab. Betrachten Sie beispielsweise den folgenden Besuch:

| `Timestamp` | `Page name` | `Site section` |
| --- | --- | --- |
| `12:00:00` | `Home` | `Foxes` |
| `12:00:30` | `Product` | `Foxes` |
| `12:02:10` | `Home` | `Foxes` |
| `12:02:20` | `(None; exit link click)` | `(None; exit link click)` |

Zur Berechnung der durchschnittlichen Besuchszeit pro Site für das Dimensionselement `Home` würde die folgende Berechnung verwendet:

```text
(30 + 10) / 2 = 20 seconds average time on site
```

Wenn Sie eine Aufschlüsselung mithilfe der Dimension [Website-Bereiche](../dimensions/site-section.md) vorgenommen haben, wird die folgende Berechnung verwendet:

```text
(30 + 10) / 1 = 40 seconds average time on site
```

Da es in der Aufschlüsselungsdimension eine einzelne Sequenz gab, verwendet sie einen anderen Nenner als ihre übergeordnete Dimension. Diese Metriken geben typischerweise ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber möglicherweise auf einer Trefferebene.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die durchschnittliche Besuchszeit pro Site der gesamten Dimension und der Zähler die durchschnittliche Besuchszeit pro Site des Dimensionselements. Wenn die durchschnittliche Besuchszeit pro Site der gesamten Dimension kürzer ist als die durchschnittliche Besuchszeit pro Site eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die durchschnittliche Besuchszeit pro Site angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](time-spent.md).
