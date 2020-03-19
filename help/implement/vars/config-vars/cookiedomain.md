---
title: cookieDomain
description: Die Variable "cookieDomain"hilft bei der Bestimmung der Domäne, in der Cookies gesetzt werden sollen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# cookieDomain

> [!IMPORTANT] Diese Variable wird eingestellt. Verwenden Sie [`trackingServer`](trackingserver.md) stattdessen.

Die `cookieDomain` Variable bestimmt die Domäne, in der AppMeasurement Cookies setzt. Mit dieser Variablen können Sie explizit die Cookie-Domäne festlegen, anstatt die [`cookieDomainPeriods`](cookiedomainperiods.md) Variable zu verwenden.

Diese Variable muss nur verwendet werden, wenn **beide** der folgenden Bedingungen erfüllt sind:

* Wenn Ihre Implementierung Erstanbieter-Cookies verwendet. Diese Variable ist bei Implementierungen mit einem [`trackingServer`](trackingserver.md) Wert, der `sc.omtrdc.net`enthält, nicht erforderlich.
* Wenn Ihre Domäne einen Punkt in ihrem Suffix hat. Beispielsweise `example.co.uk` könnte die `cookieDomain` Variable die explizite Angabe enthalten, dass die Cookie-Domäne `example.co.uk` und nicht `co.uk`lautet.

Nur eine kleine Anzahl von Implementierungen verwenden die `cookieDomain` Variable, und selbst dann können alternative Variablen wie [`cookieDomainPeriods`](cookiedomainperiods.md) verwendet werden.

## Cookie-Domäne beim Start der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.cookieDomain in AppMeasurement und benutzerdefinierten Code-Editor starten

Die `cookieDomain` Variable ist eine Zeichenfolge und auf die Domäne eingestellt, in der Sie Cookies speichern möchten.

```js
s.cookieDomain = "stats.example.com";
```
