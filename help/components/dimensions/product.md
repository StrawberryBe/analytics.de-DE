---
title: Produkt
description: Der Name des Produkts.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# Produkt

Die Dimension &quot;Produkt&quot;zeigt den Namen des Produkts im Treffer an. Es ist nützlich für Implementierungen, die die `products` Variable verwenden und Metriken um Produkte herum anzeigen möchten, wie Topverkäufe oder am meisten angezeigte Produkte. Diese Dimension kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf den zweiten Teil der Zeichenfolge in der [`products`](/help/implement/vars/page-vars/products.md) Variablen. Die Zeichen zwischen dem ersten und dem zweiten Semikolon (`;`) füllen diese Dimension.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente sind. Adobe empfiehlt, dass Sie eine konsistente Benennungsregel für Produkte festlegen. [Klassifizierungen](../c-classifications2/c-classifications.md) sind verfügbar, wenn Sie Produkte anders gruppieren oder einen benutzerfreundlicheren Namen angeben möchten. Adobe empfiehlt die Verwendung der Dimensionen &quot;Produkt&quot;und &quot;Kategorie&quot;.
