---
description: Die Variable „products“ dient zur Nachverfolgung von Produkten und Produktkategorien (sowie von Kaufmenge und Kaufpreis).
keywords: Analytics-Implementierung; products variable; Produktansicht; Erfolgsereignis
seo-description: Die Variable „products“ dient zur Nachverfolgung von Produkten und Produktkategorien (sowie von Kaufmenge und Kaufpreis).
seo-title: Detaillierte Produktansichtsseite
solution: Analytics
title: Detaillierte Produktansichtsseite
topic: Entwickler und Implementierung
uuid: 464 c 9 daf-b 042-4 fb 8-8 ca 6-e 104 c 0 bcef 45
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Detaillierte Produktansichtsseite

Die Variable „products“ dient zur Nachverfolgung von Produkten und Produktkategorien (sowie von Kaufmenge und Kaufpreis).

A success event should always be set in conjunction with the *`products`* variable.

```js
s.events="prodView"
```

>[!NOTE]
>
>While *`prodView`* is treated in implementation like an event, it does not have the same flexibility in the interface. The *`prodView`*event is an instance of the product and is only available in the *`products`* report. Adobe recommends you use a *`custom`* event in addition to the *`prodView`* event. Dadurch werden in anderen Konversions-Berichten die Produktansichtsmetriken neben anderen Metriken angezeigt.

```js
s.products=";diamond earrings (54321)"
```

>[!NOTE]
>
>Die Syntax der Produktzeichenfolge muss mit einem Semikolon beginnen. Das ist eine alte Anforderung an die Schreibweise. So wurden früher Kategorie und Produkt abgegrenzt. Nun führt dies jedoch in der Benutzeroberfläche zu Einschränkungen, falls Sie jemals die Art und Weise ändern möchten, in der Sie Produkte klassifizieren. Lassen Sie diese Variable leer und richten Sie Kategorien über „Classifications“ ein. So bleiben Sie beim Reporting so flexibel wie möglich.

## Einkaufswagenseite (scOpen, scAdd, scRemove ) {#section_469B64F4150149DFB6B2C731279C0BC7}

```js
s.events="scOpen,scAdd" 
s.products=";SKU" 
```

## Erst-Checkout-Seite {#section_E15607A9AECB44F79631926C853CF64E}

```js
s.events="scCheckout" 
s.products=”;SKU" 
```

## Bestätigungsseite {#section_E006943CD5FD42358086581CA44B9660}

```js
s.events="purchase" 
s.products=";SKU" 
```

>[!NOTE]
>
>While using the SKU in the product string may make the *`products`* report less readable, it provides the maximum flexibility later when you want to classify your products. Sie können aus der SKU Kategorien erstellen, die Angaben zu Ausführung, Hersteller, Kategorie und Unterkategorie machen.

Wenn die Variable *`products`* in Verbindung mit dem *`purchase`-Ereignis festgelegt ist, sind die Kaufmenge und der Gesamtkaufpreis im Wert der „products“-Variablen enthalten.*
