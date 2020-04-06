---
title: forceOnline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# forceOnline

Mit der `forceOnline()`-Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

>[!IMPORTANT] Verwenden Sie diese Methode nur, wenn sie aktiviert [`trackOffline`](../config-vars/trackoffline.md) ist. Die Verwendung dieser Funktion außerhalb von Offline-Tracking kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Mit der `forceOnline()`-Methode können Sie AppMeasurement zwingen, Treffer so zu behandeln, als ob das Gerät online wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Ihr einziger Zweck besteht darin, den Online-Status in AppMeasurement zu überschreiben.

## Online erzwingen in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.forceOnline() in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Sie können die `s.forceOnline()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOnline();
```
