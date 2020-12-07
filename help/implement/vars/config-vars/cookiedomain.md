---
title: cookieDomain
description: Die Variable „cookieDomain“ hilft bei der Bestimmung der Domäne, in der Cookies gesetzt werden sollen.
translation-type: tm+mt
source-git-commit: dfe2b09b2ee287219d18099c51b6fbd7c86bab21
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 100%

---


# cookieDomain

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie stattdessen [`trackingServer`](trackingserver.md).

Die `cookieDomain`-Variable bestimmt die Domäne, in der AppMeasurement Cookies setzt. Mit dieser Variablen können Sie explizit die Cookie-Domäne festlegen, anstatt die [`cookieDomainPeriods`](cookiedomainperiods.md)-Variable zu verwenden.

Diese Variable muss nur verwendet werden, wenn **beide** der folgenden Bedingungen erfüllt sind:

* Ihre Implementierung verwendet Erstanbieter-Cookies. Diese Variable ist bei Implementierungen mit einem [`trackingServer`](trackingserver.md)-Wert, der `sc.adobedc.net`enthält, nicht erforderlich.
* Ihre Domäne hat einen Punkt im Suffix. Beispielsweise könnte `example.co.uk` die `cookieDomain`-Variable die explizite Angabe enthalten, dass die Cookie-Domäne `example.co.uk` und nicht `co.uk`lautet.

Nur eine kleine Anzahl von Implementierungen verwenden die `cookieDomain`-Variable, und selbst dann können alternative Variablen wie [`cookieDomainPeriods`](cookiedomainperiods.md) verwendet werden.

## Cookie-Domäne in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.cookieDomain in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `cookieDomain`-Variable ist eine Zeichenfolge und auf die Domäne eingestellt, in der Sie Cookies speichern möchten.

```js
s.cookieDomain = "stats.example.com";
```
