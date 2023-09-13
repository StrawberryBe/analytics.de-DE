---
title: Unterstützung von Komponenten in Data Warehouse
description: Erfahren Sie, welche zusätzlichen Dimensionen und Metriken in Data Warehouse verfügbar sind und was nicht unterstützt wird.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
source-git-commit: e00a8e611e137590838b1a58571a563aac53434c
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 65%

---

# Unterstützung von Komponenten in Data Warehouse

Die eindeutige Verarbeitung in der Data Warehouse-Architektur ermöglicht einige Komponenten, die normalerweise nicht in anderen Funktionen von Adobe Analytics verfügbar sind. Aufgrund seiner speziellen Architektur stehen einige Komponenten weder für Berichte noch für Segmente zur Verfügung. Auf dieser Seite erfahren Sie, welche Komponenten verwendet werden können und welche nicht.

## Komponenten, die speziell in Data Warehouse verwendet werden

Einige Dimensionen und Metriken, die beim Data Warehouse verwendet werden können, sind bei Verwendung anderer Funktionen in Adobe Analytics nicht verfügbar.

### Ausschließlich unterstützte Dimensionen

* **Experience Cloud-ID**: Bei Implementierungen, die den Experience Cloud ID-Dienst (ECID) verwenden, eine 128-Bit-Zahl, die aus zwei verketteten 64-Bit-Zahlen mit 19 Stellen besteht.
* **Seiten-URL**: Die Seiten-URL, auf der der Treffer aufgetreten ist.
* **Kauf-IDs**: Eindeutige Kennung für einen Kauf, festgelegt mit der Variablen purchaseID.
* **Besucher-ID**: Stellt die eindeutige Kennung für den Besucher bereit. Dieser Wert entspricht dem konkatenierten Wert der Spalten `visid_high` und `visid_low` in Daten-Feeds. Weitere Informationen finden Sie unter in der [Datenspaltenreferenz](../analytics-data-feed/c-df-contents/datafeeds-reference.md) unter Daten-Feeds.

### Ausschließlich unterstützte Metriken

* **Besuche**: Diese Metrik schließt im Kontext von Data Warehouse nicht persistente Cookie-Besuche aus.
* **Besuche - Alle Besucher**: Diese Metrik hat im Kontext von Data Warehouse eine engere Parität mit der Besuchsmetrik in anderen Tools in Adobe Analytics.

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

