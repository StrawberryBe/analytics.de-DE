---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---


# timestamp

Mit dieser Variable können Sie den Zeitstempel von Treffern anpassen, ähnlich wie dies in den AppMeasurement-Bibliotheken für andere Plattformen erfolgt.


<!-- 

timestamp.xml

 -->

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 4 Byte | Datum/Zeit | Ist in Berichten nicht direkt angegeben. | Wird von Datenerfassungsservern festgelegt. |

**Syntax** {#section_1DF752B1202C4412A301AC7CC10874DF}

```js
s.timestamp="UNIX or ISO-8601 format timestamp"
```

Die Variable *`timestamp`* muss in dem Format stehen, das im nächsten Abschnitt näher beschrieben wird.

>[!IMPORTANT]
>
>Um die Variable *`timestamp`* verwenden zu können, muss die Kundenunterstützung zunächst die Unterstützung von Zeitstempeln für Ihre Report Suite aktivieren. Nachdem die Unterstützung von Zeitstempeln aktiviert wurde, müssen alle von JavaScript an diese Report Suite gesendeten Treffer manuell mit Zeitstempeln versehen werden (anhand von *`s.timestamp`*). Andernfalls werden die Treffer nicht aufgezeichnet.
>
>Des Weiteren müssen alle von JavaScript an diese Report Suite gesendeten Treffer manuell mit Zeitstempeln versehen werden (anhand von *`s.timestamp`*). Sie können Treffer mit Zeitstempel und Treffer ohne Zeitstempel nicht an ein und dieselbe Report Suite senden.
>
>Sie können auch die Einstellung [Zeitstempel optional](/help/implement/js-implementation/timestamps-overview.md) verwenden, um mit Zeitstempel versehene Daten in derselben globalen Report Suite zu kombinieren, mit Zeitstempel versehene Daten aus einer App in eine globale Report Suite zu senden und Apps zu aktualisieren, um Zeitstempel zu ermöglichen, ohne eine neue Report Suite erstellen zu müssen.

**Formate für Zeitstempel** {#section_C12CBCECCD7047D38EF63A5800761CE9}

Zeitstempel müssen im UNIX-Format (d. h. Sekunden seit dem 1.Januar 1970) oder im ISO-8601-Format stehen, wobei für das ISO-8601-Format die folgenden Einschränkungen gelten:

* Sowohl das Datum als auch die Uhrzeit müssen durch ein „T“ getrennt angegeben werden
* Das Datum muss ein vollständiges Kalenderdatum sein (Jahr, Monat und Tag). . Wochentage und Datumsangaben mit Ordnungszahlen werden nicht unterstützt.
* Das Datum kann im standardmäßigen oder im erweiterten Format (`YYYY-MM-DD` oder `YYYYMMDD`) angegeben werden, es muss jedoch die Stunde und die Minute enthalten. Sekunden sind optional ( `HH:MM`, `HH:MM:SS`, `HHMM` oder `HHMMSS`). Es können Bruchteile von Minuten und Sekunden eingereicht werden, diese Bruchteile werden jedoch ignoriert.

* Es kann eine optionale Zeitzone im standardmäßigen oder im erweiterten Format (`±HH`, `±HH:MM`, `±HH`, `±HHMM` oder Z) angegeben werden.

UNIX-Zeitstempel werden weiterhin unterstützt (Sekunden seit dem 1.Januar 1970).

**Beispiele** {#section_FA19C53D70DE4CF2AF259A5B968B84C3}

```js
s.timestamp=Math.round((new Date()).getTime()/1000);
```

```js
s.timestamp="2012-04-20T12:49:31-0700";
```

Zulässige Zeitstempel im ISO-8601-Format sehen zum Beispiel wie folgt aus:

```
2013-01-01T12:30:05+06:00 
2013-01-01T12:30:05Z 
2013-01-01T12:30:05 
2013-01-01T12:30
```

**Konfigurationseinstellungen** {#section_5275D206F2CB4009B3681E8C4457124A}

Vor der Verwendung dieser Variablen muss eine Report Suite aktiviert werden, damit benutzerdefinierte Zeitstempel vom Kundendienst entgegengenommen werden können. Nach Aktivierung benutzerdefinierter Zeitstempel müssen alle an die Report Suite gesendeten Treffer über einen Zeitstempel verfügen (andernfalls werden sie verworfen).

**Probleme, Fragen und Tipps** {#section_EFDE8F67D13C4775A461E0B00D30AFD7}

* Zeitstempel dienen hauptsächlich zur Verfolgung von Offlinedaten auf mobilen Plattformen. Benutzerdefinierte Zeitstempel sind meist deaktiviert, es sei denn, es sollen gleichzeitig sowohl Web- als auch Offline-App-Daten in der gleichen Report Suite erfasst werden.
* Daten werden mit einem Zeitstempel versehen, wenn Offlinedaten im mobilen SDK aktiviert sind (Standardeinstellung) oder wenn eine Report Suite konfiguriert ist, Daten mit Zeitstempel zu akzeptieren. Offline erfasste Daten können Stunden oder Wochen nach dem Datum des ursprünglichen Ereignisses gesendet werden. Diese Treffer werden innerhalb der Analytics-Plattform einige Minuten oder Stunden länger als Treffer ohne Zeitstempel in die Warteschlange gestellt:

   * Bei Daten mit Zeitstempel, die in sehr kurzer Zeit gesendet werden, beträgt die wahrscheinliche Verzögerung 10-15 Minuten.
   * Bei Daten mit Zeitstempel, die von gestern gesendet wurden, beträgt die wahrscheinliche Verzögerung etwa 2 Stunden.
   * Bei Daten mit Zeitstempel, die älter als gestern gesendet werden, erhöht sich die tägliche Verzögerung um etwa 2 Stunden, höchstens jedoch um 48 Stunden.

