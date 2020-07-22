---
title: eVar (Merchandising)
description: Benutzerdefinierte Variablen, die mit der Produktdimension verknüpft sind.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 25%

---


# eVar (Merchandising)

*Auf dieser Hilfeseite wird beschrieben, wie Merchandising-eVars als Dimension funktionieren. For information on how to implement merchandising eVars, see[eVars](/help/implement/vars/page-vars/evar.md)in the Implement user guide.*

Wenn Sie den Erfolg von externen Kampagnen oder externen Suchbegriffen messen möchten, wünschen Sie in der Regel einen einzigen Wert, den Sie für jedes eingetretene Erfolgsereignis der jeweiligen Kampagne oder dem Suchbegriff gutschreiben können. Wenn ein Kunde z. B. auf einen Link in einer E-Mail-Kampagne klickt, um Ihre Website zu besuchen, sollten alle daraus resultierenden Käufe dieser Kampagne gutsgeschrieben werden.

Wie sieht es mit Ereignissen aus, die von der internen Suche oder vom Durchsuchen von Kategorien angetrieben werden, wenn ein Kunde nach mehreren Artikeln sucht? For example, a customer searches your site for `"goggles"`, then adds a pair to their cart:

![Beispiel für Skibrille](assets/merch-example-goggles.png)

Before checkout, the customer searches for `"winter coat"`, then adds a down jacket to the to their cart:

![Beispiel](assets/merch-example-coat.png)

Wenn der Besucher diesen Einkauf abgeschlossen hat, haben Sie eine interne Suche nach einer `"winter coat"` Gutschrift für den Kauf einer Skibrille (vorausgesetzt, die eVar verwendet die Standardzuordnung von &quot;Zuletzt verwendet&quot;). Good for `"winter coat"`, but bad for marketing decisions:

| Interner Suchbegriff | Umsatz |
|---|---|
| Winterjacke | 157 $ |

## So können Merchandising-Variablen das Problem lösen

Mit Merchandising-eVars können Sie einem Produkt den aktuellen Wert einer eVar zum Zeitpunkt des Erfolgsereignisses zuweisen. Der Wert bleibt daraufhin mit dem Produkt verknüpft, selbst wenn später einer oder mehrere weitere Werte für die jeweilige „eVar“ gesetzt werden.

If merchandising is enabled for the eVar in the previous example, the search term `"goggles"` is tied to the snow goggles, and the search term `"winter coat"` is tied to the down jacket. Merchandising-eVars ordnen Umsatz auf Produktebene zu, sodass jeder Begriff den Umsatz für das Produkt gutschreibt, mit dem der Begriff verbunden war:

| Interner Suchbegriff | Umsatz |
|---|---|
| Winterjacke | 119 $ |
| Skibrille | 38 $ |

Implementierungsanweisungen finden Sie unter [Merchandising eVars](/help/implement/vars/page-vars/evar-merchandising.md) .

## Instanzen auf Merchandising-Variablen

Die Metrik &quot; [Instanzen](../metrics/instances.md) &quot;wird für die Verwendung in Merchandising-Variablen nicht empfohlen.

* Bei Merchandising-Variablen mit Produktsyntax werden Instanzen überhaupt nicht inkrementiert.
* Bei Merchandising-Variablen mit Konversionsvariablensyntax werden Instanzen jedes Mal gezählt, wenn die eVar eingestellt wird. Er weist jedoch dem Dimensionselement zu, `"None"` es sei denn, dass beim selben Treffer alle folgenden Ereignisse eintreten:
   * Die Merchandising-eVar wird mit einem Wert eingestellt.
   * Die `products` Variable wird mit einem Wert definiert.
   * Ein Binding-Ereignis wird gesetzt.

```js
// This merchandising eVar uses conversion variable syntax, and counts an instance.
// However, if the binding event and products variable are not both set, the instance attributes to "None".
s.eVar1 = "Tower defense";

// This merchandising eVar uses product syntax, and does not count an instance.
s.products = "Games;Wizard tower;;;;eVar2=Tower defense";
```

Da die meisten Anwendungsfälle für die Konversionsvariablensyntax die eVar- und die products-Variable bei verschiedenen Treffern erfordern, ist die Verwendung der Metrik &quot;Instanzen&quot;nicht realistisch.
