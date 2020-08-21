---
title: Produktansichten
description: Die Anzahl der Aufrufe der Produktseiten.
translation-type: ht
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
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