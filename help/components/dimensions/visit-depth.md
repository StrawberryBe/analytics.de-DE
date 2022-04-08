---
title: Besuchstiefe
description: Besuchsbasierte Dimension, die die Tiefe des Besuchs angibt.
feature: Dimensions
exl-id: 3e9aca08-2255-46ca-9949-77334ee7120e
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
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
