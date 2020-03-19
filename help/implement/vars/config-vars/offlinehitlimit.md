---
title: offlineHitLimit
description: Legen Sie die maximale Anzahl von Treffern fest, die für die Offline-Verfolgung in die Warteschlange gestellt werden sollen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# offlineHitLimit

Die Offline-Verfolgung ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Internetverbindung trennt, aber weiterhin auf Ihrer Site surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Internetverbindung herstellt. Die Offline-Verfolgung wird hauptsächlich für mobile Anwendungen verwendet.

Die `offlineHitLimit` Variable platziert eine Obergrenze für die Anzahl der Treffer, die das Gerät lokal speichert. Diese Variable funktioniert nur, wenn sie aktiviert [`trackOffline`](trackoffline.md) ist.

## Offline-Trefferbeschränkung beim Start der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.offlineHitLimit in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.offlineHitLimit` Variable ist eine Ganzzahl, die die maximale Anzahl von Treffern darstellt, die ein Gerät speichert, während es offline ist. Wenn diese Variable nicht definiert ist, gibt es keine Beschränkung für die Anzahl der Treffer, die ein Gerät speichert, während es offline ist.

```js
s.offlineHitLimit = 100;
```
