---
description: Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.
seo-description: Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.
seo-title: Funktionsweise von Data Sources
solution: Analytics
subtopic: Datenquellen
title: Funktionsweise von Data Sources
topic: Entwickler und Implementierung
uuid: ee 9 e 6 e 74-9 b 00-4733-9 a 4 b-d 9 f 2 b 954 cc 7 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Funktionsweise von Data Sources

Informationen darüber, wie Adobe Zugriff auf Data Sources bereitstellt.

>[!NOTE]
>
>Sobald die importierten Daten über die Datenquellen-Funktion übermittelt wurden, unterscheiden sich importierte Daten nicht von Berichtsdaten, die mit anderen Methoden erfasst wurden (javascript-Beacon, actionsource, Data Insertion API usw.). Nachdem die Daten importiert wurden, können sie nicht mehr entfernt werden.

![](assets/data_sources_overview.png)

Für die Übertragung von Daten stehen zwei Möglichkeiten zur Verfügung:

* [FTP](../../import/c-data-sources/datasrc-how-data-sources-works.md#section_0E70022648F94061AF5B4AD6C7145243)
* [API](../../import/c-data-sources/datasrc-how-data-sources-works.md#section_65DACC9CE00C437BBFDD02D19C25A4BD)

## FTP {#section_0E70022648F94061AF5B4AD6C7145243}

Sie erstellen und verwalten FTP-basierte Datenquellen über Marketingberichte, das zum Importieren von Datendateien in Data Sources die FTP-Dateiübertragung nutzt. Nach Erstellen einer Datenquelle bietet Adobe Ihnen einen FTP-Speicherort an, in den Sie Datenquelle-Dateien hochladen können. Data Sources erkennt und verarbeitet die Dateien nach dem Hochladen automatisch. Nach der Verarbeitung stehen die Daten zur Nutzung in Marketingberichte zur Verfügung.

## API {#section_65DACC9CE00C437BBFDD02D19C25A4BD}

Adobe bietet eine Data Sources-API, über die Sie Ihre Anwendungen programmatisch in die Datenquellen-Funktion verknüpfen können. Sie benötigen somit keinen zwischengeschalteten FTP-Server; die Daten werden mittels HTTP, SOAP und REST übertragen.

Siehe [Dokumentation zur Data Sources-API](https://marketing.adobe.com/developer/documentation/data-sources/c-data-sources-api).
