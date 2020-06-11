---
title: Tage vor dem ersten Kauf
description: Die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers und dem ersten Kauf.
translation-type: tm+mt
source-git-commit: a8dc233e962a49674a30ff3c9f0b5d0d45b09f24
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Tage vor dem ersten Kauf

Die Dimension &quot;Tage vor dem ersten Kauf&quot;zeigt die Anzahl der Tage an, die zwischen dem ersten Besuch eines Besuchers auf Ihrer Site und dem ersten Einkauf verstrichen sind. Wenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Einkauf tätigt, gehört jeder nachfolgende Besuch oder Ereignis zum Dimensionswert &quot;1 Tag&quot;.

Nachdem ein Besucher den ersten Einkauf getätigt hat, gehören sie für die restliche Cookie-Lebensdauer des Besuchers zum gleichen Dimensionswert.

## Diese Dimension mit Daten füllen

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) Ereignis in Ihrer Implementierung. Wenn Sie das `purchase` Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionswerte

Dimensionswerte umfassen die Anzahl der Tage zwischen dem ersten Besuch Ihrer Site durch einen Besucher und dem ersten Kauf. Jede Anzahl von Tagen ist ein separater Dimensionswert, wobei &quot;Am selben Tag&quot;auftritt, an dem der erste Besuch und der erste Kauf eines Besuchers am selben Tag erfolgte.
