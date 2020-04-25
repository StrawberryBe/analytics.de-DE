---
description: Beschreibt, wie Merchandising-Variablen aktiviert und implementiert werden.
keywords: Analytics Implementation;merchandising;variable;product syntax;Conversion Variable Syntax;s.products
title: Implementierung einer Merchandising-Variable
topic: Developer and implementation
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Implementierung einer Merchandising-Variable

Beschreibt, wie Merchandising-Variablen aktiviert und implementiert werden.

## Aktivieren einer Merchandising-Variablen

Merchandising kann für jede benutzerspezifische eVar unter **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Konversionsvariablen]** aktiviert werden.

![](assets/merch-enable.png)

| Einstellung | Beschreibung |
|--- |--- |
| Läuft ab nach | Legt fest, wie lange Merchandising-Werte bestehen bleiben sollen. |
| Merchandising | **Produktsyntax:** Dieser Wert wird innerhalb von `s.products` festgelegt.<br>**Konversionsvariablensyntax:** Dieser Wert wird innerhalb der festgelegten Merchandising-eVar gesetzt. |
| Merchandising-Binding-Ereignis (nur Konversionsvariablensyntax) | Gibt an, wann ein Produkt mit der aktuellen Merchandising-Kategorie verknüpft werden soll. Es können mehrere Ereignisse ausgewählt werden, indem Sie die STRG-Taste gedrückt halten und mehrere Elemente in der Liste anklicken. Sie können nur ein Ereignis auswählen, wenn „Konversionsvariablensyntax“ ausgewählt wurde. |

## Implementierung anhand der Produktsyntax

Wenn die Produktsyntax aktiviert ist, wird die Merchandising-Kategorie direkt innerhalb der Produktvariablen aufgefüllt. Daher ist es nicht erforderlich, ein Binding-Ereignis auszuwählen und festzulegen. Dies ist die empfohlene Methode und sollte verwendet werden, es sei denn, der in `s.products` festzulegende Wert ist nicht verfügbar, wenn das Erfolgsereignis stattfindet.

### Syntax

```js
s.products="category;product;quantity;price;event_incrementer;eVarN=merch_category|eVarM=merch_category2";
```

### Beispiel

```js
s.events="prodView";
s.products=";Snow Goggles;;;;eVar1=goggles";
```

Der Wert „Skibrille“ für „eVar1“ wird dem Produkt „Snow Skibrille“ zugewiesen. Alle nachfolgenden Erfolgsereignisse (dem Warenkorb hinzugefügte Produkte, Checkouts, Käufe usw.), die mit diesem Produkt in Verbindung stehen, werden dem Wert „Skibrille“ gutgeschrieben.

## Implementierung anhand der Konversionsvariablensyntax

Die Konversionsvariablensyntax sollte verwendet werden, wenn der in `s.products` festzulegende eVar-Wert nicht verfügbar ist. Das bedeutet in der Regel, dass Ihre Seite keinen Kontext für den Merchandising-Kanal oder die Suchmethode hat. In diesen Fällen müssen Sie die Merchandising-Variable festlegen, bevor Sie auf die Produktseite gelangen, wobei der Wert solange bestehen bleibt, bis das Binding-Ereignis eintritt.

Wenn das bei der Konfiguration ausgewählte Binding-Ereignis eintritt, wird der beibehaltene Wert der „eVar“ dem Produkt zugewiesen. Wenn z. B. „prodView“ als Binding-Ereignis ausgewählt wird, wird die Merchandising-Kategorie nur während des Eintretens dieses Ereignisses mit der aktuellen Produktliste verknüpft. Eine Merchandising-eVar, die bereits einem Produkt zugewiesen wurde, kann nur von nachfolgenden Binding-Ereignissen aktualisiert werden.

### Syntax

Platzierung auf derselben oder der vorhergehenden Seite vor dem Binding-Ereignis:

```js
s.eVar1="merchandising_category";
```

Platzierung auf der Seite, auf der das Binding-Ereignis eintritt:

```js
s.events="prodView";
s.products="category;product";
```

### Beispiel

Auf Seite 1 des Besuchs:

```js
s.eVar1="Outdoors"
```

Auf Seite 2 des Besuchs:

```js
s.events="prodView";
s.products=";Snow Goggles";
```

Der Wert „Outdoor“ für „eVar1“ wird dem Produkt „Snow Skibrille“ zugewiesen. Alle nachfolgenden Erfolgsereignisse (dem Warenkorb hinzugefügte Produkte, Checkouts, Käufe usw.), die mit diesem Produkt in Verbindung stehen, werden dem Wert „Snow Skibrille“ gutgeschrieben. Des Weiteren wird der aktuelle Wert der Merchandising-Variablen allen nachfolgenden Produkten zugewiesen, bis eine der folgenden Bedingungen erfüllt ist:

* „eVar“ läuft ab (basierend auf der Einstellung „Läuft ab nach“)
* Die Merchandising-eVar wird mit einem neuen Wert überschrieben.

## Zusätzliche externe Informationen

[Merchandising mit erweiterter Konversionssyntax](https://analyticsdemystified.com/adobe-analytics/advanced-conversion-syntax-merchandising/) auf [!DNL analyticsdemystified.com]
