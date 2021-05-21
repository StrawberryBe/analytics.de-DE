---
title: Besuchsnummer
description: Der n-te Besuch des Besuchers.
exl-id: daef34b3-c270-476d-a45c-a20be6138c6b
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '162'
ht-degree: 100%

---

# Besuchsnummer

Die Dimension „Besuchsnummer“ gibt an, in welchem Besuch sich der Besucher gerade befindet. Wenn ein neuer Besuch beginnt, wird dieses Dimensionselement um 1 erhöht. Diese Dimension ist hilfreich, wenn Sie verstehen möchten, wie stark Besucher interagieren, wenn sie auf Ihre Site zurückkehren. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch und kann nicht geändert werden. Sie gilt für die Lebensdauer des Besuchers, unabhängig vom Datumsbereich des Projekts.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Zu den Dimensionselementen zählen die Zeichenfolge `"Visit number"`, gefolgt von der numerischen Darstellung des Besuchs, in dem sich der Besucher derzeit befindet. Wenn der Besucher beispielsweise noch nie zuvor Ihre Site besucht hat, gehört sein erster Besuch zum Dimensionselement `"Visit number 1"`. Wenn dies der 13. Besuch des Besuchers auf Ihrer Site ist, gehört er zum Dimensionselement `"Visit number 13"`.
