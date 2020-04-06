---
title: trackOffline
description: Aktivieren oder deaktivieren Sie Offline-Tracking, wodurch sich die Datenerfassung in AppMeasurement ändert.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# trackOffline

Offline-Tracking ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin auf Ihrer Website surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Verbindung zum Internet herstellt. Offline-Tracking wird hauptsächlich für mobile Anwendungen verwendet.

Die `trackOffline`-Variable bestimmt, ob Sie Offline-Tracking in Ihrer Implementierung verwenden möchten.

>[!IMPORTANT] Sie müssen Ihre Report Suite so konfigurieren, dass sie Treffer mit Zeitstempel akzeptiert, bevor Sie diese Variable aktivieren. Wenn eine Report Suite keine Treffer mit Zeitstempel akzeptiert und diese Variable aktiviert ist, gehen diese Daten verloren und können nicht wiederhergestellt werden.

Wenn diese Option aktiviert ist, verwendet AppMeasurement den folgenden Prozess zum Senden von Daten an Adobe:

* Beim Kompilieren einer Bildanforderung wird ein Abfragezeichenfolgenparameter für Zeitstempel eingefügt.
* Wenn das Gerät nicht auf Adobe-Datenerfassungs-Server zugreifen kann, wird der Treffer lokal auf dem Gerät gespeichert.
* Bei jedem nachfolgenden Treffer versucht AppMeasurement, eine Bildanforderung an Adobe zu senden.
   * Wenn nicht auf Adobe-Datenerfassungs-Server zugegriffen werden kann, wird der Treffer Warteschlange auf dem Gerät hinzugefügt.
   * Wenn auf Adobe-Datenerfassungs-Server zugegriffen werden kann, werden der Treffer und die Warteschlange der Treffer gesendet, während das Gerät offline war.

## Offline-Verfolgen in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.trackOffline in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.trackOffline`-Variable ist ein boolescher Wert, der Offline-Tracking aktiviert oder deaktiviert. Der Standardwert lautet `false`. Setzen Sie diesen Wert auf `true`, wenn Sie Offline-Tracking aktivieren möchten.

```js
s.trackOffline = true;
```
