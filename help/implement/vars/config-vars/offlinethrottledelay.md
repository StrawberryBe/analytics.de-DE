---
title: offlineThrottleDelay
description: Legt die Häufigkeit von Treffern fest, wenn ein Gerät wieder online geht.
exl-id: fa484638-bb1f-4df9-9ba1-e9763fa6ad27
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '175'
ht-degree: 100%

---

# offlineThrottleDelay

Offline-Tracking ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin auf Ihrer Website surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Verbindung zum Internet herstellt. Offline-Tracking wird hauptsächlich für mobile Anwendungen verwendet.

Wenn ein Gerät wieder online geht, werden alle auf dem Gerät gespeicherten Treffer an die Adobe-Datenerfassungs-Server gesendet. Eine große Anzahl von Treffern in der Warteschlange kann sich möglicherweise auf die Leistung älterer Geräte auswirken. Verwenden Sie die `offlineThrottleDelay`-Variable, um festzulegen, wie oft Treffer in der Warteschlange an Adobe gesendet werden.

## Offline-Einschränkungsverzögerung in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.offlineThrottleDelay in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.offlineThrottleDelay`-Variable ist eine Ganzzahl, die die Anzahl der Millisekunden angibt, die AppMeasurement zwischen dem Senden von Treffern in der Warteschlange wartet. Der Standardwert lautet `0`, was bedeutet, dass alle Treffer in der Warteschlange gleichzeitig gesendet werden. Wenn diese Variable auf `trackOffline` `false` gesetzt ist, hat sie keine Auswirkung.

```js
s.offlineThrottleDelay = 500;
```
