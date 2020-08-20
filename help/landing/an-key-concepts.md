---
description: Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.
title: Adobe Analytics – Schlüsselkonzepte
translation-type: tm+mt
source-git-commit: 4b6107fe57787e639fb06ef957d6230d1bc45bd1
workflow-type: tm+mt
source-wordcount: '2385'
ht-degree: 100%

---


# Adobe Analytics – Schlüsselkonzepte

Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.

## Analytics-Tools {#concept_833EDD4EB056491DA1BC5A3A45FE285B}

| Produkt | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Analysis Workspace | Browserlösung zum Erstellen robuster, benutzerspezifischer Analyseprojekte und demokratisierender Erkenntnisse Bietet mehr Berichtsflexibilität als Reports &amp; Analytics. | [adobe.ly/aaworkspacedocs](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/home.html) |
| Reports &amp; Analytics (ehemals SiteCatalyst) | Browserlösung zur Berichterstellung und Analyse Starter-Tool im Analytics-Paket. | [Reports &amp; Analytics-Homepage](https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/getting-started.html) |
| Report Builder | Excel-Add-in, mit dem Sie benutzerspezifische Anfragen für Adobe Analytics-Daten erstellen und mit Microsoft Excel visualisieren können. | [Report Builder-Homepage](https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/home.html) |
| Ad Hoc Analysis (früher Discover) | Java-basiertes Tool für erweiterte digitale Analysen. | [Ad Hoc Analysis-Homepage](https://docs.adobe.com/content/help/de-DE/analytics/analyze/ad-hoc-analysis/adhoc-home.html) |
| Data Workbench (ehemals Insight) | Wurde konstruiert, um Sie bei der Sammlung, Verarbeitung, Analyse und Visualisierung von Online- und Offline-Kundeninteraktionen über mehrere Kanäle hinweg zu unterstützen. | [Data Workbench-Client](https://docs.adobe.com/content/help/de-DE/data-workbench/using/client/t-open-ins.html) |
| Data Warehouse | Unverarbeitete Rohdaten zur Speicherung und für benutzerdefinierte Berichte, die Sie durch Datenfilterung erstellen können. Nicht auf Treffer-Niveau. | [Data Warehouse-Homepage](https://docs.adobe.com/content/help/de-DE/analytics/export/data-warehouse/data-warehouse.html) |
| Adobe Mobile Services | Führt mobile Marketingfunktionen für mobile Anwendungen aus der ganzen Adobe Experience Cloud zusammen, sodass Sie Einblicke in die Benutzerinteraktionen Ihrer Anwendungen erhalten und gegebenenfalls Verbesserungen vornehmen können. | [Mobile Services-Homepage](https://docs.adobe.com/content/help/de-DE/mobile-services/using/home.html) |
| Adobe Exchange Data Connectors (früher Genesis) | Ermöglicht den Import von Nachverfolgungsdaten aus Drittanbieteranwendungen in Analytics, um eine vollständige Übersicht der Leistung an einem zentralen Ort bereitzustellen. | [Data Connectors-Homepage](https://marketing.adobe.com/developer/documentation/genesis/c-overview-how-it-works) |
| Dynamic Tag Management (DTM) | Hilft bei der Verwaltung von Analytics-, Target- und anderen Tags für alle Ihre Sites, unabhängig von der Anzahl Ihrer Domänen. | [DTM-Homepage](https://docs.adobe.com/content/help/de-DE/analytics/implementation/other/dtm/dtm-implementation-overview.html) |
| Adobe Launch | Die nächste Generation von Adobe-Verwaltungsfunktionen für Website-Tags und mobile SDKs. | [Adobe Launch-Homepage](https://docs.adobe.com/content/help/de-DE/launch/using/overview.html) |

## Wichtige Terminologie {#concept_E473ACBB8E4A42B4AC005538AC12F154}

Klicken Sie [hier](https://docs.adobe.com/content/help/de-DE/analytics/technotes/terms.html), um ein ausführliches Glossar der Adobe Analytics-Terminologie zu erhalten.

| Begriff | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Eigenschaften (benutzerspezifischer Traffic) | Dimensionen zur Verfolgung des Traffics auf Ihrer Website aufgeschlüsselt nach Seiten. Eigenschaften bestehen nicht über Seiten hinweg. Schlüsselanwendungen für Traffic-Variablen: <ul><li>Einfache Zählung zur Suche nach dem „beliebtesten“ Wert</li><li>Einsicht darein, wie die Besucher durch die Website navigieren </li></ul><br>Beispiele für Traffic-Variablen: Seitenname, Seitenabschnitte, Browser.</br> | [Props](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/traffic-variables/traffic-var.html) |
| eVar (benutzerdefinierte Konversion) | Dimensionen, die für einen Zeitraum bestehen, der von Ihnen angepasst wird. Zu den Ablaufoptionen gehören Ablauf des Ereignisses, Ablauf des Besuchs oder Ablauf nach x Tagen. Die Option sollte nach der Analyseart gewählt werden, die auf die Variable angewandt wird.<br>Wichtige Unterschiede zwischen eVars und Eigenschaften:</br><ul><li>Eigenschaften werden häufig für die Pfadanalyse verwendet, da Persistenz entfernt wird.</li><li>eVars werden häufig für die Konversionsanalyse verwendet.</li></ul><br>Beispiele für Konversionsvariablen: interne Suchbegriffe, interne Promotions, externe Kampagnen (s.campaign).</br> | [eVars](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html) |
| Ereignisse/Metriken (s.events) | Metriken zur Messung von Kernhandlungen, von denen wir möchten, dass sie Besucher auf unserer Site ausführen. Es gibt drei Ereignisarten: Zähler, numerisch und Währung. Ereignisse sind am nützlichsten, wenn sie Berichten zu Konversionsvariablen (eVar) hinzugefügt werden. Die eVar vermittelt qualitative Informationen über Geschehnisse, und das Ereignis stellt quantitative Informationen zu den Geschehnissen bereit. <br>Wichtige Unterschiede zwischen eVars und Ereignissen:</br><ul><li>eVars verraten, wer oder was die Konversion beeinflusst hat</li><li>Ereignisse messen, wie viele Konversionen stattgefunden haben</li></ul><br>Beispiele für Konversionsereignisse: Bestellungen, Anwendungsaufrufe, Leads, Umsatz.</br> | [Ereignisse](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/success-events/success-event.html) |
| Komponenten | Dimensionen, Metriken, Segmente und Zeitgranularitäten (Datumsbereiche), die Sie per Drag &amp; Drop in ein Projekt ziehen können. | [Komponenten](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html) |
| Dimensionen | Sammlung von eVars, Eigenschaften, Klassifizierungen und von Adobe erfassten Standardwerten. | [Dimensionen](https://docs.adobe.com/content/help/de-DE/analytics/components/dimensions/overview.html) |
| Metriken | Sammlung von implementierten Ereignissen und berechneten Metriken. | [Metriken](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/components/apply-create-metrics.html) |
| Berechnete Metriken | Möglichkeit, benutzerspezifische Metriken aus vorhandenen Metriken abzuleiten, die über Ihre Implementierung erfasst wurden. | [Berechnete Metriken](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/cm-overview.html) |
| Segmente | Möglichkeit, leistungsstarke, zielgerichtete Zielgruppensegmente in Ihre Analyseberichte einzuschließen, sie zu verwalten, freizugeben und anzuwenden. Segmente werden über Analytics-Produkte hinweg freigegeben und können auch in der Experience Cloud geteilt werden. | [Segmentierung](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/seg-home.html) |
| Zeit (Datumsbereiche) | Möglichkeit, das Datum nach einem beliebigen Zeitraum zu filtern und benutzerdefinierte Datumsbereiche zu erstellen, die in Ihrer Analyse wiederverwendet werden können. | [Datumsbereiche](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) |
| Visualisierungen | Umfangreiche Visualisierungen, die dazu beitragen können, Daten in Ihren Projekten zum Leben zu erwecken. | [Visualisierungen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) |
| Kuratierung | Möglichkeit, die in einem Projekt oder in einer Virtual Report Suite verfügbaren Komponenten zu beschränken. | [VRS-Kuratierung](https://docs.adobe.com/content/help/de-DE/analytics/components/virtual-report-suites/vrs-components.html)<br>[Projektkuratierung](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/curate.html)</br><br>[Vergleich](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate-projects-vrs.html) |

## Wichtige Berichte

| Bericht | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Vollständige Liste der Dimensionen/Berichte | Vollständige Liste der Dimensionen/Berichte, die in Adobe Analytics verfügbar sind. | [Dimensionen](https://docs.adobe.com/content/help/de-DE/analytics/components/dimensions/overview.html) |
| Advertising Analytics | Analysieren Sie in Adobe Analytics alle Google- und Bing-Paid Search-Daten gleichzeitig. Die durch die Integration erstellten Dimensionen umfassen Anzeigenplattform, Keyword, Übereinstimmungstyp usw. Zu den erstellten Metriken gehören AMO-Impressionen, AMO-Klicks, AMO-Kosten, durchschnittl. Position und durchschnittl. Qualitätsbewertung. | [Advertising Analytics](https://docs.adobe.com/help/de-DE/analytics/integration/advertising-analytics/overview.html) |
| Audience Analytics | Richten Sie eingehende Analytics-Treffer mit der Zielgruppenmitgliedschaft eines Benutzers in AAM ein. Sie können AAM-Zielgruppendaten – wie beispielsweise demografische Daten (z. B. Geschlecht oder Verdienstniveau), psychografische Daten (z. B. Interessen und Hobbys), CRM-Daten oder Ad-Impression-Daten – in einen beliebigen Analytics-Workflow einbetten. Durch diese Integration erstellte Dimensionen sind Zielgruppen-ID und Zielgruppenname. | [Audience Analytics](https://docs.adobe.com/content/help/de-DE/analytics/integration/audience-analytics/mc-audiences-aam.html) |
| Attribution IQ | Hiermit können Sie nachvollziehen, wie aussagekräftig die Interaktion in der gesamten Customer Journey ist, und auf intelligente Weise Wendepunkte identifizieren, mit deren Hilfe Kunden zu gewünschten Handlungen bewegt und somit die Marketinginitiativen effektiv optimiert werden können. Zu den Modellen gehören „Erster“, „Letzter“, „Linear“, „Beteiligung“, „J-förmig“, „Umgekehrt J-förmig“, „U-förmig“, „Gleicher Kontakt“, „Benutzerdefiniert“ und „Zeitverfall“. | [Attribution IQ](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/panels/attribution.html) |
| Anomalieerkennung | Eine statistische Methode, mit der festgestellt wird, wie sich eine bestimmte Metrik in Bezug auf frühere Daten verändert hat. Die Anzeige ist standardmäßig für alle Trendvisualisierungen im Analysis Workspace aktiviert. | [Anomalieerkennung](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) |
| Beitragsanalyse | Untersucht die Gründe für auftretende Anomalien anhand einer automatischen Analyse jeder einzelnen Metrik und Dimension, auf die Sie Zugriff haben. | [Beitragsanalyse](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Kohortenanalyse | Eine Kohorte ist eine Personengruppe mit gemeinsamen Merkmalen innerhalb eines vorgegebenen Zeitraums. Die Kohortenanalyse unterstützt Sie bei der Analyse der Kundenbindung und -abwanderung. | [Kohortenanalyse](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) |
| Berichte zur Customer Journey | Zeigt Informationen über den Pfad an, den Ihre Benutzer auf Ihrer Site oder in Ihrer App nehmen. Eigenschaften, eVars und Ereignisse können in dieser Analyse in Analysis Workspace verwendet werden. | [Analysis Workspace-Fallout](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html)[Analysis Workspace-Fluss](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/flow/flow.html)[Reports &amp; Analytics-Pathing](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/flow/flow.html) |
| Marketing-Kanäle | Mithilfe von Berichte erfahren Sie mehr zu den externen Kanälen, über die Besucher auf Ihre Site gelangen, und welche davon bei der Generierung von Konversionen am effektivsten sind. Zuordnungsansichten für die erste und letzte Berührung werden bereitgestellt. Das ist die bevorzugte externe Traffic-Berichtsquelle in Adobe Analytics (anders als Kampagnen oder Traffic-Quellen), da sie den umfassendsten Überblick sowohl über gezahlte als auch über organische Kanäle bietet. | [Marketing-Kanäle](https://docs.adobe.com/content/help/de-DE/analytics/components/marketing-channels/c-getting-started-mchannel.html) |
| Mobile | Zeigt Informationen zu mit Mobilgeräten oder Tablets geöffneten Websites an. | [Mobil-Bericht](https://docs.adobe.com/content/help/de-DE/analytics/components/variables/dimensions-reports/reports-mobile.html) |
| Mobile App | Zeigt grundlegende Nutzungsinformationen in Bezug auf Ihre mobilen Anwendungen an. Diese Berichte sind verfügbar, wenn Ihre SDK implementiert und die Berichtsfunktion aktiviert wurde.  Zudem hat Adobe Mobile Services eine eigene Benutzeroberfläche für mobile Anwendungen erstellt, die vollständigere Anwendungsdaten anzeigt und es Ihnen ermöglicht, die Benutzerinteraktionen zu verstehen und zu verbessern.  Greifen Sie [hier](https://mobilemarketing.adobe.com) auf die Oberfläche zu. | [Adobe Mobile Services](https://docs.adobe.com/content/help/de-DE/mobile-services/using/home.html) | Produkte | Identifiziert, wie einzelne Produkte bzw. Produktgruppen (Kategorien) zu verschiedenen Konversionsmetriken wie Umsatz oder Checkouts beitragen. | [Produktbericht](https://docs.adobe.com/content/help/de-DE/analytics/components/variables/dimensions-reports/reports-products.html) |
| Segmentvergleich | Erkennt die meisten statistisch signifikanten Unterschiede zwischen Segmenten mithilfe einer automatischen Analyse jeder einzelnen Metrik und Dimension, auf die Sie Zugriff haben. | [Segmentvergleich](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html) |
| Site-Inhaltsbericht | Zeigt an, welche Seiten und Bereiche Ihrer Site am aktivsten sind und welche Server am häufigsten genutzt werden. | [Site-Inhaltsbericht](https://docs.adobe.com/content/help/de-DE/analytics/components/dimensions/page.html) |
| Site-Metrikbericht | Zeigt quantitative Informationen über Ihre Website an, z. B. Unique Visitor, Bestellungen, Umsatz usw. Jede Metrik kann in andere elementbasierte Berichte übernommen werden. | [Site-Metrikbericht](https://docs.adobe.com/content/help/de-DE/analytics/components/metrics/overview.html) |
| Besucherprofil | Mit diesen Berichten können Sie Kaufmuster von Kunden aus verschiedenen Profilkategorien (z. B. Ländern, Bundesländern, Postleitzahlen oder Domänen) ersehen. | [Besucherprofil](https://docs.adobe.com/content/help/de-DE/analytics/components/dimensions/language.html) |
| Besuchertreue | Zeigt Informationen über die Treue Ihrer Kunden an, z. B. wie viele Benutzer auf Ihre Site zurückkehren und wie oft sie das tun. | [Besuchertreue](https://docs.adobe.com/content/help/de-DE/analytics/components/dimensions/customer-loyalty.html) |
| Projektverknüpfung, -freigabe und -planung | Methoden zum Speichern und/oder Freigeben Ihrer Arbeit für andere über die Analytics-Benutzeroberfläche. | [Dateien senden und planen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/send-schedule-files.html) |

## Schlüsselmetriken {#concept_392819DC275C48688E2CE4ABD4C5EE43}

| Kennzahlname | Definition | Dokumentationslink |
|---|---|---|
| Vollständige Metrikliste | Definition aller Metriken in Adobe Analytics. | [Übersicht über Metriken](https://docs.adobe.com/content/help/de-DE/analytics/components/metrics/overview.html) |
| Unique Visitors | Die Anzahl der nicht duplizierten Website-Besucher über einen festgelegten Zeitraum hinweg. | [Unique Visitors](https://docs.adobe.com/content/help/de-DE/analytics/components/metrics/unique-visitors.html) |
| Besuche | Eine Folge von Seitenansichten während einer Sitzung. Der Besuch beginnt, wenn eine Person eine Seite der Website erstmalig ansieht, und endet nach einer Inaktivitätsperiode von 30 Minuten. | [Besuche](https://docs.adobe.com/content/help/de-DE/analytics/components/metrics/visits.html) |
| Seitenansichten | Eine Seitenansicht tritt auf, wenn ein Besucher eine Seite auf Ihrer Website aufruft. | [Seitenansichten](https://docs.adobe.com/content/help/de-DE/analytics/components/metrics/page-views.html) |
| Instanzen | Die Häufigkeit, mit der eine Variable definiert wurde. Jedes Mal, wenn Adobe Analytics einen Wert in einer Variablen feststellt, werden die entsprechenden Instanzen im Bericht um eine Stufe erhöht. | [Instanzen](https://docs.adobe.com/content/help/de-DE/analytics/components/metrics/instances.html) |
| Vorfälle | Die Häufigkeit, mit der eine Variable definiert oder beibehalten wurde. | [Vorfälle](https://docs.adobe.com/content/help/de-DE/analytics/components/metrics/occurrences.html) |

## Importoptionen {#concept_7C6DF03B5F9149E2A77F36C739432059}

| Option | Beschreibung | Dokumentationslink |
|---|---|---|
| Classification Importer | Metadaten gegen erfasste Abmessungen über Browser- oder FTP-Upload importieren. Manuelles Verfahren im Vergleich zu Rule Builder. | [Classification Importer](https://docs.adobe.com/content/help/de-DE/analytics/components/classifications/classifications-importer/c-working-with-saint.html) |
| Regel-Builder | Automatisch Metadaten-Classifications von Abmessungen beruhend auf benutzerdefinierten Regeln erstellen. | [Classification Rule Builder](https://docs.adobe.com/content/help/de-DE/analytics/components/classifications/classifications-rulebuilder/classification-rule-builder.html) |
| Kundenattribute | CRM-Daten, die zur Verwendung in Adobe Analytics und Adobe Target in die Experience Cloud hochgeladen wurden. | [Kundenattribute](https://docs.adobe.com/content/help/de-DE/core-services/interface/customer-attributes/attributes.html) |
| Data Sources | Offline-Metriken gegen Dimensionen oder einfach nach Tagen in Analytics importieren. | [Data Sources](https://docs.adobe.com/content/help/de-DE/analytics/import/data-sources/datasrc-home.html) |
| Adobe Exchange Data Connectors | Siehe [Analytics-Werkzeuge](/help/landing/an-key-concepts.md). |  |
| Native Integrationen | Audience Analytics &amp; Advertising Analytics. | Siehe Abschnitt „Wichtige Berichte“. |

## Exportoptionen {#concept_C62B688E259141CF92C048E8110464BE}

| Option | Beschreibung | Dokumentationslink |
|---|---|---|
| Downloads und Planung der Benutzeroberfläche | Daten aus Analysis Workspace als CSV oder PDF exportieren. | [PDF- oder CSV-Dateien herunterladen](/help/analyze/analysis-workspace/curate-share/download-send.md) |
| Report Builder | Siehe Analytics-Werkzeuge. |
| Analytics-API | Erstellen Sie Ihre eigenen Anfragen für Analysedaten. | <ul><li>[API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)</li><li>[API 1.4](https://github.com/AdobeDocs/analytics-1.4-apis)</li></ul> |
| Data Warehouse | Siehe Analytics-Werkzeuge. |  |
| Analytics-Daten-Feed | Die präziseste Möglichkeit, Daten aus Analytics zu erhalten Erstellen Sie einen trefferbasierten Feed, der über Analytics funktioniert. | [Analytics Data Feed](https://docs.adobe.com/content/help/de-DE/analytics/export/analytics-data-feed/data-feed-overview.html) |

## Datensammlung und -validierung {#concept_E07350D4CA5047DAA7D81F762F29606A}

| Methode/Ressource | Beschreibung | Dokumentationslink |
|--- |--- |--- |
| Entwicklungsressourcen | Dokumentation, die die verfügbaren Bibliotheken zur Sammlung von Analysedaten über alle verfügbaren Plattformen hinweg enthält (Web, mobile Anwendung, Video, Flash usw.) | [Dokumente für Entwickler](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| Implementierungshandbuch | Eine Beschreibung der Datenerfassungsvariablen und Einzelheiten zur Implementierung von Datenerfassungscode in JavaScript. | [Implementierungshandbuch](https://docs.adobe.com/content/help/de-DE/analytics/implementation/home.html) |
| AppMeasurement (s_code) | Globale Variablenverwaltung. | [AppMeasurement](https://docs.adobe.com/content/help/de-DE/analytics/implementation/js/migrate-from-hcode.html) |
| Anwendungs-SDKs | Benutzerdefiniertes Paket, das eine vorausgefüllte Version der Konfigurationsdatei für Anwendungen enthält. | <ul><li>[iOS](https://docs.adobe.com/content/help/de-DE/mobile-services/ios/overview.html)</li><li>[Android](https://docs.adobe.com/content/help/de-DE/mobile-services/android/getting-started-android/requirements.html)</li></ul> |
| DTM und Adobe Launch | Siehe Analytics-Werkzeuge. |  |
| VISTA | Ermöglicht die Anwendung serverseitiger Logik zum Ändern oder Segmentieren von Daten während der Erfassung. | [VISTA-Regeln](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/processing-rule-order.html) |
| Verarbeitungsregeln | Möglichkeit, Variablen in der Benutzeroberfläche von Analytics festzulegen, zu ändern und zu kopieren, um die erfassten Daten anzupassen. | [Verarbeitungsregeln](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/processing-rules/processing-rules.html) |
| Debugger-Optionen | Es stehen mehrere Debugger und Paket-Sniffer zur Verfügung, mit denen Sie Ihre Implementierung überprüfen können, einschließlich des Adobe Experience Cloud-Debuggers. | [Adobe Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=de) |
| Dateneinfüge-API | Die Dateneinfüge-API bietet einen Mechanismus zur serverseitigen Datenerfassung und -übermittlung an Experience Cloud-Server. Statt JavaScript-Beacons auf jeder Webseite zu verwenden, um Besucherdaten an Experience Cloud-Server zu übermitteln, werden bei der serverseitigen Datenerfassung ausschließlich Daten auf der Grundlage von Webbrowser-Anforderungen und Webserver-Antworten erfasst. | [Schritte zur Implementierung der Adobe Analytics-Dateneinfüge-API mit POST](https://helpx.adobe.com/de/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) |
