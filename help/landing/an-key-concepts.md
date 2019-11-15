---
description: Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.
title: Adobe Analytics – Schlüsselkonzepte
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Adobe Analytics – Schlüsselkonzepte

Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.

## Analytics tools {#concept_833EDD4EB056491DA1BC5A3A45FE285B}

| Produkt | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Analysis Workspace | Browserlösung zum Erstellen robuster, benutzerdefinierter Analyseprojekte und Demokratisieren von Einblicken. Bietet mehr Berichtsflexibilität als Reports &amp; Analysen | [adobe.ly/aaworkspacedocs](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/analysis-workspace-features.html) |
| Reports &amp; Analysen (ehemals SiteCatalyst) | Browserlösung für die Berichterstellung und Analyse. Starter-Tool im Analytics-Paket. | [Reports &amp; Analysen - Startseite](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/getting-started.html) |
| Report Builder | Excel-Add-in, mit dem Sie benutzerdefinierte Anforderungen aus Adobe Analytics-Daten erstellen und diese mithilfe von Microsoft Excel visualisieren können. | [ReportBuilder-Startseite](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/home.html) |
| Ad-hoc-Analysen (früher Discover) | Java-basiertes Tool für erweiterte digitale Analysen. | [Ad-hoc-Analysen-Homepage](https://docs.adobe.com/content/help/en/analytics/analyze/ad-hoc-analysis/adhoc-home.html) |
| Data Workbench (ehemals Insight) | Wurde konstruiert, um Sie bei der Sammlung, Verarbeitung, Analyse und Visualisierung von Online- und Offline-Kundeninteraktionen über mehrere Kanäle hinweg zu unterstützen. | [Data Workbench Client](https://marketing.adobe.com/resources/help/en_US/insight/client/) |
| Data Warehouse | Unverarbeitete Rohdaten zur Speicherung und für benutzerdefinierte Berichte, die Sie durch Datenfilterung erstellen können. Nicht auf Treffer-Niveau. | [Data Warehouse - Home](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) |
| Adobe Mobile Services | Führt mobile Marketingfunktionen für mobile Anwendungen aus der ganzen Adobe Experience Cloud zusammen, sodass Sie Einblicke in die Benutzerinteraktionen Ihrer Anwendungen erhalten und gegebenenfalls Verbesserungen vornehmen können. | [Mobile Services - Startseite](https://docs.adobe.com/content/help/en/mobile-services/using/home.html) |
| Adobe Exchange Data Connectors (früher Genesis) | Importieren Sie Verfolgungsdaten aus Drittanbieteranwendungen in Analytics, um eine durchgängige Sichtbarkeit der Leistung an einem zentralen Ort zu gewährleisten. | [Data Connectors-Startseite](https://marketing.adobe.com/developer/documentation/genesis/c-overview-how-it-works) |
| Dynamisches Tag-Management (DTM) | Hilft bei der Verwaltung von Analytics-, Target- und anderen Tags für alle Ihre Sites, unabhängig von der Anzahl Ihrer Domänen. | [DTM-Startseite](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/dtm-implementation-overview.html) |
| Adobe Launch | Die nächste Generation von Website-Tag- und mobilen SDK-Verwaltungsfunktionen von Adobe. | [Adobe Launch Home](https://docs.adobe.com/content/help/en/launch/using/overview.html) |

## Key terminology {#concept_E473ACBB8E4A42B4AC005538AC12F154}

Klicken Sie [hier](https://docs.adobe.com/content/help/en/analytics/technotes/terms.html), um ein ausführliches Glossar der Adobe Analytics-Terminologie zu erhalten.

| Begriff | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Props (benutzerspezifischer Traffic) | Dimensionen, die zur Verfolgung der Traffic-Aktivität auf einzelnen Seiten verwendet werden. Eigenschaften bestehen nicht über Seiten hinweg. Schlüsselanwendungen für Traffic-Variablen: <ul><li>Einfache Zählung zur Suche nach dem beliebtesten Wert</li><li>Sichtbarkeit der Pfade von Benutzern durch Ihre Site </li></ul><br>Beispiele für Traffic-Variablen: Seitenname, Seitenabschnitte, Browser</br> | [Props](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/traffic-variables/traffic-var.html) |
| eVar (benutzerdefinierte Konversion) | Dimensionen, die für einen Zeitraum bestehen, der von Ihnen angepasst wird. Zu den Ablaufoptionen gehören Ablauf des Ereignisses, Ablauf des Besuchs oder Ablauf nach x Tagen. Die Option sollte nach der Analyseart gewählt werden, die auf die Variable angewandt wird.<br>Wichtige Unterschiede zwischen eVars und Props:</br><ul><li>Eigenschaften werden häufig für die Pfadanalyse verwendet, da Persistenz entfernt wird.</li><li>eVars werden häufig für die Konversionsanalyse verwendet.</li></ul><br>Beispiele für Konversionsvariablen: interne Suchbegriffe, interne Promotions, externe Kampagnen (s.campaign)</br> | [eVars](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html) |
| Ereignisse/Metriken (s.events) | Metriken, die wichtige Aktionen messen, die unsere Besucher auf unserer Site ausführen sollen. Es gibt drei Ereignisarten: Zähler, numerisch und Währung. Ereignisse sind am nützlichsten, wenn sie Berichten zu Konversionsvariablen (eVar) hinzugefügt werden. Die eVar gibt qualitative Informationen über Ereignisse und das Ereignis stellt die quantitative Information zu den Geschehnissen bereit. <br>Wichtige Unterschiede zwischen eVars und Ereignissen:</br><ul><li>eVars sagen uns, wer, was oder was die Konversion beeinflusst hat</li><li>Ereignisse messen, wie viele Konversionen stattgefunden haben</li></ul><br>Beispiele für Konversionsereignisse: Bestellungen, Anwendungsaufrufe, Leads, Umsatz.</br> | [Ereignisse](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/success-events/success-event.html) |
| Komponenten | Dimensionen, Metriken, Segmente und Zeitgranularitäten (Datumsbereiche), die Sie per Drag &amp; Drop in ein Projekt ziehen können. | [Komponenten](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html) |
| Dimensionen | Erfassung von eVars, Props, Classifications und von Adobe erfassten Standardwerten. | [Dimensionen](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-descriptions.html) |
| Metriken | Erfassung implementierter Ereignisse und berechneter Metriken. | [Metriken](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/apply-create-metrics.html) |
| Berechnete Metriken | Möglichkeit, benutzerspezifische Metriken aus vorhandenen Metriken abzuleiten, die über Ihre Implementierung erfasst wurden. | [Berechnete Metriken](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/cm-overview.html) |
| Segmente | Möglichkeit, leistungsstarke, zielgerichtete Zielgruppensegmente in Ihre Analyseberichte einzuschließen, sie zu verwalten, freizugeben und anzuwenden. Segmente werden über Analytics-Produkte hinweg freigegeben und können auch in der Experience Cloud geteilt werden. | [Segmentierung](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-home.html) |
| Zeit (Datumsbereiche) | Möglichkeit, das Datum auf einen beliebigen Zeitraum zu filtern und benutzerdefinierte Datumsbereiche zu erstellen, die in Ihrer Analyse wiederverwendet werden können. | [Datumsbereiche](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) |
| Visualisierungen | Reiche Visualisierungen, die dazu beitragen können, Daten in Ihren Projekten zum Leben zu erwecken. | [Visualisierungen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) |
| Kuratierung | Möglichkeit, die in einem Projekt oder in einer Virtual Report Suite verfügbaren Komponenten zu beschränken. | [VRS](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-components.html)<br>[curationProject](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html)</br><br>[curationComparison](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate-projects-vrs.html) |

## Wichtige Berichte

| Bericht | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Vollständige Liste der Dimensionen/Berichte | Vollständige Liste der Dimensionen/Berichte, die in Adobe Analytics verfügbar sind. | [Dimensionen](https://marketing.adobe.com/resources/help/en_US/reference/reports_descriptions.html) |
| Advertising Analytics | Analysieren Sie in Adobe Analytics alle Google- und Bing Paid Search-Daten nebeneinander. Die durch die Integration erstellten Dimensionen umfassen Anzeigenplattform, Suchbegriff, Übereinstimmungstyp usw. Zu den erstellten Metriken gehören AMO-Impressionen, AMO-Klicks, AMO-Kosten, Avg. Position und Durchschn. Qualitätsbewertung | [Advertising Analytics](https://docs.adobe.com/help/en/analytics/integration/advertising-analytics/overview.html) |
| Audience Analytics | Richten Sie eingehende Analytics-Treffer mit der Zielgruppenmitgliedschaft eines Benutzers in AAM ein. Sie können AAM-Zielgruppendaten wie demografische Informationen (z. B. Geschlecht oder Einkommensstufe), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten und Anzeigenimpressionsdaten in einen beliebigen Analytics-Arbeitsablauf einbeziehen. Durch diese Integration erstellte Dimensionen sind Zielgruppen-ID und Zielgruppenname. | [Audience Analytics](https://docs.adobe.com/content/help/en/analytics/integration/audience-analytics/mc-audiences-aam.html) |
| Attribution IQ | Ermöglicht es Ihnen, zu verstehen, wie bedeutsames Engagement während der gesamten Customer Journey stattfindet. Dabei werden auf intelligente Weise Inflationspunkte identifiziert, die Kunden zu zielgerichteten Ergebnissen führen, und Marketinginitiativen effektiv optimiert. Zu den Modellen gehören first, last, linear, Participation, j-förmig, umgekehrt j-förmig, u-form, same Touch, custom und time decay. | [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution.html) |
| Anomalieerkennung | Eine statistische Methode zur Bestimmung, wie sich eine bestimmte Metrik im Vergleich zu früheren Daten verändert hat. Die Anzeige ist standardmäßig für alle Trendvisualisierungen im Analysis Workspace aktiviert. | [Anomalieerkennung](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) |
| Beitragsanalyse | Erforscht das "Warum" hinter den auftretenden Anomalien, indem eine automatisierte Analyse jeder einzelnen Metrik und Dimension, auf die Sie Zugriff haben, durchgeführt wird. | [Beitragsanalyse](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Kohortenanalyse | Eine Kohorte ist eine Gruppe von Personen, die über einen bestimmten Zeitraum gemeinsame Merkmale aufweisen. Die Kohortenanalyse unterstützt Sie bei der Analyse der Kundenbindung und -abwandlung. | [Kohortenanalyse](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) |
| Berichte zur Customer Journey | Zeigt Informationen über den Pfad an, den Ihre Benutzer durch Ihre Site oder App nehmen. Eigenschaftsvariablen, eVars und Ereignisse können in dieser Analyse im Arbeitsbereich für Analysen verwendet werden. | [Trichteranalyse](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html)[im Arbeitsbereich für Analysen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/flow/flow.html)[FlowBerichte und Analysen](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-paths.html) |
| Marketing-Kanäle | Mithilfe von Berichte erfahren Sie mehr zu den externen Kanälen, über die Besucher auf Ihre Site gelangen, und welche davon bei der Generierung von Konversionen am effektivsten sind. Zuordnungsansichten für die erste und letzte Berührung werden bereitgestellt. Das ist die bevorzugte externe Traffic-Berichtsquelle in Adobe Analytics (anders als Kampagnen oder Traffic-Quellen), da sie den umfassendsten Überblick sowohl über gezahlte als auch organische Kanäle bietet. | [Marketing-Kanäle](https://docs.adobe.com/content/help/en/analytics/components/marketing-channels/c-getting-started-mchannel.html) |
| Mobile | Zeigt Informationen zu mit Mobilgeräten oder Tablets geöffneten Websites an. | [Mobilbericht | (https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-mobile.html) |
| Mobile Anwendung | Zeigt grundlegende Nutzungsinformationen in Bezug auf Ihre mobilen Anwendungen an. Diese Berichte sind verfügbar, wenn Ihre SDK implementiert und die Berichtsfunktion aktiviert wurde.  Zudem hat Adobe Mobile Services eine eigene Benutzeroberfläche für mobile Anwendungen erstellt, die vollständigere Anwendungsdaten anzeigt und es Ihnen ermöglicht, die Benutzerinteraktionen zu verstehen und zu verbessern.  Greifen Sie [hier](https://mobilemarketing.adobe.com)auf die Oberfläche zu. | [Adobe Mobile-Dienste](https://docs.adobe.com/content/help/en/mobile-services/using/home.html) | Produkte | Identifiziert, wie einzelne Produkte bzw. Produktgruppen (Kategorien) zu verschiedenen Konversionsmetriken wie Umsatz oder Checkouts beitragen. | [Produktbericht](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-products.html) |
| Segmentvergleich | Erkennt die statistisch signifikantesten Unterschiede zwischen Segmenten durch eine automatisierte Analyse jeder einzelnen Metrik und Dimension, auf die Sie Zugriff haben. | [Segmentvergleich](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html) |
| Site-Inhaltsbericht | Zeigt an, welche Seiten und Bereiche Ihrer Site am aktivsten sind und welche Server am häufigsten genutzt werden. | [Site-Inhaltsbericht](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-site-content.html) |
| Site-Metrikbericht | Zeigen quantitative Informationen über Ihre Website an, z. B. Unique Visitor, Bestellungen, Umsatz usw. Jede Metrik kann in andere elementbasierte Berichte übernommen werden. | [Site-Metrikbericht](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-site-metrics.html) |
| Besucherprofil | Mit diesen Berichten können Sie Kaufmuster von Kunden aus verschiedenen Profilkategorien (z. B. Ländern, Bundesländern, Postleitzahlen oder Domänen) ersehen. | [Besucherprofil](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-visitor-profile.html) |
| Besuchertreue | Zeigt Informationen über die Treue Ihrer Kunden an, z. B. wie viele Benutzer auf Ihre Site zurückkehren und wie oft sie das tun. | [Besuchertreue](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-visitor-retention.html) |
| Projektverknüpfung, Freigabe und Planung | Methoden zum Speichern und/oder Freigeben Ihrer Arbeit für andere über die Analytics-Benutzeroberfläche. | [Senden und Planen von Dateien](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/send-schedule-files.html) |

## Key metrics {#concept_392819DC275C48688E2CE4ABD4C5EE43}

| Kennzahlname | Definition | Dokumentationslink |
|---|---|---|
| Vollständige Metrikliste | Definition aller Metriken in Adobe Analytics. | [Übersicht über Metriken](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-overview.html) |
| Unique Visitors | Die Anzahl der nicht duplizierten Website-Besucher über einen festgelegten Zeitraum hinweg. | [Unique Visitors](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-unique-visitors-v15-dsc.html) |
| Besuche | Eine Folge von Seitenansichten während einer Sitzung. Der Besuch beginnt, wenn eine Person eine Seite der Website erstmalig ansieht, und endet nach einer Inaktivitätsperiode von 30 Minuten. | [Besuche](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-visit.html) |
| Seitenansichten | Eine Seitenansicht tritt auf, wenn ein Besucher eine Seite auf Ihrer Website aufruft. | [Seitenansichten](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-page-view.html) |
| Instanzen | Die Häufigkeit, mit der eine Variable definiert wurde. Jedes Mal, wenn Adobe Analytics einen Wert in einer Variablen feststellt, werden die entsprechenden Instanzen im Bericht um eine Stufe erhöht. | [Instanzen](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-instance.html) |
| Vorfälle | Die Frequenz, mit der eine Variable definiert oder beibehalten wurde. | [Vorfälle](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-occurrences.html) |

## Importoptionen {#concept_7C6DF03B5F9149E2A77F36C739432059}

| Option | Beschreibung | Dokumentationslink |
|---|---|---|
| Classification Importer | Metadaten gegen erfasste Abmessungen über Browser- oder FTP-Upload importieren. Manuelles Verfahren im Vergleich zu Rule Builder. | [Classification Importer](https://marketing.adobe.com/resources/help/en_US/reference/c_working_with_saint.html) |
| Regel-Builder | Automatisch Metadaten-Classifications von Abmessungen beruhend auf benutzerdefinierten Regeln erstellen. | [Classification Rule Builder](https://marketing.adobe.com/resources/help/en_US/reference/classification_rule_builder.html) |
| Kundenattribute | CRM-Daten, die zur Verwendung in Adobe Analytics und Adobe Target in die Experience Cloud hochgeladen wurden. | [Kundenattribute](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html) |
| Data Sources | Importieren Sie Offline-Metriken nach Dimensionen oder einfach nach Tagen in Analytics. | [Data Sources](https://docs.adobe.com/content/help/en/analytics/import/data-sources/datasrc-home.html) |
| Adobe Exchange Data Connectors | Siehe [Analytics-Tools](/help/landing/an-key-concepts.md) |  |
| Native Integrationen | Zielgruppenanalysen und Anzeigen-Analysen. | Siehe "Wichtige Berichte". |

## Export options {#concept_C62B688E259141CF92C048E8110464BE}

| Option | Beschreibung | Dokumentationslink |
|---|---|---|
| Downloads und Planung der Benutzeroberfläche | Daten aus dem Analysis Workspace als CSV oder PDF exportieren | [PDF- oder CSV-Dateien herunterladen](/help/analyze/analysis-workspace/curate-share/download-send.md) |
| Report Builder | Siehe Analytics-Werkzeuge. |
| Analytics-API | Erstellen Sie Ihre eigenen Anfragen für Analysedaten. | <ul><li>[API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)</li><li>[API 1.4](https://github.com/AdobeDocs/analytics-1.4-apis)</li></ul> |
| Data Warehouse | Siehe Analytics-Werkzeuge. |  |
| Analytics Data Feed | Die präziseste Möglichkeit, Daten aus Analytics zu erhalten Erstellen Sie einen trefferbasierten Feed, der über Analytics funktioniert. | [Analytics Data Feed](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/get-started/data-feed-overview.html) |

## Data collection and validation {#concept_E07350D4CA5047DAA7D81F762F29606A}

| Methode/Ressource | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Entwicklungsressourcen | Dokumentation, die die verfügbaren Bibliotheken zur Sammlung von Analysedaten über alle verfügbaren Plattformen hinweg enthält (Web, mobile Anwendung, Video, Flash usw.) | [Entwicklerdocs](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| Implementierungshandbuch | Eine Beschreibung der Datenerfassungsvariablen und Einzelheiten zur Implementierung von Datenerfassungscode in JavaScript. | [Implementierungshandbuch](https://docs.adobe.com/content/help/en/analytics/implementation/home.html) |
| AppMeasurement (s_code) | Globale Variablenverwaltung | [AppMeasurement](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html) |
| Anwendungs-SDKs | Benutzerdefiniertes Paket, das eine vorausgefüllte Version der Konfigurationsdatei für Anwendungen enthält. | <ul><li>[iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html)</li><li>[Android](https://docs.adobe.com/content/help/en/mobile-services/android/getting-started-android/requirements.html)</li></ul> |
| DTM und Adobe Launch | Siehe Analytics-Werkzeuge. |  |
| VISTA | Ermöglicht die Anwendung serverseitiger Logik zum Ändern oder Segmentieren von Daten während der Erfassung. | [VISTA-Regeln](https://marketing.adobe.com/resources/help/en_US/reference/VISTA.html) |
| Verarbeitungsregeln | Möglichkeit, Variablen in der Benutzeroberfläche von Analytics festzulegen, zu ändern und zu kopieren, um die erfassten Daten zu ändern. | [Verarbeitungsregeln](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules.html) |
| Debugger-Optionen | Es stehen mehrere Debugger und Paket-Sniffer zur Verfügung, mit denen Sie Ihre Implementierung überprüfen können, einschließlich des Adobe Experience Cloud-Debuggers. | [Adobe Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=en) |
| Dateneinfüge-API | Die Dateneinfüge-API bietet einen Mechanismus zur serverseitigen Datenerfassung und -übermittlung an Experience Cloud-Server. Statt JavaScript-Beacons auf jeder Webseite zu verwenden, um Besucherdaten an Experience Cloud-Server zu übermitteln, werden bei der serverseitigen Datenerfassung ausschließlich Daten auf der Grundlage von Webbrowser-Anforderungen und Webserver-Antworten erfasst. | [Schritte zur Implementierung der Adobe Analytics-Dateneinfüge-API mit POST](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) |
