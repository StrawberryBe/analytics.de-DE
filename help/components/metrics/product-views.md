---
title: Produktansichten
description: Die Anzahl der Aufrufe der Produktseiten.
exl-id: 6217391d-8b42-4fdf-b05e-b9b117598ad2
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '94'
ht-degree: 100%

---

# Produktansichten

Die Metrik „Produktansichten“ zeigt an, wie oft ein Produkt angezeigt wurde. Diese Metrik ist nützlich, wenn Sie Ihre am häufigsten angezeigten Ansichten sehen möchten oder sehen wollen, wie sich die Gesamtproduktansichten im Laufe der Zeit entwickeln.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, die mit **einer** der folgenden Aussage übereinstimmen:

* Der Wert `prodView` ist in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden oder
* Die [`products`](/help/implement/vars/page-vars/products.md)-Variable ist festgelegt, und es gibt keine Warenkorbereignisse in der `events`-Variable. Jedes Ereignis, das nicht benutzerspezifisch ist (`event1` – `event1000`), ist ein Warenkorbereignis.
