---
title: trackOffline
description: Aktivieren oder deaktivieren Sie Offline-Tracking, wodurch sich die Datenerfassung in AppMeasurement ändert.
feature: Variables
exl-id: 23a17ddc-01e6-42b6-81b0-c60f15a07231
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 83%

---

# trackOffline

Offline-Tracking ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin auf Ihrer Website surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Verbindung zum Internet herstellt. Offline-Tracking wird hauptsächlich für mobile Anwendungen verwendet.

Die `trackOffline`-Variable bestimmt, ob Sie Offline-Tracking in Ihrer Implementierung verwenden möchten.

>[!WARNING]
>
>Sie müssen Ihre Report Suite so konfigurieren, dass sie Treffer mit Zeitstempel akzeptiert, bevor Sie diese Variable aktivieren. Wenn eine Report Suite keine Treffer mit Zeitstempel akzeptiert und diese Variable aktiviert ist, gehen diese Daten verloren und können nicht wiederhergestellt werden.

Wenn diese Option aktiviert ist, verwendet AppMeasurement den folgenden Prozess zum Senden von Daten an Adobe:

* Beim Kompilieren einer Bildanforderung wird ein Abfragezeichenfolgenparameter für Zeitstempel eingefügt.
* Wenn das Gerät nicht auf Adobe-Datenerfassungs-Server zugreifen kann, wird der Treffer lokal auf dem Gerät gespeichert.
* Bei jedem nachfolgenden Treffer versucht AppMeasurement, eine Bildanforderung an Adobe zu senden.
   * Wenn nicht auf Adobe-Datenerfassungs-Server zugegriffen werden kann, wird der Treffer Warteschlange auf dem Gerät hinzugefügt.
   * Wenn auf Adobe-Datenerfassungs-Server zugegriffen werden kann, werden der Treffer und die Warteschlange der Treffer gesendet, während das Gerät offline war.

## Offline-Tracking mit dem Web SDK

Das Web SDK unterstützt kein Offline-Tracking.

## Offline-Tracking mit der Adobe Analytics-Erweiterung

Es gibt kein spezielles Feld in der Adobe Analytics-Erweiterung, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.trackOffline in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.trackOffline`-Variable ist ein boolescher Wert, der Offline-Tracking aktiviert oder deaktiviert. Der Standardwert lautet `false`. Setzen Sie diesen Wert auf `true`, wenn Sie Offline-Tracking aktivieren möchten.

```js
s.trackOffline = true;
```
