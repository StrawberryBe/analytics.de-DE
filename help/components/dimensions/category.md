---
title: Kategorie
description: Die Kategorie des Treffers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# Kategorie

Die Dimension &quot;Kategorie&quot;zeigt die Kategorie des Produkts des Treffers an. Es ist nützlich für Implementierungen, die die `products` Variable verwenden und Metriken zur Kategorie des Produkts anzeigen möchten, z. B. Topverkäufe oder am meisten angezeigte Artikel. Diese Dimension kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf den ersten Teil der Zeichenfolge in der [`products`](/help/implement/vars/page-vars/products.md) Variablen. Diese Dimension wird mit allen Elementen vor dem ersten Semikolon (`;`) gefüllt.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente sind. Adobe empfiehlt, einzelne Produkte in aussagekräftige Kategorien zu gruppieren, wobei sowohl die Produktabmessungen als auch die Kategorie verwendet werden.

>[!TIP]
>
>In früheren Versionen von Adobe Analytics wurden aufgrund der Verarbeitungsarchitektur Einschränkungen der Dimension &quot;Kategorie&quot;auferlegt. Diese Einschränkungen wurden seitdem entfernt, sodass Sie alle Metriken und Aufschlüsselungen verwenden können.
