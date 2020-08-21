---
title: Zeit vor Ereignis
description: Die Zeit zwischen der Metrik und dem ersten Treffer des Besuchs.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 78%

---


# Zeit vor Ereignis

Die Dimension „Zeit vor Ereignis“ zeigt den Zeitraum an, der zwischen dem ersten Treffer des Besuchs und der gewünschten Metrik verstrichen ist. Diese Dimension ist nützlich, um die Zeitdauer zu bestimmen, die zum Erzielen eines Erfolgsereignisses (z. B. einer Formularübermittlung oder eines Kaufs) benötigt wird.

## Füllen dieser Dimension mit Daten

Obwohl diese Dimension technisch bei allen Implementierungen vorkonfiguriert ist, funktioniert sie am besten mit benutzerspezifischen und Kaufereignissen. Adobe empfiehlt die Implementierung benutzerspezifischer Ereignisse auf Ihrer Site. Wenn Sie benutzerspezifische Ereignisse implementieren, ist für diese Dimension keine zusätzliche Implementierung erforderlich.

## Dimensionen

Dimension items include time-based buckets ranging from `"Less than 1 minute"` to `"More than 15 hours"`. For example, if it took a visitor 23 minutes from their first hit to a purchase, it would belong under the `"10 to 30 minutes"` dimension item.
