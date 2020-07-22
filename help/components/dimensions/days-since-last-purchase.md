---
title: Tage seit dem letzten Kauf
description: Die Anzahl der Tage zwischen dem aktuellen Treffer und dem letzten Kauf, den sie getätigt haben.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Tage seit dem letzten Kauf

Die Dimension &quot;Tage seit dem letzten Kauf&quot;misst den Zeitraum, der zwischen dem aktuellen Treffer des Besuchers und dem letzten Kauf zu diesem Zeitpunkt verstrichen ist. Diese Dimension hilft Ihnen dabei, das Verhalten zu verstehen, das Besucher nach dem Kauf von etwas auf Ihrer Site vornehmen.

Besucher, die noch nie etwas gekauft haben, werden nicht in diese Dimension einbezogen. Außerdem werden Treffer, die vor dem ersten Kauf eines Besuchers ausgelöst wurden, auch nicht berücksichtigt. Es werden nur Treffer nach dem ersten Kauf des Besuchers berücksichtigt.

## Diese Dimension mit Daten füllen

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) Ereignis in Ihrer Implementierung. Wenn Sie das `purchase` Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Dimensionselemente enthalten die Anzahl der Tage zwischen dem letzten Kauf eines Besuchers und dem aktuellen Treffer. Jede Anzahl von Tagen ist ein separater Dimensionselement, wobei &quot;Am selben Tag&quot;auftritt, an dem der letzte Einkauf und der aktuelle Treffer eines Besuchers am selben Tag erfolgten.
