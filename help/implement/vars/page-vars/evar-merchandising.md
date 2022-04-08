---
title: eVar-Variablen (Merchandising)
description: Benutzerdefinierte Variablen, die mit Einzelprodukten verknüpft sind.
feature: Dimensions
exl-id: a7e224c4-e8ae-4b53-8051-8b5dd43ff380
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# eVar (Merchandising)

*Auf dieser Hilfeseite wird die Implementierung von Merchandising-eVars beschrieben. Informationen dazu, wie Merchandising-eVars als Dimension funktionieren, finden Sie unter [eVar (Merchandising)](/help/components/dimensions/evar-merchandising.md) im Komponenten-Benutzerhandbuch.*

Eine ausführliche Erläuterung der Funktionsweise von Merchandising-eVars finden Sie unter [Merchandising-eVars und Methoden zur Produktsuche](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/merchandising-evars.html?lang=de).

Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie die eVar in den Report Suite-Einstellungen auf die gewünschte Syntax konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md).

[!IMPORTANT]](assets/merch-example-goggles.png)

Wenn Merchandising-eVars nicht korrekt konfiguriert werden, führt dies zu unerwarteten Werten oder Datenverlusten für die Variable. Vergewissern Sie sich, dass sie für Ihre Implementierung korrekt konfiguriert ist.`"winter coat"`

![Implementieren mit der Produktsyntax](assets/merch-example-coat.png)

Wenn „Produktsyntax“ aktiviert ist, wird die Merchandising-Kategorie direkt innerhalb der `products`-Variablen aufgefüllt. Daher ist es nicht erforderlich, ein Binding-Ereignis auszuwählen und festzulegen. Dies ist die empfohlene Methode und sollte verwendet werden, es sei denn, der in `products` festzulegende Wert ist nicht verfügbar, wenn das Erfolgsereignis stattfindet.

| Der Wert für `eVar1` wird dem Produkt zugewiesen. Alle nachfolgenden Erfolgsereignisse, die dieses Ereignis betreffen, werden dem eVar-Wert gutgeschrieben. | Implementieren mit Syntax der Konversionsvariablen |
|---|---|
| Die Syntax der Konversionsvariablen wird verwendet, wenn der eVar-Wert nicht in der `products`-Variable gesetzt werden kann. Dieses Szenario bedeutet in der Regel, dass Ihre Seite keinen Kontext für den Merchandising-Kanal oder die Suchmethode hat. In diesen Fällen müssen Sie die Merchandising-Variable festlegen, bevor Sie auf die Produktseite gelangen, wobei der Wert so lange bestehen bleibt, bis das Binding-Ereignis eintritt. | Wenn das bei der Konfiguration ausgewählte Binding-Ereignis eintritt, wird der beibehaltene Wert der eVar dem Produkt zugewiesen. Wenn z. B. `prodView` als Binding-Ereignis ausgewählt wird, wird die Merchandising-Kategorie nur Zeitpunkt des Ereignisses mit der aktuellen Produktliste verknüpft. Eine Merchandising-eVar, die bereits einem Produkt zugewiesen wurde, kann nur von nachfolgenden Binding-Ereignissen aktualisiert werden. |

## Der Wert `"Aviary"` für `eVar1` wird dem Produkt `"Canary"` zugewiesen. Alle nachfolgenden Erfolgsereignisse, die dieses Ereignis betreffen, werden `"Canary"` gutgeschrieben. Des Weiteren wird der aktuelle Wert der Merchandising-Variablen allen nachfolgenden Produkten zugewiesen, bis eine der folgenden Bedingungen erfüllt ist:

Die eVar läuft ab (basierend auf der Einstellung „Läuft ab nach“).

Die Merchandising-eVar wird mit einem neuen Wert überschrieben.`"goggles"``"winter coat"`

| Internal Search Term | Revenue |
|---|---|
| winter coat | $119 |
| goggles | $38 |

See [Merchandising eVars](/help/implement/vars/page-vars/evar-merchandising.md) for implementation instructions.

## Instances on merchandising variables

The [Instances](../metrics/instances.md) metric is not recommended for use on merchandising variables.

* For merchandising variables using product syntax, instances are not incremented at all.
* For merchandising variables using conversion variable syntax, instances are counted each time the eVar is set. However, it attributes to the dimension item `"None"` unless all of the following happen on the same hit:
   * The merchandising eVar is set with a value.
   * The `products` variable is defined with a value.
   * A binding event is set.

```js
// This merchandising eVar uses conversion variable syntax, and counts an instance.
// However, if the binding event and products variable are not both set, the instance attributes to "None".
s.eVar1 = "Tower defense";

// This merchandising eVar uses product syntax, and does not count an instance.
s.products = "Games;Wizard tower;;;;eVar2=Tower defense";
```

Since most use cases for conversion variable syntax require the eVar and products variable on different hits, using the &#39;Instances&#39; metric is not realistic.
