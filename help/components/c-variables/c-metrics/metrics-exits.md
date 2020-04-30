---
description: Gibt an, wie oft ein Wert als letzter Wert bei einem Besuch erfasst wird. Ausstiege können nur einmal pro Besuch auftreten.
title: Ausstiege
topic: Metrics
uuid: cd5436ef-65d3-431b-a24f-aceff8542c50
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Ausstiege

Gibt an, wie oft ein Wert als letzter Wert bei einem Besuch erfasst wird. Ausstiege können nur einmal pro Besuch auftreten.

Exitpages werden pro Besuch aufgeschlüsselt, d. h., sie werden für alle Hits für einen Besuch beibehalten. Weitere Informationen finden Sie unter [Aufschlüsselung und Segmentierungscontainer](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-overview.html).

Bei Anwendung auf eine Dimension werden Ausstiege beim letzten Wert eines Besuchs gezählt, der bei jedem Treffer während des Besuchs erfolgen kann. Falls es beim letzten Treffer keinen Wert gibt, wird der Ausstieg dem aktuellsten Wert zugeordnet.

Wenn ein Ausstieg außerhalb des Berichtsbereichs für einen Besuch innerhalb des Berichtsbereichs erfolgt, wird er einbezogen, solange er sich nicht entlang einer Monatsgrenze (innerhalb des Datensatzes) befindet.
