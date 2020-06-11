---
title: Besuchstiefe
description: Besuchsbasierte Dimension, die die Besuchstiefe meldet.
translation-type: tm+mt
source-git-commit: 05ea2778cd5cd324c660fd0f1d2ac02373829f0f
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# Besuchstiefe

Die Dimension &quot;Besuchstiefe&quot;gibt an, wie viele Ansichten der Besucher während des gesamten Besuchs gesehen hat. Die Besuchstiefe erhöht sich nur, wenn es sich bei dem Treffer um eine Ansicht der Seite handelt und die Dimension &quot; [Seite](page.md) &quot;nicht mit dem Dimensionswert der letzten Ansicht übereinstimmt. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch. Diese Variable wird für alle Treffer eines Besuchs nach Abschluss des Besuchs festgelegt.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionswerte

Zu den Dimensionswerten zählen die Zeichenfolge `"Pages per visit"` gefolgt von einer Zahl, die die Anzahl der Seiten im Besuch darstellt. Der Dimensionswert von `"Pages per visit: 1"` steht für einen Einzelseitenbesuch, während der Dimensionswert einen Besuch mit 8 Seitenaufrufen (und beliebig vielen Linktracking-Ansichten) `"Pages per visit: 8"` darstellt.

## Vergleich mit Treffertiefe

Siehe [Treffertiefe](hit-depth.md) für einen Vergleich zwischen Dimensionen.