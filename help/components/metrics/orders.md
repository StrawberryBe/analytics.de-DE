---
title: Bestellungen
description: Die Anzahl der getätigten Käufe.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '91'
ht-degree: 100%

---


# Bestellungen

Die Metrik „Bestellungen“ zeigt die Gesamtzahl der Kaufereignisse auf Ihrer Site an. Diese Metrik ist für eCommerce-Sites bei der Konversionsmessung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente zu einer Bestellung beigetragen haben. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension [Trackingcode](../dimensions/tracking-code.md)) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen, die zu Käufen beigetragen haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen `purchase` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist.
