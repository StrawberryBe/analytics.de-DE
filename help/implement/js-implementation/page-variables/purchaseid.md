---
description: Erfahren Sie mehr über die Variable purchaseID, die verhindert, dass doppelte Käufe in Adobe Analytics angezeigt werden.
keywords: duplicate,purchase,purchaseid,s.purchaseid
subtopic: Variables
title: purchaseID
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# purchaseID

The `purchaseID` variable is used to keep an order from being counted multiple times in reporting. Whenever the purchase event is used on your site, Adobe recommends using the `purchaseID` variable.

Wenn ein Besucher einen Artikel von Ihrer Site kauft, `purchaseID` wird er normalerweise auf der Seite "Vielen Dank"oder "Auftragsbestätigung"ausgefüllt. Legen Sie die `purchaseID` Variable gleichzeitig fest, wenn ein Kaufereignis ausgelöst wird. Wenn ein eindeutiger Wert definiert `purchaseID` ist, zählen die Werte der Konversionsvariablen nur für Treffer mit dieser eindeutigen Kauf-ID. Die Definition `purchaseID` ist nützlich, da Besucher normalerweise eine Kaufbestätigungsseite für ihre eigenen Zwecke mit einem Lesezeichen versehen. Wenn Ihre Implementierung nicht verwendet `purchaseID`wird, können Konversionsdaten (z. B. Umsatz) leicht durch die Aktualisierung von Seiten durch die Besucher aufgebläht werden.

Zusätzlich zu den Kaufdaten werden alle Konversionsvariablen und -ereignisse nicht mehrmals für Treffer mit derselben Kauf-ID gezählt.

## Syntax

Die `purchaseID` Variable kann einen beliebigen alphanumerischen Wert bis zu maximal 20 Byte enthalten. Wenn Sie eine Kauf-ID festlegen, die länger als 20 Byte ist, wird der Wert abgeschnitten.

```js
s.purchaseID = "uniqueid";
```
