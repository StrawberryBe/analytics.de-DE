---
title: Kundenloyalität
description: Kategorien, die auf der Anzahl der vorherigen Käufe des Besuchers basieren.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 100%

---


# Kundenloyalität

Die Dimension “Kundenloyalität“ zeigt die Anzahl der Besucher auf Ihrer Site an, die 0 frühere Käufe, 1 früheren Kauf, 2 frühere Käufe oder 3+ frühere Käufe getätigt haben. Diese Dimension ist hilfreich, um zu verstehen, wie sich Ihre Website auf das Kaufverhalten auswirkt. Sie können diese Dimension auch in einem Segment verwenden, um sich auf Besucher zu konzentrieren, die zum Kauf zurückkehren, damit Sie ähnliche Verhaltensweisen bei neuen Besuchern fördern können.

## Füllen dieser Dimension mit Daten

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md)-Ereignis in Ihrer Implementierung. Wenn Sie das `purchase`-Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehören:

* **Kein Kunde**: Zum Zeitpunkt des Treffers hat der Besucher noch nie zuvor einen Kauf getätigt.
* **Neue Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor einen Kauf getätigt.
* **Rückkehrende Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor zwei Käufe getätigt.
* **Loyale Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor drei oder mehr Käufe getätigt.

Wenn ein Besucher einen Kauf tätigt (das `purchase`-Ereignis auslöst), werden dieser Treffer und alle nachfolgenden Treffer in den nächsten „Behälter“ verschoben. Wenn ein Besucher beispielsweise zum ersten Mal ein Produkt von Ihrer Site kauft, wechselt er von „Kein Kunde“ zu „Neuer Kunde“, wobei die Bestellung „Neuer Kunde“ zugeordnet wird. Dem Dimensionselement „Kein Kunde“ können keine Bestellungen zugeordnet werden.
