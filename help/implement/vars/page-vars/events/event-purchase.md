---
title: Kaufereignis
description: Verwenden Sie das Kaufereignis, um Daten zu den Metriken "Bestellungen", "Einheiten"und "Umsatz"zu erfassen.
translation-type: tm+mt
source-git-commit: 7a1c3c7ed0e509969e281e865e8ff2c969a18bcb

---


# Kaufereignis

Das purchase-Ereignis ist ein Wert in der `events` Variablen. Dieser Wert ist nützlich für Organisationen, die Daten über den Umsatz erfassen möchten, den ihre Site generiert. Es ist stark abhängig von den `products` und `purchaseID` Variablen.

Wenn Sie ein Kaufereignis festlegen, wirkt sich dies auf die folgenden Metriken aus:

* Die Metrik &quot;Bestellungen&quot;erhöht sich um 1
* Die Metrik &quot;Einheiten&quot;erhöht sich um die Anzahl der Produkte in der `products` Variablen
* Die Metrik &quot;Umsatz&quot;erhöht sich um die Summe der Preisparameter in der `products` Variablen

## Festlegen des Kaufereignisses beim Starten der Adobe Experience Platform

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie im Abschnitt &quot; [!UICONTROL Ereignisse] &quot;nach und legen Sie im Dropdown-Menü &quot;Ereignisse&quot;den [!UICONTROL Kauf]fest.

Andere abhängige Variablen wie `products` und verfügen `purchaseID` nicht über dedizierte Felder in Launch. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax für diese Variablen.

## Festlegen des Kaufereignisses in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Das purchase-Ereignis ist eine Zeichenfolge, die als Teil der events-Variablen festgelegt wird.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## Deduplizierung des Kaufereignisses

Wenn Sie ein Kaufereignis auslösen, prüft Adobe Folgendes:

* Enthält der Treffer die `purchaseID` Variable? Andernfalls verwendet Adobe Informationen aus dem Treffer, um eine &quot;temporäre Kauf-ID&quot;zu erstellen. Diese temporäre Kauf-ID gilt nur für den Besucher des Treffers. Die vorherigen 5 temporären Kauf-IDs werden für jede Besucher-ID pro Report Suite gespeichert.
* Stimmt die ID des temporären Kaufs mit einer der letzten fünf gespeicherten IDs für temporäre Käufe überein? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
* Wenn die `purchaseID` Variable definiert ist, stimmt sie mit einem Wert überein, der bereits in der Report Suite für alle Besucher erfasst wurde? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
