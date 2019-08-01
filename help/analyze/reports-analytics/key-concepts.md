---
description: Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.
seo-description: Dieser Abschnitt enthält die Schlüsselkonzepte für Adobe Analytics, eine kurze Beschreibung des Konzepts sowie einen spezifischen Link zur Dokumentation mit weiteren Details zum Thema.
seo-title: Adobe Analytics - Schlüsselkonzepte
title: Adobe Analytics - Schlüsselkonzepte
uuid: ef 5701 c 5-2 d 3 e -4847-851 f -9312 d 55 db 1 a 8
translation-type: tm+mt
source-git-commit: d3819975bb65ccf345d60474e268ed9d1b1606a7

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

## Key features {#concept_216E78AD39DD453D940AE857F4C7D4DF}

<table id="table_5CD38BD3BE854E69B6925EA3F02AFC92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Bericht </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
   <th colname="col3" class="entry"> Dokumentationslink </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Vollständige Berichtsliste </td> 
   <td colname="col2"> Definition aller Berichte in Adobe Analytics. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_descriptions.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_descriptions.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Benutzerdefinierter Traffic (Eigenschaft) </td> 
   <td colname="col2">Wird zur Verfolgung des Traffics auf Ihrer Website aufgeschlüsselt nach Seiten verwendet. Eigenschaften bestehen nicht über Seiten hinweg. Schlüsselanwendungen für Traffic-Variablen: 
    <ul id="ul_A935EC5271684B9599F683C7B31400ED"> 
     <li id="li_58E0596050A34ACC821916EA61E946EF">Erhalt eines Wertes, der mit Seitenansichten, Besuchen, Besuchern und Instanzen in Verbindung gebracht werden kann. </li> 
     <li id="li_2B4C557AAD0544BE8204C0D7CE587175">Finden der „beliebtesten“ Variablen eines bestimmten Werts. </li> 
     <li id="li_7FA62BE657F047459DF439BFB9F332F5">Feststellung, wie die Besucher durch die Website navigieren. </li> 
    </ul> <p>Beispiele für Traffic-Variablen: Seitenname, Seitenabschnitte, Browser. </p> </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/traffic_var.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/traffic_var.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Benutzerdefinierte Konversion (eVar) </td> 
   <td colname="col2">Hauptsächlich für die Berichte zu Konversionsereignissen verwendet. Besteht für eine von Ihnen festgelegte Dauer. Zu den Ablaufoptionen gehören Ablauf des Ereignisses, Ablauf des Besuchs oder Ablauf nach x Tagen. Die Option sollte nach der Analyseart gewählt werden, die auf die Variable angewandt wird. <p>Wichtige Unterschiede zwischen Konversionsvariablen und Traffic-Variablen: </p> 
    <ul id="ul_B0A7482A81B94C5F86C06E5507DB393D"> 
     <li id="li_272E414520AA4603AE5EC397B0F93630"> Benutzerdefinierte Traffic-Variablen sind an Traffic-Metriken gebunden, nicht an Konversionen. Sie werden oft für die Pfadanalyse eingesetzt. </li> 
     <li id="li_EBBF9A35C64845FE9683540DFA89E7E9">Benutzerdefinierte Konversionsvariablen können an Traffic und Konversion gebunden werden und werden oft für die Konversionsanalyse eingesetzt. </li> 
    </ul> <p>Beispiele für Konversionsvariablen: interne Suchbegriffe, interne Promotions, externe Kampagnen (s.campaign). </p> </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/conversion_var_admin.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Erfolgsereignisse (s.events) </td> 
   <td colname="col2"> <p>Messung von Kernhandlungen, von denen wir möchten, dass sie Besucher auf unserer Site ausführen. </p> <p>Es gibt drei Ereignisarten: Zähler, numerisch und Währung. Ereignisse sind am nützlichsten, wenn sie Berichten zu Konversionsvariablen (eVar) hinzugefügt werden. Die eVar gibt qualitative Informationen über Ereignisse und das Ereignis stellt die quantitative Information zu den Geschehnissen bereit. </p> <p>Wichtige Unterschiede zwischen Konversionsvariablen und benutzerdefinierten Ereignissen: </p> 
    <ul id="ul_2B95D7437DE444DD9618DBFE6A8612D1"> 
     <li id="li_5951858853334EFA931A5BC57E5C933F">Konversionsvariablen verraten, wer oder was die Konversion beeinflusst hat. </li> 
     <li id="li_339755C842714E0DB8DB4DFAA43AB4F7"> Benutzerdefinierte Ereignisse messen, wie viele Konversionen stattgefunden haben. </li> 
    </ul> <p>Beispiele für Konversionsereignisse: Bestellungen, Anwendungsaufrufe, Leads, Umsatz. </p> </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/success_event.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/success_event.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sitemetriken </td> 
   <td colname="col2"> Zeigen quantitative Informationen über Ihre Website an, z. B. Unique Visitor, Bestellungen, Umsatz usw. Jede Metrik kann in andere elementbasierte Berichte übernommen werden. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_site_metrics.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_site_metrics.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Site-Content </td> 
   <td colname="col2"> Zeigt an, welche Seiten und Bereiche Ihrer Site am aktivsten sind und welche Server am häufigsten genutzt werden. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_site_content.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_site_content.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobil </td> 
   <td colname="col2"> Zeigt Informationen zu mit Mobilgeräten oder Tablets geöffneten Websites an. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_mobile.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_mobile.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobile Anwendung </td> 
   <td colname="col2"> <p>Zeigt grundlegende Nutzungsinformationen in Bezug auf Ihre mobilen Anwendungen an. Diese Berichte sind verfügbar, wenn Ihre SDK implementiert und die Berichtsfunktion aktiviert wurde. </p> <p>Zudem hat Adobe Mobile Services eine eigene Benutzeroberfläche für mobile Anwendungen erstellt, die vollständigere Anwendungsdaten anzeigt und es Ihnen ermöglicht, die Benutzerinteraktionen zu verstehen und zu verbessern. </p> <p>Zugriff auf die Benutzeroberfläche unter: </p> <p><a href="https://mobilemarketing.adobe.com" format="https" scope="external"> https://mobilemarketing.adobe.com</a> </p> </td> 
   <td colname="col3"> <p>Adobe Mobile Services: </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/mobile/" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/mobile/</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pfadberichte </td> 
   <td colname="col2"> Zeigt Informationen zur Reihenfolge an, in der die Seiten Ihrer Website aufgerufen werden. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_paths.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_paths.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Produkte </td> 
   <td colname="col2"> Identifiziert, wie einzelne Produkte bzw. Produktgruppen (Kategorien) zu verschiedenen Konversionsmetriken wie Umsatz oder Checkouts beitragen. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_products.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_products.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchertreue </td> 
   <td colname="col2"> Zeigt Informationen über die Treue Ihrer Kunden an, z. B. wie viele Benutzer auf Ihre Site zurückkehren und wie oft sie das tun. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_visitor_retention.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_visitor_retention.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besucherprofil </td> 
   <td colname="col2"> Mit diesen Berichten können Sie Kaufmuster von Kunden aus verschiedenen Profilkategorien (z. B. Ländern, Bundesländern, Postleitzahlen oder Domänen) ersehen. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_visitor_profile.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_visitor_profile.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Marketingkanäle </td> 
   <td colname="col2">Mithilfe von Berichte erfahren Sie mehr zu den externen Kanälen, über die Besucher auf Ihre Site gelangen, und welche davon bei der Generierung von Konversionen am effektivsten sind. Zuordnungsansichten für die erste und letzte Berührung werden bereitgestellt. <p>Das ist die bevorzugte externe Traffic-Berichtsquelle in Adobe Analytics (anders als Kampagnen oder Traffic-Quellen), da sie den umfassendsten Überblick sowohl über gezahlte als auch organische Kanäle bietet. </p> </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/mchannel/index.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/mchannel/index.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Benutzerdefinierte Berichte, Berichtslink, Lesezeichen und Dashboards </td> 
   <td colname="col2"> Methoden zum Speichern und/oder Freigeben Ihrer Arbeit für andere über die Analytics-Benutzeroberfläche. </td> 
   <td colname="col3">Benutzerspezifische Berichte: <p><a href="https://marketing.adobe.com/resources/help/en_US/reference/reports_custom.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/reports_custom.html</a> </p> <p>Berichtslink: </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/sc/user/t_reports_share_link.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/sc/user/t_reports_share_link.html</a> </p> <p>Lesezeichen </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/sc/user/bookmarks.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/sc/user/bookmarks.html</a> </p> <p>Dashboards </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/sc/user/dashboard.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/sc/user/dashboard.html</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Key metrics {#concept_392819DC275C48688E2CE4ABD4C5EE43}

| Kennzahlname | Definition | Dokumentationslink |
|---|---|---|
| Vollständige Metrikliste | Definition aller Metriken in Adobe Analytics. | [https://marketing.adobe.com/resources/help/de_DE/reference/metrics.html](https://marketing.adobe.com/resources/help/en_US/reference/metrics.html) |
| Unique Visitors | Die Anzahl der nicht duplizierten Website-Besucher über einen festgelegten Zeitraum hinweg. | [https://marketing.adobe.com/resources/help/de_DE/reference/metrics_unique_visitors.html](https://marketing.adobe.com/resources/help/en_US/reference/metrics_unique_visitors.html) |
| Besuche | Eine Folge von Seitenansichten während einer Sitzung. Der Besuch beginnt, wenn eine Person eine Seite der Website erstmalig ansieht, und endet nach einer Inaktivitätsperiode von 30 Minuten. | [https://marketing.adobe.com/resources/help/de_DE/reference/metrics_visit.html](https://marketing.adobe.com/resources/help/en_US/reference/metrics_visit.html) |
| Seitenansichten | Eine Seitenansicht tritt auf, wenn ein Besucher eine Seite auf Ihrer Website aufruft. | [https://marketing.adobe.com/resources/help/de_DE/reference/metrics_page_view.html](https://marketing.adobe.com/resources/help/en_US/reference/metrics_page_view.html) |
| Instanzen | Die Häufigkeit, mit der eine Variable definiert wurde. Jedes Mal, wenn Adobe Analytics einen Wert in einer Variablen feststellt, werden die entsprechenden Instanzen im Bericht um eine Stufe erhöht. | [https://marketing.adobe.com/resources/help/de_DE/reference/metrics_instance.html](https://marketing.adobe.com/resources/help/en_US/reference/metrics_instance.html) |
| Berechnete Metriken | Benutzerdefinierte Metriken, die Sie aus bestehenden Metriken erstellen können. Stehen Ihnen beispielsweise Umsatz und Anzahl der Besuche zur Verfügung, können Sie eine benutzerdefinierte Metrik zur Berechnung des durchschnittlichen Umsatzes pro Besuch oder des Umsatzes geteilt durch die Besuche (Umsatz/Besuche) erstellen. | [https://marketing.adobe.com/resources/help/de_DE/analytics/calcmetrics/](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/) |

## Importoptionen {#concept_7C6DF03B5F9149E2A77F36C739432059}

| Option | Beschreibung | Dokumentationslink |
|---|---|---|
| Classification Importer | Metadaten gegen erfasste Abmessungen über Browser- oder FTP-Upload importieren. Manuelles Verfahren im Vergleich zu Rule Builder. | [https://marketing.adobe.com/resources/help/de_DE/reference/c_working_with_saint.html](https://marketing.adobe.com/resources/help/en_US/reference/c_working_with_saint.html) |
| Regel-Builder | Automatisch Metadaten-Classifications von Abmessungen beruhend auf benutzerdefinierten Regeln erstellen. | [https://marketing.adobe.com/resources/help/de_DE/reference/classification_rule_builder.html](https://marketing.adobe.com/resources/help/en_US/reference/classification_rule_builder.html) |
| Data Sources | Offline-Metriken gegen Dimensionen oder einfach nach Tagen in Analytics importieren. | [https://marketing.adobe.com/resources/help/en_US/sc/datasources/datasrc_home.html](https://marketing.adobe.com/resources/help/en_US/sc/datasources/datasrc_home.html) |
| Data Connectors | Siehe [Produkte](../../analyze/reports-analytics/key-concepts.md#concept_833EDD4EB056491DA1BC5A3A45FE285B). |  |

## Export options {#concept_C62B688E259141CF92C048E8110464BE}


<table id="table_99867D82082D4756872FC3ABD83A33A1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Optionen </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
   <th colname="col3" class="entry"> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Download von Benutzeroberflächenberichten </td> 
   <td colname="col2"> Die einfachste Möglichkeit, Daten aus Analytics zu exportieren. </td> 
   <td colname="col3">https://microsite.omniture.com/t2/help/en_US/survey/index.html#Downloading_a_Report_Using_ <p>Basic_Options </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Data Warehouse </td> 
   <td colname="col2">Siehe <a href="../../analyze/reports-analytics/key-concepts.md#concept_833EDD4EB056491DA1BC5A3A45FE285B" format="dita" scope="local">Produkte</a>. </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ReportBuilder </td> 
   <td colname="col2">Siehe <a href="../../analyze/reports-analytics/key-concepts.md#concept_833EDD4EB056491DA1BC5A3A45FE285B" format="dita" scope="local">Produkte</a>. </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Analytics-API </td> 
   <td colname="col2"> Erstellen Sie Ihre eigenen Anfragen für Analysedaten. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/developer/documentation" format="https" scope="external"> https://marketing.adobe.com/developer/de/documentation</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Clickstream Data Feeds </td> 
   <td colname="col2"> Die präziseste Möglichkeit, Daten aus Analytics zu erhalten. Erstellen Sie einen trefferbasierten Feed, der über Analytics funktioniert. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/sc/clickstream/datafeeds_reference.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/sc/clickstream/datafeeds_reference.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Planungsdaten </td> 
   <td colname="col2"> Die meisten Exportoptionen von Adobe Analytics verfügen über Funktionen, die das Planen von Daten- und Berichtslieferungen an E-Mail-Adressen oder FTP-Sites ermöglichen. </td> 
   <td colname="col3"> - </td> 
  </tr> 
 </tbody> 
</table>

## Data collection and validation {#concept_E07350D4CA5047DAA7D81F762F29606A}

<table id="table_53039DCCAC1D47F7A1E3485609D13E4D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Methode/Ressource </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
   <th colname="col3" class="entry"> Dokumentationslink </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Entwicklungsressourcen </td> 
   <td colname="col2"> Dokumentation, die die verfügbaren Bibliotheken zur Sammlung von Analysedaten über alle verfügbaren Plattformen hinweg enthält (Web, mobile Anwendung, Video, Flash usw.) </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/developer.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/developer.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Implementierungshandbuch </td> 
   <td colname="col2"> Eine Beschreibung der Datenerfassungsvariablen und Einzelheiten zur Implementierung von Datenerfassungscode in JavaScript. </td> 
   <td colname="col3"> <p><a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/sc/implement/index.html</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> AppMeasurement (s_code) </td> 
   <td colname="col2"> Globale Variablenverwaltung </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/appmeasure_mjs.html#" format="html" scope="external"> https://marketing.adobe.com/resources/help/de_DE/sc/implement/appmeasure_mjs.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Anwendungs-SDKs </td> 
   <td colname="col2"> Benutzerdefiniertes Paket, das eine vorausgefüllte Version der Konfigurationsdatei für Anwendungen enthält. </td> 
   <td colname="col3">iOS: <p><a href="https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=requirements" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/mobile/ios/?f=requirements</a> </p> <p>Android: </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/mobile/android/requirements.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/mobile/android/requirements.html</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dynamic Tag Management (DTM) </td> 
   <td colname="col2">Siehe <a href="../../analyze/reports-analytics/key-concepts.md#concept_833EDD4EB056491DA1BC5A3A45FE285B" format="dita" scope="local">Produkte</a>. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VISTA </td> 
   <td colname="col2"> Ein serverseitiger Ansatz zum Ausfüllen von Berichtsvariablen. VISTA verwendet Besuchersegmentierungsregeln, um eine Echtzeitsegmentierung aller Onlinedaten zu erstellen. Mithilfe dieser Regeln können Sie Daten auf nahezu jede beliebige Weise ändern oder segmentieren, ohne eine komplexe Logik auf Ihrer Site implementieren zu müssen. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/VISTA.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/VISTA.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verarbeitungsregeln </td> 
   <td colname="col2"> Eine Methode zur Vereinfachung der Datensammlung und Inhaltsverwaltung, bei der die Daten für die Berichterstellung durch die Admin Tools gesendet werden. Verarbeitungsregeln vereinfachen die Interaktion mit IT-Gruppen und Web-Entwicklern, da sie eine Schnittstelle für die Erstellung, Modifizierung und das Kopieren von Variablen bereitstellen. </td> 
   <td colname="col3"><a href="https://marketing.adobe.com/resources/help/en_US/reference/processing_rules.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/reference/processing_rules.html</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Debugger-Optionen </td> 
   <td colname="col2"> Es stehen mehrere Debugger und Sniffer zur Verfügung, die bei der Validierung Ihrer Implementierung helfen. Unser bevorzugter Debugger ist Charles. Andere verfügbare Optionen sind Adobe Debugger, HTTPFox, Firebug, Omnibug, Fiddler und HTTPWatch. </td> 
   <td colname="col3">Adobe Debugger: <p><a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/de_DE/sc/implement/debugger.html</a> </p> <p>Charles: </p> <p><a href="https://www.charlesproxy.com/" format="http" scope="external"> https://www.charlesproxy.com/</a> </p> </td> 
  </tr> 
 </tbody> 
</table>
