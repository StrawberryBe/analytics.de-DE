---
title: Unterstützung von Komponenten in Data Warehouse
description: Erfahren Sie, welche zusätzlichen Dimensionen und Metriken in Data Warehouse verfügbar sind und was nicht unterstützt wird.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 100%

---


# Unterstützung von Komponenten in Data Warehouse

Dank der einzigartigen Verarbeitungsarchitektur von Data Warehouse sind hier einige Komponenten vorhanden, die in anderen Funktionen von Adobe Analytics normalerweise nicht verfügbar sind. Aufgrund seiner speziellen Architektur stehen einige Komponenten weder für Berichte noch für Segmente zur Verfügung. Auf dieser Seite erfahren Sie, welche Komponenten verwendet werden können und welche nicht.

## Komponenten, die speziell in Data Warehouse verwendet werden

Einige Dimensionen und Metriken können in Data Warehouse verwendet werden, nicht jedoch in anderen Funktionen in Adobe Analytics.

### Ausschließlich unterstützte Dimensionen

* Experience Cloud ID: Bei Implementierungen, die den Experience Cloud ID-Dienst (ECID) verwenden, eine 128-Bit-Zahl, die aus zwei konkatenierten 64-Bit-Zahlen und 19 Ziffern besteht.
* Seiten-URL: Die Seiten-URL, auf der der Treffer aufgetreten ist.
* Kauf-IDs: Eindeutige ID für einen Kauf, definiert mit der Variablen purchaseID.
* Besucher-ID: die eindeutige Kennung des Besuchers. Dieser Wert entspricht dem konkatenierten Wert der Spalten `visid_high` und `visid_low` in Daten-Feeds. Weitere Informationen finden Sie unter in der [Datenspaltenreferenz](../analytics-data-feed/c-df-contents/datafeeds-reference.md) unter Daten-Feeds.

### Ausschließlich unterstützte Metriken

* Besuche: In dieser Metrik werden im Zusammenhang mit Data Warehouse nicht persinstente Cookie-Besuche ausgeschlossen.
* Besuche – alle Besucher: Diese Metrik weist im Zusammenhang mit Data Warehouse eine bessere Parität mit der Besuchsmetrik in anderen Tools innerhalb Adobe Analytics auf.

## Nicht in Data Warehouse unterstützte Komponenten

Einige Dimensionen und Metriken werden in Data Warehouse nicht unterstützt.

>[!NOTE]
>
>Wenn eine Dimension oder Metrik in Data Warehouse nicht unterstützt wird, werden Segmente, die diese Komponenten verwenden, auch nicht unterstützt. Überprüfen Sie beim Erstellen oder Bearbeiten eines Segments immer die Produktkompatibilität.

### Nicht unterstützte Dimensionen

* Einige zeitbasierte Dimensionen, darunter:
   * Vormittag/Nachmittag
   * Tag des Monats
   * Wochentag
   * Tag des Jahres
   * Stunde des Tages
   * Minute
   * Monat des Jahres
   * Quartal des Jahres
   * Wochentag/Wochenende
   * Jahr
* Einige pfadbasierte Dimensionen, darunter:
   * Alle Entry-Dimensionen, außer Entrypage
   * Alle Exit-Dimensionen, außer Exitpage und Exitlink
   * Treffertiefe
   * Rückkehrhäufigkeit
   * Zeit vor Ereignis
   * Besuchszeit pro Seite – zusammengefasst
   * Zeit pro Besuch – zusammengefasst
   * Besuchstiefe
* Rangansicht aller Suchseiten
* Hierarchievariablen
* Treffertyp
* Nicht gefundene Seiten (als Dimension verfügbar; nicht unterstützt für Segmentierung)
* Paid Search
* Einzelseitenbesuche
* Nachverfolgen des Abmeldegrunds
* US-Staaten

### Nicht unterstützte Metriken

* Einige pfadbasierte Metriken, darunter:
   * Absprünge
   * Einstiege
   * Ausstiege
   * Neuladungen
   * Einzelzugriff
   * Besuchszeit-Metriken
