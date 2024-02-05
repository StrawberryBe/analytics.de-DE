---
description: Systemanforderungen und ein Vergleich von Analysis Workspace, Report Builder, Data Warehouse und Data Workbench
title: Analytics – Produktvergleich und Voraussetzungen
exl-id: 5adc6c10-cbbb-48d5-a7ab-367cbaff5e8a
feature: Analytics Basics
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: ht
source-wordcount: '340'
ht-degree: 100%

---

# Analytics – Produktvergleich und Voraussetzungen

Diese Seite enthält einen Vergleich verschiedener Adobe Analytics-Produkte: Analysis Workspace, Report Builder, Data Warehouse, Daten-Feeds und Analytics-API 2.0.

Informationen dazu, welches Adobe Analytics-Produkt verwendet werden sollte, finden Sie unter [Welches Adobe Analytics-Tool sollte ich verwenden?](/help/analyze/get-started/which-analytics-tool.md).

| Produktname und Link zur Hilfe | [Analysis Workspace](/help/analyze/analysis-workspace/home.md) | [Report Builder](/help/analyze/report-builder/home.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Data Feeds](/help/export/analytics-data-feed/data-feed-overview.md) | [Analytics-API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|
| **Zugriffsmethode** | [Browser](/help/analyze/get-started/sys-reqs.md) | [MS Excel für Windows](/help/analyze/report-builder/setup/system-requirements.md) | Einrichtung über den Browser. [Weitere Informationen](/help/analyze/get-started/sys-reqs.md) | Einrichtung über den Browser. [Weitere Informationen](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful-API-Tools. Melden Sie sich mit Adobe Developer-Anmeldeinformationen an. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| **Datengranularität** | Aggregiert | Aggregiert | Aggregiert | Treffer | Aggregiert |
| **Experience Cloud ID (ECID) verfügbar** | Nein | Nein | Ja | Ja | Nein |
| **Zeitstempel verfügbar** | Nein | Nein | Nein | Ja | Nein |
| **Verarbeitungsstufe** | Vollständig verarbeitet | Vollständig verarbeitet, mit separatem [Echtzeitbericht](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md) | Vollständig verarbeitet | Vollständig verarbeitet | Vollständig verarbeitet |
| **Admin-Bot-Filterdaten enthalten** <br> [Weitere Infos](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md) | Nein | Ja - separater Bot-Bericht | Nein | Nein | Nein |
| **Geringer Traffic (Individuelle Werte überschritten) wird angezeigt** <br> [Weitere Informationen](/help/technotes/low-traffic.md) | Ja | Ja | Nein | Nein | Ja |
| **Begrenzung der sichtbaren Zeilen (vor der Paginierung)** | 400 | 50000 | Unbegrenzt | Unbegrenzt | 50000 |
| **Mehrere Report Suites** | [Ja](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | Ja | Nein | Ja | Nein | Ja |
| **Anzahl der Aufschlüsselungen** | Unbegrenzt | Bis zu 2 | Unbegrenzt | Unbegrenzt | Unbegrenzt, über mehrere Abfragen ausführen |
| **Segmentierung** <br> [Weitere Informationen](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | Ja | Ja | Ja, mit [Einschränkungen](/help/components/segmentation/seg-reference/seg-compatibility.md) | Nein | Ja |
| **Berechnete Metriken** <br> [Weitere Infos](/help/components/c-calcmetrics/cm-overview.md) | Ja, mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) | Ja, mit Attribution | Ja | Nein | Ja, mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Marketing-Kanäle** <br> [Weitere Infos](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | Ja | Ja | Ja | Ja – [va_finder, va_closer](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | Ja |
| **Kohortenanalyse** | [Ja](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | Ja | Nein | Nein | Nein |
| **Attribution** | Ja, mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) | Begrenzt | Nein | Nein | Ja, mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) | Nein |
| **Kuratierung** <br> [Weitere Infos](/help/analyze/analysis-workspace/curate-share/curate.md) | Ja – Projekt und Virtual Report Suite | Nein | Nein | Nein | Ja – nur Virtual Report Suite |
| **Projektfreigabe** <br> [Weitere Infos](/help/analyze/analysis-workspace/curate-share/share-projects.md) | Ja, mit Projektrollen | Ja | Nein | Nein | Nein |
| **Geplanter Versand** | Ja | Ja | Ja | Ja | Nein |
| **Versandziele** | E-Mail | E-Mail, FTP, SFTP, [Veröffentlichung auf Microsoft Power BI](/help/analyze/report-builder/c-publish-power-bi/power-bi.md) | Amazon S3, Google Cloud Platform, Azure SAS, Azure RBAC und E-Mail | Amazon S3, Azure RBAC, Azure SAS und Google Cloud Platform | – |
| **Berichtszeitverarbeitung von Virtual Report Suite** <br> [Weitere Informationen](/help/components/vrs/vrs-report-time-processing.md) | Ja | Nein | Nein | Nein | Ja |
