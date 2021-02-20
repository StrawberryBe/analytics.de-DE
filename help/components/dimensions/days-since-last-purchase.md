---
title: Tage seit letztem Kauf
description: Die Anzahl der Tage zwischen dem aktuellen Treffer und dem letzten Kauf, den er getätigt hat.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 100%

---


# Tage seit letztem Kauf

Die Dimension „Tage seit dem letzten Kauf“ misst die Zeitdauer, die zwischen dem aktuellen Treffer des Besuchers und seinem letzten Kauf zu diesem Zeitpunkt verstrichen ist. Diese Dimension hilft Ihnen, das Verhalten der Besucher nach einem Kauf auf Ihrer Website zu verstehen.

Besucher, die noch nie etwas gekauft haben, werden in dieser Dimension nicht berücksichtigt. Auch Treffer, die vor dem ersten Kauf eines Besuchers erzielt wurden, sind nicht enthalten. Es werden nur Treffer nach dem ersten Kauf des Besuchers berücksichtigt.

## Füllen dieser Dimension mit Daten

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md)-Ereignis in Ihrer Implementierung. Wenn Sie das `purchase`-Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der Tage zwischen dem letzten Kauf eines Besuchers und dem aktuellen Treffer. Jede Anzahl von Tagen ist ein eigenes Dimensionselement, wobei „Gleicher Tag“ dann auftritt, wenn der letzte Kauf eines Besuchers und der aktuelle Treffer am selben Tag stattgefunden haben.
