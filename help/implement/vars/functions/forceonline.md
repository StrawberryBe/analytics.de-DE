---
title: forceOnline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
feature: Variables
exl-id: 318408bf-bec6-49aa-a762-9d2eebab233e
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 80%

---

# forceOnline

Mit der `forceOnline()`-Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

>[!WARNING]
>
>Verwenden Sie diese Methode nur, wenn [`trackOffline`](../config-vars/trackoffline.md) aktiviert ist. Die Verwendung dieser Funktion außerhalb von Offline-Tracking kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Mit der `forceOnline()`-Methode können Sie AppMeasurement zwingen, Treffer so zu behandeln, als ob das Gerät online wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Ihr einziger Zweck besteht darin, den Online-Status in AppMeasurement zu überschreiben.

## Online mithilfe des Web SDK erzwingen

Das Web SDK unterstützt kein Offline-Tracking.

## Online mithilfe der Adobe Analytics-Erweiterung erzwingen

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.forceOnline() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Sie können die `s.forceOnline()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOnline();
```
