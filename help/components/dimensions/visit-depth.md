---
title: Besuchstiefe
description: Besuchsbasierte Dimension, die die Tiefe des Besuchs angibt.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 100%

---


# Besuchstiefe

Die Dimension „Besuchstiefe“ gibt die Anzahl der Seitenansichten an, die der Besucher während des gesamten Besuchs gesehen hat. Die Besuchstiefe erhöht sich nur, wenn es sich bei dem Treffer um eine Seitenansicht handelt und die Dimension [Seite](page.md) nicht mit dem Dimensionselement der letzten Seitenansicht übereinstimmt. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch. Diese Variable wird für alle Treffer eines Besuchs nach Abschluss des Besuchs festgelegt.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Zu den Dimensionselementen zählen die Zeichenfolge `"Pages per visit"`, gefolgt von einer Zahl, die die Anzahl der Seiten im Besuch darstellt. Das Dimensionselement `"Pages per visit: 1"` steht für einen Einzelseitenbesuch, während das Dimensionselement `"Pages per visit: 8"` einen Besuch mit 8 Seitenansichten (und beliebig vielen Linktracking-Aufrufen) darstellt.

## Vergleich mit Treffertiefe

Einen Vergleich der Dimensionen finden Sie unter [Treffertiefe](hit-depth.md).