---
description: Beim Kaufereignis werden Analytics-Variablen verwendet, um Informationen zu dem jeweiligen Einkauf zu erfassen. Mithilfe der Variablen „s.purchaseID“ wird das Ereignis serialisiert (d. h., Duplikate werden entfernt).
keywords: Analytics-Implementierung
seo-description: Beim Kaufereignis werden Analytics-Variablen verwendet, um Informationen zu dem jeweiligen Einkauf zu erfassen. Mithilfe der Variablen „s.purchaseID“ wird das Ereignis serialisiert (d. h., Duplikate werden entfernt).
seo-title: Kaufereignisse
solution: Analytics
title: Kaufereignisse
topic: Entwickler und Implementierung
uuid: d 90 cdec 7-7397-445 a -84 e 5-31014 f 7 ff 875
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kaufereignisse

Beim Kaufereignis werden Analytics-Variablen verwendet, um Informationen zu dem jeweiligen Einkauf zu erfassen. Mithilfe der Variablen „s.purchaseID“ wird das Ereignis serialisiert (d. h., Duplikate werden entfernt).

The *`purchaseID`* is limited to 20 characters. Die Variable *`purchaseID`* serialisiert alle Ereignisse, die in der Variablen [!UICONTROL s.events] übergeben werden, und überschreibt alle Serialisierungswerte für Ereignisse. If *`purchaseID`* is left blank, each instance of the purchase event, even page reloads, is counted.

Wenn ein Kaufereignis ohne die Variable *`purchaseID`* aufgerufen wird, wird anhand der Variablen *`s.products`* und *`s.events`automatisch eine eindeutige ID generiert.* Diese automatisch generierte Variable *`purchaseID`wird im Browser des Besuchers lokal als Cookie gespeichert und wird an keine Report Suite-Tabellen gesendet.* Manually defined *`purchaseID`*s on the other hand are sent to a back-end table within the report suite. The last five purchases made by a visitor (with or without *`purchaseID`*) are stored in the local cookie.

Wenn ein Besucher einen Einkauf abschließt, werden die folgenden Prüfungen durchgeführt:

* Entspricht die *`purchaseID`* einem der fünf Cookie-Werte? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
* If *`purchaseID`* is defined, does it match any value in the report suite's back-end table? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
* Wenn die Variable *`purchaseID`* weder mit einem der fünf im Cookie gespeicherten Werte übereinstimmt noch mit einer Variablen *`purchaseID`in der Tabelle der Report Suite, ist die Bildanforderung eindeutig und wird in das Reporting aufgenommen.* Wenn das lokale Cookie beispielsweise bereits fünf Käufe enthält, wird der älteste Wert überschrieben.

Mithilfe von speziellem serverseitigem Code kann die eindeutige Nummer generiert werden (ein alphanumerischer Wert), die in den HTML-Quellcode eingebettet wird. Zu diesem Zweck wird meist die Bestell-ID oder ein ähnlicher alphanumerischer Wert verwendet. Dieser Wert sollte sich nicht ändern, wenn der Benutzer die Seite aktualisiert. Nachfolgend ist ein kurzes Beispiel dargestellt (der *`purchaseID`*-Code ist fettgedruckt):

## Syntax {#section_4FBF138093BD41F59885D2ACC429FF5B}

```js
s.products="Category;ProductName;Qty;total_price [,Category2;ProductName2;Qty;total_price]" 
s.state="XX" 
s.zip="00000" 
 
<b>s.purchaseID="<%=getPurchaseID()%>"</b> 
s.events="purchase" 
```

## Beispiele {#section_2CBA9B6386A146C0BEF375E1B55687BC}

```js
s.products="Footwear;Hiking Boots (1234);1;170.00" 
s.state="UT" 
s.zip="84097" 
s.purchaseID="12341234" 
s.events="purchase"
```

## Weitere Hinweise {#section_5A0590B8FD4F40DC89776F55ED9DE668}

* Achten Sie darauf, zum Generieren der eindeutigen ID für das Ereignis serverseitigen Code einzusetzen. Verwenden Sie dazu keine Zufallsfunktion von JavaScript, weil dann sobald die Seite geladen wird (d. h. bei jeder [!UICONTROL Instanz]/[!UICONTROL pageview]-Zählung) eine neue eindeutige ID generiert würde.

* Die eindeutigen IDs gelten für alle Benutzer in sämtlichen Sitzungen. Daher müssen Sie sicherstellen, dass diese IDs über alle Benutzer und Sitzungen hinweg eindeutig sind. Wenn sich zum Beispiel die Bestell-ID nach 30 Tagen wiederholt, hängen Sie am Ende der Bestellung das Datum an, damit die [!UICONTROL Bestell-ID] ausreichend eindeutig ist.
* Als Serialisierungswerte sind alphanumerische Werte mit einer Länge von maximal 20 Zeichen zulässig. Das ist die gleiche Einschränkung wie bei [!UICONTROL s.purchaseID] (bei G Code muss „s.“ mit „s_“ ersetzt werden).
* Die Variable [!UICONTROL s.purchaseID] serialisiert alle Ereignisse, die in der Variablen [!UICONTROL s.events] übergeben werden, und überschreibt alle Serialisierungswerte für Ereignisse. Nehmen Sie keine [!UICONTROL Ereignis-Serialisierung] bei Ereignissen vor, wenn die Variable [!UICONTROL s.purchaseID] auf der aktuellen Seite verwendet wird (bei G Code muss „s.“ mit „s_“ ersetzt werden).

