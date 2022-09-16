---
title: Besuchsnummer
description: Der n-te Besuch des Besuchers.
feature: Dimensions
exl-id: daef34b3-c270-476d-a45c-a20be6138c6b
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 100%

---

# Besuchsnummer

Die Dimension „Besuchsnummer“ gibt an, in welchem Besuch sich der Besucher gerade befindet. Wenn ein neuer Besuch beginnt, wird dieses Dimensionselement um 1 erhöht. Diese Dimension ist hilfreich, wenn Sie verstehen möchten, wie stark Besucher interagieren, wenn sie auf Ihre Site zurückkehren. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch und kann nicht geändert werden. Sie gilt für die Lebensdauer des Besuchers, unabhängig vom Datumsbereich des Projekts.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Zu den Dimensionselementen zählen die Zeichenfolge `"Visit number"`, gefolgt von der numerischen Darstellung des Besuchs, in dem sich der Besucher derzeit befindet. Wenn der Besucher beispielsweise noch nie zuvor Ihre Site besucht hat, gehört sein erster Besuch zum Dimensionselement `"Visit number 1"`. Wenn dies der 13. Besuch des Besuchers auf Ihrer Site ist, gehört er zum Dimensionselement `"Visit number 13"`.
