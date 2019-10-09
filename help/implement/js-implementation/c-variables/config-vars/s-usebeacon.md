---
title: useBeacon
description: Mit useBeacon können Sie AppMeasurement zur Verwendung der Browser sendBeacon API zwingen
keywords: Analytics-Implementierung
seo-description: Mit useBeacon können Sie AppMeasurement zur Verwendung der Browser sendBeacon API zwingen
translation-type: tm+mt
source-git-commit: f89d909e539cee2b78798c165fcb405773418056

---


# s.useBeacon

Die `s.useBeacon` Variable zwingt die nächste Anforderung zur Verwendung der [sendBeacon-API](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/sendBeacon)des Browsers. Mithilfe dieser Funktion `s.sendBeacon` kann eine HTTP-Anforderung außerhalb des Kontexts einer Seite gesendet werden. Es ist nützlich für Ausstiegslinks und andere Situationen, in denen Sie Informationen vor dem Entladen der Seite senden möchten.

Das Festlegen dieses Werts gilt nur für die nächste Anforderung, die AppMeasurement auslöst. Nachdem die Anforderung ausgelöst wurde, wird `s.useBeacon` sie auf "false"zurückgesetzt. Diese Variable gilt für Bildanforderungen `s.t()` und `s.tl()` Bildanforderungen.

Für die Verwendung der `s.useBeacon` Variablen ist AppMeasurement 2.17.0 oder höher erforderlich.

> [!NOTE] [ExitLinks](s-linktrackvars.md) verwendet diese Variable automatisch ohne zusätzliche Konfiguration.

## Syntax

```js
s.useBeacon = true;
```
