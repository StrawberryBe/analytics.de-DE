---
title: Kategorie
description: Die Produktkategorie des Treffers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 85%

---


# Kategorie

Die Dimension „Kategorie“ gibt die Produktkategorie des Treffers an. Dies ist für Implementierungen nützlich, die die `products`-Variable verwenden und Metriken für die Produktkategorie anzeigen möchten, wie am häufigsten verkaufte oder angezeigte Artikel. Diese Dimension kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf den ersten Teil der Zeichenfolge in der [`products`](/help/implement/vars/page-vars/products.md)-Variable. Diese Dimension wird mit allen Elementen vor dem ersten Semikolon (`;`) gefüllt.

## Dimensionen

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente sind. Adobe empfiehlt, einzelne Produkte in aussagekräftige Kategorien zu gruppieren und dabei sowohl die Dimensionen „Produkt“ als auch „Kategorie“ zu verwenden.

>[!TIP]
>
>In früheren Versionen von Adobe Analytics waren der Dimension „Kategorie“ aufgrund ihrer Verarbeitungsarchitektur einige Einschränkungen auferlegt. Diese Einschränkungen wurden inzwischen entfernt, sodass Sie alle Metriken und Aufschlüsselungen verwenden können.
