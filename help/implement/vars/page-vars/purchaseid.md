---
title: purchaseID
description: Deduplizieren Sie Treffer basierend auf einer eindeutigen Kaufkennung.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 98%

---


# purchaseID

Die `purchaseID`-Variable verhindert, dass Berichte durch Treffer mit demselben Kauf erhöht werden. Wenn ein Besucher z. B. Ihre Kaufbestätigungsseite erreicht, senden Sie normalerweise Daten zum Umsatz, der durch die Transaktion generiert wurde, an Adobe. Wenn der Benutzer diese Seite mehrmals aktualisiert oder die Seite zu einem späteren Zeitpunkt mit Lesezeichen markiert, können diese Treffer die Berichte überhöhen. Die `purchaseID`-Variable dedupliziert Metriken, wenn mehrere Treffer dieselbe Kauf-ID haben.

Wenn Adobe einen Treffer als doppelten Kauf erkennt, werden alle Konversionsdaten (wie z. B. eVars und Ereignisse) nicht in der Berichterstellung angezeigt. In Daten-Feeds wird die `duplicate_purchase`-Spalte auf `1` gesetzt.

Die Kauf-IDs gelten für alle Besucher und laufen nicht ab. Wenn ein Besucher eine bestimmte Kauf-ID festlegt und ein anderer Besucher dieselbe Kauf-ID ein Jahr später festlegt, wird der zweite Kauf dedupliziert.

## Kauf-ID in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.purchaseID in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.purchaseID`-Variable ist eine Zeichenfolge, die eine eindeutige Kennung für einen Kauf enthält. Sie wird bei demselben Treffer wie ein Kaufereignis gesetzt. Verwenden Sie nur alphanumerische Zeichen, um diese Variable zu füllen.

Diese Variable kann maximal 20 Byte speichern. Werte, die länger als 20 Byte sind, werden abgeschnitten. Wenn dieser abgeschnittene Wert mit nachfolgenden abgeschnittenen Werten übereinstimmt, werden diese nachfolgenden Treffer dedupliziert.

```js
s.purchaseID = "ABC123";
```

Bei Verwendung der `digitalData` Datenschicht [](../../prepare/data-layer.md):

```js
s.purchaseID = digitalData.transaction.transactionID;
```

>[!CAUTION]
>
>Verwenden Sie keine Randomisierungsfunktion, um eine Kauf-ID zu generieren.