---
title: Produkt
description: Der Name des Produkts.
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 100%

---


# Produkt

Die Dimension „Produkt“ zeigt den Namen des Produkts im Treffer an. Dies ist für Implementierungen nützlich, die die `products`-Variable verwenden und Metriken für die Produkte anzeigen möchten, wie am häufigsten verkaufte oder angezeigte Artikel. Diese Dimension kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf den zweiten Teil der Zeichenfolge in der [`products`](/help/implement/vars/page-vars/products.md)-Variable. Diese Dimension wird mit den Zeichen zwischen dem ersten und dem zweiten Semikolon (`;`) gefüllt.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt Ihnen, eine konsistente Namenskonvention für Produkte einzuführen. [Klassifizierungen](../classifications/c-classifications.md) sind verfügbar, wenn Sie Produkte anders gruppieren oder einen benutzerfreundlicheren Namen angeben möchten. Adobe empfiehlt die Verwendung der Dimensionen „Produkt“ und „Kategorie“.
