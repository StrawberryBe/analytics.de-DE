---
title: Kundentreue
description: Kategorien, die auf der Anzahl der vorherigen Käufe eines Besuchers basieren.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Kundentreue

Die Dimension &quot;Kundentreue&quot;zeigt die Anzahl der Besucher auf Ihrer Site an, die zuvor 0 Einkäufe, 1 Einkäufe vor dem Kauf, 2 Einkäufe oder 3+ Einkäufe getätigt haben. Diese Dimension ist wertvoll, um zu verstehen, wie Ihre Site das Kaufverhalten beeinflusst. Sie können diese Dimension auch in einem Segment verwenden, um sich auf Besucher zu konzentrieren, die zum Einkauf zurückkehren, damit Sie ähnliche Verhaltensweisen für neue Besucher fördern können.

## Diese Dimension mit Daten füllen

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) Ereignis in Ihrer Implementierung. Wenn Sie das `purchase` Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Dimensionselemente umfassen Folgendes:

* **Kein Kunde**: Zum Zeitpunkt des Treffers hat der Besucher noch nie zuvor einen Kauf getätigt.
* **Neue Kunden**: Zum Zeitpunkt des Treffers tätigte der Besucher zuvor einen einzigen Einkauf.
* **Rückkehrende Kunden**: Zum Zeitpunkt des Treffers tätigte der Besucher zuvor zwei Einkäufe.
* **Loyale Kunden**: Zum Zeitpunkt des Treffers tätigte der Besucher zuvor drei oder mehr Einkäufe.

Wenn ein Besucher einen Kauf tätigt (löst das `purchase` Ereignis aus), werden dieser Treffer und alle nachfolgenden Treffer in den nächsten &quot;Behälter&quot;verschoben. Wenn ein Besucher beispielsweise zum ersten Mal ein Produkt von Ihrer Site kauft, wird er von &quot;Kein Kunde&quot;zu &quot;Neukunden&quot;umgestellt, wobei die Bestellung &quot;Neukunden&quot;zugeordnet wird. Dem Dimensionselement &quot;Kein Kunde&quot;können keine Bestellungen zugeordnet werden.
