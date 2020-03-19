---
title: forceOnline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# forceOnline

Mit der `forceOnline()` Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

> [!IMPORTANT] Verwenden Sie diese Methode nur, wenn sie aktiviert [`trackOffline`](../config-vars/trackoffline.md) ist. Die Verwendung dieser Funktion außerhalb der Offline-Verfolgung kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Sie können die `forceOnline()` Methode verwenden, um AppMeasurement zu zwingen, Treffer so zu behandeln, als ob das Gerät online wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Sein einziger Zweck besteht darin, den Online-Status in AppMeasurement außer Kraft zu setzen.

## Online in Adobe Experience Platform Launch erzwingen

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.forceOnline() in AppMeasurement und Benutzerdefinierter Code-Editor starten

Sie können die `s.forceOnline()` Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOnline();
```
