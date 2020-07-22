---
title: Tage vor dem ersten Kauf
description: Die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers und dem ersten Kauf.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Tage vor dem ersten Kauf

Die Dimension &quot;Tage vor dem ersten Kauf&quot;zeigt die Anzahl der Tage an, die zwischen dem ersten Besuch eines Besuchers auf Ihrer Site und dem ersten Einkauf verstrichen sind. Wenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Einkauf tätigt, gehört jeder nachfolgende Besuch oder Ereignis zum Dimensionselement &quot;1 Tag&quot;.

Nachdem ein Besucher den ersten Einkauf getätigt hat, gehören sie für die restliche Cookie-Lebensdauer des Besuchers zum gleichen Dimensionselement.

## Diese Dimension mit Daten füllen

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) Ereignis in Ihrer Implementierung. Wenn Sie das `purchase` Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Dimensionselemente beinhalten die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers auf Ihrer Site und dem ersten Kauf. Jede Anzahl von Tagen ist ein separater Dimensionselement, wobei &quot;Am selben Tag&quot;auftritt, an dem der erste Besuch und der erste Kauf eines Besuchers am selben Tag erfolgte.
