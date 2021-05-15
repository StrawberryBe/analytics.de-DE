---
description: In diesem Abschnitt werden die Dateien beschrieben, die in einer Daten-Feed-Auslieferung enthalten sind.
keywords: Datenfeed;Auftrag;Inhalt;Manifest;Datei;Suche;Trefferdaten;Versand-Inhalt
subtopic: data feeds
title: Daten-Feed-Inhalte – Übersicht
feature: Grundlegendes zu Reports & Analytics
uuid: 82a86314-4841-4133-a0dc-4e7c6cd14fc1
exl-id: 7456ed99-c2f3-4b19-a63e-6b4e457e7d55
source-git-commit: 7312b61b8d73f45afa3eb9aac73cc4d5fd39bc82
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 98%

---

# Daten-Feed-Inhalte – Übersicht

In diesem Abschnitt werden die Dateien beschrieben, die in einer Daten-Feed-Auslieferung enthalten sind.

## Manifestdatei {#feed-manifest}

Die Manifestdatei enthält folgende Details zu den einzelnen Dateien, die Bestandteil des hochgeladenen Datensatzes sind:

* Dateiname
* Dateigröße
* MD5-Hash
* Anzahl der in der Datei enthaltenen Datensätze

Die Manifestdatei hat dasselbe Format wie eine Java-JAR-Manifestdatei.

Die Manifestdatei wird immer abschließend in Form einer separaten `.txt`-Datei gesendet. Mit der Manifestdatei wird signalisiert, dass der vollständige Datensatz für den Anforderungszeitraum ausgeliefert wurde. Manifestdateien werden nach folgendem Muster benannt:

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

Einige Feeds sind so konfiguriert, dass sie eine `.fin`-Datei anstelle einer `.txt`-Manifestdatei erhalten. Dabei gibt die `.fin`-Datei an, dass der Upload abgeschlossen ist. Die Datei enthält jedoch keine Metadaten zum Upload.

## Lookup-Dateien

In manchen Daten-Feed-Spalten wird eine Zahl ausgegeben, die einem Wert entspricht. Lookup-Dateien werden verwendet, um diese Zahl in einer Daten-Feed-Spalte einem tatsächlichen Wert zuzuordnen. Beispielsweise bedeutet der Wert „497“ in der Spalte mit den `browser`-Trefferdaten, dass der Treffer von „Microsoft Internet Explorer 8“ stammte, wie in `browser.tsv` ersichtlich ist.

Beachten Sie, dass `column_headers.tsv` und `event_list.tsv` spezifisch für den Daten-Feed und die Report Suite sind. Andere Dateien, z. B. `browser.tsv`, sind hingegen generisch.

Lookup-Dateien werden in einer komprimierten ZIP-Datei bereitgestellt, die nach folgendem Muster benannt ist:

```text
[rsid]_[YYYY-mm-dd]-lookup_data.[compression_suffix]
```

* [!DNL column_headers.tsv] (angepasst für diesen Daten-Feed)
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
* [!DNL event_lookup.tsv] (angepasst für diesen Daten-Feed)

## Trefferdatendateien

Die Trefferdaten werden in der Datei [!DNL hit_data.tsv] bereitgestellt. Die Menge an Daten in dieser Datei richtet sich nach dem Auslieferungsformat (stündlich oder täglich sowie danach, ob die Auslieferung in einer oder in mehreren Dateien erfolgt). Diese Datei enthält nur die Trefferdaten. Die Spaltenkopfzeilen werden separat mit den Lookup-Dateien geliefert. Jede Zeile in dieser Datei entspricht einem einzelnen Server-Aufruf.

Die von Adobe bereitgestellten Dateien variieren je nach Art des konfigurierten Daten-Feeds. Alle Dateien sind ISO-8859-1-kodiert.

* `[rsid]` Bezeichnet die Report Suite-ID, aus der der Daten-Feed stammt.
* `[index]` wird nur bei mehreren Datei-Feeds verwendet und bezieht sich auf die richtige Reihenfolge paginierter Dateien.
* `[YYYY-mm-dd]` bezeichnet den Starttag des Daten-Feed.
* `[HHMMSS]` wird nur in stündlichen Feeds verwendet und bezeichnet den Startzeitpunkt des Daten-Feed.
* `[compression_suffix]` bezeichnet die Art der verwendeten Komprimierung. Normalerweise werden Daten-Feeds in `tar.gz`- oder `zip`-Dateien komprimiert.

### Täglich; einzelne Datei

Nachdem die Daten einen Tag lang erfasst wurden, erhalten Sie eine einzelne komprimierte Datendatei und eine Manifestdatei. Die Datendatei hat den Namen:

`[rsid]_[YYYY-mm-dd].[compression_suffix]`

Nach dem Extrahieren enthält die Datendatei eine einzelne `hit_data.tsv`-Datei, die alle Daten für diesen Tag beinhaltet, sowie Lookup-Dateien für alle erforderlichen Spalten.

### Täglich; mehrere Dateien

Nachdem die Daten einen Tag lang erfasst wurden, erhalten Sie eine oder mehrere komprimierte Datendateien und eine Manifestdatei. Die Datendatei hat den Namen:

`[index]-[rsid]_[YYYY-mm-dd].[compression_suffix]`

Nach dem Extrahieren enthält jede Datendatei eine einzelne `hit_data.tsv`-Datei, die ca. 2 GB unkomprimierte Daten beinhaltet, sowie Lookup-Dateien für alle erforderlichen Spalten.

### Stündlich; einzelne Datei

Nachdem die Daten eine Stunde lang erfasst wurden, erhalten Sie eine einzelne komprimierte Datendatei und eine Manifestdatei. Die Datendatei hat den Namen:

`[rsid]_[YYYYmmdd]-[HHMMSS].[compression_suffix]`

Nach dem Extrahieren enthält die Datendatei eine einzelne `hit_data.tsv`-Datei, die alle Daten für diese Stunde beinhaltet, sowie Lookup-Dateien für alle erforderlichen Spalten.

### Stündlich; mehrere Dateien

Nachdem die Daten eine Stunde lang erfasst wurden, erhalten Sie eine oder mehrere komprimierte Datendateien und eine Manifestdatei. Die Datendatei hat den Namen:

`[index]-[rsid]_[YYYYmmdd]-[HHMMSS].[compression_suffix]`

Nach dem Extrahieren enthält jede Datendatei eine einzelne `hit_data.tsv`-Datei, die ca. 2 GB unkomprimierte Daten beinhaltet, sowie Lookup-Dateien für alle erforderlichen Spalten.

## Größe der Datendatei

Die Größe der Trefferdatei kann in Abhängigkeit von der Anzahl der aktiv genutzten Variablen und dem Traffic an die Report Suite stark variieren. Eine Datenzeile ist durchschnittlich 500 B (komprimiert) oder 2 KB (unkomprimiert) groß. Dieser Wert multipliziert mit der Anzahl der Server-Aufrufe ergibt einen ungefähren Schätzwert zur Größe einer Daten-Feed-Datei. Sobald Ihr Unternehmen Daten-Feed-Dateien empfängt, können Sie eine genauere Zahl feststellen, indem Sie die Anzahl der Zeilen in `hit_data.tsv` durch die Gesamtdateigröße dividieren.
