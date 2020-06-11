---
title: Einheiten
description: Die Gesamtzahl der innerhalb aller Bestellungen gekauften Produkte.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Einheiten

Die Metrik &quot;Einheiten&quot;zeigt die Gesamtzahl der Produkte an, die innerhalb aller Bestellungen gekauft wurden. Diese Metrik ist für eCommerce-Sites bei der Messung der Umrechnung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionswerte zur Anzahl der gekauften Produkte beigetragen haben. Sie könnten beispielsweise die wichtigsten Kampagnen (unter Verwendung der Dimension [Rückverfolgungscode](../dimensions/tracking-code.md) ) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen, die zu den gekauften Produkten beitrugen.

## Berechnung dieser Metrik

Summieren Sie für jeden Treffer, bei dem die Variable `purchase` vorhanden ist, das Feld &quot;Menge&quot;innerhalb der [`events`](/help/implement/vars/page-vars/events/events-overview.md) [`products`](/help/implement/vars/page-vars/products.md) Variablen.

## Bestellungen und Einheiten vergleichen

Die [Bestellmetrik](orders.md) zeichnet nur die Anzahl der Ereignis auf. Die Metrik &quot;Einheiten&quot;ist in der Regel höher als &quot;Bestellungen&quot;, da Kunden mehr als ein Produkt erwerben können. In diesen Fällen gibt es eine einzige Bestellung mit mehreren Einheiten.

Wenn Sie Bestellungen über mehr als Einheiten haben, empfiehlt Adobe, die Integrität Ihrer Implementierung zu überprüfen. Es ist wahrscheinlich, dass Ihre `products` Variable bei Käufen nicht richtig eingestellt ist, was normalerweise unerwünschtes Verhalten ist.
