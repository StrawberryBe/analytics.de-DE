---
title: Besuchstiefe
description: Besuchsbasierte Dimension, die die Besuchstiefe meldet.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# Besuchstiefe

Die Dimension &quot;Besuchstiefe&quot;gibt an, wie viele Ansichten der Besucher während des gesamten Besuchs gesehen hat. Die Besuchstiefe erhöht sich nur, wenn es sich bei dem Treffer um eine Seitendimension handelt und die [Seitendimension](page.md) nicht mit dem Dimensionselement der letzten Ansicht übereinstimmt. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch. Diese Variable wird für alle Treffer eines Besuchs nach Abschluss des Besuchs festgelegt.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Dimensionselemente enthalten die Zeichenfolge `"Pages per visit"` gefolgt von einer Zahl, die die Anzahl der Seiten im Besuch darstellt. Das Dimensionselement von `"Pages per visit: 1"` stellt einen Einzelseitenbesuch dar, während das Dimensionselement einen Besuch mit 8 Seitenaufrufen `"Pages per visit: 8"` darstellt (und beliebig viele Linkverfolgungsaufrufe).

## Vergleich mit Treffertiefe

Siehe [Treffertiefe](hit-depth.md) für einen Vergleich zwischen Dimensionen.