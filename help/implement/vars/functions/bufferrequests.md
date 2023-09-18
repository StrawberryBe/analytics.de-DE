---
title: bufferRequests
description: Erhöhen Sie die Zuverlässigkeit bei der Erfassung von Linktracking-Anforderungen für Browser, die die Seite sofort entladen.
feature: Variables
source-git-commit: 58a82151a8cbc80318e4f4ab4186fcabef3f35ab
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 6%

---

# bufferRequests

Die `bufferRequests()` -Methode ermöglicht es Ihnen, Bildanforderungen auf der aktuellen Seite zwischenzuspeichern, anstatt sie an Adobe zu senden. Das Auslösen dieser Methode ist in Szenarien nützlich, in denen ein Browser nicht unterstützt [`navigator.sendBeacon()`](https://developer.mozilla.org/de-DE/docs/Web/API/Navigator/sendBeacon) oder anderweitig Bildanforderungen beim Entladen einer Seite abbricht. Viele Versionen von WebKit-Browsern wie Safari zeigen normalerweise das Verhalten, eine Bildanforderung beim Klicken auf einen Link zu stoppen. Die `bufferRequests()` -Methode ist für alle Versionen von AppMeasurement v2.25.0 oder höher verfügbar.

Wenn Sie [`t()`](t-method.md) oder [`tl()`](tl-method.md) auf einer nachfolgenden Seite in derselben Browsersitzung und `bufferRequests()` noch nicht auf dieser Seite aufgerufen wurde, werden alle gepufferten Anfragen zusätzlich zur Bildanforderung dieser Seite gesendet. Pufferte Anforderungen werden in der richtigen Reihenfolge gesendet, wobei die Bildanforderung der aktuellen Seite zuletzt gesendet wird.

>[!TIP]
>
>Der Zeitstempel der gepufferten Anforderungen wird für die Seite freigegeben, an die Daten gesendet werden. Wenn Sie in der exakten Sekunde, in der eine gepufferte Anforderung aufgezeichnet wird, mehr Präzision wünschen, können Sie die [`timestamp`](../page-vars/timestamp.md) Seitenvariable vor der Pufferung der Anforderung. Wenn Sie diese Variable verwenden, stellen Sie sicher, dass [Zeitstempel optional](/help/technotes/timestamps-optional.md) aktiviert ist - wenn nicht, gehen alle Treffer mit Zeitstempel dauerhaft verloren.

## Einschränkungen

Beim Aufrufen der `bufferRequests()` -Methode verwenden, beachten Sie die folgenden Einschränkungen. Da diese Methode verwendet [`Window.sessionStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API), gelten viele der gleichen Einschränkungen:

* Der Ziel-Link muss sich in derselben Domäne und Subdomäne befinden. Gebuchte Anforderungen funktionieren nicht domänenübergreifend oder unterdomänenübergreifend, auch wenn beide über dieselbe Adobe Analytics-Implementierung verfügen. Diese Einschränkung bedeutet auch, dass Sie gepufferte Anfragen nicht zur Verfolgung von Exitlinks verwenden können.
* Der Ziel-Link muss dasselbe Protokoll wie die aktuelle Seite verwenden. Sie können keine gepufferten Anfragen zwischen HTTP und HTTPS senden.
* Pufferte Anforderungen werden gespeichert, bis Sie `t()` oder `tl()` ohne Aufruf `bufferRequests()` , oder bis der Browser oder die Registerkarte geschlossen ist. Wenn eine Browsersitzung beendet wird, bevor Sie diese Daten an Adobe senden können, gehen nicht gesendete gepufferte Anfragen dauerhaft verloren.
* Wenn ein Browser die [Web-Speicher-API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) oder [JSON-API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON), wird eine Warnung an die Browser-Konsole ausgegeben und AppMeasurement versucht, die Bildanforderung sofort mit der `t()` -Methode.

## Pufferte Anforderungen im Web SDK

Das Web SDK bietet derzeit keine Möglichkeit zum Puffern von Anforderungen.

## Pufferte Anforderungen mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.bufferRequests() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `bufferRequests()` -Methode vor dem Aufruf `t()` oder `tl()`. Wann `bufferRequests()` aufgerufen wird, werden nachfolgende Tracking-Aufrufe in die Sitzungsspeicherung geschrieben, anstatt an Adobe-Datenerfassungsserver gesendet zu werden.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Flag the request to be buffered
s.bufferRequests();

// The t() or tl() method then writes the data to session storage instead of sending it to Adobe
s.tl(true,"o","Example link click");

// On a subsequent page, the tracking call sends both the above link tracking call and the page view call
s.t();
```
