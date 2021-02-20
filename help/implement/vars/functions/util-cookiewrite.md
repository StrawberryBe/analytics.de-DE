---
title: Util.cookieWrite
description: Schreibt einen Wert für ein Cookie.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 100%

---


# Util.cookieWrite

Cookies können Informationen über Seiten in derselben Domäne hinweg speichern und abrufen. Verwenden Sie die `Util.cookieWrite()`-Methode, um einen Wert für ein Cookie festzulegen. Sie können die [`Util.cookieRead()`](util-cookieread.md)-Methode verwenden, um mit `Util.cookieWrite()` eingestellte Werte abzurufen.

## Setzen von Cookies in Adobe Experience Platform Launch

Launch bietet keine Möglichkeit, Cookies in der Oberfläche einzustellen. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.Util.cookieWrite() in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

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
