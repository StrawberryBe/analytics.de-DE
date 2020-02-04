---
title: „products“
description: Senden Sie Daten darüber, welche Produkte oder Produkte im Warenkorb angezeigt werden.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# „products“

Die `products` Variable verfolgt mit ihnen verbundene Produkte und Eigenschaften. Diese Variable wird normalerweise auf einzelnen Produktseiten, Warenkorbseiten und Kaufbestätigungsseiten eingestellt. Es handelt sich um eine Variable mit mehreren Werten. Das bedeutet, dass Sie mehrere Produkte im selben Treffer senden können und Adobe den Wert in separate Dimensionswerte analysiert.

> [!NOTE] Wenn diese Variable in einem Treffer ohne Warenkorbereignis in der `events` Variablen festgelegt wird, wird die Metrik &quot;Produktansichten&quot;um 1 inkrementiert. Stellen Sie sicher, dass Sie bei jedem Treffer das entsprechende Warenkorbereignis festlegen.

## Produkte in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable festzulegen. Es gibt jedoch mehrere Erweiterungen von Drittanbietern, um Hilfe zu leisten.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf [!UICONTROL Katalog] , um alle verfügbaren Erweiterungen anzuzeigen.
4. Suchen Sie nach dem Begriff &quot;Produkt&quot;, der mehrere verfügbare Erweiterungen enthält, um diese Variable einzustellen.

Sie können eine dieser Erweiterungen verwenden oder den benutzerdefinierten Code-Editor nach der AppMeasurement-Syntax weiter unten verwenden.

## s.products in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.products` Variable ist eine Zeichenfolge, die mehrere getrennte Felder pro Produkt enthält. Jedes einzelne Produkt kann bis zu 100 Byte über alle Felder hinweg enthalten. Übergeben Sie jedes Feld mit einem Semikolon (`;`) in der Zeichenfolge.

* **Kategorie** (optional): Die übergreifende Produktkategorie. Ihr Unternehmen entscheidet, wie Produkte in Kategorien unterteilt werden.
* **Produktname** (erforderlich): Der Name des Produkts.
* **Menge** (optional): Wie viele dieser Produkte sind im Einkaufswagen. Dieses Feld gilt nur für Treffer mit dem Kaufereignis.
* **Preis** (optional): Der Gesamtpreis des Produkts als Dezimalzahl. Ist die Menge mehr als ein Produkt, so setzen Sie den Preis auf den Gesamtpreis und nicht auf den individuellen Produktpreis. Richten Sie die Währung dieses Werts an die `currencyCode` Variable aus. Fügen Sie in diesem Feld nicht das Währungssymbol ein. Dieses Feld gilt nur für Treffer mit dem Kaufereignis.
* **Ereignisse** (optional): Ereignisse, die mit dem Produkt verknüpft sind. Senden Sie mehrere Ereignisse mit einer Pipe (`|`). Weitere Informationen finden Sie unter [Ereignisse](events/events-overview.md) .
* **eVars** (optional): Merchandising-eVars, die mit dem Produkt verknüpft sind. Senden Sie mehrere Merchandising-eVars mit einer Pipe (`|`). Weitere Informationen finden Sie unter [Merchandising eVars](../../../components/c-variables/c-merch-variables/var-merchandising.md) .

```js
// Set a single product using all available fields
s.products = "Example category;Example product;1;3.50;event1=4.99|event2=5.99;eVar1=Example merchandising value 1|eVar2=Example merchandising value 2";
```

Diese Variable unterstützt mehrere Produkte im selben Treffer. Es ist wertvoll für Einkaufswagen und Einkäufe mit mehreren Produkten. Während pro Produkt ein Grenzwert von 100 Byte gilt, beträgt die Gesamtlänge der `products` Variablen 64 K. Trennen Sie jedes Produkt durch ein Komma (`,`) in der Zeichenfolge.

```js
// Set multiple products - useful for when a visitor views their shopping cart
s.products = "Example category 1;Example product 1;1;3.50,Example category 2;Example product 2,1,5.99";
```

> [!IMPORTANT] Achten Sie darauf, alle Semikolons, Kommas und Rohre aus Produktnamen, Kategorien und Merchandising-eVar-Werten zu entfernen. Wenn ein Produktname ein Komma enthält, analysiert AppMeasurement es als Beginn eines neuen Produkts. Diese fehlerhafte Analyse löst den Rest der Produktzeichenfolge aus und führt zu fehlerhaften Daten in Dimensionen und Berichten.

## Beispiele

Die `products` Variable ist flexibel, wenn Felder ausgelassen und mehrere Produkte einbezogen werden. Durch diese Flexibilität kann es leicht sein, ein Trennzeichen zu verpassen, wodurch Ihre Implementierung falsche Daten an Adobe sendet.

```js
// Include only product and category. Common on individual product pages
s.products = "Example category;Example product";

// Include only product name if you do not want to use product category
s.products = ";Example product";

// One product has a category, the other does not. Note the comma and adjacent semicolon to omit category
s.products = "Example category;Example product,;Example product";

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
