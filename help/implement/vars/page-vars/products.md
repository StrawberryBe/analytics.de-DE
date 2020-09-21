---
title: products
description: Senden Sie Daten darüber, welche Produkte angezeigt werden oder sich im Warenkorb befinden.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 97%

---


# products

Die `products`-Variable verfolgt Produkte und die mit ihnen verbundenen Eigenschaften. Diese Variable wird normalerweise auf einzelnen Produktseiten, Warenkorbseiten und Kaufbestätigungsseiten eingestellt. Es handelt sich um eine mehrwertige Variable, d. h. Sie können mehrere Produkte mit demselben Treffer senden, und Adobe parst den Wert in separate Dimensionselemente.

>[!NOTE]
>
>Wenn diese Variable in einem Treffer ohne Warenkorbereignis in der [`events`](events/events-overview.md)-Variable festgelegt wird, wird die Metrik [Produktansichten](/help/components/metrics/product-views.md) um 1 inkrementiert. Stellen Sie sicher, dass Sie bei jedem Treffer mit der Variable `products` das entsprechende Warenkorbereignis festlegen.

## Produkte in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu setzen. Es gibt jedoch mehrere Erweiterungen von Drittanbietern, die helfen können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie auf [!UICONTROL Katalog], um alle verfügbaren Erweiterungen anzuzeigen.
4. Suchen Sie nach dem Begriff „product“, der mehrere verfügbare Erweiterungen zum Festlegen dieser Variablen anzeigt.

Sie können eine dieser Erweiterungen oder den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax unten verwenden.

## s.products in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.products`-Variable ist eine Zeichenfolge, die mehrere getrennte Felder pro Produkt enthält. Jedes einzelne Produkt kann über alle Felder hinweg bis zu 100 Byte enthalten. Übergeben Sie jedes Feld mit einem Semikolon (`;`) in der Zeichenfolge.

* **Kategorie** (optional): Die übergeordnete Produktkategorie. Ihr Unternehmen entscheidet, wie Produkte in Kategorien unterteilt werden.
* **Produktname** (erforderlich): Der Name des Produkts.
* **Menge** (optional): Die Anzahl dieser Produkte im Warenkorb. Dieses Feld gilt nur für Treffer mit dem Kaufereignis.
* **Preis** (optional): Der Gesamtpreis des Produkts als Dezimalzahl. Ist die Menge größer als 1, setzen Sie den Preis auf den Gesamtpreis und nicht auf den Einzelproduktpreis. Stellen Sie sicher, dass die Währung dieses Werts mit der [`currencyCode`](../config-vars/currencycode.md)-Variablen übereinstimmt. Fügen Sie in diesem Feld nicht das Währungssymbol ein. Dieses Feld gilt nur für Treffer mit dem Kaufereignis.
* **Ereignisse** (optional): Ereignisse, die mit dem Produkt verknüpft sind. Trennen Sie mehrere Ereignisse mit einem senkrechten Strich (`|`). Weitere Informationen finden Sie unter [Ereignisse](events/events-overview.md).
* **eVars** (optional): Merchandising-eVars, die mit dem Produkt verknüpft sind. Trennen Sie mehrere Merchandising-eVars mit einem senkrechten Strich (`|`). Weitere Informationen finden Sie unter [Merchandising eVars](evar-merchandising.md).

```js
// Set a single product using all available fields
s.products = "Example category;Example product;1;3.50;event1=4.99|event2=5.99;eVar1=Example merchandising value 1|eVar2=Example merchandising value 2";
```

Diese Variable unterstützt mehrere Produkte im selben Treffer. Sie ist beim Warenkorb und bei Käufen mit mehreren Produkten hilfreich. Während pro Produkt ein 100-Byte-Grenze gilt, beträgt die Gesamtlänge der `products`-Variablen 64 KB. Trennen Sie jedes Produkt durch ein Komma (`,`) in der Zeichenfolge.

```js
// Set multiple products - useful for when a visitor views their shopping cart
s.products = "Example category 1;Example product 1;1;3.50,Example category 2;Example product 2,1,5.99";
```

>[!IMPORTANT]
>
>Entfernen Sie alle Semikolons, Kommas und senkrechte Striche aus Produktnamen, Kategorien und Merchandising-eVar-Werten. Wenn ein Produktname ein Komma enthält, analysiert AppMeasurement es als Beginn eines neuen Produkts. Durch dieses fehlerhafte Parsing wird der Rest der Produktzeichenfolge falsch analysiert. Das führt zu fehlerhaften Daten in Dimensionen und Berichten.

## Beispiele

Die `products`-Variable ist flexibel, wenn Felder ausgelassen und mehrere Produkte einbezogen werden. Durch diese Flexibilität kann es leicht sein, ein Trennzeichen zu verpassen, wodurch Ihre Implementierung falsche Daten an Adobe sendet.

```js
// Include only product and category. Common on individual product pages
s.products = "Example category;Example product";

// Include only product name if you do not want to use product category
s.products = ";Example product";

// One product has a category, the other does not. Note the comma and adjacent semicolon to omit category
s.products = "Example category;Example product 1,;Example product 2";

// A visitor purchases a single product; record quantity and price
s.events = "purchase";
s.products = "Example category;Example product;1;6.99";

// A visitor purchases multiple products with different quantities
s.events = "purchase";
s.products = "Example category;Example product 1;9;26.91,Example category;Example product 2;4;9.96";

// Attribute currency event1 only to product 2 and not product 1
s.events = "event1";
s.products = "Example category 1;Example product 1;1;1.99,Example category 2;Example product 2;1;2.69;event1=1.29";

// Use multiple numeric events in the product string
s.events = "event1,event2";
s.products = "Example category;Example product;1;4.20;event1=2.3|event2=5";

// Use merchandising eVars without any events. Note the adjacent semicolons to skip events
s.products = "Example category;Example product;1;6.69;;eVar1=Merchandising value";

// Use merchandising eVars without category, quantity, price, or events
s.products = ";Example product;;;;eVar1=Merchandising value";

// Multiple products using multiple different events and multiple different merchandising eVars
s.events = "event1,event2,event3,event4,purchase";
s.products = "Example category 1;Example product 1;3;12.60;event1=1.4|event2=9;eVar1=Merchandising value|eVar2=Another merchandising value,Example category 2;Example product 2;1;59.99;event3=6.99|event4=1;eVar3=Merchandising value 3|eVar4=Example value four";
```

Wenn Sie die `digitalData` Datenschicht [verwenden, können Sie das](../../prepare/data-layer.md)`digitalData.product` Objektarray durchlaufen:

```js
for(var i=0; i<digitalData.product.length; i++) {
    // Add individual product info to the product string
    s.products += digitalData.product[i].category.primaryCategory + ";" + digitalData.product[i].productInfo.productName;
    // If there are more products, add a comma
    if(i != digitalData.product.length-1) {
        s.products += ",";
    }
}
```
