---
title: useBeacon
description: Mit useBeacon können Sie AppMeasurement zur Verwendung der sendBeacon-API des Browsers zwingen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# useBeacon

Die meisten modernen Browser beinhalten die native Methode `navigator.sendBeacon()`. Es sendet asynchron eine kleine Menge Daten über HTTP an einen Webserver. AppMeasurement kann die `navigator.sendBeacon()` Methode verwenden, wenn die `useBeacon` Variable aktiviert ist. Es ist nützlich für Ausstiegslinks und andere Situationen, in denen Sie Informationen senden möchten, bevor die Seite entladen wird.

Wenn `useBeacon` diese Option aktiviert ist, verwendet der nächste an Adobe gesendete Treffer die `navigator.sendBeacon()` Methode des Browsers anstelle einer Standard- `GET` Bildanforderung. Diese Variable gilt für [`s.t()`](../functions/t-method.md)- und [`s.tl()`](../functions/tl-method.md)-Bildanforderungen. Hierfür ist AppMeasurement 2.17.0 oder höher erforderlich.

> [!TIP] AppMeasurement aktiviert automatisch `useBeacon` Ausstiegslink-Bildanforderungen.

Die `useBeacon` Variable wird ignoriert, wenn der Besucher einen Browser verwendet, der nicht unterstützt `navigator.sendBeacon()`. Für die Verwendung dieser Variablen ist AppMeasurement 2.16.0 oder höher erforderlich.

## Beacon in Adobe Experience Platform Launch verwenden

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.useBeacon in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.useBeacon` Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `navigator.sendBeacon()` Methode des Browsers verwendet. Its default value is `false`. Legen Sie diese Variable auf `true` vor dem Aufruf einer Verfolgungsfunktion fest, wenn Sie die asynchrone Natur von verwenden möchten `navigator.sendBeacon()`.

```js
s.useBeacon = true;
```

> [!NOTE] Nach Ausführung eines Tracking-Aufrufs wird diese Variable auf `false`zurückgesetzt. Wenn Ihre Implementierung mehrere Bildanforderungen beim Laden derselben Seite sendet (z. B. Einzelseitenanwendungen), stellen Sie diese Variable auf `true` vor jedem Verfolgungsaufruf ein.
