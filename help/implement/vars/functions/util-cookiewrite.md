---
title: Util.cookieWrite
description: Schreibt einen Wert für ein Cookie.
feature: Variables
exl-id: 079dbe50-5568-467b-a67c-f44481a4a20b
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 100%

---

# Util.cookieWrite

Cookies können Informationen über Seiten in derselben Domain hinweg speichern und abrufen. Verwenden Sie die `Util.cookieWrite()`-Methode, um einen Wert für ein Cookie festzulegen. Sie können die [`Util.cookieRead()`](util-cookieread.md)-Methode verwenden, um mit `Util.cookieWrite()` eingestellte Werte abzurufen.

## Setzen von Cookies mithilfe von Tags in Adobe Experience Platform

Die Datenerfassungs-Benutzeroberfläche bietet keine Möglichkeit, Cookies in der Benutzeroberfläche festzulegen. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.Util.cookieWrite() in AppMeasurement und im benutzerdefinierten Code-Editor

Rufen Sie die `s.Util.cookieWrite()`-Methode auf, um ein Cookie auf einen gewünschten Wert festzulegen.

```js
s.Util.cookieWrite("example_cookie","Example cookie value")
```

Es ist ein optionales drittes Argument verfügbar, das bestimmt, wann das Cookie abläuft. Cookies, die mit `s.Util.cookieWrite()` gesetzt werden, laufen standardmäßig am Ende der Browser-Sitzung ab.

```js
// Set a cookie with an expiration 6 months from now
var cookieDate = new Date();
cookieDate.setMonth(cookieDate.getMonth() + 6);
s.Util.cookieWrite("example_cookie","Example 6-month cookie",cookieDate);
```

## Beispiele

Sie können eine Variable instanziieren, wenn ein Cookie erfolgreich geschrieben wurde. Diese Variable ist ein boolescher Wert.

```js
var success = s.Util.cookieWrite("example_cookie","Example cookie value");
if (success) {
  console.log("Cookie written successfully");
} else {
  console.log("Cookie write failed");
}
```
