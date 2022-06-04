---
title: forceOnline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
feature: Variables
exl-id: 318408bf-bec6-49aa-a762-9d2eebab233e
source-git-commit: 3f4d8df911c076a5ea41e7295038c0625a4d7c85
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# forceOnline

Mit der `forceOnline()`-Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

>[!WARNING]
>
>Verwenden Sie diese Methode nur, wenn [`trackOffline`](../config-vars/trackoffline.md) aktiviert ist. Die Verwendung dieser Funktion außerhalb von Offline-Tracking kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Mit der `forceOnline()`-Methode können Sie AppMeasurement zwingen, Treffer so zu behandeln, als ob das Gerät online wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Ihr einziger Zweck besteht darin, den Online-Status in AppMeasurement zu überschreiben.

## Erzwingen von Online mithilfe von Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.forceOnline() in AppMeasurement und im benutzerdefinierten Code-Editor

Sie können die `s.forceOnline()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOnline();
```
