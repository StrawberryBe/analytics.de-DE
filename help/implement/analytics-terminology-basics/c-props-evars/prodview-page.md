---
description: Die Variable „products“ dient zur Nachverfolgung von Produkten und Produktkategorien (sowie von Kaufmenge und Kaufpreis).
keywords: Analytics Implementation;products variable;product view;success event
title: Detaillierte Produktansicht (Seite)
topic: Developer and implementation
uuid: 464c9daf-b042-4fb8-8ca6-e104c0bcef45
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Detaillierte Produktansicht (Seite)

Die Variable „products“ dient zur Nachverfolgung von Produkten und Produktkategorien (sowie von Kaufmenge und Kaufpreis).

Ein Erfolgsereignis sollte immer mit der Variable *`products`* eingestellt werden.

```js
s.events="prodView"
```

> [!NOTE] Während *`prodView`* in der Implementierung wie ein Ereignis behandelt wird, verfügt es in der Schnittstelle nicht über die gleiche Flexibilität. *`prodView`* ist eine Instanz des Produkts und steht nur im *`products`*-Bericht zur Verfügung. Adobe empfiehlt die Verwendung eines *`custom`*-Ereignisses zusätzlich zum *`prodView`*-Ereignis. Dadurch werden in anderen Konversions-Berichten die Produktansichtsmetriken neben anderen Metriken angezeigt.

```js
s.products=";diamond earrings (54321)"
```

> [!NOTE] Die Syntax der Produktzeichenfolge muss mit einem Semikolon beginnen. Das ist eine alte Anforderung an die Schreibweise. So wurden früher Kategorie und Produkt abgegrenzt. Nun führt dies jedoch in der Benutzeroberfläche zu Einschränkungen, falls Sie jemals die Art und Weise ändern möchten, in der Sie Produkte klassifizieren. Lassen Sie diese Variable leer und richten Sie Kategorien über „Classifications“ ein. So bleiben Sie beim Reporting so flexibel wie möglich.

## Einkaufswagenseite (scOpen, scAdd, scRemove ) {#section_469B64F4150149DFB6B2C731279C0BC7}

```js
s.events="scOpen,scAdd"
s.products=";SKU"
```

## Erst-Checkout-Seite {#section_E15607A9AECB44F79631926C853CF64E}

```js
s.events="scCheckout"
s.products=";SKU"
```

## Bestätigungsseite {#section_E006943CD5FD42358086581CA44B9660}

```js
s.events="purchase"
s.products=";SKU"
```

> [!NOTE] Die Verwendung der SKU in der Produktzeichenfolge kann dazu führen, dass der *`products`*-Bericht schlechter lesbar ist, bietet jedoch die größtmögliche Flexibilität, wenn Sie Ihre Produkte klassifizieren möchten. Sie können aus der SKU Kategorien erstellen, die Angaben zu Ausführung, Hersteller, Kategorie und Unterkategorie machen.

Wenn die Variable *`products`* in Verbindung mit dem *`purchase`-Ereignis festgelegt ist, sind die Kaufmenge und der Gesamtkaufpreis im Wert der Variable „products“ enthalten.*
