---
title: Rückkehrhäufigkeit
description: Die gebuchtete Zeitspanne zwischen dem aktuellen Besuch und dem vorherigen Besuch.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 4%

---


# Rückkehrhäufigkeit

Die Dimension &quot;Rückkehrhäufigkeit&quot;zeigt die Zeitdauer an, die zwischen Besuchen von zurückkehrenden Besuchern vergeht. Wenn ein Besucher zu Ihrer Site zurückkehrt, prüft Adobe, wie lange der vorherige Besuch zurückliegt, und fasst den Treffer in den entsprechenden Dimensionswert zusammen. Diese Dimension ist nützlich, um die Attraktivität und Relevanz Ihrer Website für Besucher im Laufe der Zeit zu messen. Es kann auch dabei helfen, die Auswirkungen des Inhalts und der Promotions Ihrer Site auf Ihre Besucher zu identifizieren.

>[!TIP]
>
>Diese Dimension umfasst keine erstmaligen Besucher.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

Die Daten für diese Dimension werden beim ersten Treffer des Besuchs festgelegt und bleiben für die gesamte Dauer des Besuchs erhalten. Der Wert kann sich während des Besuchs nicht ändern.

## Dimensionswerte

Dimensionswerte enthalten zeitbasierte Behälter, abhängig von der verstrichenen Zeit ab dem vorherigen Besuch.

* Weniger als ein Tag
* 1 bis 3 Tage
* 3 bis 7 Tage
* 7 bis 14 Tage
* 14 Tage bis 1 Monat
* Länger als 1 Monat

## Dimensionswerte werden unter Behältern außerhalb des Datumsbereichs des Projekts angezeigt.

Wenn Sie den Datumsbereich eines Projekts festlegen, wird häufig das Attribut &quot;Dimensionswerte&quot;für Besuche außerhalb des Datumsbereichs angezeigt. Ein Besucher besucht Ihre Site beispielsweise im Juli und kommt dann im September zweimal zurück. Die Dimension &quot;Rückkehrhäufigkeit&quot;für den Monat September würde einen Besuch unter &quot;Länger als 1 Monat&quot;und einen Besuch unter &quot;Weniger als 1 Tag&quot;anzeigen.