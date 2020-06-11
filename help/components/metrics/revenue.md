---
title: Umsatz
description: Der Geldbetrag der Produkte, die innerhalb aller Bestellungen gekauft wurden.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---


# Umsatz

Die Metrik &quot;Umsatz&quot;zeigt den Geldbetrag der Produkte an, die innerhalb aller Bestellungen gekauft wurden. Diese Metrik ist für eCommerce-Sites bei der Messung der Umrechnung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionswerte zum Umsatz beigetragen haben. Sie können beispielsweise die wichtigsten Kampagnen (unter Verwendung der Dimension [Rückverfolgungscode](../dimensions/tracking-code.md) ) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen.

## Berechnung dieser Metrik

Summieren Sie für jeden Treffer, bei dem die Variable `purchase` vorhanden ist, das Feld &quot;Preis&quot;innerhalb der [`events`](/help/implement/vars/page-vars/events/event-purchase.md) [`products`](/help/implement/vars/page-vars/products.md) Variablen.

Diese Metrik basiert auf der Variablen [currencyCode](/help/implement/vars/config-vars/currencycode.md) , wenn die Währung auf der Seite sich von der nativen Währung der Report Suite unterscheidet.
