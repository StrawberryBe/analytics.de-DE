---
description: Beim Kaufereignis werden Analytics-Variablen verwendet, um Informationen zu dem jeweiligen Einkauf zu erfassen. Mithilfe der Variablen „s.purchaseID“ wird das Ereignis serialisiert (d. h., Duplikate werden entfernt).
keywords: Analytics Implementation
title: Kaufereignisse
topic: Developer and implementation
uuid: d90cdec7-7397-445a-84e5-31014f7ff875
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Kaufereignisse

Beim Kaufereignis werden Analytics-Variablen verwendet, um Informationen zu dem jeweiligen Einkauf zu erfassen. Mithilfe der Variablen `s.purchaseID` wird das Ereignis serialisiert (d. h. Duplikate werden entfernt).

Wenn ein Treffer mit einem Kaufereignis ohne Kauf-ID weitergeleitet wird, verwendet Adobe Analytics Informationen aus dem Treffer (s.purchase und s.events), um eine "temporäre Kauf-ID"zu erstellen. Diese temporäre Kauf-ID gilt nur für den Besucher des Treffers. Die vorherigen 5 temporären Kauf-IDs werden für jede Besucher-ID (pro Report Suite) gespeichert.

Wenn ein Besucher einen Einkauf abschließt, werden die folgenden Prüfungen durchgeführt:

* Entspricht die ID für temporären Kauf mit einer der letzten fünf gespeicherten ID für temporären Kauf übereinstimmen? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
* Entspricht `s.purchaseID` es, falls definiert, einem Wert, der bereits in der Report Suite erfasst wurde? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.

Mithilfe von speziellem serverseitigem Code kann die eindeutige Nummer generiert werden (ein alphanumerischer Wert), die in den HTML-Quellcode eingebettet wird. Zu diesem Zweck wird meist die Bestell-ID oder ein ähnlicher alphanumerischer Wert verwendet. Dieser Wert sollte sich nicht ändern, wenn der Benutzer die Seite aktualisiert.

## Syntax

```js
s.purchaseID="12345678";
```

## Beispiele

```js
s.products="Footwear;Hiking Boots;1;170.00";
s.purchaseID="12345678";
s.events="purchase";
```

## Weitere Hinweise

* Verwenden Sie keine JavaScript-Randomisierungsfunktion, um eine Zahl zu generieren, die bei jedem Laden der Seite eindeutige Zahlen generiert. Adobe empfiehlt die Verwendung einer Datenschicht zum Speichern einer bestimmten Kauf-ID.
* Die eindeutigen IDs gelten für alle Benutzer in sämtlichen Sitzungen. Stellen Sie sicher, dass alle Kauf-IDs wirklich eindeutig sind.
* Gültige Werte sind alphanumerische Werte mit einer Länge von bis zu 20 Zeichen.
* Die Variable `s.purchaseID``s.events` serialisiert alle Ereignisse, die in der Variablen   übergeben werden, und überschreibt alle Serialisierungswerte für Ereignisse. Verwenden Sie keine [!UICONTROL Ereignis-Serialisierung] für Ereignisse, wenn die `s.purchaseID` Variable auf der aktuellen Seite verwendet wird.
* If the `s.purchaseID` variable is left blank, each instance of the purchase event, even page reloads, is counted.
