---
title: Umsatz
description: Der Geldbetrag der bei allen Bestellungen gekauften Produkte.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 100%

---


# Umsatz

Die Metrik „Umsatz“ zeigt den Geldbetrag der bei allen Bestellungen gekauften Produkte an. Diese Metrik ist für eCommerce-Sites bei der Konversionsmessung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente zum Umsatz beigetragen haben. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension [Trackingcode](../dimensions/tracking-code.md)) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen.

## Berechnung dieser Metrik

Summieren Sie für jeden Treffer, bei dem `purchase` in der [`events`](/help/implement/vars/page-vars/events/event-purchase.md)-Variable vorhanden ist, das Feld „Preis“ innerhalb der [`products`](/help/implement/vars/page-vars/products.md)-Variable.

Diese Metrik basiert auf der Variablen [currencyCode](/help/implement/vars/config-vars/currencycode.md), wenn die Währung auf der Seite sich von der nativen Währung der Report Suite unterscheidet.
