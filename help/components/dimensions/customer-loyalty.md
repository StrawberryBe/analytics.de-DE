---
title: Kundenloyalität
description: Kategorien, die auf der Anzahl der vorherigen Käufe des Besuchers basieren.
feature: Dimensions
exl-id: 48ac1fdf-9a32-4bcc-8b23-bf58358a3470
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 90%

---

# Kundenloyalität

Die &quot;Kundentreue&quot; [Dimension](overview.md) gibt die Anzahl der Besucher Ihrer Site an, die 0 frühere Käufe, 1 vorherigen Kauf, 2 vorherige Käufe oder mehr als 3 frühere Käufe getätigt haben. Diese Dimension ist hilfreich, um zu verstehen, wie sich Ihre Website auf das Kaufverhalten auswirkt. Sie können diese Dimension auch in einem Segment verwenden, um sich auf Besucher zu konzentrieren, die zum Kauf zurückkehren, damit Sie ähnliche Verhaltensweisen bei neuen Besuchern fördern können.

## Füllen dieser Dimension mit Daten

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md)-Ereignis in Ihrer Implementierung. Wenn Sie das `purchase`-Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehören:

* **Kein Kunde**: Zum Zeitpunkt des Treffers hat der Besucher noch nie zuvor einen Kauf getätigt.
* **Neue Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor einen Kauf getätigt.
* **Rückkehrende Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor zwei Käufe getätigt.
* **Loyale Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor drei oder mehr Käufe getätigt.

Wenn ein Besucher einen Kauf tätigt (das `purchase`-Ereignis auslöst), werden dieser Treffer und alle nachfolgenden Treffer in den nächsten „Behälter“ verschoben. Wenn ein Besucher beispielsweise zum ersten Mal ein Produkt von Ihrer Site kauft, wechselt er von „Kein Kunde“ zu „Neuer Kunde“, wobei die Bestellung „Neuer Kunde“ zugeordnet wird. Dem Dimensionselement „Kein Kunde“ können keine Bestellungen zugeordnet werden.
