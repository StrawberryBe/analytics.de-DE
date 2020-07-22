---
title: Zeit vor dem Ereignis
description: Die Zeit zwischen der Metrik und dem ersten Treffer des Besuchs.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Zeit vor dem Ereignis

Die Dimension &quot;Zeit vor dem Ereignis&quot;zeigt den Zeitraum an, der zwischen dem ersten Treffer des Besuchs und der gewünschten Metrik verstrichen ist. Diese Dimension ist nützlich, um die Zeitdauer zu bestimmen, die zum Erzielen eines Erfolgsereignisses benötigt wird, z. B. eine Formularübermittlung oder ein Kauf.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert zwar für alle Implementierungen standardmäßig, funktioniert aber am besten mit benutzerdefinierten Ereignissen und Kaufprogrammen. Adobe empfiehlt die Implementierung benutzerdefinierter Ereignis auf Ihrer Site. Wenn Sie benutzerdefinierte Ereignis implementieren, ist für diese Dimension keine zusätzliche Implementierung erforderlich.

## Dimensionselemente

Zu den Dimensionselementen gehören zeitbasierte Behälter von `"Less than 1 minute"` bis `"More than 15 hours"`. Wenn es beispielsweise 23 Minuten vom ersten Treffer eines Besuchers bis zum ersten Einkauf dauerte, gehörte er zum `"10 to 30 minutes"` Dimensionselement.
