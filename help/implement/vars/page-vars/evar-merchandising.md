---
title: eVar (Merchandising)
description: Benutzerspezifische Variablen, die mit einzelnen Produkten verknüpft sind.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 29%

---


# eVar (Merchandising)

*Auf dieser Hilfeseite wird beschrieben, wie Merchandising-eVars implementiert werden. For information on how merchandising eVars work as a dimension, see[eVars (Merchandising)](/help/components/dimensions/evar-merchandising.md)in the Components user guide.*

## Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie die eVar in den Report Suite-Einstellungen auf die gewünschte Syntax konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md).

>[!IMPORTANT]
>
>Wenn Merchandising-eVars nicht korrekt konfiguriert werden, führt dies zu unerwarteten Werten oder Datenverlusten für die Variable. Vergewissern Sie sich, dass es für Ihre Implementierung richtig konfiguriert ist.

## Implementierung mit der Produktsyntax

When &#39;Product Syntax&#39; is enabled, the merchandising category is populated directly within the `products` variable, so selecting and setting a binding event is not required. Dies ist die empfohlene Methode und sollte verwendet werden, es sei denn, der in `products` festzulegende Wert ist nicht verfügbar, wenn das Erfolgsereignis stattfindet.

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to a different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

Der Wert für `eVar1` wird dem Produkt zugewiesen. Alle nachfolgenden Erfolgsereignisse, die dieses Ereignis betreffen, werden dem eVar-Wert gutgeschrieben.

## Implementierung mit Konversionsvariablensyntax

Conversion Variable Syntax is used when the eVar value is not available to set in the `products` variable. Dies bedeutet in der Regel, dass Ihre Seite keinen Kontext mit dem Merchandising-Kanal oder der Suchmethode hat. In diesen Fällen legen Sie die Merchandising-Variable fest, bevor Sie zur Produktseite gelangen, und der Wert bleibt bestehen, bis das Binding-Ereignis eintritt.

Wenn das bei der Konfiguration ausgewählte Binding-Ereignis eintritt, wird der beibehaltene Wert der „eVar“ dem Produkt zugewiesen. For example, if `prodView` is specified as the binding event, the merchandising category is tied to the current product list only at the time the event occurs. Eine Merchandising-eVar, die bereits einem Produkt zugewiesen wurde, kann nur von nachfolgenden Binding-Ereignissen aktualisiert werden.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = "Birds;Canary";
```

Der Wert `"Aviary"` für `eVar1` wird dem Produkt zugewiesen `"Canary"`. Alle nachfolgenden Erfolgsereignisse, an denen dieses Ereignis beteiligt ist, werden gutgeschrieben `"Canary"`. Des Weiteren wird der aktuelle Wert der Merchandising-Variablen allen nachfolgenden Produkten zugewiesen, bis eine der folgenden Bedingungen erfüllt ist:

* Die eVar läuft ab (basierend auf der Einstellung &quot;Läuft ab nach&quot;)
* Die Merchandising-eVar wird mit einem neuen Wert überschrieben.
