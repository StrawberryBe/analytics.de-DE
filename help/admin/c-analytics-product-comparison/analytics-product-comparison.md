---
description: Systemanforderungen und ein Vergleich von Analysis Workspace, Reports & Analytics, Ad Hoc Analysis, Report Builder, Data Warehouse und Data Workbench
title: Analytics – Produktvergleich und Voraussetzungen
translation-type: tm+mt
source-git-commit: 54d6b4c2993c5b0391b9243c76661db1da4087b8
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 54%

---


# Analytics  – Produktvergleich und Voraussetzungen

Diese Seite enthält einen Vergleich verschiedener Adobe Analytics-Produkte: Analysis Workspace, Reports &amp; Analytics, Report Builder, Data warehouse, Data Workbench, Data Feeds und Analytics API 2.0.

Informationen zu den zu verwendenden Adobe Analytics-Produkten finden Sie [hier](/help/admin/c-analytics-product-comparison/which-analytics-tool.md).

| Produktname und Link zur Hilfe | [Analysis Workspace](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/home.html) | [Reports &amp; Analytics](https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/getting-started.html) | [Report Builder](https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/home.html) | [Data Warehouse](https://docs.adobe.com/content/help/de-DE/analytics/export/data-warehouse/data-warehouse.html) | [Data Workbench](https://docs.adobe.com/content/help/de-DE/data-workbench/using/home.html) | [Data Feeds](https://docs.adobe.com/content/help/de-DE/analytics/export/analytics-data-feed/data-feed-overview.html) | [Analytics API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|---|---|
| **Zugriffsmethode** | [Browser](https://docs.adobe.com/content/help/de-DE/analytics/admin/sys-reqs.html) | [Browser](https://docs.adobe.com/content/help/de-DE/analytics/admin/sys-reqs.html) | [MS Excel für Windows](https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/report-builder-setup/system-requirements.html) | Einrichtung über den Browser. [Mehr Infos](https://docs.adobe.com/content/help/de-DE/analytics/admin/sys-reqs.html) | [Windows 64 Bit](https://docs.adobe.com/content/help/de-DE/data-workbench/using/install/c-data-workbench-client-install.html) | Einrichtung über den Browser. [Mehr Infos](https://docs.adobe.com/content/help/de-DE/analytics/export/analytics-data-feed/data-feed-overview.html) | RESTful-API-Tools. Melden Sie sich mit Adobe-E/A-Anmeldeinformationen an. [Mehr Infos](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| **Datengranularität** | Aggregiert | Aggregiert | Aggregiert | Aggregiert | Treffer | Treffer | Aggregiert |
| **Verfügbare Experience Cloud ID (ECID)** | Nein | Nein | Nein | Ja | Ja | Ja | Nein |
| **Zeitstempel verfügbar** | Nein | Nein | Nein | Nein | Ja | Ja | Nein |
| **Verarbeitungsstufe** | Vollständig verarbeitet | Vollständig verarbeitet, mit separatem [Echtzeitbericht](https://docs.adobe.com/content/help/en/analytics/components/real-time-reporting/realtime.html) | Vollständig verarbeitet, mit separatem [Echtzeitbericht](https://docs.adobe.com/content/help/en/analytics/components/real-time-reporting/realtime.html) | Vollständig verarbeitet | Vollständig verarbeitet | Vollständig verarbeitet | Vollständig verarbeitet |
| **Admin-Bot-Filterdaten enthalten** <br>[Weitere Informationen](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/bot-removal/bot-removal.html) | Nein | Ja - gesonderter Bot-Bericht | Ja - gesonderter Bot-Bericht | Nein | Nein | Nein | Nein |
| **Geringer Traffic (Individuelle Werte überschritten) wird angezeigt** <br>[Weitere Informationen](https://docs.adobe.com/content/help/de-DE/analytics/technotes/low-traffic.html) | Ja | Ja | Ja | Nein | Nein | Nein | Ja |
| **Sichtbare Zeilenbegrenzung (vor Paginierung)** | 400 | 200 | 50000 | Unbegrenzt | Unbegrenzt | Unbegrenzt | 50000 |
| **Mehrere Report Suites** | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html) | Ja, mit Einschränkungen | Ja | Nein | Ja | Nein | Ja |
| **Anzahl der Aufschlüsselungen** | Unbegrenzt | Bis zu 2 | Bis zu 2 | Unbegrenzt | Unbegrenzt | Unbegrenzt | Unbegrenzt, mehrere Abfragen |
| **Segmentierung** <br>[Weitere Informationen](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-workflow.html) | Ja | Ja | Ja | Ja, mit [Einschränkungen](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segment-reference/seg-compatibility.html) | Ja | Nein | Ja |
| **Berechnete Metriken** <br>[Weitere Informationen](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/cm-overview.html) | Ja, mit [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) | Ja | Ja | Nein | Ja | Nein | Ja, mit [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) |
| **Marketing-Kanal** <br>[Weitere Informationen](https://docs.adobe.com/content/help/de-DE/analytics/components/marketing-channels/c-getting-started-mchannel.html) | Ja | Ja | Ja | Ja | Ja | Ja - [va_finder, va_closer](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html) | Ja |
| **Kohorte-Analyse** | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) | Nein | Nein | Nein | Ja | Nein | Nein |
| **Attribution** | Ja, mit [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) | Limited | Limited | Nein | Ja | Nein | Ja, mit [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) |
| **Funktionen** von Virtual Analyst <br>[Weitere Informationen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/virtual-analyst/overview.html) | Ja | Nein | Nein | Nein | Nein | Nein | Ja |
| **Kuratierung** <br>[Weitere Informationen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/curate.html) | Ja - Projekt und fRS | Nein | Nein | Nein | Nein | Nein | Ja - nur VRS |
| **Projektfreigabe** <br>[Weitere Informationen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/share-projects.html) | Ja, mit Projektrollen | Ja | Ja | Nein | Ja | Nein | Nein |
| **Geplante Bereitstellung** | Ja | Ja | Ja | Ja | Nein | Ja | Nein |
| **Versand-Ziele** | E-Mail | E-Mail | E-Mail, FTP, SFTP, [Veröffentlichung auf Microsoft PowerBI](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/publish-powerbi/power-bi.html) | E-Mail, FTP. Wenden Sie sich an die Kundenunterstützung, um weitere Unterstützung für das Ziel zu erhalten, einschließlich SFTP, Azurblauch, Amazon S3 | – | FTP, SFTP, Azurblauch, Amazon S3 | – |
| **VRS-Berichtszeitverarbeitung** <br>[Weitere Informationen](https://docs.adobe.com/content/help/de-DE/analytics/components/virtual-report-suites/vrs-report-time-processing.html) | Ja | Nein | Nein | Nein | Nein | Nein | Ja |
