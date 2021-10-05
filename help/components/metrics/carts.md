---
title: Warenkorb
description: Die Anzahl der Treffer, bei denen ein Besucher sein erstes Produkt einem Warenkorb hinzugefügt hat.
exl-id: 890bbaba-0140-4995-bbd2-c69aedc801e5
source-git-commit: e804907aa6655b4cfac146a34fb6a3774631818e
workflow-type: ht
source-wordcount: '135'
ht-degree: 100%

---

# Warenkorb

Die Metrik „Warenkörbe“ zeigt die Anzahl der Treffer, bei denen ein Besucher sein erstes Produkt zu einem Warenkorb hinzugefügt hat.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen `scOpen` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist.

## Unterschiede zwischen „Warenkorb“ und „Warenkorbansicht“

Da „Warenkorb“ und „Warenkorbansicht“ Ereignisse sind, die implementiert werden müssen, entscheidet Ihr Unternehmen über den genauen Unterschied zwischen diesen beiden Metriken. Adobe hat diese Metriken jedoch für Folgendes entwickelt:

* „Warenkorb“ wird nur einmal pro Kauf ausgelöst, wenn ein Besucher sein erstes Produkt in den Warenkorb legt.
* „Zusatz zum Warenkorb“ wird für jedes Produkt ausgelöst, das in den Warenkorb gelegt wird.

Beim ersten Produkt werden sowohl „Warenkorb“ als auch „Zusatz zum Warenkorb“ ausgelöst. Diese Richtlinien sind aber nicht verpflichtend. Ihre Organisation bestimmt die genaue Implementierungslogik.
