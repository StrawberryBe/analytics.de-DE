---
title: forceOffline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# forceOffline

Mit der `forceOffline` Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

> [!IMPORTANT] Verwenden Sie diese Funktion nur, wenn sie aktiviert `trackOffline` ist. Die Verwendung dieser Funktion außerhalb der Offline-Verfolgung kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Mit der `forceOffline` Methode können Sie AppMeasurement zwingen, Treffer so zu behandeln, als ob das Gerät offline wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Sein einziger Zweck besteht darin, den Online-Status in AppMeasurement zu überschreiben.

## Offline-Start in Adobe Experience Platform erzwingen

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.forceOffline() in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Sie können die `s.forceOffline()` Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOffline();
```
