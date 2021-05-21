---
title: usePlugins
description: Aktivieren oder deaktivieren Sie die doPlugins()-Funktion.
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '95'
ht-degree: 100%

---

# usePlugins

Wenn `usePlugins` aktiviert ist, wird die [`doPlugins()`](../functions/doplugins.md)-Funktion kurz vor der AppMeasurement-Kompilierung ausgeführt und ein Treffer an Adobe gesendet. Aktivieren Sie diese Variable, wenn Sie die `doPlugins()`-Funktion verwenden.

## Verwenden von Plug-ins in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.usePlugins in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.usePlugins`-Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `doPlugins()`-Funktion aufruft. Der Standardwert lautet `false`. Setzen Sie diese Variable auf `true`, wenn Sie die `doPlugins()`-Funktion in Ihrer Implementierung verwenden.

```js
s.usePlugins = true;
```
