---
title: usePlugins
description: Aktivieren oder deaktivieren Sie die doPlugins()-Funktion.
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 76%

---

# usePlugins

Wenn `usePlugins` aktiviert ist, wird die [`doPlugins()`](../functions/doplugins.md)-Funktion kurz vor der AppMeasurement-Kompilierung ausgeführt und ein Treffer an Adobe gesendet. Aktivieren Sie diese Variable, wenn Sie die `doPlugins()`-Funktion verwenden.

## Verwenden von Plug-ins mit Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein dediziertes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.usePlugins in AppMeasurement und im benutzerdefinierten Code-Editor in 

Die `s.usePlugins`-Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `doPlugins()`-Funktion aufruft. Der Standardwert lautet `false`. Setzen Sie diese Variable auf `true`, wenn Sie die `doPlugins()`-Funktion in Ihrer Implementierung verwenden.

```js
s.usePlugins = true;
```
