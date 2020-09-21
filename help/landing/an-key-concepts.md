---
description: Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.
title: Adobe Analytics – Schlüsselkonzepte
translation-type: tm+mt
source-git-commit: ed7b4de020c2258a4ba95370293ed1cf1dd9a1ed
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 98%

---


# Adobe Analytics – Schlüsselkonzepte

Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.

## Analytics-Tools {#concept_833EDD4EB056491DA1BC5A3A45FE285B}

| Produkt | Beschreibung | Dokumentationslink |
| --- | --- | --- |
| Analysis Workspace | Browserlösung zum Erstellen robuster, benutzerspezifischer Analyseprojekte und demokratisierender Erkenntnisse Angebote bieten mehr Berichtsflexibilität als Reports and Analytics | [Analysis Workspace Home](/help/analyze/analysis-workspace/home.md) |
| Reports and Analytics (früher SiteCatalyst) | Browserlösung zur Berichterstellung und Analyse Starter-Tool im Analytics-Paket. | [Reports and Analytics Home](/help/analyze/reports-analytics/getting-started.md) |
| Report Builder | Excel-Add-in, mit dem Sie benutzerspezifische Anfragen für Adobe Analytics-Daten erstellen und mit Microsoft Excel visualisieren können. | [Report Builder-Homepage](/help/analyze/report-builder/home.md) |
| Ad Hoc Analysis (früher Discover) | Java-basiertes Tool für erweiterte digitale Analysen. | [Ad Hoc Analysis-Homepage](/help/analyze/ad-hoc-analysis/adhoc-home.md) |
| Data Workbench (ehemals Insight) | Wurde konstruiert, um Sie bei der Sammlung, Verarbeitung, Analyse und Visualisierung von Online- und Offline-Kundeninteraktionen über mehrere Kanäle hinweg zu unterstützen. | [Data Workbench-Client](https://docs.adobe.com/content/help/de-DE/data-workbench/using/client/t-open-ins.html) |
| Data Warehouse | Unverarbeitete Rohdaten zur Speicherung und für benutzerdefinierte Berichte, die Sie durch Datenfilterung erstellen können. Nicht auf Treffer-Niveau. | [Data Warehouse-Homepage](/help/export/data-warehouse/data-warehouse.md) |
| Adobe Mobile Services | Führt mobile Marketingfunktionen für mobile Anwendungen aus der ganzen Adobe Experience Cloud zusammen, sodass Sie Einblicke in die Benutzerinteraktionen Ihrer Anwendungen erhalten und gegebenenfalls Verbesserungen vornehmen können. | [Mobile Services-Homepage](https://docs.adobe.com/content/help/de-DE/mobile-services/using/home.html) |
| Adobe Exchange Data Connectors (früher Genesis) | Ermöglicht den Import von Nachverfolgungsdaten aus Drittanbieteranwendungen in Analytics, um eine vollständige Übersicht der Leistung an einem zentralen Ort bereitzustellen. | [Data Connectors-Homepage](/help/import/data-connectors/data-connectors-eol.md) |
| Dynamic Tag Management (DTM) | Hilft bei der Verwaltung von Analytics-, Target- und anderen Tags für alle Ihre Sites, unabhängig von der Anzahl Ihrer Domänen. | [DTM-Homepage](/help/implement/other/dtm/dtm-implementation-overview.md) |
| Adobe Launch | Die nächste Generation von Adobe-Verwaltungsfunktionen für Website-Tags und mobile SDKs. | [Adobe Launch-Homepage](https://docs.adobe.com/content/help/de-DE/launch/using/overview.html) |

## Wichtige Terminologie {#concept_E473ACBB8E4A42B4AC005538AC12F154}

Klicken Sie [hier](/help/technotes/terms.md), um ein ausführliches Glossar der Adobe Analytics-Terminologie zu erhalten.

| Begriff | Beschreibung | Dokumentationslink |
| --- | --- | --- |
| Eigenschaften (benutzerspezifischer Traffic) | Dimensionen zur Verfolgung des Traffics auf Ihrer Website aufgeschlüsselt nach Seiten. Eigenschaften bestehen nicht über Seiten hinweg. Schlüsselanwendungen für Traffic-Variablen: <ul> <li>Einfache Zählung zur Suche nach dem „beliebtesten“ Wert</li> <li>Einsicht darein, wie die Besucher durch die Website navigieren</li> </ul> <br>Beispiele für Traffic-Variablen: Seitenname, Seitenabschnitte, Browser. | [Props](/help/admin/admin/c-traffic-variables/traffic-var.md) |
| eVar (benutzerdefinierte Konversion) | Dimensionen, die für einen Zeitraum bestehen, der von Ihnen angepasst wird. Zu den Ablaufoptionen gehören Ablauf des Ereignisses, Ablauf des Besuchs oder Ablauf nach x Tagen. Die Option sollte nach der Analyseart gewählt werden, die auf die Variable angewandt wird. <br> Wichtige Unterschiede zwischen eVars und Eigenschaften: <ul> <li>Eigenschaften werden häufig für die Pfadanalyse verwendet, da Persistenz entfernt wird.</li> <li>eVars werden häufig für die Konversionsanalyse verwendet.</li> </ul> <br>Beispiele für Konversionsvariablen: interne Suchbegriffe, interne Promotions, externe Kampagnen (s.campaign). | [eVars](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) |
| Ereignisse/Metriken (s.events) | Metriken zur Messung von Kernhandlungen, von denen wir möchten, dass sie Besucher auf unserer Site ausführen. Es gibt drei Ereignisarten: Zähler, numerisch und Währung. Ereignisse sind am nützlichsten, wenn sie Berichten zu Konversionsvariablen (eVar) hinzugefügt werden. Die eVar vermittelt qualitative Informationen über Geschehnisse, und das Ereignis stellt quantitative Informationen zu den Geschehnissen bereit. <br> Wichtige Unterschiede zwischen eVars und Ereignissen: <ul> <li>eVars verraten, wer oder was die Konversion beeinflusst hat</li> <li>Ereignisse messen, wie viele Konversionen stattgefunden haben</li> </ul> <br> Beispiele für Konversionsereignisse: Bestellungen, Anwendungsaufrufe, Leads, Umsatz. | [Ereignisse](/help/admin/admin/c-success-events/success-event.md) |
| Komponenten | Dimensionen, Metriken, Segmente und Zeitgranularitäten (Datumsbereiche), die Sie per Drag &amp; Drop in ein Projekt ziehen können. | [Komponenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) |
| Dimensionen | Sammlung von eVars, Eigenschaften, Klassifizierungen und von Adobe erfassten Standardwerten. | [Dimensionen](/help/components/dimensions/overview.md) |
| Metriken | Sammlung von implementierten Ereignissen und berechneten Metriken. | [Metriken](/help/analyze/analysis-workspace/components/apply-create-metrics.md) |
| Berechnete Metriken | Möglichkeit, benutzerspezifische Metriken aus vorhandenen Metriken abzuleiten, die über Ihre Implementierung erfasst wurden. | [Berechnete Metriken](/help/components/c-calcmetrics/cm-overview.md) |
| Segmente | Möglichkeit, leistungsstarke, zielgerichtete Zielgruppensegmente in Ihre Analyseberichte einzuschließen, sie zu verwalten, freizugeben und anzuwenden. Segmente werden über Analytics-Produkte hinweg freigegeben und können auch in der Experience Cloud geteilt werden. | [Segmentierung](/help/components/segmentation/seg-home.md) |
| Zeit (Datumsbereiche) | Möglichkeit, das Datum nach einem beliebigen Zeitraum zu filtern und benutzerdefinierte Datumsbereiche zu erstellen, die in Ihrer Analyse wiederverwendet werden können. | [Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md) |
| Visualisierungen | Umfangreiche Visualisierungen, die dazu beitragen können, Daten in Ihren Projekten zum Leben zu erwecken. | [Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) |
| Kuratierung | Möglichkeit, die in einem Projekt oder in einer Virtual Report Suite verfügbaren Komponenten zu beschränken. | [VRS-Kuratierung](/help/components/vrs/vrs-components.md) <br> [Projektkuratierung](/help/analyze/analysis-workspace/curate-share/curate.md) |

## Wichtige Berichte

| Bericht | Beschreibung | Dokumentationslink |
| --- | --- | --- |
| Vollständige Liste der Dimensionen/Berichte | Vollständige Liste der Dimensionen/Berichte, die in Adobe Analytics verfügbar sind. | [Dimensionen](/help/components/dimensions/overview.md) |
| Advertising Analytics | Analysieren Sie in Adobe Analytics alle Google- und Bing-Paid Search-Daten gleichzeitig. Die durch die Integration erstellten Dimensionen umfassen Anzeigenplattform, Keyword, Übereinstimmungstyp usw. Zu den erstellten Metriken gehören AMO-Impressionen, AMO-Klicks, AMO-Kosten, durchschnittl. Position und durchschnittl. Qualitätsbewertung. | [Advertising Analytics](/help/integrate/c-advertising-analytics/overview.md) |
| Audience Analytics | Richten Sie eingehende Analytics-Treffer mit der Zielgruppenmitgliedschaft eines Benutzers in AAM ein. Sie können AAM-Zielgruppendaten – wie beispielsweise demografische Daten (z. B. Geschlecht oder Verdienstniveau), psychografische Daten (z. B. Interessen und Hobbys), CRM-Daten oder Ad-Impression-Daten – in einen beliebigen Analytics-Workflow einbetten. Durch diese Integration erstellte Dimensionen sind Zielgruppen-ID und Zielgruppenname. | [Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md) |
| Attribution IQ | Hiermit können Sie nachvollziehen, wie aussagekräftig die Interaktion in der gesamten Customer Journey ist, und auf intelligente Weise Wendepunkte identifizieren, mit deren Hilfe Kunden zu gewünschten Handlungen bewegt und somit die Marketinginitiativen effektiv optimiert werden können. Zu den Modellen gehören „Erster“, „Letzter“, „Linear“, „Beteiligung“, „J-förmig“, „Umgekehrt J-förmig“, „U-förmig“, „Gleicher Kontakt“, „Benutzerdefiniert“ und „Zeitverfall“. | [Attribution IQ](/help/analyze/analysis-workspace/c-panels/attribution.md) |
| Anomalieerkennung | Eine statistische Methode, mit der festgestellt wird, wie sich eine bestimmte Metrik in Bezug auf frühere Daten verändert hat. Die Anzeige ist standardmäßig für alle Trendvisualisierungen im Analysis Workspace aktiviert. | [Anomalieerkennung](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) |
| Beitragsanalyse | Untersucht die Gründe für auftretende Anomalien anhand einer automatischen Analyse jeder einzelnen Metrik und Dimension, auf die Sie Zugriff haben. | [Beitragsanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md) |
| Kohortenanalyse | Eine Kohorte ist eine Personengruppe mit gemeinsamen Merkmalen innerhalb eines vorgegebenen Zeitraums. Die Kohortenanalyse unterstützt Sie bei der Analyse der Kundenbindung und -abwanderung. | [Kohortenanalyse](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) |
| Berichte zur Customer Journey | Zeigt Informationen über den Pfad an, den Ihre Benutzer auf Ihrer Site oder in Ihrer App nehmen. Eigenschaften, eVars und Ereignisse können in dieser Analyse in Analysis Workspace verwendet werden. | [Analysis Workspace-Trichteranalyse](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md) <br> [Analysis Workspace Flow](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) <br> [Reports and Analytics-Pfade](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) |
| Marketing-Kanäle | Mithilfe von Berichte erfahren Sie mehr zu den externen Kanälen, über die Besucher auf Ihre Site gelangen, und welche davon bei der Generierung von Konversionen am effektivsten sind. Zuordnungsansichten für die erste und letzte Berührung werden bereitgestellt. Das ist die bevorzugte externe Traffic-Berichtsquelle in Adobe Analytics (anders als Kampagnen oder Traffic-Quellen), da sie den umfassendsten Überblick sowohl über gezahlte als auch über organische Kanäle bietet. | [Marketing-Kanäle](/help/components/c-marketing-channels/c-getting-started-mchannel.md) |
| Mobile | Zeigt Informationen zu mit Mobilgeräten oder Tablets geöffneten Websites an. | [Mobil-Bericht](/help/components/dimensions/mobile-dimensions.md) |
| Mobile App | Zeigt grundlegende Nutzungsinformationen in Bezug auf Ihre mobilen Anwendungen an. Diese Berichte sind verfügbar, wenn Ihre SDK implementiert und die Berichtsfunktion aktiviert wurde.  Zudem hat Adobe Mobile Services eine eigene Benutzeroberfläche für mobile Anwendungen erstellt, die vollständigere Anwendungsdaten anzeigt und es Ihnen ermöglicht, die Benutzerinteraktionen zu verstehen und zu verbessern.  Greifen Sie [hier](https://mobilemarketing.adobe.com) auf die Oberfläche zu. | [Adobe Mobile Services](https://docs.adobe.com/content/help/de-DE/mobile-services/using/home.html) |
| Produkte | Identifiziert, wie einzelne Produkte bzw. Produktgruppen (Kategorien) zu verschiedenen Konversionsmetriken wie Umsatz oder Checkouts beitragen. | [Produktbericht](/help/components/dimensions/product.md) |
| Segmentvergleich | Erkennt die meisten statistisch signifikanten Unterschiede zwischen Segmenten mithilfe einer automatischen Analyse jeder einzelnen Metrik und Dimension, auf die Sie Zugriff haben. | [Segmentvergleich](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md) |
| Site-Inhaltsbericht | Zeigt an, welche Seiten und Bereiche Ihrer Site am aktivsten sind und welche Server am häufigsten genutzt werden. | [Site-Inhaltsbericht](/help/components/dimensions/page.md) |
| Site-Metrikbericht | Zeigt quantitative Informationen über Ihre Website an, z. B. Unique Visitor, Bestellungen, Umsatz usw. Jede Metrik kann in andere elementbasierte Berichte übernommen werden. | [Site-Metrikbericht](/help/components/metrics/overview.md) |
| Besucherprofil | Mit diesen Berichten können Sie Kaufmuster von Kunden aus verschiedenen Profilkategorien (z. B. Ländern, Bundesländern, Postleitzahlen oder Domänen) ersehen. | [Besucherprofil](/help/components/dimensions/language.md) |
| Besuchertreue | Zeigt Informationen über die Treue Ihrer Kunden an, z. B. wie viele Benutzer auf Ihre Site zurückkehren und wie oft sie das tun. | [Besuchertreue](/help/components/dimensions/customer-loyalty.md) |
| Projektverknüpfung, -freigabe und -planung | Methoden zum Speichern und/oder Freigeben Ihrer Arbeit für andere über die Analytics-Benutzeroberfläche. | [Dateien senden und planen](/help/analyze/analysis-workspace/curate-share/send-schedule-files.md) |

## Schlüsselmetriken {#concept_392819DC275C48688E2CE4ABD4C5EE43}

| Kennzahlname | Definition | Dokumentationslink |
| --- | --- | --- |
| Vollständige Metrikliste | Definition aller Metriken in Adobe Analytics. | [Übersicht über Metriken](/help/components/metrics/overview.md) |
| Unique Visitors | Die Anzahl der nicht duplizierten Website-Besucher über einen festgelegten Zeitraum hinweg. | [Unique Visitors](/help/components/metrics/unique-visitors.md) |
| Besuche | Eine Folge von Seitenansichten während einer Sitzung. Der Besuch beginnt, wenn eine Person eine Seite der Website erstmalig ansieht, und endet nach einer Inaktivitätsperiode von 30 Minuten. | [Besuche](/help/components/metrics/visits.md) |
| Seitenansichten | Eine Seitenansicht tritt auf, wenn ein Besucher eine Seite auf Ihrer Website aufruft. | [Seitenansichten](/help/components/metrics/page-views.md) |
| Instanzen | Die Häufigkeit, mit der eine Variable definiert wurde. Jedes Mal, wenn Adobe Analytics einen Wert in einer Variablen feststellt, werden die entsprechenden Instanzen im Bericht um eine Stufe erhöht. | [Instanzen](/help/components/metrics/instances.md) |
| Vorfälle | Die Häufigkeit, mit der eine Variable definiert oder beibehalten wurde. | [Vorfälle](/help/components/metrics/occurrences.md) |

## Importoptionen {#concept_7C6DF03B5F9149E2A77F36C739432059}

| Option | Beschreibung | Dokumentationslink |
| --- | --- | --- |
| Classification Importer | Metadaten gegen erfasste Abmessungen über Browser- oder FTP-Upload importieren. Manuelles Verfahren im Vergleich zu Rule Builder. | [Classification Importer](/help/components/classifications/importer/c-working-with-saint.md) |
| Regel-Builder | Automatisch Metadaten-Classifications von Abmessungen beruhend auf benutzerdefinierten Regeln erstellen. | [Classification Rule Builder](/help/components/classifications/crb/classification-rule-builder.md) |
| Kundenattribute | CRM-Daten, die zur Verwendung in Adobe Analytics und Adobe Target in die Experience Cloud hochgeladen wurden. | [Kundenattribute](https://docs.adobe.com/content/help/de-DE/core-services/interface/customer-attributes/attributes.html) |
| Data Sources | Offline-Metriken gegen Dimensionen oder einfach nach Tagen in Analytics importieren. | [Data Sources](/help/import/c-data-sources/datasrc-home.md) |
| Adobe Exchange Data Connectors | Siehe [Analytics-Werkzeuge](/help/import/data-connectors/data-connectors-eol.md). |  |
| Native Integrationen | Audience Analytics &amp; Advertising Analytics. | Siehe Abschnitt „Wichtige Berichte“. |

## Exportoptionen {#concept_C62B688E259141CF92C048E8110464BE}

| Option | Beschreibung | Dokumentationslink |
| --- | --- | --- |
| Downloads und Planung der Benutzeroberfläche | Daten aus Analysis Workspace als CSV oder PDF exportieren. | [PDF- oder CSV-Dateien herunterladen](/help/analyze/analysis-workspace/curate-share/download-send.md) |
| Report Builder | Siehe Analytics-Werkzeuge. |  |
| Analytics-API  | Erstellen Sie Ihre eigenen Anfragen für Analysedaten. | <ul><li>[API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)</li><li>[API 1.4](https://github.com/AdobeDocs/analytics-1.4-apis)</li></ul> |
| Data Warehouse | Siehe Analytics-Werkzeuge. |  |
| Analytics-Daten-Feed | Die präziseste Möglichkeit, Daten aus Analytics zu erhalten Erstellen Sie einen trefferbasierten Feed, der über Analytics funktioniert. | [Analytics Data Feed](/help/export/analytics-data-feed/data-feed-overview.md) |

## Datensammlung und -validierung {#concept_E07350D4CA5047DAA7D81F762F29606A}

| Methode/Ressource | Beschreibung | Dokumentationslink |
| --- | --- | --- |
| Entwicklungsressourcen | Dokumentation, die die verfügbaren Bibliotheken zur Sammlung von Analysedaten über alle verfügbaren Plattformen hinweg enthält (Web, mobile Anwendung, Video, Flash usw.) | [Dokumente für Entwickler](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| Implementierungshandbuch | Eine Beschreibung der Datenerfassungsvariablen und Einzelheiten zur Implementierung von Datenerfassungscode in JavaScript. | [Implementierungshandbuch](/help/implement/home.md) |
| AppMeasurement (s_code) | Globale Variablenverwaltung. | [AppMeasurement](/help/implement/js/migrate-from-hcode.md) |
| Anwendungs-SDKs | Benutzerdefiniertes Paket, das eine vorausgefüllte Version der Konfigurationsdatei für Anwendungen enthält. | <ul><li>[iOS](https://docs.adobe.com/content/help/de-DE/mobile-services/ios/overview.html)</li><li>[Android](https://docs.adobe.com/content/help/de-DE/mobile-services/android/getting-started-android/requirements.html)</li></ul> |
| DTM und Adobe Launch | Siehe Analytics-Werkzeuge. |  |
| VISTA | Ermöglicht die Anwendung serverseitiger Logik zum Ändern oder Segmentieren von Daten während der Erfassung. | [VISTA-Regeln](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/processing-rule-order.md) |
| Verarbeitungsregeln | Möglichkeit, Variablen in der Benutzeroberfläche von Analytics festzulegen, zu ändern und zu kopieren, um die erfassten Daten anzupassen. | [Verarbeitungsregeln](/help/admin/admin/c-processing-rules/processing-rules.md) |
| Debugger-Optionen | Es stehen mehrere Debugger und Paket-Sniffer zur Verfügung, mit denen Sie Ihre Implementierung überprüfen können, einschließlich des Adobe Experience Cloud-Debuggers. | [Adobe Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=de) |
| Dateneinfüge-API | Die Dateneinfüge-API bietet einen Mechanismus zur serverseitigen Datenerfassung und -übermittlung an Experience Cloud-Server. Statt JavaScript-Beacons auf jeder Webseite zu verwenden, um Besucherdaten an Experience Cloud-Server zu übermitteln, werden bei der serverseitigen Datenerfassung ausschließlich Daten auf der Grundlage von Webbrowser-Anforderungen und Webserver-Antworten erfasst. | [Schritte zur Implementierung der Adobe Analytics-Dateneinfüge-API mit POST](https://helpx.adobe.com/de/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) |
