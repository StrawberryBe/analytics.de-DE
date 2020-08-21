---
title: Besuchstiefe
description: Besuchsbasierte Dimension, die die Tiefe des Besuchs angibt.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 57%

---


# Besuchstiefe

Die Dimension „Besuchstiefe“ gibt die Anzahl der Seitenansichten an, die der Besucher während des gesamten Besuchs gesehen hat. Visit depth increases only if the hit is a page view, and the [Page](page.md) dimension is not the same as the last page view&#39;s dimension item. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch. Diese Variable wird für alle Treffer eines Besuchs nach Abschluss des Besuchs festgelegt.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionen

Dimension items include the string `"Pages per visit"` followed by a number representing the number of pages in the visit. The dimension item of `"Pages per visit: 1"` represents a single-page visit, while the dimension item `"Pages per visit: 8"` represents a visit with 8 page views (and any number of link tracking calls).

## Vergleich mit Treffertiefe

Einen Vergleich der Dimensionen finden Sie unter [Treffertiefe](hit-depth.md).