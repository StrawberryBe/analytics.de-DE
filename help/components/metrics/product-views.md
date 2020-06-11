---
title: Ansichten
description: Die Anzahl der Ansichten auf Produktseiten.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Ansichten

Die Metrik &quot;Ansichten&quot;zeigt an, wie oft ein Produkt angezeigt wurde. Diese Metrik ist nützlich, wenn Sie Ihre am häufigsten angezeigten Ansichten oder den Trend der Gesamtproduktentwicklung im Zeitverlauf anzeigen möchten.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, die mit **einer der folgenden übereinstimmen** :

* Der Wert `prodView` ist in der [`events`](/help/implement/vars/page-vars/events/events-overview.md) Variablen vorhanden. oder
* Die [`products`](/help/implement/vars/page-vars/products.md) Variable ist festgelegt, und es gibt keine Warenkorbdaten in der `events` Variablen. Jedes Ereignis, das nicht benutzerspezifisch ist (`event1` - `event1000`), ist ein Einkaufswagen-Ereignis.