---
title: products
description: Senden Sie Daten darüber, welche Produkte angezeigt werden oder sich im Warenkorb befinden.
feature: Variables
exl-id: f26e7c93-f0f1-470e-a7e5-0e310ec666c7
source-git-commit: 3edb7208f4b11a2fa58a2f7c696444ab998a6bfe
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 77%

---

# products

Die `products`-Variable verfolgt Produkte und die mit ihnen verbundenen Eigenschaften. Diese Variable wird normalerweise auf einzelnen Produktseiten, Warenkorbseiten und Kaufbestätigungsseiten eingestellt. Es handelt sich um eine mehrwertige Variable, d. h. Sie können mehrere Produkte mit demselben Treffer senden, und Adobe parst den Wert in separate Dimensionselemente.

>[!NOTE]
>
>Wenn diese Variable in einem Treffer ohne die Variable [`events`](events/events-overview.md) festgelegt wird, wird die Metrik [Produktansichten](/help/components/metrics/product-views.md) um 1 inkrementiert. Stellen Sie sicher, dass Sie bei jedem Treffer mit der Variablen `products` die entsprechenden Ereignisse festlegen.

## Produkte mit dem Web SDK

Produkte sind [für Adobe Analytics zugeordnet](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) unter mehreren XDM-Feldern:

* Die Kategorie ist zugeordnet zu `productListItems[].lineItemId`.
* Das Produkt ist `productListItems[].name`.
* Menge wird zugeordnet zu `productListItems[].quantity`.
* Der Preis wird `productListItems[].priceTotal`.
* Merchandising-eVars werden zugeordnet zu `productListItems._experience.analytics.customDimensions.eVars.eVar1` nach `productListItems._experience.analytics.customDimensions.eVars.eVar250`, je nachdem, welche eVar Sie an ein Produkt binden möchten.
* Merchandising-Ereignisse werden zugeordnet zu `productListItems[]._experience.analytics.event1to100.event1.value` nach `productListItems._experience.analytics.event901to1000.event1000.value`, je nachdem, welches Ereignis Sie an ein Produkt binden möchten.

## Produkte mit der Adobe Analytics-Erweiterung

Es gibt kein dediziertes Feld in der Adobe Experience Platform-Datenerfassung, um diese Variable festzulegen. Es gibt jedoch mehrere Drittanbietererweiterungen, die helfen.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie auf [!UICONTROL Katalog], um alle verfügbaren Erweiterungen anzuzeigen.
4. Suchen Sie nach dem Begriff „product“, der mehrere verfügbare Erweiterungen zum Festlegen dieser Variablen anzeigt.

Sie können eine dieser Erweiterungen oder den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax unten verwenden.

## s.products in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.products`-Variable ist eine Zeichenfolge, die mehrere getrennte Felder pro Produkt enthält. Trennen Sie die Felder in der Zeichenfolge mit einem Semikolon voneinander (`;`).

* **Kategorie** (optional): Die Produktkategorie. Die maximale Länge für dieses Feld beträgt 100 Byte.
* **Produktname** (erforderlich): Der Name des Produkts. Die maximale Länge für dieses Feld beträgt 100 Byte.
* **Menge** (optional): Die Anzahl dieser Produkte im Warenkorb. Dieses Feld gilt nur für Treffer mit dem Kaufereignis.
* **Preis** (optional): Der Gesamtpreis des Produkts als Dezimalzahl. Ist die Menge größer als 1, setzen Sie den Preis auf den Gesamtpreis und nicht auf den Einzelproduktpreis. Stellen Sie sicher, dass die Währung dieses Werts mit der [`currencyCode`](../config-vars/currencycode.md)-Variablen übereinstimmt. Fügen Sie in diesem Feld nicht das Währungssymbol ein. Dieses Feld gilt nur für Treffer mit dem Kaufereignis.
* **Ereignisse** (optional): Ereignisse, die mit dem Produkt verknüpft sind. Trennen Sie mehrere Ereignisse mit einem senkrechten Strich (`|`). Weitere Informationen finden Sie unter [Ereignisse](events/events-overview.md).
* **eVars** (optional): Merchandising-eVars, die mit dem Produkt verknüpft sind. Trennen Sie mehrere Merchandising-eVars mit einem senkrechten Strich (`|`). Weitere Informationen finden Sie unter [Merchandising eVars](evar-merchandising.md).

```js
// Set a single product using all available fields
s.products = "Example category;Example product;1;3.50;event1=4.99|event2=5.99;eVar1=Example merchandising value 1|eVar2=Example merchandising value 2";
```

Diese Variable unterstützt mehrere Produkte im selben Treffer. Sie ist beim Warenkorb und bei Käufen mit mehreren Produkten hilfreich. Die maximale Länge für die gesamte `products`-Zeichenfolge beträgt 64 K. Trennen Sie jedes Produkt durch ein Komma (`,`) in der Zeichenfolge.

```js
// Set multiple products - useful for when a visitor views their shopping cart
s.products = "Example category 1;Example product 1;1;3.50,Example category 2;Example product 2;1;5.99";
```

>[!WARNING]
>
>Entfernen Sie alle Semikolons, Kommas und senkrechte Striche aus Produktnamen, Kategorien und Merchandising-eVar-Werten. Wenn ein Produktname ein Komma enthält, analysiert AppMeasurement es als Beginn eines neuen Produkts. Durch dieses fehlerhafte Parsing wird der Rest der Produktzeichenfolge falsch analysiert. Das führt zu fehlerhaften Daten in Dimensionen und Berichten.

## Beispiele

Die `products`-Variable ist flexibel, wenn Felder ausgelassen und mehrere Produkte einbezogen werden. Durch diese Flexibilität kann es leicht sein, ein Trennzeichen zu verpassen, wodurch Ihre Implementierung falsche Daten an Adobe sendet.

```js
// Include only product and category. Common on individual product pages
s.products = "Example category;Example product";

// Include only product name
s.products = ";Example product";

// One product has a category, the other does not. Note the comma and adjacent semicolon to omit category
s.products = "Example category;Example product 1,;Example product 2";

// A visitor purchases a single product; record quantity and price
s.events = "purchase";
s.products = ";Example product;1;6.99";

// A visitor purchases multiple products with different quantities
s.events = "purchase";
s.products = ";Example product 1;9;26.91,Example category;Example product 2;4;9.96";

// Attribute currency event1 only to product 2 and not product 1
s.events = "event1";
s.products = ";Example product 1;1;1.99,Example category 2;Example product 2;1;2.69;event1=1.29";

// Use multiple numeric events in the product string
s.events = "event1,event2";
s.products = ";Example product;1;4.20;event1=2.3|event2=5";

// Use merchandising eVars without any events. Note the adjacent semicolons to skip events
s.products = ";Example product;1;6.69;;eVar1=Merchandising value";

// Use merchandising eVars without category, quantity, price, or events
s.products = ";Example product;;;;eVar1=Merchandising value";

// Multiple products using multiple different events and multiple different merchandising eVars
s.events = "event1,event2,event3,event4,purchase";
s.products = "Example category 1;Example product 1;3;12.60;event1=1.4|event2=9;eVar1=Merchandising value|eVar2=Another merchandising value,Example category 2;Example product 2;1;59.99;event3=6.99|event4=1;eVar3=Merchandising value 3|eVar4=Example value four";
```

Wenn Sie die `digitalData`-[Datenschicht](../../prepare/data-layer.md) verwenden, können Sie das `digitalData.product`-Objekt-Array iterativ durchlaufen:

```js
for(var i = 0; i < digitalData.product.length; i++) {
    // Add individual product info to the product string
    s.products += digitalData.product[i].category.primaryCategory + ";" + digitalData.product[i].productInfo.productName;
    // If there are more products, add a comma
    if(i != digitalData.product.length - 1) {
        s.products += ",";
    }
}
```
