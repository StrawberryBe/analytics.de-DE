---
title: cookieDomain
description: Die Variable „cookieDomain“ hilft bei der Bestimmung der Domäne, in der Cookies gesetzt werden sollen.
exl-id: 7e8c26b8-d1a7-49f7-9c12-45fb1633c9d7
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 87%

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

## Cookie-Domäne in der Adobe Experience Platform-Datenerfassung

In der Datenerfassungs-Benutzeroberfläche gibt es kein dediziertes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.cookieDomain in AppMeasurement und im benutzerdefinierten Code-Editor in 

Die `cookieDomain`-Variable ist eine Zeichenfolge und auf die Domäne eingestellt, in der Sie Cookies speichern möchten.

```js
s.cookieDomain = "stats.example.com";
```
