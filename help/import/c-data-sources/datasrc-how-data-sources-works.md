---
description: Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.
subtopic: Data sources
title: Funktionsweise von Data Sources
topic: Developer and implementation
uuid: ee9e6e74-9b00-4733-9a4b-d9f2b954cc7c
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Funktionsweise von Data Sources

Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.

>[!NOTE] Sobald importierte Daten über Data Sources übertragen wurden, sind sie nicht mehr von Berichtsdaten zu unterscheiden, die mit anderen Methoden erfasst wurden (JavaScript-Beacon, ActionSource, Data Insertion API usw.). Die Daten können nach dem Import nicht mehr entfernt werden.

![](assets/data_sources_overview.png)

Es stehen zwei Methoden zum Senden von Daten zur Verfügung:

* [FTP](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_0E70022648F94061AF5B4AD6C7145243)
* [API](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_65DACC9CE00C437BBFDD02D19C25A4BD)

## FTP {#section_0E70022648F94061AF5B4AD6C7145243}

Sie können FTP-basierte Datenquellen über Marketing-Berichte erstellen und verwalten, die Datendateien über FTP-Dateiübertragung in Data Sources importieren. Nachdem Sie eine Datenquelle erstellt haben, stellt Adobe Ihnen einen FTP-Speicherort zur Verfügung, den Sie zum Hochladen der Datenquellendateien verwenden können. Nach dem Hochladen werden sie von Data Sources automatisch gefunden und verarbeitet. Nach der Verarbeitung stehen die Daten für Marketingberichte zur Verfügung.

## API  {#section_65DACC9CE00C437BBFDD02D19C25A4BD}

Adobe Angebots eine Data Sources-API, mit der Sie Ihre Anwendungen programmgesteuert mit Data Sources verknüpfen können. Dadurch entfällt der Bedarf an einem Zwischenserver für FTP und die Übertragung von Daten über HTTP, SOAP und REST.

Siehe [Data Sources-API-Dokumentation](https://github.com/AdobeDocs/analytics-1.4-apis/tree/master/docs/data-sources-api).
