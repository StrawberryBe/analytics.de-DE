---
title: Bestellungen
description: Die Anzahl der getätigten Käufe.
exl-id: b05abb6d-983f-43fe-80ad-a0ddf90de466
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '91'
ht-degree: 100%

---

# Bestellungen

Die Metrik „Bestellungen“ zeigt die Gesamtzahl der Kaufereignisse auf Ihrer Site an. Diese Metrik ist für eCommerce-Sites bei der Konversionsmessung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente zu einer Bestellung beigetragen haben. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension [Trackingcode](../dimensions/tracking-code.md)) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen, die zu Käufen beigetragen haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen `purchase` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist.
