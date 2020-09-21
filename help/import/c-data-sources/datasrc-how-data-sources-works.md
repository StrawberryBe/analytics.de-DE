---
description: Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.
subtopic: Data sources
title: Funktionsweise von Data Sources
topic: Developer and implementation
uuid: ee9e6e74-9b00-4733-9a4b-d9f2b954cc7c
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '179'
ht-degree: 100%

---


# Funktionsweise von Data Sources

Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.

>[!NOTE]
>
>Sobald importierte Daten über Data Sources übertragen wurden, sind sie nicht mehr von Berichtsdaten zu unterscheiden, die mit anderen Methoden erfasst wurden (JavaScript-Beacon, ActionSource, Data Insertion API usw.). Nachdem die Daten importiert wurden, können sie nicht mehr entfernt werden.

![](assets/data_sources_overview.png)

Für die Übertragung von Daten stehen zwei Möglichkeiten zur Verfügung:

* [FTP](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_0E70022648F94061AF5B4AD6C7145243)
* [API](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_65DACC9CE00C437BBFDD02D19C25A4BD)

## FTP {#section_0E70022648F94061AF5B4AD6C7145243}

Sie erstellen und verwalten FTP-basierte Datenquellen über Marketingberichte, das zum Importieren von Datendateien in Data Sources die FTP-Dateiübertragung nutzt. Nach Erstellen einer Datenquelle bietet Adobe Ihnen einen FTP-Speicherort an, in den Sie Datenquelle-Dateien hochladen können. Data Sources erkennt und verarbeitet die Dateien nach dem Hochladen automatisch. Nach der Verarbeitung stehen die Daten zur Nutzung in Marketingberichte zur Verfügung.

## API  {#section_65DACC9CE00C437BBFDD02D19C25A4BD}

Adobe bietet eine Data Sources-API, über die Sie Ihre Anwendungen programmatisch in die Datenquellen-Funktion verknüpfen können. Sie benötigen somit keinen zwischengeschalteten FTP-Server; die Daten werden mittels HTTP, SOAP und REST übertragen.

Siehe [Dokumentation zur Data Sources-API](https://github.com/AdobeDocs/analytics-1.4-apis/tree/master/docs/data-sources-api).
