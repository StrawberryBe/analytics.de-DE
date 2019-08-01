---
description: Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.
seo-description: Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.
seo-title: Adobe Analytics - Schlüsselkonzepte
title: Adobe Analytics - Schlüsselkonzepte
uuid: ef 5701 c 5-2 d 3 e -4847-851 f -9312 d 55 db 1 a 8
translation-type: tm+mt
source-git-commit: d7553fb973d4daddc46533f76769b383966c5c7d

---


# Adobe Analytics - Schlüsselkonzepte

Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.

## Analytics tools {#concept_833EDD4EB056491DA1BC5A3A45FE285B}

| Produkt | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Analysis Workspace | Browserlösung zum Erstellen robuster, benutzerdefinierter Analyseprojekte und demokratisierender Einblicke. Bietet mehr Berichtsflexibilität als Reports &amp; Analysen | [adobe.ly/aaworkspacedocs](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/analysis-workspace-features.html) |
| Reports &amp; Analysen (ehemals SiteCatalyst) | Browserlösung für Berichte und Analysen. Starter-Tool im Analytics-Paket. | [Startseite für Reports &amp; Analysen](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/getting-started.html) |
| Report Builder | Excel-Add-in, mit dem Sie benutzerdefinierte Anforderungen aus Adobe Analytics-Daten erstellen und mit Microsoft Excel visualisieren können. | [Reportbuilder-Startseite](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/home.html) |
| Ad-hoc-Analysen (früher Discover) | Java-basiertes Tool für erweiterte digitale Analysen. Für das Ende des Lebenszyklus in Q 3 2019 behoben. | [Home Ad-hoc-Analysen](https://docs.adobe.com/content/help/en/analytics/analyze/ad-hoc-analysis/adhoc-home.html) |
| Data Workbench (ehemals Insight) | Wurde konstruiert, um Sie bei der Sammlung, Verarbeitung, Analyse und Visualisierung von Online- und Offline-Kundeninteraktionen über mehrere Kanäle hinweg zu unterstützen. | [Data Workbench-Client](https://marketing.adobe.com/resources/help/en_US/insight/client/) |
| Data Warehouse | Unverarbeitete Rohdaten zur Speicherung und für benutzerdefinierte Berichte, die Sie durch Datenfilterung erstellen können. Nicht auf Treffer-Niveau. | [Data Warehouse-Startseite](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) |
| Adobe Mobile Services | Führt mobile Marketingfunktionen für mobile Anwendungen aus der ganzen Adobe Experience Cloud zusammen, sodass Sie Einblicke in die Benutzerinteraktionen Ihrer Anwendungen erhalten und gegebenenfalls Verbesserungen vornehmen können. | [Mobile Services-Startseite](https://docs.adobe.com/content/help/en/mobile-services/using/home.html) |
| Adobe Exchange Data Connectors (ehemals Genesis) | Importieren Sie Tracking-Daten aus Drittanbieteranwendungen in Analytics, um die Leistung an einer zentralen Stelle an die Leistung zu bringen. | [Data Connectors-Startseite](https://marketing.adobe.com/developer/documentation/genesis/c-overview-how-it-works) |
| Dynamisches Tag-Management (DTM) | Hilft bei der Verwaltung von Analytics-, Target- und anderen Tags für alle Ihre Sites, unabhängig von der Anzahl Ihrer Domänen. | [DTM-Startseite](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/dtm-implementation-overview.html) |
| Adobe Launch | Die nächste Generation der Website-Tag- und mobilen SDK-Verwaltungsfunktionen von Adobe. | [Startseite von Adobe](https://docs.adobe.com/content/help/en/launch/using/overview.html) |

## Key terminology {#concept_E473ACBB8E4A42B4AC005538AC12F154}

Klicken Sie [hier](https://docs.adobe.com/content/help/en/analytics/technotes/terms.html), um ein ausführliches Glossar der Adobe Analytics-Terminologie zu erhalten.

| Begriff | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Props (benutzerspezifischer Traffic) | Dimensionen, die zum Verfolgen der Traffic-Aktivität vonseiten pro Seite verwendet werden. Eigenschaften bestehen nicht über Seiten hinweg. Schlüsselanwendungen für Traffic-Variablen: <ul><li>Einfache Zählung zur Suche nach'beliebter'eines bestimmten Werts</li><li>Sichtbarkeit, wie Benutzer durch Ihre Site pfaden </li></ul><br>Beispiele für Traffic-Variablen: Seitenname, Seitenabschnitte, Browser</br> | [Props](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/traffic-variables/traffic-var.html) |
| Evar (benutzerdefinierte Konversion) | Dimensionen, die über einen bestimmten Zeitraum persistent sind. Zu den Ablaufoptionen gehören Ablauf des Ereignisses, Ablauf des Besuchs oder Ablauf nach x Tagen. Die Option sollte nach der Analyseart gewählt werden, die auf die Variable angewandt wird.<br>Wichtige Unterschiede zwischen evars und Props:</br><ul><li>Props werden oft für Pfadanalysen verwendet, da die Persistenz entfernt wird.</li><li>Evars werden häufig für die Konversionsanalyse verwendet.</li></ul><br>Beispiele für Konversionsvariablen: interne Suchbegriffe, interne Promotions, externe Kampagnen (s.campaign)</br> | [eVars](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html) |
| Ereignisse/Metriken (s. events) | Metriken, die wichtige Aktionen messen, die unsere Besucher auf unserer Site ausführen möchten. Es gibt drei Ereignisarten: Zähler, numerisch und Währung. Ereignisse sind am nützlichsten, wenn sie Berichten zu Konversionsvariablen (eVar) hinzugefügt werden. Die eVar gibt qualitative Informationen über Ereignisse und das Ereignis stellt die quantitative Information zu den Geschehnissen bereit. <br>Wesentliche Unterschiede zwischen evars und Ereignissen:</br><ul><li>Evars teilen uns mit, wer, was oder welche die Umrechnung beeinflusst hat.</li><li>Ereignisse messen, wie viele Konversionen stattgefunden haben</li></ul><br>Beispiele für Konversionsereignisse: Bestellungen, Anwendungsaufrufe, Leads, Umsatz.</br> | [Ereignisse](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/success-events/success-event.html) |
| Komponenten | Dimensionen, Metriken, Segmente und Zeitgranularitäten (Datumsbereiche), die per Drag &amp; Drop in einem Projekt abgelegt werden können. | [Komponenten](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html) |
| Dimensionen | Sammlung von evars, Props, Classifications und standardwerten von Adobe. | [Dimensionen](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-descriptions.html) |
| Metriken | Sammlung von implementierten Ereignissen und berechneten Metriken. | [Metriken](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/apply-create-metrics.html) |
| Berechnete Metriken | Möglichkeit, benutzerspezifische Metriken aus vorhandenen Metriken abzuleiten, die über Ihre Implementierung erfasst wurden. | [Berechnete Metriken](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/cm-overview.html) |
| Segmente | Möglichkeit, leistungsstarke, zielgerichtete Zielgruppensegmente in Ihre Analyseberichte einzuschließen, sie zu verwalten, freizugeben und anzuwenden. Segmente werden über Analytics-Produkte hinweg freigegeben und können auch in der Experience Cloud geteilt werden. | [Segmentierung](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-home.html) |
| Zeit (Datumsbereiche) | Möglichkeit, Datum in einen beliebigen Zeitraum zu filtern und benutzerdefinierte Datumsbereiche zu erstellen, die in Ihrer Analyse wiederverwendet werden können. | [Datumsbereiche](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) |
| Visualisierungen | Umfangreiche Visualisierungen, mit denen Daten in Ihren Projekten gesammelt werden können. | [Visualisierungen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) |
| Kuratierung | Möglichkeit, die in einem Projekt oder einer Virtual Report Suite verfügbaren Komponenten einzuschränken. | [VRS curationproject](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-components.html)<br>[curationcomparison](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html)</br><br>[](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate-projects-vrs.html) |

## Key reports {#concept_216E78AD39DD453D940AE857F4C7D4DF}

| Bericht | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Vollständige Liste der Dimensionen/Berichte | Vollständige Liste der Dimensionen/Berichte, die in Adobe Analytics verfügbar sind. | [Dimensionen](https://marketing.adobe.com/resources/help/en_US/reference/reports_descriptions.html) |
| Advertising Analytics | Analysieren Sie alle Google- und Bing gebührenpflichtigen Suchdaten nebeneinander in Adobe Analytics. Zu den über die Integration erstellten Dimensionen gehören Anzeigenplattform, Suchbegriff, Übereinstimmungstyp usw. Metriken sind AMO-Impressionen, AMO-Klicks, AMO-Kosten, Avg. Position und Durchschn. Qualitätsbewertung | [Advertising Analytics](https://docs.adobe.com/help/en/analytics/integration/advertising-analytics/overview.html) |
| Audience Analytics | Fügen Sie eingehende Analytics-Treffer mit der Zielgruppenmitgliedschaft eines Benutzers in AAM ein. Sie können AAM-Zielgruppendaten wie demografische Informationen (z. B. Geschlecht oder Einkommensstufe), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten und Daten zur Anzeigenimpressionsdaten in einem beliebigen Analytics-Arbeitsablauf integrieren. Durch diese Integration erstellte Dimensionen sind Zielgruppen-ID und Zielgruppenname. | [Audience Analytics](https://docs.adobe.com/content/help/en/analytics/integration/audience-analytics/mc-audiences-aam.html) |
| Attribution IQ | Damit können Sie verstehen, wie aussagekräftige Interaktionen auf der Kundenpfade stattfinden, und eine intelligente Identifizierung von Inflationspunkten vornehmen, die Kunden zur Erreichung ihrer Ergebnisse führen und Marketinginitiativen effektiv optimieren. Zu den Modellen gehören first, last, linear, participation, j-shape, inverse j-shape, u-shape, same touch, custom and time disay. | [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution.html) |
| Anomalieerkennung | Eine statistische Methode, die festlegt, wie sich eine bestimmte Metrik im Verhältnis zu vorherigen Daten verändert hat. AD ist standardmäßig für alle Trendvisualisierungen im Analysis Workspace aktiviert. | [Anomalieerkennung](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) |
| Beitragsanalyse | Erkundung des "warum" hinter Anomalien, indem Sie eine automatische Analyse jeder einzelnen Metrik und Dimension ausführen, auf die Sie Zugriff haben. | [Beitragsanalyse](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Kohortenanalyse | Eine Kohorte ist eine Gruppe von Personen, die über einen bestimmten Zeitraum gemeinsame Merkmale freigeben. Kohortenanalyse-Aides helfen bei der Analyse und Analyse von Ihren Benutzern. | [Kohortenanalyse](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) |
| Customer Journey-Berichte | Zeigt Informationen über den Pfad an, den Ihre Benutzer durch Ihre Site oder App nehmen. Prop, evars und Ereignisse können in Analysis Workspace verwendet werden. | [Analysis Workspace falloutanalysis](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html)[Workspace -](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/flow/flow.html)[pfade und Analysen](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-paths.html) |
| Marketingkanäle | Mithilfe von Berichte erfahren Sie mehr zu den externen Kanälen, über die Besucher auf Ihre Site gelangen, und welche davon bei der Generierung von Konversionen am effektivsten sind. Zuordnungsansichten für die erste und letzte Berührung werden bereitgestellt. Das ist die bevorzugte externe Traffic-Berichtsquelle in Adobe Analytics (anders als Kampagnen oder Traffic-Quellen), da sie den umfassendsten Überblick sowohl über gezahlte als auch organische Kanäle bietet. | [Marketing-Kanäle](https://docs.adobe.com/content/help/en/analytics/components/marketing-channels/c-getting-started-mchannel.html) |
| Mobil | Zeigt Informationen zu mit Mobilgeräten oder Tablets geöffneten Websites an. | [Mobilbericht | (https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-mobile.html) |
| Mobile Anwendung | Zeigt grundlegende Nutzungsinformationen in Bezug auf Ihre mobilen Anwendungen an. Diese Berichte sind verfügbar, wenn Ihre SDK implementiert und die Berichtsfunktion aktiviert wurde.  Zudem hat Adobe Mobile Services eine eigene Benutzeroberfläche für mobile Anwendungen erstellt, die vollständigere Anwendungsdaten anzeigt und es Ihnen ermöglicht, die Benutzerinteraktionen zu verstehen und zu verbessern.  Access the interface [here](https://mobilemarketing.adobe.com). | [Adobe Mobile-Dienste](https://docs.adobe.com/content/help/en/mobile-services/using/home.html) | Produkte | Identifiziert, wie einzelne Produkte bzw. Produktgruppen (Kategorien) zu verschiedenen Konversionsmetriken wie Umsatz oder Checkouts beitragen. | [Produktbericht](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-products.html) |
| Segmentvergleich | Erkennt die meisten statistisch signifikanten Unterschiede zwischen den Segmenten durch eine automatische Analyse jeder einzelnen Metrik und Dimension, auf die Sie Zugriff haben. | [Segmentvergleich](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html) |
| Site-Content-Bericht | Zeigt an, welche Seiten und Bereiche Ihrer Site am aktivsten sind und welche Server am häufigsten genutzt werden. | [Site-Content-Bericht](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-site-content.html) |
| Site-Metrikbericht | Zeigen quantitative Informationen über Ihre Website an, z. B. Unique Visitor, Bestellungen, Umsatz usw. Jede Metrik kann in andere elementbasierte Berichte übernommen werden. | [Site-Metrikbericht](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-site-metrics.html) |
| Besucherprofil | Mit diesen Berichten können Sie Kaufmuster von Kunden aus verschiedenen Profilkategorien (z. B. Ländern, Bundesländern, Postleitzahlen oder Domänen) ersehen. | [Besucherprofil](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-visitor-profile.html) |
| Besuchertreue | Zeigt Informationen über die Treue Ihrer Kunden an, z. B. wie viele Benutzer auf Ihre Site zurückkehren und wie oft sie das tun. | [Besuchertreue](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-visitor-retention.html) |
| Projektverknüpfung, Freigabe und Planung | Methoden zum Speichern und/oder Freigeben Ihrer Arbeit für andere über die Analytics-Benutzeroberfläche. | [Dateien senden und planen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/send-schedule-files.html) |


## Key metrics {#concept_392819DC275C48688E2CE4ABD4C5EE43}

| Kennzahlname | Definition | Dokumentationslink |
|---|---|---|
| Vollständige Metrikliste | Definition aller Metriken in Adobe Analytics. | [Metriken - Übersicht](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-overview.html) |
| Unique Visitors | Die Anzahl der nicht duplizierten Website-Besucher über einen festgelegten Zeitraum hinweg. | [Unique Visitors](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-unique-visitors-v15-dsc.html) |
| Besuche | Eine Folge von Seitenansichten während einer Sitzung. Der Besuch beginnt, wenn eine Person eine Seite der Website erstmalig ansieht, und endet nach einer Inaktivitätsperiode von 30 Minuten. | [Besuche](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-visit.html) |
| Seitenansichten | Eine Seitenansicht tritt auf, wenn ein Besucher eine Seite auf Ihrer Website aufruft. | [Seitenansichten](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-page-view.html) |
| Instanzen | Die Häufigkeit, mit der eine Variable definiert wurde. Jedes Mal, wenn Adobe Analytics einen Wert in einer Variablen feststellt, werden die entsprechenden Instanzen im Bericht um eine Stufe erhöht. | [Instanzen](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-instance.html) |
| Vorfälle | Die Häufigkeit, mit der eine Variable definiert oder beibehalten wurde. | [Vorfälle](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-occurrences.html) |

## Importoptionen {#concept_7C6DF03B5F9149E2A77F36C739432059}

| Option | Beschreibung | Dokumentationslink |
|---|---|---|
| Classification Importer | Metadaten gegen erfasste Abmessungen über Browser- oder FTP-Upload importieren. Manuelles Verfahren im Vergleich zu Rule Builder. | [Classification Importer](https://marketing.adobe.com/resources/help/en_US/reference/c_working_with_saint.html) |
| Regel-Builder | Automatisch Metadaten-Classifications von Abmessungen beruhend auf benutzerdefinierten Regeln erstellen. | [Classification Rule Builder](https://marketing.adobe.com/resources/help/en_US/reference/classification_rule_builder.html) |
| Kundenattribute | In Experience Cloud hochgeladene CRM-Daten zur Verwendung in Adobe Analytics und Adobe Target. | [Kundenattribute](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html) |
| Data Sources | Offline-Metriken in Analytics gegen Dimensionen oder einfach nach Tagen. | [Data Sources](https://docs.adobe.com/content/help/en/analytics/import/data-sources/datasrc-home.html) |
| Adobe Exchange Data Connectors | See [Adobe Analytics Tools](../../analyze/reports-analytics/key-concepts.md#concept_833EDD4EB056491DA1BC5A3A45FE285B). |  |
| Native Integrationen | Audience Analytics &amp; Advertising Analytics. | Siehe Abschnitt "Wichtige Berichte" . |

## Export options {#concept_C62B688E259141CF92C048E8110464BE}

| Optionen | Beschreibung |  |
|--- |--- |--- |
| Downloads und Planung der Benutzeroberfläche | Daten aus Analysis Workspace als CSV- oder PDF-Datei exportieren | [PDF- oder CSV-Dateien herunterladen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/download-send.html) |
| Report Builder | Siehe Analytics-Werkzeuge. | - |
| Analytics-API | Erstellen Sie Ihre eigenen Anfragen für Analysedaten. | <ul><li>[API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)</li><li>[API 1.4](https://github.com/AdobeDocs/analytics-1.4-apis)</li></ul> |
| Data Warehouse | Siehe Analytics-Werkzeuge. | - |
| Analytics Data Feed | Die präziseste Möglichkeit, Daten aus Analytics zu erhalten Erstellen Sie einen trefferbasierten Feed, der über Analytics funktioniert. | [Analytics Data Feed](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/get-started/data-feed-overview.html) |


## Data collection and validation {#concept_E07350D4CA5047DAA7D81F762F29606A}

| Methode/Ressource | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Entwicklungsressourcen | Dokumentation, die die verfügbaren Bibliotheken zur Sammlung von Analysedaten über alle verfügbaren Plattformen hinweg enthält (Web, mobile Anwendung, Video, Flash usw.) | [Entwicklerdokumente](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| Implementierungshandbuch | Eine Beschreibung der Datenerfassungsvariablen und Einzelheiten zur Implementierung von Datenerfassungscode in JavaScript. | [Implementierungshandbuch](https://docs.adobe.com/content/help/en/analytics/implementation/home.html) |
| AppMeasurement (s_code) | Globale Variablenverwaltung | [AppMeasurement](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html) |
| Anwendungs-SDKs | Benutzerdefiniertes Paket, das eine vorausgefüllte Version der Konfigurationsdatei für Anwendungen enthält. | <ul><li>[iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html)</li><li>[Android](https://docs.adobe.com/content/help/en/mobile-services/android/getting-started-android/requirements.html)</li></ul> |
| DTM und Adobe Launch | Siehe Analytics-Tools. |  |
| VISTA | Damit können Sie serverseitige Logik anwenden, um Daten beim Erfassen zu ändern oder zu segmentieren. | [VISTA-Regeln](https://marketing.adobe.com/resources/help/en_US/reference/VISTA.html) |
| Verarbeitungsregeln | Möglichkeit, Variablen in der Analytics-Benutzeroberfläche festzulegen, zu ändern und zu kopieren, um die erfassten Daten zu ändern. | [Verarbeitungsregeln](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules.html) |
| Debugger-Optionen | Es gibt mehrere Debugger und Paket-Sniffer zur Überprüfung Ihrer Implementierung, einschließlich des Adobe Experience Cloud-Debuggers. | [Adobe Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=en) |
| Dateneinfüge-API | Die Dateneinfüge-API bietet einen Mechanismus für die serverseitige Datenerfassung und -übermittlung auf Experience Cloud-Servern. Anstatt javascript-Beacons auf jeder Webseite zu verwenden, um Besucherdaten an Experience Cloud-Server zu übertragen, erfasst die serverseitige Datenerfassung Daten, die ausschließlich auf Webbrowser-Anforderungen und Webserverantworten basieren. | [Schritte zum Implementieren der Adobe Analytics-Dateneinfüge-API mit POST](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) |
