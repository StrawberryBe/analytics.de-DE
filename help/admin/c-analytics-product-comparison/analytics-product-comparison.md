---
description: Systemanforderungen und ein Vergleich von Analysis Workspace, Reports & Analytics, Ad Hoc Analysis, Report Builder, Data Warehouse und Data Workbench
title: Analytics – Produktvergleich und Voraussetzungen
translation-type: tm+mt
source-git-commit: 456459eab5ae26b49d16d9648a52e46a5818df44
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 83%

---


# Analytics  – Produktvergleich und Voraussetzungen

Systemanforderungen und ein Vergleich von Analysis Workspace, Reports &amp; Analytics, ReportBuilder, Data warehouse, Data Workbench, Analytics API 2.0, Data Feeds und Customer Journey Analytics.

Informationen zu den zu verwendenden Adobe Analytics-Produkten finden Sie [hier](/help/admin/c-analytics-product-comparison/which-analytics-tool.md).

| Produktname und Link zur Hilfe | [Analysis Workspace](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/home.html) | [Reports &amp; Analytics](https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/getting-started.html) | [Report Builder](https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/home.html) | [Data Warehouse](https://docs.adobe.com/content/help/de-DE/analytics/export/data-warehouse/data-warehouse.html) | [Data Workbench](https://docs.adobe.com/content/help/de-DE/data-workbench/using/home.html) | Analytics API 2.0 | Daten-Feeds |
|---|---|---|---|---|---|---|---|
| **Zugriffsmethode** | Browserlösung zum Erstellen robuster, benutzerspezifischer Analyseprojekte und demokratisierender Erkenntnisse | Browserlösung für digitale Analysen | Browserlösung, die Berichte im CSV-Format generiert. Kann Dateien im Tableau-Format generieren. | Mehrkanalanalysetool für erweiterte Analysen, wie benutzerspezifische Zuordnungsmodelle, Predictive Analytics und Rundum-Kundenanalysen |  |  |  |
| **Berichtsaufschlüsselungen** | Unbegrenzt | Bis zu 2 Korrelationen | Bis zu 2 Korrelationen | Führt vollständig erweiterte, uneingeschränkte Aufschlüsselungen nach Segment durch | Unbegrenzt |  |  |
| **Segmentvergleiche** | Unbegrenzt | Bis zu 2 Segmente | Unbegrenzt (Stapelung von Datenanforderungen) | 1 Segment. Unterstützt mehrere (gestapelte) Segmente | Unbegrenzt |  |  |
| **Zeilenausgabegrenze** | 400 | 200 | 50.000 | Unbegrenzt | Anpassbar |  |  |
| **** Grenzen für individuelle Werte (in eVar-/prop-Berichten) | 500.000–2.000.000 | 500.000–2.000.000 | 500.000–2.000.000 | Unbegrenzt | Anpassbar |  |  |
| **Trichter/Pfadsetzung** | Ja: [Trichteranalyse](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html)/[Fluss](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/flow/flow.html) | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/reports.html) | Ja | Nein | Ja |  |  |
| **Advanced Customer Journey-Analyse** | Yes: [Customer Journey Analytics](https://docs.adobe.com/content/help/de-DE/analytics-platform/using/cja-landing.html) | Nein | Nein | Nein | Ja |  |  |
| **Kohortenanalyse** | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) | Nein | Nein | Nein | Ja |  |  |
| **Erweiterte Attribution** | Ja: [Zuordnung IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution-iq.html) | Begrenzt – erste/letzte/linear | Begrenzt – erste/letzte/linear | Begrenzt – erste/letzte/linear | Ja |  |  |
| **Verbesserte Visualisierungsoptionen** | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) | Nein | Ja | Nein | Ja |  |  |
| **Anpassbares Layout** | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/home.html) | Ja – [Dashboards](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/dashboard.html) | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/layout/configure-the-custom-layout.html) | Ergebnissortierung nach Aufschlüsselung oder nach Metrik | Ja |  |  |
| **** Projektkuratierung (vereinfachte Berichte für Nicht-Analytiker) | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/curate.html) | Nein | Ja | Nein | Ja |  |  |
| **Projektfreigabe** | [Ja: alle/beliebige Benutzer](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/curate.html) | [Ja: alle/beliebige Benutzer](https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/scheduling.html) | Ja: alle/beliebige Benutzer | Nein | Ja |  |  |
| **Versand für terminierte Berichte** | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/schedule-projects.html) | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/scheduling.html) | [Ja](https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/t-schedule-a-data-request.html) | Ja | Ja |  |  |
| **Systemanforderungen** | <br>[BrowserMehr...](https://docs.adobe.com/content/help/de-DE/analytics/admin/sys-reqs.html) | <br>[BrowserMehr...](https://docs.adobe.com/content/help/de-DE/analytics/admin/sys-reqs.html) | Windows, MS<br>[ExcelMehr...](https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/report-builder-setup/system-requirements.html) | Browser und Programm zum Öffnen von CSV-Dateien wie MS Excel, Kann Dateien im Tableau-Format generieren. | Windows 64 bit, good graphics adapter for OpenGL 3.2 [More...](https://docs.adobe.com/content/help/de-DE/data-workbench/using/install/c-data-workbench-client-install.html) |  |  |  |
| **Kompatibilität mit Virtual Report Suite (Berichtszeitverarbeitung)** | Ja | Ja | Ja | Nein | Ja? |  |  |
| **Mehrere Report Suites** | Ja | Nein | Nein | Nein | Ja? |  |  |
| **Berechnete Metriken** | Ja | Ja | Ja | Ja | Ja |  |  |
| **Kompatibilität mit Marketing Kanal** | Ja | Ja | Ja | ? | ? |  |  |
| **Granularitätsstufe** |  |  |  |  |  |  |  |
| **Anomalieerkennung** | Ja | Nein |  |  |  |  |  |
| **Beitragsanalyse** | Ja | Nein | Nein | Nein | Ja |  |  |
| **Segmenttypen** |  |  |  |  |  |  |  |