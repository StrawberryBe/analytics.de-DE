---
description: Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.
seo-description: Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.
seo-title: Funktionsweise von Data Sources
solution: Analytics
subtopic: Datenquellen
title: Funktionsweise von Data Sources
topic: Entwickler und Implementierung
uuid: ee9e6e74-9b00-4733-9a4b-d9f2b954cc7c
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Funktionsweise von Data Sources

Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.

> [!NOTE] Sobald importierte Daten über die Datenquellen-Funktion übermittelt wurden, sind sie nicht von Berichtsdaten zu unterscheiden, die mit anderen Methoden (JavaScript-Beacon, ActionSource, Data Insertion API usw.) erfasst wurden. Nachdem die Daten importiert wurden, können sie nicht mehr entfernt werden.

![](assets/data_sources_overview.png)

Für die Übertragung von Daten stehen zwei Möglichkeiten zur Verfügung:

* [FTP](../../import/c-data-sources/datasrc-how-data-sources-works.md#section_0E70022648F94061AF5B4AD6C7145243)
* [API](../../import/c-data-sources/datasrc-how-data-sources-works.md#section_65DACC9CE00C437BBFDD02D19C25A4BD)

## FTP {#section_0E70022648F94061AF5B4AD6C7145243}

Sie erstellen und verwalten FTP-basierte Datenquellen über Marketingberichte, das zum Importieren von Datendateien in Data Sources die FTP-Dateiübertragung nutzt. Nach Erstellen einer Datenquelle bietet Adobe Ihnen einen FTP-Speicherort an, in den Sie Datenquelle-Dateien hochladen können. Data Sources erkennt und verarbeitet die Dateien nach dem Hochladen automatisch. Nach der Verarbeitung stehen die Daten zur Nutzung in Marketingberichte zur Verfügung.

## API {#section_65DACC9CE00C437BBFDD02D19C25A4BD}

Adobe bietet eine Data Sources-API, über die Sie Ihre Anwendungen programmatisch in die Datenquellen-Funktion verknüpfen können. Sie benötigen somit keinen zwischengeschalteten FTP-Server; die Daten werden mittels HTTP, SOAP und REST übertragen.

Siehe [Dokumentation zur Data Sources-API](https://marketing.adobe.com/developer/documentation/data-sources/c-data-sources-api).
