---
title: Warenkorb
description: Die Anzahl der Treffer, bei denen ein Besucher sein erstes Produkt zu einem Einkaufswagen hinzugefügt hat.
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# Warenkorb

Die Metrik &quot;Entnahmen aus Einkaufswagen&quot;zeigt an, wie oft ein Besucher etwas aus dem Einkaufswagen entfernt hat. Diese Metrik ist hilfreich, wenn Sie den Teil des Konversionstrichter verstehen möchten, in dem Kunden kein Interesse mehr an einem Produkt haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, die in der `scOpen` Variablen vorhanden [`events`](/help/implement/vars/page-vars/events/events-overview.md) sind.

## Unterschiede zwischen &quot;Warenkorb&quot; und &quot;Ansichten im Warenkorb&quot;

Da &quot;Einkaufswagen&quot;und &quot;Ansichten im Einkaufswagen&quot;Ereignis sind, die implementiert werden müssen, entscheidet Ihr Unternehmen über den genauen Unterschied zwischen diesen beiden Metriken. Adobe hat diese Metriken jedoch für Folgendes entwickelt:

* &quot;Einkaufswagen&quot;werden nur einmal pro Einkauf ausgelöst, wenn ein Besucher sein erstes Produkt in den Einkaufswagen legt.
* &quot;Zusatz zum Einkaufswagen&quot;löst jedes Produkt aus, das in den Einkaufswagen gelegt wurde.

Beim ersten Produkt wird sowohl der Zusatz &quot;Einkaufswagen&quot;als auch der Zusatz &quot;Einkaufswagen&quot;ausgelöst. Auch diese Leitlinien sind nicht konkret. Ihre Organisation legt die genaue Implementierungslogik fest.
