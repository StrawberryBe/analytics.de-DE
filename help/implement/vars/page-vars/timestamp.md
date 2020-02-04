---
title: timestamp
description: Legen Sie manuell den Zeitstempel des Treffers fest.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# timestamp

Die `timestamp` Variable legt manuell den Zeitstempel des Treffers für zeitstempelfähige Report Suites fest.

> [!WARNING] Verwenden Sie diese Variable nicht, wenn Ihre Report Suite nicht explizit für die Annahme von Treffern mit Zeitstempel konfiguriert ist. AppMeasurement legt die Zeit eines Treffers für Report Suites, die keine Treffer mit Zeitstempel unterstützen, automatisch fest. Wenn Sie einen Treffer mit dieser Variablen an eine Report Suite senden, die keine Zeitstempel unterstützt, gehen diese Daten dauerhaft verloren.

## Zeitstempel beim Start der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.timestamp in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.timestamp` Variable ist eine Zeichenfolge, die das Datum und die Uhrzeit des Treffers enthält. Gültige Zeitstempelformate sind [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) und [Unix Time](https://en.wikipedia.org/wiki/Unix_time).

```js
// Timestamp using ISO 8601
s.timestamp = "2020-01-01T00:00:00Z";

// Timestamp using Unix timestamp
s.timestamp = "1577836800";

// Automatically get the current Unix timestamp
s.timestamp = Math.round(new Date().getTime()/1000);

// Automatically get the current ISO 8601 timestamp
s.timestamp = new Date().toISOString();
```

## Werte nach ISO 8601

Die in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) ausgedrückten Daten und Zeiten können in verschiedenen Formen verwendet werden. Adobe unterstützt nicht alle Funktionen von ISO 8601.

* Both the date and time must be provided, separated by `T`.
* Stunden und Minuten sind erforderlich; Sekunden sind optional, werden aber empfohlen.
* Wochentage und Datumsangaben mit Ordnungszahlen werden nicht unterstützt.
* Das Datum kann im standardmäßigen oder im erweiterten Format angegeben werden. Zum Beispiel `2020-01-01T00:00:00Z` und `20200101T000000Z` sind beide gültig.
* Bruchminuten und Sekunden sind technisch gültig, aber die Bruchzahlen werden von Adobe ignoriert.
* Zeitzonen werden in Standard- und erweiterten Formaten unterstützt.

Die folgenden Werte sind in der `timestamp` Variablen ein gültiges Beispiel für ISO 8601-Werte:

```text
2020-01-01T00:00:00+00:00
2020-01-01T00:00:00Z
2020-01-01T00:00:00
2020-01-01T00:00
20200101T000000+0000
20200101T000000Z
20200101T000000
20200101T0000
```
