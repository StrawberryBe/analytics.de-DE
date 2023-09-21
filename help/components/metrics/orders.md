---
title: Bestellungen
description: Die Anzahl der getätigten Käufe.
feature: Metrics
exl-id: b05abb6d-983f-43fe-80ad-a0ddf90de466
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 84%

---

# Bestellungen

Die &quot;Bestellungen&quot; [Metrik](overview.md) zeigt die Gesamtzahl der Kaufereignisse auf Ihrer Site an. Diese Metrik ist für eCommerce-Sites bei der Konversionsmessung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente zu einer Bestellung beigetragen haben. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension [Trackingcode](../dimensions/tracking-code.md)) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen, die zu Käufen beigetragen haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen `purchase` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist.
