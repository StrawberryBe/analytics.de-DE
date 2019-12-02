---
title: Verwalten von Datenfeed-Aufträgen
description: Erfahren Sie, wie Sie einzelne Aufträge in Data Feeds verwalten.
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Verwalten von Datenfeed-Aufträgen

Aufträge sind einzelne Aufgaben, die eine komprimierte Datei ausgeben. Sie werden von Feeds erstellt und verwaltet.

Gehen Sie wie folgt vor, um auf die Verwaltung von Data Feed-Aufträgen zuzugreifen:

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
2. Klicken Sie oben rechts auf das 9-Raster-Menü und dann auf [!UICONTROL Analytics].
3. Klicken Sie im oberen Menü auf [!UICONTROL Admin] &gt; [!UICONTROL Datenfeeds].
4. Klicken Sie oben auf die Registerkarte "Aufträge".

![Datenfeed-Menü](assets/AdminMenu.png)

## Navigieren in der Oberfläche

Ein Datenfeed-Auftrag ist eine einzelne Instanz, in der Adobe eine komprimierte Datei für ein bestimmtes Berichtsfenster verarbeitet und ausgibt. Der Job Manager bietet eine verfeinerte Ansicht, um den Status einzelner Aufträge zu sehen.

![Aufträge](assets/jobs.jpg)

### Filter und Suche

Verwenden Sie Filter und suchen Sie nach dem gewünschten Auftrag.

Klicken Sie ganz links auf das Filtersymbol, um die Filteroptionen ein- oder auszublenden. Filter sind nach Kategorie geordnet. Klicken Sie auf das Chevron, um die Filterkategorien zu reduzieren oder zu erweitern. Markieren Sie das Kontrollkästchen, um diesen Filter anzuwenden.

![Filter](assets/jobs-filter.jpg)

Verwenden Sie die Suche, um einen Auftrag nach Namen zu suchen.

![Durchsuchen](assets/search.jpg)

### Feeds und Aufträge

Klicken Sie auf die Registerkarte Feeds, um allgemeine Feeds anzuzeigen, die diese Aufträge erstellen. See [Manage data feeds](df-manage-feeds.md).

### Spalten

Jeder Auftrag zeigt mehrere Spalten mit Informationen dazu an. Klicken Sie auf eine Spaltenüberschrift, um sie in aufsteigender Reihenfolge zu sortieren. Klicken Sie erneut auf eine Spaltenüberschrift, um sie in absteigender Reihenfolge zu sortieren. Wenn eine bestimmte Spalte nicht angezeigt wird, klicken Sie auf das Spaltensymbol oben rechts.

![Spaltensymbol](assets/job-cols.jpg)

* **Feed-ID**: Zeigt die Feed-ID an, eine eindeutige ID. Aufträge, die von demselben Feed erstellt werden, haben dieselbe Feed-ID.
* **Auftrag-ID**: Eine eindeutige ID für den Auftrag. Alle Aufträge haben eine andere Job-ID.
* **Feed-Name**: Erforderliche Spalte. Zeigt den Feed-Namen an. Aufträge, die von demselben Feed erstellt werden, haben denselben Feed-Namen.
* **Report Suite**: Die Report Suite, aus der der Auftrag Daten referenziert.
* **Report Suite-ID**: Die eindeutige Kennung der Report Suite.
* **Startzeit**: Der Zeitpunkt, zu dem der Auftrag gestartet wurde. Datum und Uhrzeit werden in der Zeitzone der Report Suite mit GMT-Versatz angezeigt. Tägliche Feeds beginnen üblicherweise nahe Mitternacht in der Zeitzone der Report Suite.
* **Status**: Der Status des Feeds.
   * Warten auf Daten: Der Auftrag ist betriebsbereit und Daten für das Berichtsfenster werden erfasst.
   * Verarbeitung: Der Auftrag erstellt die Datendateien und bereitet das Senden vor.
   * Abgeschlossen: Der Auftrag wurde ohne Probleme abgeschlossen.
   * Fehlgeschlagen: Der Auftrag wurde nicht abgeschlossen. Informationen zur Ermittlung der Fehlerursache finden Sie unter [Fehlerbehebung bei Aufträgen](jobs-troubleshooting.md) .
   * Warten auf Export: Die Daten für das Berichtsfenster wurden noch nicht vollständig verarbeitet.
   * Keine Daten: Die Report Suite für das angeforderte Berichtsfenster enthält keine Daten.
* **Abschlusszeit**: Der Zeitpunkt, zu dem der Auftrag beendet wurde. Datum und Uhrzeit werden in der Zeitzone der Report Suite mit GMT-Versatz angezeigt.
* **Angefordertes Datum**: Das Berichtsfenster der Datei. Tägliche Feeds zeigen in der Regel 00:00 - 23:59 mit einem GMT-Offset an, was einen vollständigen Tag basierend auf der Zeitzone der Report Suite anzeigt. Stündliche Feeds zeigen die einzelne Stunde an, für die der Auftrag ausgeführt wird.
