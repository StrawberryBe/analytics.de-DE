---
title: forceOnline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# forceOnline

Mit der `forceOnline` Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

> [!IMPORTANT] Verwenden Sie diese Funktion nur, wenn sie aktiviert `trackOffline` ist. Die Verwendung dieser Funktion außerhalb der Offline-Verfolgung kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Sie können die `forceOnline` Methode verwenden, um AppMeasurement zu zwingen, Treffer so zu behandeln, als ob das Gerät online wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Sein einziger Zweck besteht darin, den Online-Status in AppMeasurement zu überschreiben.

## Online in Adobe Experience Platform Launch erzwingen

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.forceOnline() in AppMeasurement und Benutzerdefinierter Code-Editor starten

Sie können die `s.forceOnline()` Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOnline();
```
