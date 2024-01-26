---
title: forceOffline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
feature: Variables
exl-id: 2e48bdf6-7de7-4976-86dd-ef3d558769c7
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 80%

---

# forceOffline

Mit der `forceOffline()`-Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

>[!WARNING]
>
>Verwenden Sie diese Funktion nur, wenn [`trackOffline`](../config-vars/trackoffline.md) aktiviert ist. Die Verwendung dieser Funktion außerhalb von Offline-Tracking kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Mit der `forceOffline()`-Methode können Sie AppMeasurement zwingen, Treffer so zu behandeln, als ob das Gerät offline wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Ihr einziger Zweck besteht darin, den Online-Status in AppMeasurement zu überschreiben.

## Offline mit dem Web SDK erzwingen

Das Web SDK unterstützt kein Offline-Tracking.

## Offline erzwingen mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.forceOffline() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Sie können die `s.forceOffline()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOffline();
```
