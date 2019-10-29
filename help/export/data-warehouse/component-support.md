---
title: Komponentenunterstützung in Data Warehouse
description: Erfahren Sie, welche zusätzlichen Dimensionen und Metriken in Data Warehouse verfügbar sind und was nicht unterstützt wird.
translation-type: tm+mt
source-git-commit: 00d4d59cb4c922b54a97ef7000e294ef3bf61f20

---


# Komponentenunterstützung in Data Warehouse

Die einzigartige Verarbeitungsarchitektur von Data Warehouse ermöglicht einige Komponenten, die normalerweise nicht in anderen Funktionen von Adobe Analytics verfügbar sind. Aufgrund seiner einzigartigen Architektur stehen einige Komponenten weder für Berichte noch für Segmente zur Verfügung. Verwenden Sie diese Seite, um zu verstehen, was verwendet werden kann und was nicht.

## Für Data Warehouse spezifische Komponenten

Einige Dimensionen und Metriken können in Data Warehouse verwendet werden, nicht jedoch mit anderen Funktionen in Adobe Analytics.

### Ausschließlich unterstützte Dimensionen

* Experience Cloud ID: Bei Implementierungen, die den Experience Cloud ID-Dienst (ECID) verwenden, eine 128-Bit-Zahl, die aus zwei verketteten 64-Bit-Zahlen besteht, die zu 19 Ziffern hinzugefügt werden.
* Seiten-URL: Die Seiten-URL, auf der der Treffer aufgetreten ist.
* Kauf-IDs: Eindeutige ID für einen Kauf, festgelegt mit der Variablen purchaseID.
* Besucher-ID: Stellt die eindeutige Kennung des Besuchers bereit. Dieser Wert entspricht dem verketteten Wert von `visid_high` und `visid_low` Spalten in Datenfeeds. Weitere Informationen finden Sie unter Datenspaltenverweis[ ](../analytics-data-feed/c-df-contents/datafeeds-reference.md)unter Datenfeeds.

### Exklusiv unterstützte Metriken

* Besuche: Diese Metrik im Zusammenhang mit Data Warehouse schließt nicht beständige Cookie-Besuche aus.
* Besuche - Alle Besucher: Diese Metrik im Zusammenhang mit Data Warehouse ist mit der Besuchsmetrik in anderen Tools in Adobe Analytics enger verknüpft.

## Komponenten, die in Data Warehouse nicht unterstützt werden

Einige Dimensionen und Metriken werden in Data Warehouse nicht unterstützt.

> [!NOTE] Wenn eine Dimension oder Metrik in Data Warehouse nicht unterstützt wird, werden Segmente, die diese Komponenten verwenden, auch nicht unterstützt. Überprüfen Sie beim Erstellen oder Bearbeiten eines Segments immer die Produktkompatibilität.

### Dimensionen werden nicht unterstützt

* Einige zeitbasierte Dimensionen, darunter:
   * Vormittag/Nachmittag
   * Tag des Monats
   * Wochentag
   * Tag des Jahres
   * Stunde des Tages
   * Minute
   * Monat des Jahres
   * Viertel des Jahres
   * Wochentag/Wochenende
   * Jahr
* Einige pfadbasierte Dimensionen, darunter:
   * Alle Entrypabmessungen außer Entrypage
   * Alle Ausstiegsdimensionen außer Ausstiegsseite und Ausstiegslink
   * Treffertiefe
   * Rückkehrhäufigkeit
   * Zeit vor Ereignis
   * Besuchszeit pro Seite – Zusammengefasst
   * Zeit pro Besuch – Zusammengefasst
   * Besuchstiefe
* Rangansicht aller Suchseiten
* Hierarchievariablen
* Treffertyp
* nicht gefundene Seiten (als Dimension verfügbar) nicht unterstützt für Segmentierung)
* Gebührenpflichtige Suche
* Einzelseitenbesuche
* Nachverfolgung der Gründe für den Ausstieg
* US-Staaten

### Nicht unterstützte Metriken

* Einige pfadbasierte Metriken, darunter:
   * Absprünge
   * Einträge
   * Ausstiege
   * Neuladungen
   * Einzelzugriff
   * Besuchszeit-Metriken
