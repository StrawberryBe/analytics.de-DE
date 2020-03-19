---
title: Kaufereignis
description: Verwenden Sie das Ereignis purchase, um Daten zu den Metriken "Bestellungen", "Einheiten"und "Umsatz"zu erfassen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Kaufereignis

Das purchase-Ereignis ist ein Wert in der `events` Variablen. Dieser Wert ist nützlich für Organisationen, die Daten über den Umsatz erfassen möchten, den ihre Site generiert. Es ist stark abhängig von den [`products`](../products.md) und [`purchaseID`](../purchaseid.md) Variablen.

Wenn Sie ein Ereignis zum Einkauf festlegen, wirkt sich dies auf die folgenden Metriken aus:

* Die Metrik &quot;Bestellungen&quot;erhöht sich um 1
* Die Metrik &quot;Einheiten&quot;erhöht sich um die Anzahl der Produkte in der `products` Variablen
* Die Metrik &quot;Umsatz&quot;erhöht sich um die Summe der Preisparameter in der `products` Variablen

## Festlegen des Ereignisses purchase in Adobe Experience Platform Launch

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Suchen Sie den [!UICONTROL Events] Abschnitt und legen Sie im Dropdown-Menü &quot;Ereignis&quot; [!UICONTROL purchase]fest.

Andere abhängige Variablen wie `products` und verfügen `purchaseID` nicht über dedizierte Felder in Launch. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax für diese Variablen.

## Festlegen des Ereignisses purchase in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Das purchase-Ereignis ist eine Zeichenfolge, die als Teil der Variablen &quot;Ereignisses&quot;festgelegt wird.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## Deduplizierung des Ereignisses im Kauf

Wenn Sie ein Ereignis zum Kauf auslösen, prüft Adobe Folgendes:

* Enthält der Treffer die `purchaseID` Variable? Andernfalls verwendet Adobe Informationen aus dem Treffer, um eine &quot;temporäre Kauf-ID&quot;zu erstellen. Diese temporäre Kauf-ID gilt nur für den Besucher des Treffers. Die vorherigen 5 temporären Kauf-IDs werden für jede Besucher-ID pro Report Suite gespeichert.
* Stimmt die ID des temporären Kaufs mit einer der letzten fünf gespeicherten IDs für temporäre Käufe überein? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
* Wenn die `purchaseID` Variable definiert ist, stimmt sie mit einem Wert überein, der bereits in der Report Suite für alle Besucher erfasst wurde? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
