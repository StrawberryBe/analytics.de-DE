---
title: Produktansichten
description: Die Anzahl der Aufrufe der Produktseiten.
feature: Metrics
exl-id: 6217391d-8b42-4fdf-b05e-b9b117598ad2
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 72%

---

# Produktansichten

Die Produktansichten [Metrik](overview.md) zeigt an, wie oft ein Produkt angezeigt wurde. Diese Metrik ist nützlich, wenn Sie Ihre am häufigsten angezeigten Ansichten sehen möchten oder sehen wollen, wie sich die Gesamtproduktansichten im Laufe der Zeit entwickeln.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, die mit **einer** der folgenden Aussage übereinstimmen:

* Der Wert `prodView` ist in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden oder
* Die [`products`](/help/implement/vars/page-vars/products.md) festgelegt ist und die `events` leer ist.
