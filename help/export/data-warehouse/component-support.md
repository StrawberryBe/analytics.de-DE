---
title: Komponentenunterstützung in Data Warehouse
description: Erfahren Sie, welche zusätzlichen Dimensionen und Metriken in Data Warehouse verfügbar sind und was nicht unterstützt wird.
translation-type: tm+mt
source-git-commit: 6bae6861586fc2aba33888cadfec3b1399898b90

---


# Komponentenunterstützung in Data Warehouse

Die eindeutige Verarbeitungsarchitektur von Data Warehouse ermöglicht einige Komponenten, die normalerweise nicht in anderen Funktionen von Adobe Analytics verfügbar sind. Aufgrund der einzigartigen Architektur sind einige Komponenten nicht für Berichte oder Segmente verfügbar. Verwenden Sie diese Seite, um zu verstehen, was verwendet werden kann und was nicht.

## Eindeutige Komponenten von Data Warehouse

Einige Dimensionen und Metriken können in Data Warehouse verwendet werden, während sie nicht mit anderen Funktionen in Adobe Analytics verfügbar sind.

### Dimensionen, die exklusiv unterstützt werden

* Experience Cloud-Besucher-ID:
* IP:
* Seiten-URL:
* Kauf-IDs:
* Besucher-ID: Gibt den eindeutigen Bezeichner für den Besucher an. Dieser Wert ist identisch mit verketteten Werten und `visid_high``visid_low` Spalten in Datenfeeds. Weitere Informationen finden Sie unter [Datenspaltenreferenz](../analytics-data-feed/c-df-contents/datafeeds-reference.md) unter Datenfeeds.

### Metriken, die exklusiv unterstützt werden

* Besuche: Diese Metrik im Kontext von Data Warehouse schließt nicht beständige Cookie-Besuche ein.
* Besuche - Alle Besucher: Diese Metrik im Kontext von Data Warehouse hat eine engere Gleichheit mit der Besuchsmetrik in anderen Tools in Adobe Analytics.

## Komponenten, die in Data Warehouse nicht unterstützt werden

Einige Dimensionen und Metriken werden in Data Warehouse nicht unterstützt.

> [!IMPORTANT] Wenn eine Dimension oder Metrik in Data Warehouse nicht unterstützt wird, werden Segmente, die diese Komponenten verwenden, nicht unterstützt. Prüfen Sie stets die Produktkompatibilität, wenn Sie ein Segment erstellen oder bearbeiten.

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
   * Alle Dimensionen der Einsendung außer Entrypage
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
* Seiten nicht gefunden (nur Segmente)
* Gebührenpflichtige Suche
* Einzelseitenbesuche
* Nachverfolgung der Gründe für den Ausstieg
* US-Staaten

### Metriken werden nicht unterstützt

* Einige pfadbasierte Metriken, darunter:
   * Absprünge
   * Einträge
   * Ausstiege
   * Neuladungen
   * Einzelzugriff
   * Besuchszeitmetriken
