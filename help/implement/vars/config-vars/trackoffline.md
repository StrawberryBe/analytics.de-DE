---
title: trackOffline
description: Aktivieren oder deaktivieren Sie die Offline-Verfolgung, wodurch sich die Datenerfassung in AppMeasurement ändert.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackOffline

Die Offline-Verfolgung ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin auf Ihrer Site surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Verbindung zum Internet herstellt. Die Offline-Verfolgung wird hauptsächlich für mobile Anwendungen verwendet.

Die `trackOffline` Variable bestimmt, ob Sie die Offline-Verfolgung in Ihrer Implementierung verwenden möchten.

> [!IMPORTANT] Sie müssen Ihre Report Suite so konfigurieren, dass sie Treffer mit Zeitstempel akzeptiert, bevor Sie diese Variable aktivieren. Wenn eine Report Suite keine Treffer mit Zeitstempel akzeptiert und diese Variable aktiviert ist, gehen diese Daten verloren und können nicht wiederhergestellt werden.

Wenn diese Option aktiviert ist, verwendet AppMeasurement den folgenden Prozess zum Senden von Daten an Adobe:

* Beim Kompilieren einer Bildanforderung wird ein Abfragezeichenfolgen-Parameter für Zeitstempel eingefügt.
* Wenn das Gerät nicht auf Adobe-Datenerfassungsserver zugreifen kann, wird der Treffer lokal auf dem Gerät gespeichert.
* Bei jedem nachfolgenden Treffer versucht AppMeasurement, eine Bildanforderung an Adobe zu senden.
   * Wenn der Treffer nicht auf Adobe-Datenerfassungsserver zugreifen kann, wird er der Warteschlange auf dem Gerät hinzugefügt.
   * Wenn das Gerät Adobe-Datenerfassungsserver erreichen kann, werden der Treffer und die Warteschlange der Treffer gesendet, während das Gerät offline war.

## Offline verfolgen beim Starten der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.trackOffline in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.trackOffline` Variable ist ein boolescher Wert, der die Offline-Verfolgung aktiviert oder deaktiviert. Its default value is `false`. Legen Sie diesen Wert fest, `true` wenn Sie die Offline-Verfolgung aktivieren möchten.

```js
s.trackOffline = true;
```
