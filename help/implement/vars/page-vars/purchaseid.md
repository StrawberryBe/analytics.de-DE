---
title: purchaseID
description: Deduplizieren Sie Treffer basierend auf einer eindeutigen Kaufkennung.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# purchaseID

Die `purchaseID` Variable verhindert, dass Berichte durch Treffer mit demselben Kauf erhöht werden. Wenn ein Besucher z. B. Ihre Kaufbestätigungsseite erreicht, senden Sie normalerweise Daten zum Umsatz, der durch die Transaktion generiert wurde, an Adobe. Wenn der Benutzer diese Seite mehrmals aktualisiert oder die Seite zu einem späteren Zeitpunkt mit Lesezeichen markiert, können diese Treffer die Berichte in die Höhe treiben. Die `purchaseID` Variable dedupliziert Metriken, wenn mehrere Treffer dieselbe Kauf-ID haben.

Wenn Adobe einen Treffer als doppelten Kauf erkennt, werden nicht alle Konversionsdaten (wie z. B. eVars und Ereignisse) in Berichten angezeigt. In Datenfeeds wird die `duplicate_purchase` Spalte auf `1`.

Die Kauf-IDs gelten für alle Besucher und laufen nicht ab. Wenn ein Besucher eine bestimmte Kauf-ID festlegt und ein anderer Besucher dieselbe Kauf-ID ein Jahr später festlegt, wird der zweite Kauf dedupliziert.

## Kauf-ID beim Start der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.purchaseID in AppMeasurement und benutzerdefinierten Code-Editor starten

Die `s.purchaseID` Variable ist eine Zeichenfolge, die einen eindeutigen Bezeichner für einen Kauf enthält. Er wird für denselben Treffer wie ein Kaufereignis festgelegt. Verwenden Sie nur alphanumerische Zeichen, um diese Variable zu füllen.

Diese Variable kann maximal 20 Byte speichern. Werte, die länger als 20 Byte sind, werden abgeschnitten. Wenn dieser abgeschnittene Wert mit nachfolgenden abgeschnittenen Werten übereinstimmt, werden diese nachfolgenden Treffer dedupliziert.

```js
s.purchaseID = "ABC123";
```

> [!NOTE] Verwenden Sie keine Randomisierungsfunktion, um eine Kauf-ID zu generieren. Adobe recommends using a [data layer](../../prepare/data-layer.md) to store a given purchase ID.
