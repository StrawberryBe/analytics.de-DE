---
title: Rückkehrhäufigkeit
description: Die zusammengefasste Zeitspanne zwischen dem aktuellen Besuch und dem vorherigen Besuch.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 100%

---


# Rückkehrhäufigkeit

Die Dimension „Rückkehrhäufigkeit“ gibt die Zeitspanne an, die zwischen Besuchen von wiederkehrenden Besuchern vergeht. Wenn ein Besucher zu Ihrer Site zurückkehrt, prüft Adobe, wie lange der vorherige Besuch zurückliegt, und erfasst den Treffer im entsprechenden Dimensionselement. Diese Dimension ist nützlich, um die Attraktivität und Relevanz Ihrer Website für Besucher im Zeitverlauf einzuschätzen. Sie kann auch dazu beitragen, die Auswirkungen der Inhalte und Werbeaktionen Ihrer Website auf Ihre Besucher zu ermitteln.

>[!TIP]
>
>Diese Dimension umfasst keine erstmaligen Besucher.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

Die Daten für diese Dimension werden beim ersten Treffer des Besuchs festgelegt und bleiben für die gesamte Dauer des Besuchs erhalten. Der Wert kann sich während des Besuchs nicht ändern.

## Dimensionselemente

Zu den Dimensionselementen gehören zeitbasierte Behälter, abhängig von der seit ihrem letzten Besuch verstrichenen Zeit.

* Weniger als ein Tag
* 1 bis 3 Tage
* 3 bis 7 Tage
* 7 bis 14 Tage
* 14 Tage bis 1 Monat
* Länger als 1 Monat

## Die Dimensionselemente werden unter den Behältern außerhalb des Datumsbereichs des Projekts angezeigt.

Wenn Sie den Datumsbereich eines Projekts festlegen, können Sie üblicherweise Dimensionselemente sehen, die sich auf Besuche außerhalb des Datumsbereichs beziehen. Beispiel: Ein Besucher besucht Ihre Site im Juli und zweimal an einem Tag im September. Die Dimension „Rückkehrhäufigkeit“ für den Monat September würde einen Besuch unter „Länger als 1 Monat“ und einen Besuch unter „Weniger als 1 Tag“ ausweisen.