---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: e9820869d16b8656ebebe11e397a3d7d8123fbcf

---


# „products“

Die Variable „“ dient zur Nachverfolgung von Produkten und Produktkategorien (sowie von Kaufmenge und Kaufpreis). „Products“ wird normalerweise zusammen mit einem Warenkorbereignis oder einem Ereignis festgelegt.

<!-- 

products.xml

 -->

>[!IMPORTANT]
>
>Im Januar 2016 haben wir die Logik aktualisiert, mit der das *`prodView`*-Ereignis automatisch eingestellt wird, was passiert, wenn *`product`*, aber nicht *`event`* vorhanden ist. Diese Aktualisierung kann zu einer gesteigerten Anzahl an *`prodView`*-Ereignissen führen. *`prodViews`* nimmt nur zu, wenn:
>
>1. Die Ereignisvariable ausschließlich ein nicht erkanntes Ereignis, wie beispielsweise *`shoppingCart`* oder *`cart`* enthält, bei denen es sich nicht um gültige Ereignisse handelt.
   >
   >
1. Die Variable *`products`* nicht leer ist.
>
>
Als mögliche Nebenwirkung werden möglicherweise Merchandising-eVars, die durch *`prodView`*-Ereignisse ausgelöst werden, einem leeren *`product`* zugeordnet. Das ist jedoch nur dann der Fall, wenn die *`product list`* nur ein ungültiges Produkt enthält (z. B. ein Semikolon ohne angegebenes Produkt).

Die Variable *`products`* dient zur Verfolgung der Interaktionen von Besuchern mit Produkten auf einer Site. So kann zum Beispiel in der Variablen „products“ verfolgt werden, wie oft ein Produkt angezeigt, in den Warenkorb gelegt, ausgecheckt und gekauft wird. Außerdem können Sie mit der Variablen auch die relative Effizienz von Merchandising-Kategorien auf Ihrer Site verfolgen. Nachfolgend sind einige der häufigsten Szenarien für den Einsatz der Variablen „products“ aufgeführt.

Die Variable *`products`* sollte immer in Verbindung mit einem Erfolgsereignis festgelegt werden.

<table id="table_D5A11AFDDD364D0993D387906343DDF3"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Die Zeichenfolge <span class="wintitle">Produkte</span> hat eine maximale Größe von 64.000. </p> </td> 
   <td> „products“ </td> 
   <td> Produkte <p>Kategorien (optional) </p> <p>Umsatz (optional) </p> <p>Einheiten (optional) </p> <p>Benutzerspezifische Ereignisse (optional) </p> <p>eVars (optional) </p> </td> 
   <td> " " </td> 
  </tr> 
 </tbody> 
</table>

**Syntax**

```js
"Category;Product;Quantity;Price;eventN=X[|eventN2=X2];eVarN=merch_category[|eVarN2=merch_category2]"
```

| Feld | Definition |
|---|---|
| Kategorie | Enthält die zugehörige Produktkategorie. In Version 15 können Produkte mit mehreren Kategorien verknüpft werden. Damit wird eine Einschränkung aus Version 14 aufgehoben. Wenn Sie eine Produktkategorie zuvor nicht aufgezeichnet haben, sollten Sie dieses Feld nun für Reports Suites ausfüllen, die in Version 15 vorhanden sind. |
| Produkt | (Erforderlich) Der Bezeichner, der zum Verfolgen eines Produkts dient. Anhand dieses Bezeichners wird der Bericht Produkte aufgefüllt. Achten Sie darauf, bis zum Checkout-Prozess immer den gleichen Bezeichner zu verwenden. |
| Quantität | Die Anzahl der gekauften Artikel. Dieses Feld muss bei einem Kaufereignis, das aufgezeichnet werden soll, festgelegt sein. |
| Preis | Bezieht sich auf die kombinierten Kosten der insgesamt gekauften Menge (Einheiten x individueller Stückpreis) und nicht auf den individuellen Preis. Dieses Feld muss bei einem Kaufereignis, das aufgezeichnet werden soll, festgelegt sein. |
| Ereignisse | Mit dem angegebenen Produkt verknüpfte Währungsereignisse. Siehe [Produktspezifische Währungsereignisse](https://helpx.adobe.com/analytics/kb/comparing-event-types.html) und [Auf Bestellung bezogene Währungsereignisse](https://helpx.adobe.com/analytics/kb/comparing-event-types.html). |
| eVars | Merchandising eVar-Werte, die mit einem bestimmten Produkt verknüpft sind. Siehe [Merchandising-Variablen](/help/components/c-variables/c-merch-variables/var-merchandising.md). |

Die in der Variable *`products`* enthaltenen Werte basieren auf dem Typ des aufgezeichneten Ereignisses. Wenn Kategorien ausgelassen werden, ist das Trennzeichen zwischen Kategorie/Produkt (;) als Platzhalter erforderlich. Andere Trennzeichen sind nur erforderlich, wenn sie zum Hervorheben des aufzunehmenden Parameters notwendig sind, wie in den Beispielen auf dieser Seite dargestellt.

**Festlegen von „products“ mit anderen als einem „purchase“-Ereignis**

Die Variable *`products`* muss in Verbindung mit einem Erfolgsereignis festgelegt werden.

**Festlegen von „products“ mit einem „purchase“-Ereignis**

Das *`purchase`*-Ereignis sollte auf die endgültige Bestätigung („Vielen Dank!“) des Bestellvorgangs gesetzt werden. Produktname, Kategorie, Menge und Preis werden alle in der Variablen *`products`* festgelegt. Obwohl die Variable *`purchaseID`* nicht erforderlich ist, wird ihre Verwendung ausdrücklich empfohlen, damit Bestellungen nicht doppelt entgegengenommen werden.

**Produktspezifische Währungsereignisse**

Wenn ein Währungsereignis einen Wert in der Variable *`products`* anstelle der Ereignisvariable erhält, gilt dies nur für diesen Wert. Dies ist nützlich, um produktspezifische Rabatte, den Produktversand und ähnliche Werte zu verfolgen. Beispiel: Wenn Sie Ereignis 1 konfigurieren, um den Produktversand zu verfolgen, kann ein Produkt mit einer Versandgebühr von 4,50 wie folgt angezeigt werden:

```js
s.events="event1" 
s.products="Footwear;Running Shoes;1;99.99;event1=4.50"
```

In diesem Beispiel wird der Wert 4,50 direkt mit dem Produkt „Running Shoes“ verknüpft. Wenn Sie event1 zum Produktbericht hinzufügen, wird „4,50“ für das Einzelelement „Running Shoes“ aufgeführt. Ähnlich wie beim Preis sollte dieser Wert die Summe für die aufgeführte Menge widerspiegeln. Wenn 2 Artikel mit einer Versandgebühr von jeweils 4,50 vorliegen, sollte event1 „9,00“ lauten.

**Auf Bestellung bezogene Währungsereignisse**

Wenn ein Währungsereignis einen Wert in der Ereignisliste anstelle der Variable *`products`* erhält, gilt dies für alle Produkte in der Variable *`products`*. Dies ist nützlich, wenn Sie Rabatte, Versandkosten und ähnliche Werte, die für die gesamte Bestellung gelten, verfolgen möchten, ohne den Produktpreis zu ändern oder ihn separat in der Produktliste zu verfolgen.

Beispiel: Wenn Sie event10 so konfiguriert haben, dass es einen auftragsweiten Rabatt enthält, sieht ein Kauf mit 10 % Rabatt ungefähr so aus:

```js
s.events="purchase,event10=9.95" 
s.products="Footwear;Running Shoes;1;69.95,Running Essentials;Running Socks;10;29.50" 
s.purchaseID="1234567890"
```

In Währungsberichten ist der Gesamtwert nicht die Summe der Ereigniswerte der einzelnen Produkte, sondern der deduplizierte Gesamtwert des Ereignisses (in diesem Beispiel die Summe aller im Berichterstattungszeitraum gewährten Rabatte). Beispiel: „9,95“ würde sowohl für „Running Shoes“ als auch für „Running Socks“ aufgeführt werden, und die Summe wäre ebenfalls „9,95“.

> [!NOTE] Wenn ein Wert für dasselbe numerische/Währungs-Ereignis in der Variable *`products`* und in der Variable *`events`* angegeben ist, wird der Wert aus dem *`events`*-Wert verwendet.

**Probleme, Fragen und Tipps**

* Die Variable *`products`* sollte immer in Verbindung mit einem Erfolgsereignis (Ereignisse) gesetzt werden. Wenn kein Erfolgsereignis angegeben ist, lautet das Standardereignis prodView.

* Entfernen Sie alle Kommas und Semikolons aus Produkt- und Kategorienamen, bevor diese in „products“ übernommen werden.
* Entfernen Sie alle HTML-Zeichen (Warenzeichen, Symbole für eingetragene Marken usw.).
* Entfernen Sie alle Währungssonderzeichen ($) aus dem Preis.

**Beispiele**

<table id="table_6F1334E73CE048A5AC0CC28B561C1B2D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <code> s.products="Category;ABC123" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category2;ABC123,;ABC456" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category3;ABC123;1;10" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category;ABC123;1;10,;ABC456;2;19.98" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;;;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99,;ABC123;2;19.98;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping|evar2=3 Stars" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping, ;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2,event3" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping,;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping,;;;;event3=2.9;evar3=20% off" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2,event3=9.95" </code> <p> <code> s.products="Category;ABC123;,;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping,;;;;event3=2.9;evar3=20% off" </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

