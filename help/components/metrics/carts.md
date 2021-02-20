---
title: Warenkorb
description: Die Anzahl der Treffer, bei denen ein Besucher sein erstes Produkt einem Warenkorb hinzugefügt hat.
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 100%

---


# Warenkorb

Die Metrik „Entnahme aus Warenkorb“ zeigt an, wie oft ein Besucher etwas aus dem Warenkorb entfernt hat. Diese Metrik ist hilfreich, wenn Sie den Teil des Konversionstrichter verstehen möchten, in dem Kunden kein Interesse mehr an einem Produkt haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen `scOpen` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist.

## Unterschiede zwischen „Warenkorb“ und „Warenkorbansicht“

Da „Warenkorb“ und „Warenkorbansicht“ Ereignisse sind, die implementiert werden müssen, entscheidet Ihr Unternehmen über den genauen Unterschied zwischen diesen beiden Metriken. Adobe hat diese Metriken jedoch für Folgendes entwickelt:

* „Warenkorb“ wird nur einmal pro Kauf ausgelöst, wenn ein Besucher sein erstes Produkt in den Warenkorb legt.
* „Zusatz zum Warenkorb“ wird für jedes Produkt ausgelöst, das in den Warenkorb gelegt wird.

Beim ersten Produkt werden sowohl „Warenkorb“ als auch „Zusatz zum Warenkorb“ ausgelöst. Diese Richtlinien sind aber nicht verpflichtend. Ihre Organisation bestimmt die genaue Implementierungslogik.
