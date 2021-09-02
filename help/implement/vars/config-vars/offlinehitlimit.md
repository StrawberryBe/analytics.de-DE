---
title: offlineHitLimit
description: Legen Sie die maximale Anzahl von Treffern fest, die zum Offline-Tracking in die Warteschlange gestellt werden sollen.
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '158'
ht-degree: 100%

---

# offlineHitLimit

Offline-Tracking ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin auf Ihrer Website surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Verbindung zum Internet herstellt. Offline-Tracking wird hauptsächlich für mobile Anwendungen verwendet.

Die `offlineHitLimit` Variable legt eine Obergrenze für die Anzahl der Treffer fest, die das Gerät lokal speichert. Diese Variable funktioniert nur, wenn [`trackOffline`](trackoffline.md) aktiviert ist.

## Offline-Treffergrenze bei Verwendung von Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.offlineHitLimit in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.offlineHitLimit`-Variable ist eine Ganzzahl, die die maximale Anzahl von Treffern darstellt, die ein Gerät speichert, während es offline ist. Wenn diese Variable nicht definiert ist, gibt es keine Beschränkung für die Anzahl der Treffer, die ein Gerät speichert, während es offline ist.

```js
s.offlineHitLimit = 100;
```
