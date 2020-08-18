---
description: Systemanforderungen und ein Vergleich von Analysis Workspace, Reports & Analytics, Ad Hoc Analysis, Report Builder, Data Warehouse und Data Workbench
title: Analytics – Produktvergleich und Voraussetzungen
translation-type: tm+mt
source-git-commit: 8a48a5bd9e7ef38ffc90ecb9c640166bb3ac4405
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 54%

---


# Analytics – Produktvergleich und Voraussetzungen

Diese Seite enthält einen Vergleich verschiedener Adobe Analytics-Produkte: Analysis Workspace, Reports &amp; Analysen, Report Builder, Data Warehouse, Data Workbench, Data Feeds und Analytics API 2.0.

Informationen zu den zu verwendenden Adobe Analytics-Produkten finden Sie [hier](/help/admin/c-analytics-product-comparison/which-analytics-tool.md).

| Produktname und Link zur Hilfe | [Analysis Workspace](/help/analyze/analysis-workspace/home.md) | [Reports &amp; Analytics](/help/analyze/reports-analytics/getting-started.md) | [Report Builder](/help/analyze/report-builder/home.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Data Workbench](https://docs.adobe.com/content/help/de-DE/data-workbench/using/home.html) | [Data Feeds](/help/export/analytics-data-feed/data-feed-overview.md) | [Analytics API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|---|---|
| **Zugriffsmethode** | [Browser](/help/admin/sys-reqs.md) | [Browser](/help/admin/sys-reqs.md) | [MS Excel für Windows](/help/analyze/report-builder/setup/system-requirements.md) | Einrichtung über den Browser. [Weitere Infos](/help/admin/sys-reqs.md) | [Windows 64 Bit](https://docs.adobe.com/content/help/de-DE/data-workbench/using/install/c-data-workbench-client-install.html) | Einrichtung über den Browser. [Weitere Infos](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful-API-Tools. Melden Sie sich mit Adobe-E/A-Anmeldeinformationen an. [Weitere Infos](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| **Datengranularität** | Aggregiert | Aggregiert | Aggregiert | Aggregiert | Treffer | Treffer | Aggregiert |
| **Experience Cloud-ID (ECID) verfügbar** | Nein | Nein | Nein | Ja | Ja | Ja | Nein |
| **Zeitstempel verfügbar** | Nein | Nein | Nein | Nein | Ja | Ja | Nein |
| **Verarbeitungsstufe** | Vollständig verarbeitet | Vollständig verarbeitet, mit separatem [Echtzeitbericht](/help/components/c-real-time-reporting/realtime.md) | Vollständig verarbeitet, mit separatem [Echtzeitbericht](/help/components/c-real-time-reporting/realtime.md) | Vollständig verarbeitet | Vollständig verarbeitet | Vollständig verarbeitet | Vollständig verarbeitet |
| **Admin-Bot-Filterdaten enthalten** <br> [Weitere Infos](/help/admin/admin/bot-removal/bot-removal.md) | Nein | Ja - gesonderter Bot-Bericht | Ja - gesonderter Bot-Bericht | Nein | Nein | Nein | Nein |
| **Geringer Traffic (Individuelle Werte überschritten) wird angezeigt** <br> [Weitere Infos](/help/technotes/low-traffic.md) | Ja | Ja | Ja | Nein | Nein | Nein | Ja |
| **Sichtbare Zeilenbegrenzung (vor Paginierung)** | 400 | 200 | 50000 | Unbegrenzt | Unbegrenzt | Unbegrenzt | 50000 |
| **Mehrere Report Suites** | [Ja](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | Ja, mit Einschränkungen | Ja | Nein | Ja | Nein | Ja |
| **Anzahl der Aufschlüsselungen** | Unbegrenzt | Bis zu 2 | Bis zu 2 | Unbegrenzt | Unbegrenzt | Unbegrenzt | Unbegrenzt, mehrere Abfragen |
| **Segmentierung** <br> [Weitere Infos](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | Ja | Ja | Ja | Ja, mit [Einschränkungen](/help/components/segmentation/seg-reference/seg-compatibility.md) | Ja | Nein | Ja |
| **Berechnete Metriken** <br> [Weitere Infos](/help/components/c-calcmetrics/cm-overview.md) | Ja, mit [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) | Ja | Ja | Nein | Ja | Nein | Ja, mit [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Marketing-Kanäle** <br> [Weitere Infos](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | Ja | Ja | Ja | Ja | Ja | Ja - [va_finder, va_closer](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | Ja |
| **Kohorte-Analyse** | [Ja](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | Nein | Nein | Nein | Ja | Nein | Nein |
| **Attribution** | Ja, mit [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) | Limited | Limited | Nein | Ja | Nein | Ja, mit [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Virtual Analytics-Funktionen** <br> [Weitere Infos](/help/analyze/analysis-workspace/virtual-analyst/overview.md) | Ja | Nein | Nein | Nein | Nein | Nein | Ja |
| **Kuratierung** <br> [Weitere Infos](/help/analyze/analysis-workspace/curate-share/curate.md) | Ja - Projekt und fRS | Nein | Nein | Nein | Nein | Nein | Ja - nur VRS |
| **Projektfreigabe** <br> [Weitere Infos](/help/analyze/analysis-workspace/curate-share/share-projects.md) | Ja, mit Projektrollen | Ja | Ja | Nein | Ja | Nein | Nein |
| **Geplante Bereitstellung** | Ja | Ja | Ja | Ja | Nein | Ja | Nein |
| **Versand-Ziele** | E-Mail | E-Mail | E-Mail, FTP, SFTP, [Veröffentlichung auf Microsoft PowerBI](/help/analyze/report-builder/c-publish-power-bi/power-bi.md) | E-Mail, FTP. Wenden Sie sich an die Kundenunterstützung, um weitere Unterstützung für das Ziel zu erhalten, einschließlich SFTP, Azurblauch, Amazon S3 | – | FTP, SFTP, Azurblauch, Amazon S3 | – |
| **VRS-Berichtszeitverarbeitung** <br> [Weitere Infos](/help/components/vrs/vrs-report-time-processing.md) | Ja | Nein | Nein | Nein | Nein | Nein | Ja |
