---
title: Produktansichten
description: Die Anzahl der Aufrufe der Produktseiten.
feature: Metrics
exl-id: 6217391d-8b42-4fdf-b05e-b9b117598ad2
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 100%

---

# Produktansichten

Die Metrik „Produktansichten“ zeigt an, wie oft ein Produkt angezeigt wurde. Diese Metrik ist nützlich, wenn Sie Ihre am häufigsten angezeigten Ansichten sehen möchten oder sehen wollen, wie sich die Gesamtproduktansichten im Laufe der Zeit entwickeln.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, die mit **einer** der folgenden Aussage übereinstimmen:

* Der Wert `prodView` ist in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden oder
* Die [`products`](/help/implement/vars/page-vars/products.md)-Variable ist festgelegt, und es gibt keine Warenkorbereignisse in der `events`-Variable. Jedes Ereignis, das nicht benutzerspezifisch ist (`event1` – `event1000`), ist ein Warenkorbereignis.
