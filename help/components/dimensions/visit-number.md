---
title: Besuchsnummer
description: Der n-te Besuch des Besuchers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 59%

---


# Besuchsnummer

Die Dimension „Besuchsnummer“ gibt an, in welchem Besuch sich der Besucher gerade befindet. Wenn ein neuer Besuch Beginn, wird dieses Dimensionselement um 1 erhöht. Diese Dimension ist hilfreich, wenn Sie verstehen möchten, wie stark Besucher interagieren, wenn sie auf Ihre Site zurückkehren. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch und kann nicht geändert werden. Sie gilt für die Lebensdauer des Besuchers, unabhängig vom Datumsbereich des Projekts.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionen

Dimension items include the string `"Visit number"` followed by the numeric representation of the visit the visitor is currently on. For example, if the visitor has never been to your site before, their first visit belongs to the dimension item `"Visit number 1"`. If this is the visitor&#39;s 13th visit to your site, they belong to the dimension item `"Visit number 13"`.
