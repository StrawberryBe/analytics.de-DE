---
title: timestamp
description: Setzen Sie den Zeitstempel des Treffers manuell fest.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '243'
ht-degree: 100%

---


# timestamp

Die `timestamp`-Variable legt den Zeitstempel des Treffers für Report Suites mit aktiviertem Zeitstempel manuell fest.

>[!WARNING]
>
>Verwenden Sie diese Variable nicht, wenn Ihre Report Suite nicht explizit für die Annahme von Treffern mit Zeitstempel konfiguriert ist. AppMeasurement legt die Zeit eines Treffers für Report Suites automatisch fest, die keine Treffer mit Zeitstempel unterstützen. Wenn Sie einen Treffer mit dieser Variablen an eine Report Suite senden, die keine Zeitstempel unterstützt, gehen diese Daten dauerhaft verloren.

## Zeitstempel in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.timestamp in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.timestamp`-Variable ist eine Zeichenfolge, die das Datum und die Uhrzeit des Treffers enthält. Gültige Zeitstempelformate sind [ISO 8601](https://de.wikipedia.org/wiki/ISO_8601) und [UnixZeit](https://de.wikipedia.org/wiki/Unixzeit).

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

Die nach [ISO 8601](https://de.wikipedia.org/wiki/ISO_8601) angegebenen Daten und Zeiten können in verschiedenen Formen verwendet werden. Adobe unterstützt nicht alle Funktionen von ISO 8601.

* Sowohl das Datum als auch die Uhrzeit müssen durch `T` getrennt angegeben werden.
* Stunden und Minuten sind erforderlich; Sekunden sind optional, werden aber empfohlen.
* Wochentage und Datumsangaben mit Ordnungszahlen werden nicht unterstützt.
* Das Datum kann im standardmäßigen oder im erweiterten Format angegeben werden. Zum Beispiel sind `2020-01-01T00:00:00Z` und `20200101T000000Z` beide gültig.
* Bruchteile von Minuten und Sekunden sind technisch gültig. Die Bruchteile werden allerdings von Adobe ignoriert.
* Zeitzonen werden in Standard- und erweiterten Formaten unterstützt.

Die folgenden Beispiele sind gültige Werte nach ISO 8601 in der `timestamp`-Variablen:

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
