---
title: usePlugins
description: Aktivieren oder deaktivieren Sie die Funktion doPlugins().
translation-type: tm+mt
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# usePlugins

Wenn `usePlugins` diese Option aktiviert ist, wird die `doPlugins()` Funktion kurz vor der AppMeasurement-Kompilierung ausgeführt und ein Treffer an Adobe gesendet. Aktivieren Sie diese Variable, wenn Sie die `doPlugins()` Funktion verwenden.

## Verwenden von Plug-ins in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.usePlugins in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.usePlugins` Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `doPlugins()` Funktion aufruft. Its default value is `false`. Legen Sie diese Variable auf `true` fest, wenn Sie die `doPlugins()` Funktion in Ihrer Implementierung verwenden.

```js
s.usePlugins = true;
```
