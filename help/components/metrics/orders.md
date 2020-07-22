---
title: Bestellungen
description: Die Anzahl der getätigten Käufe.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---


# Bestellungen

Die Metrik &quot;Bestellungen&quot;zeigt die Gesamtzahl der auf Ihrer Site getätigten Ereignis an. Diese Metrik ist für eCommerce-Sites bei der Messung der Umrechnung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente zu einer Bestellung beigetragen haben. Sie könnten beispielsweise die wichtigsten Kampagnen (unter Verwendung der Dimension [Rückverfolgungscode](../dimensions/tracking-code.md) ) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen, die zu Käufen beigetragen haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, die in der `purchase` Variablen vorhanden [`events`](/help/implement/vars/page-vars/events/events-overview.md) sind.
