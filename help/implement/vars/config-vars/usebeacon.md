---
title: useBeacon
description: Mit useBeacon können Sie AppMeasurement zur Verwendung der sendBeacon-API des Browsers zwingen.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# useBeacon

Die meisten modernen Browser enthalten die native Methode `navigator.sendBeacon()`. Es sendet asynchron eine kleine Menge Daten über HTTP an einen Webserver. AppMeasurement kann die `navigator.sendBeacon()` Methode verwenden, wenn die `useBeacon` Variable aktiviert ist. Es ist nützlich für Ausstiegslinks und andere Situationen, in denen Sie Informationen senden möchten, bevor die Seite entladen wird.

Wenn `useBeacon` diese Option aktiviert ist, verwendet der nächste an Adobe gesendete Treffer die `navigator.sendBeacon()` Methode des Browsers anstelle einer Standard- `GET` Bildanforderung. Diese Variable gilt für `s.t()`- und `s.tl()`-Bildanforderungen. Es erfordert AppMeasurement 2.17.0 oder höher.

> [!TIP] AppMeasurement aktiviert automatisch `useBeacon` Ausstiegslink-Bildanforderungen.

Die `useBeacon` Variable wird ignoriert, wenn der Besucher einen Browser verwendet, der nicht unterstützt `navigator.sendBeacon()`.

## Beacon in Adobe Experience Platform Launch verwenden

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.useBeacon in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.useBeacon` Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `navigator.sendBeacon()` Methode des Browsers verwendet. Its default value is `false`. Legen Sie diese Variable auf `true` vor Aufruf einer Verfolgungsfunktion fest, wenn Sie die asynchrone Natur von verwenden möchten `navigator.sendBeacon()`.

```js
s.useBeacon = true;
```

> [!NOTE] Nach Ausführung eines Tracking-Aufrufs wird diese Variable auf `false`zurückgesetzt. Wenn Ihre Implementierung mehrere Bildanforderungen beim Laden derselben Seite sendet (z. B. Einzelseitenanwendungen), stellen Sie diese Variable auf `true` vor jedem Verfolgungsaufruf ein.
