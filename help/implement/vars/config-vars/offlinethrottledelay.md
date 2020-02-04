---
title: offlineThrottleDelay
description: Legt die Häufigkeit von Treffern fest, wenn ein Gerät wieder online ist.
translation-type: tm+mt
source-git-commit: f313fd0c9ffda054a18ad1d457a74602b08e51fa

---


# offlineThrottleDelay

Die Offline-Verfolgung ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin auf Ihrer Site surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Verbindung zum Internet herstellt. Die Offline-Verfolgung wird hauptsächlich für mobile Anwendungen verwendet.

Wenn ein Gerät wieder online ist, werden alle auf dem Gerät gespeicherten Treffer an die Adobe-Datenerfassungsserver gesendet. Eine große Anzahl von Treffern in der Warteschlange kann sich möglicherweise auf die Leistung älterer Geräte auswirken. Verwenden Sie die `offlineThrottleDelay` Variable, um festzulegen, wie oft Treffer in der Warteschlange an Adobe gesendet werden.

## Zeitverzögerung bei Offline-Throttle beim Start der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.offlineThrottleDelay in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.offlineThrottleDelay` Variable ist eine Ganzzahl, die die Anzahl der Millisekunden angibt, die AppMeasurement zwischen dem Senden von Treffern in der Warteschlange wartet. Der Standardwert lautet `0`also, dass alle Treffer in der Warteschlange gleichzeitig gesendet werden. Wenn `trackOffline` dies `false`der Fall ist, hat diese Variable nichts.

```js
s.offlineThrottleDelay = 500;
```
