---
title: useBeacon
description: Mit useBeacon können Sie AppMeasurement zur Verwendung der sendBeacon-API des Browsers zwingen.
keywords: Analytics Implementation
translation-type: ht
source-git-commit: 6c57780d0ecf65669c1a5306dde267f6e48f1cc4

---


# s.useBeacon

Die `s.useBeacon`-Variable zwingt die nächste Anforderung zur Verwendung der [sendBeacon-API](https://developer.mozilla.org/de-DE/docs/Web/API/Navigator/sendBeacon) des Browsers. Mithilfe von `s.sendBeacon` kann eine HTTP-Anforderung außerhalb des Kontexts einer Seite versendet werden. Es ist nützlich für Exitlinks und andere Situationen, in denen Sie Informationen vor dem Entladen der Seite senden möchten.

Das Festlegen dieses Werts gilt nur für die nächste Anforderung, die AppMeasurement auslöst. Nachdem die Anforderung ausgelöst wurde, wird `s.useBeacon` wieder auf „false“ zurückgesetzt. Diese Variable gilt für `s.t()`- und `s.tl()`-Bildanforderungen.

Für die Verwendung der `s.useBeacon`-Variable ist AppMeasurement 2.17.0 oder höher erforderlich.

> [!NOTE] [Exitlinks](s-linktrackvars.md) verwenden diese Variable automatisch ohne zusätzliche Konfiguration.

## Syntax

```js
s.useBeacon = true;
```
