---
title: cookieDomain
description: Die Variable „cookieDomain“ hilft bei der Bestimmung der Domain, in der Cookies gesetzt werden sollen.
feature: Variables
exl-id: 7e8c26b8-d1a7-49f7-9c12-45fb1633c9d7
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 74%

---

# cookieDomain

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie stattdessen [`trackingServer`](trackingserver.md).

Die `cookieDomain`-Variable bestimmt die Domain, in der AppMeasurement Cookies setzt. Mit dieser Variablen können Sie explizit die Cookie-Domäne festlegen, anstatt die [`cookieDomainPeriods`](cookiedomainperiods.md)-Variable zu verwenden.

Diese Variable muss nur verwendet werden, wenn **beide** der folgenden Bedingungen erfüllt sind:

* Ihre Implementierung verwendet Erstanbieter-Cookies. Diese Variable ist bei Implementierungen mit einem [`trackingServer`](trackingserver.md)-Wert, der `sc.adobedc.net`enthält, nicht erforderlich.
* Ihre Domain hat einen Punkt im Suffix. Beispielsweise könnte `example.co.uk` die `cookieDomain`-Variable die explizite Angabe enthalten, dass die Cookie-Domäne `example.co.uk` und nicht `co.uk`lautet.

Nur eine kleine Anzahl von Implementierungen verwenden die `cookieDomain`-Variable, und selbst dann können alternative Variablen wie [`cookieDomainPeriods`](cookiedomainperiods.md) verwendet werden.

## Cookie-Domäne, die das Web SDK verwendet

Das Web SDK kann die richtige Cookie-Speicherdomäne ohne diese Variable ermitteln.

## Cookie-Domäne, die die Adobe Analytics-Erweiterung verwendet

Es gibt kein spezielles Feld in der Adobe Analytics-Erweiterung, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.cookieDomain in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `cookieDomain`-Variable ist eine Zeichenfolge und auf die Domain eingestellt, in der Sie Cookies speichern möchten.

```js
s.cookieDomain = "stats.example.com";
```
