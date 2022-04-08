---
title: forceOffline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
feature: Variables
exl-id: 2e48bdf6-7de7-4976-86dd-ef3d558769c7
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '141'
ht-degree: 100%

---

# forceOffline

Mit der `forceOffline()`-Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

>[!IMPORTANT]
>
>Verwenden Sie diese Funktion nur, wenn [`trackOffline`](../config-vars/trackoffline.md) aktiviert ist. Die Verwendung dieser Funktion außerhalb von Offline-Tracking kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Mit der `forceOffline()`-Methode können Sie AppMeasurement zwingen, Treffer so zu behandeln, als ob das Gerät offline wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Ihr einziger Zweck besteht darin, den Online-Status in AppMeasurement zu überschreiben.

## Erzwingen von Offline mithilfe von Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.forceOffline() in AppMeasurement und im benutzerdefinierten Code-Editor

Sie können die `s.forceOffline()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOffline();
```
