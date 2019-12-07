---
description: In diesem Abschnitt werden die Dateien beschrieben, die in einer Datenfeed-Auslieferung enthalten sind.
keywords: Data Feed;job;contents;manifest;file;lookup;hit data;delivery contents
subtopic: data feeds
title: Daten-Feed-Inhalte – Übersicht
topic: Reports and analytics
uuid: 82a86314-4841-4133-a0dc-4e7c6cd14fc1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Daten-Feed-Inhalte – Übersicht

In diesem Abschnitt werden die Dateien beschrieben, die in einer Datenfeed-Auslieferung enthalten sind.

## Manifestdatei

Die Manifestdatei enthält folgende Details zu den einzelnen Dateien, die Bestandteil des hochgeladenen Datensatzes sind:

* Dateiname
* Dateigröße
* MD5-Hash
* Anzahl der in der Datei enthaltenen Datensätze

Die Manifestdatei folgt demselben Format wie eine Java-JAR-Manifestdatei.

The manifest file is always delivered last as a separate `.txt` file, so that its existence indicates that the complete data set for that request period has already been delivered. Manifestdateien werden nach folgendem Muster benannt:

```text
[rsid]_[YYYY-mm-dd].txt
```

Eine typische Manifestdatei enthält Daten, die folgendem Schema entsprechen:

```text
Datafeed-Manifest-Version: 1.0
 Lookup-Files: 1
 Data-Files: 1
 Total-Records: 611

 Lookup-File: rsid_date-lookup_data.tar.gz
 MD5-Digest: af6de42d8b945d4ec1cf28360085308
 File-Size: 63750

 Data-File: 01-rsid_date.tsv.gz
 MD5-Digest: 9c70bf783cb3d0095a4836904b72c991
 File-Size: 122534
 Record-Count: 611
```

Jede Manifestdatei enthält eine Kopfzeile, in der die Gesamtanzahl der Lookup-Dateien, Datendateien sowie die Gesamtanzahl der Datensätze in allen Datendateien angegeben sind. Nach dieser Kopfzeile folgen verschiedene Abschnitte mit Informationen zu den einzelnen Dateien, die in der Datenfeedauslieferung enthalten sind.

Some feeds are configured to receive a `.fin` file instead of a `.txt` manifest. The `.fin` indicates that the upload is complete, but it contains no metadata about the upload.

## Suchdateien

Einige Datenfeed-Spalten geben eine Zahl aus, die ihrem tatsächlichen Wert entspricht. Suchdateien werden verwendet, um eine Zahl aus einer Datenfeed-Spalte zuzuordnen und sie einem tatsächlichen Wert zuzuordnen. Ein Wert von "497"in der Spalte mit den `browser` Trefferdaten zeigt beispielsweise an, dass der Treffer von "Microsoft Internet Explorer 8"kam, wenn Sie hineinschauen `browser.tsv`.

Note that the `column_headers.tsv` and `event_list.tsv` are specific to the data feed and report suite. Andere Dateien, z. B. `browser.tsv`, sind hingegen generisch.

Lookup-Dateien werden in einer komprimierten ZIP-Datei bereitgestellt, die nach folgendem Muster benannt ist:

```text
[rsid]_[YYYY-mm-dd]-lookup_data.[compression_suffix]
```

* [!DNL column_headers.tsv] (angepasst für diesen Datenfeed)
* [!DNL browser.tsv]
* [!DNL browser_type.tsv]
* [!DNL color_depth.tsv]
* [!DNL connection_type.tsv]
* [!DNL country.tsv]
* [!DNL javascript_version.tsv]
* [!DNL languages.tsv]
* [!DNL operating_systems.tsv]
* [!DNL plugins.tsv]
* [!DNL resolution.tsv]
* [!DNL referrer_type.tsv]
* [!DNL search_engines.tsv]
* [!DNL event_lookup.tsv] (angepasst für diesen Datenfeed)

## Trefferdatendateien

Hit data is provided in a [!DNL hit_data.tsv] file. Die Menge an Daten in dieser Datei richtet sich nach dem Auslieferungsformat (stündlich oder täglich sowie danach, ob die Auslieferung in einer oder in mehreren Dateien erfolgt). Diese Datei enthält nur die Trefferdaten. Die Spaltenkopfzeilen werden separat mit den Lookup-Dateien geliefert. Jede Zeile in dieser Datei entspricht einem einzelnen Server-Aufruf.

Von Adobe bereitgestellte Dateien variieren je nach konfiguriertem Datenfeed. Alle Dateien werden mit ISO-8859-1 kodiert.

* `[rsid]` bezieht sich auf die Report Suite-ID, aus der der Datenfeed stammt.
* `[index]` wird nur in mehreren Datei-Feeds verwendet und bezieht sich auf die richtige Reihenfolge paginierter Dateien.
* `[YYYY-mm-dd]` bezieht sich auf den Starttag, für den der Datenfeed beginnt.
* `[HHMMSS]` wird nur in stündlichen Feeds verwendet und bezieht sich auf die Startzeit, für die der Datenfeed ausgeführt wird.
* `[compression_suffix]` bezieht sich auf die Art der verwendeten Komprimierung. Normalerweise werden Datenfeeds in `tar.gz` oder `zip` Dateien komprimiert.

### Täglich; einzelne Datei

Nachdem die Daten für einen Tag erfasst wurden, erhalten Sie eine einzelne komprimierte Datendatei und eine Manifestdatei. Die Datendatei hat den Namen:

`[rsid]_[YYYY-mm-dd].[compression_suffix]`

Nach dem Extrahieren enthält die Datendatei eine einzelne `hit_data.tsv` Datei mit allen Daten für diesen Tag sowie Lookup-Dateien für alle erforderlichen Spalten.

### Täglich mehrere Dateien

Nachdem die Daten für einen Tag erfasst wurden, erhalten Sie eine oder mehrere komprimierte Datendateien und eine Manifestdatei. Die Datendatei hat den Namen:

`[index]-[rsid]_[YYYY-mm-dd].[compression_suffix]`

Nach dem Extrahieren enthält jede Datendatei eine einzelne Datei `hit_data.tsv` mit ca. 2 GB unkomprimierten Daten sowie Lookup-Dateien für alle erforderlichen Spalten.

### Stündlich; einzelne Datei

Nachdem die Daten eine Stunde lang erfasst wurden, erhalten Sie eine einzelne komprimierte Datendatei und eine Manifestdatei. Die Datendatei hat den Namen:

`[rsid]_[YYYY-mm-dd]-[HHMMSS].[compression_suffix]`

Nach dem Extrahieren enthält die Datendatei eine einzelne `hit_data.tsv` Datei mit allen Daten für diese Stunde sowie Lookup-Dateien für alle erforderlichen Spalten.

### Stündlich mehrere Dateien

Nachdem die Daten eine Stunde lang erfasst wurden, erhalten Sie eine oder mehrere komprimierte Datendateien und eine Manifestdatei. Die Datendatei hat den Namen:

`[index]-[rsid]_[YYYY-mm-dd]-[HHMMSS].[compression_suffix]`

Nach dem Extrahieren enthält jede Datendatei eine einzelne Datei `hit_data.tsv` mit ca. 2 GB unkomprimierten Daten sowie Lookup-Dateien für alle erforderlichen Spalten.

## Datendateigröße

Die Größe der Trefferdatendatei hängt stark von der Anzahl der aktiv verwendeten Variablen und dem Traffic ab, der an die Report Suite gesendet wird. Eine Datenzeile ist durchschnittlich 500 B (komprimiert) oder 2 KB (unkomprimiert) groß. Die Multiplikation mit der Anzahl der Serveraufrufe kann eine grobe Schätzung der Größe einer Datenfeed-Datei liefern. Sobald Ihre Unternehmen mit dem Empfang von Datenfeed-Dateien beginnen, können Sie eine genauere Zahl finden, indem Sie die Anzahl der Zeilen durch die Gesamtdateigröße `hit_data.tsv` dividieren.
