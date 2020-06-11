---
title: Besuch-Nr.
description: Der n-te Besuch des Besuchers.
translation-type: tm+mt
source-git-commit: 05ea2778cd5cd324c660fd0f1d2ac02373829f0f
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# Besuch-Nr.

Die Dimensionsberichte &quot;Besuchnummer&quot;für den Besuch des Besuchers sind aktuell aktiviert. Wenn ein neuer Besuch Beginn, wird dieser Dimensionswert um 1 erhöht. Diese Dimension ist hilfreich, wenn Sie verstehen möchten, wie engagierte Besucher bei der Rückkehr zu Ihrer Site sind. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch und kann nicht geändert werden. Sie gilt für die Lebensdauer des Besuchers, unabhängig vom Datumsbereich des Projekts.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionswerte

Zu den Dimensionswerten zählen die Zeichenfolge `"Visit number"` gefolgt von der numerischen Darstellung des Besuchs, auf dem sich der Besucher derzeit befindet. Wenn der Besucher beispielsweise noch nie zuvor Ihre Site besucht hat, gehört sein erster Besuch zum Dimensionswert `"Visit number 1"`. Wenn dies der 13. Besuch des Besuchers auf Ihrer Site ist, gehören sie zum Dimensionswert `"Visit number 13"`.
