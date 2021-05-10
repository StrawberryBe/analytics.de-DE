---
title: In Adobe Analytics verwendete Begriffe
description: Glossar für Adobe Analytics, das häufig verwendete Begriffe definiert.
exl-id: 07507ba1-a512-48d9-8022-6084de4ae262
translation-type: tm+mt
source-git-commit: f3eb3c024a80d0b65729929960173f8b3a4267b0
workflow-type: tm+mt
source-wordcount: '2433'
ht-degree: 100%

---

# In Adobe Analytics verwendete Begriffe

Verwenden Sie dieses Glossar, um den Kontext vieler Begriffe zu verstehen, die Adobe Analytics verwendet.

* **Activity Map:** ein Browser-Plugin, das anzeigt, auf welche Bereiche auf Ihrer Site am häufigsten geklickt wurde. Siehe [Activity Map](/help/analyze/activity-map/activity-map.md) im Benutzerhandbuch zu Analysen.
* **Admin Console:** kann sich auf Folgendes beziehen:
   * Alte Admin Tools, in denen Report Suite-Einstellungen in Adobe Analytics verwaltet werden. In früheren Versionen von Adobe Analytics wurden hier auch Anwenderberechtigungen verwaltet. Siehe [Admin Tools](/help/admin/admin/c-admin-tools.md) im Administratorhandbuch.
   * Die Adobe Admin Console, in der der Produktzugriff bereitgestellt und Anwenderberechtigungen verwaltet werden. Siehe [Admin Console](/help/admin/admin-console/home.md) im Administratorhandbuch.
* **Zuordnung:** Wenn eine Konversionsvariable während eines Besuchs auf mehr als einen Wert trifft, bestimmt die Zuordnungseinstellung der Variablen, welcher Wert beibehalten wird. Siehe [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) im Administratorhandbuch.
* **Anomalie:** Eine Anomalie wird mithilfe statistischer Modellierung entdeckt, um automatisch nach unerwarteten Trends in Daten zu suchen. Das Modell analysiert Metriken und ermittelt Ober- und Untergrenze sowie eine erwartete Bandbreite von Werten. Siehe [Anomalieerkennung](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) im Benutzerhandbuch zu Analysen.
* **AppMeasurement:** die Code-Bibliothek, mit der Daten erfasst und an Adobe gesendet werden. Siehe [Startseite](/help/implement/home.md) des Benutzerhandbuchs zu Implementierungen.
* **ASI-Slot:** Dieser ist nicht mehr vorhanden. In früheren Versionen von Adobe Analytics boten die ASI-Slots einen temporären Report Suite-Container, um segmentierte Daten anzuzeigen. In der aktuellen Version von Adobe Analytics können Segmente sofort auf jeden Bericht angewendet werden.
* **Aufschlüsselung:** ermöglicht die Anzeige einer Dimension im Kontext einer anderen Dimension. Siehe [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md) im Benutzerhandbuch zu Analysen.
* **Absprung:** ein Besuch, der aus einem einzelnen Treffer besteht. Siehe [Absprünge](/help/components/metrics/bounces.md) im Benutzerhandbuch zu Komponenten. Siehe auch „Einzelzugriff“.
* **Berechnete Metrik:** ermöglicht die Kombination vorhandener Metriken, statistischer Funktionen und Formeln zur Verwendung in Berichten. Siehe [Berechnete Metriken](/help/components/c-calcmetrics/cm-overview.md) im Benutzerhandbuch zu Komponenten.
* **Kampagne:** kann sich auf Folgendes beziehen:
   * Die Kampagnenvariable, die die Dimension „Trackingcode“ ausfüllt. Siehe [Kampagne](../implement/vars/page-vars/campaign.md) im Benutzerhandbuch zu Implementierungen.
   * Eine Standard-Classification der Dimension „Trackingcode“; automatisch für alle Report Suites erstellt.
   * Adobe Campaign, Teil der Adobe Experience Cloud. Weitere Informationen finden Sie auf [Adobe.com](https://www.adobe.com/de/marketing/campaign.html).
* **Kanal:** kann sich auf Folgendes beziehen:
   * Die Kanalvariable, die die Dimension „Sitebereiche“ füllt. Siehe [Seitenvariablen](/help/implement/vars/page-vars/page-variables.md) im Benutzerhandbuch zu Implementierungen.
   * „Marketing-Kanäle“, eine Komponente, die veranschaulicht, wie Anwender zu Ihrer Site gelangen. Siehe [Marketing-Kanäle](/help/components/c-marketing-channels/c-getting-started-mchannel.md) im Benutzerhandbuch zu Komponenten.
* **Klassifizierung:** eine Funktion in Adobe Analytics, die die Gruppierung von Dimensionselementen ermöglicht. Siehe [Klassifizierungen](/help/components/classifications/c-classifications.md) im Benutzerhandbuch zu Komponenten.
* **ClickMap:** wird nicht mehr verwendet. Ein veraltetes Browser-Plugin, das anzeigt, auf welche Bereiche auf Ihrer Site am häufigsten geklickt wurde. Dieses Tool wurde zugunsten von Activity Map eingestellt.
* **Clickstream-Feed:** Siehe „Daten-Feed“.
* **Kohorte:** eine Gruppe von Personen, die über einen bestimmten Zeitraum gemeinsame Merkmale aufweisen. Siehe [Was ist eine Kohortenanalyse?](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) im Benutzerhandbuch zu Analysen.
* **Erfassungs-Server:** Siehe „Datenerfassungs-Server“.
* **Kontextdatenvariablen:** temporäre Variablen, die ausschließlich in Verarbeitungsregeln verwendet werden. Die Werte der Kontextdatenvariablen gehen dauerhaft verloren, wenn eine Verarbeitungsregel sie nicht in eine Konversions- oder Traffic-Variable kopiert. Siehe [Kontextdatenvariablen](../implement/vars/page-vars/contextdata.md) im Benutzerhandbuch zu Implementierungen.
* **Konversionsvariable:** Auch als „eVars“ bezeichnet. Speichert einen benutzerspezifischen Wert und behält den Variablenwert bei, bis er abläuft. Weitere Informationen finden Sie unter der Dimension [eVar](/help/components/dimensions/evar.md) im Komponenten-Benutzerhandbuch.
* **Korrelation:** wird nicht mehr als Begriff verwendet; durch Dimensionsaufschlüsselungen ersetzt. In früheren Versionen von Adobe Analytics wurden durch Korrelationen Traffic-Variablen aufgeschlüsselt. Siehe [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md) im Benutzerhandbuch zu Analysen.
* **Aktuelle Daten:** eine Option in einigen Berichten, mit der kürzlich gesammelte Daten, die noch nicht vollständig verarbeitet wurden, aufgenommen werden können. Siehe [Aktuelle Daten](/help/analyze/reports-analytics/current-data.md) im Benutzerhandbuch zu Analysen.
* **Benutzerspezifischer Link:** ein Treffertyp, der Daten enthält, die keine Seitenansichten sind. Siehe [s.tl()-Funktion](../implement/vars/functions/tl-method.md) im Benutzerhandbuch zu Implementierungen. Siehe auch „Treffer“.
* **Kundenattribute:** eine Experience Cloud-Funktion, mit der Attributdaten hochgeladen werden können. Siehe [Kundenattribute](https://docs.adobe.com/content/help/de-DE/core-services/interface/customer-attributes/attributes.html) im Benutzerhandbuch zu zentralen Diensten.
* **Support-Beauftragter:** ein bestimmter Anwender, der zur direkten Interaktion mit der Adobe-Kundenunterstützung bestimmt ist. Siehe [Support-Beauftragte](https://helpx.adobe.com/de/experience-cloud/supported-users.html) in der Experience Cloud-Wissensdatenbank.
* **Datenerfassungs-Server:** Adobe-eigene Server, die Daten empfangen und verarbeiten. Bildanforderungen werden zur Verwendung in Berichten an die Datenerfassungs-Server von Adobe gesendet.
* **Daten-Connectoren:** eine vollständige Entwicklungslösung, die es Drittanbietern ermöglicht, das Hochladen von Daten in Adobe Analytics zu automatisieren. Kunden dieser Drittanbieter können einen Daten-Connector verwenden, um ihre Daten in Adobe Analytics zu erweitern. Die meisten Daten-Connectoren verwenden einen ähnlichen Workflow wie den in Data Sources. Siehe „Data Connectors“ im Benutzerhandbuch zu Importen.
* **Daten-Feed:** ein Rohdatenexport, der jeden Treffer als Zeile und Variablen als separate Spalten auflistet. Am häufigsten werden Adobe Analytics-Daten in Datenbanken von Drittanbietern exportiert. Siehe [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) im Benutzerhandbuch zu Exporten.
* **Datenquellen:** Ermöglicht dem Anwender das Hochladen von Daten aus einer Datei in Adobe Analytics. Die Datei wird normalerweise von einer FTP-Site abgerufen. Siehe [Data Sources](/help/import/c-data-sources/datasrc-home.md) im Benutzerhandbuch zu Importen.
* **Data Warehouse:** Eine Funktion in Adobe Analytics, mit der Sie größere Berichte anfordern können. Siehe [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) im Benutzerhandbuch zu Exporten.
* **Dimension:** ein Komponententyp, der Variablenwerte wie Text enthält. Beispiele sind Seitenname, Trackingcode oder Referrer-Domäne. Eine Metrik bildet normalerweise ihr Gegenstück.
* **Ereignis-Serialisierung:** der Prozess der Implementierung von Maßnahmen zur Vermeidung der Erfassung doppelter Ereignisse. Siehe [Ereignis-Serialisierung](../implement/vars/page-vars/events/event-serialization.md) im Benutzerhandbuch zu Implementierungen.
* **eVar:** Siehe „Konversionsvariable“.
* **Ereignis:** Siehe „Erfolgsereignis“.
* **ExcelClient:** wird nicht mehr als Begriff verwendet. Name des Vorgängers von Report Builder.
* **Gültigkeit:** wie lange der Wert im Backend einer Konversionsvariablen erhalten bleibt. Durch diese Persistenz können Ereignisse mit Variablenwerten vor dem Treffer des Ereignisses verknüpft werden. Siehe [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) im Administratorhandbuch.
* **Fluss:** ein Visualisierungstyp in Analysis Workspace, der zeigt, welche Pfade Anwender auf Ihrer Site genutzt haben. Siehe [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) im Benutzerhandbuch zu Analysen.
* **Genesis:** wird nicht mehr als Begriff verwendet. Früherer Name von Data Connectors.
* **Globale Report Suite:** ein informeller Begriff, der für eine Report Suite bestimmt ist, die Treffer von mehreren Sites erfasst.
* **H-Code:** ein Vorgänger von AppMeasurement. In früheren Versionen von Adobe Analytics wurden Code-Versionen nach „H-Version“ gemessen, z. B. H.27.5, H.26 usw.
* **Treffer:** eine Bildanforderung, die an Adobe-Datenerfassungs-Server gesendet wird. Seitenansichten und benutzerspezifische Links können beide als Treffer bezeichnet werden.
* **Bildanforderung:** ein transparentes 1x1-Pixelbild, das zur Kommunikation mit Adobe-Datenerfassungs-Servern verwendet wird. Eine Website fordert dieses unsichtbare Bild mit einer langen Abfragezeichenfolge voller Daten an. Adobe gibt das unsichtbare Bild zurück und analysiert die empfangene Abfragezeichenfolge.
* **Insight:** kann sich auf Folgendes beziehen:
   * Der frühere Name von Data Workbench.
   * Custom Insight, ein alter Name für benutzerspezifische Traffic-Variablen.
* **KPI:** Abkürzung für Key Performance Indicator. Metriken, die einem Unternehmen helfen, die Leistung seiner Site zu verstehen. Jede Organisation verfügt über unterschiedliche KPIs, die verschiedene Aspekte ihres Geschäfts messen. Siehe [Lösungsdesigndokument erstellen](/help/implement/prepare/solution-design.md) im Benutzerhandbuch zu Implementierungen.
* **Latenz:** die Verzögerung zwischen der Datenerfassung und der Verfügbarkeit in Berichten. Die typische Latenz in einer Report Suite beträgt 30 bis 90 Minuten. Siehe [Latenz](/help/technotes/latency.md) im Benutzerhandbuch zu technischen Informationen.
* **Launch:** Kurzform von Adobe Experience Platform Launch, der aktuellen Implementierungslösung von Adobe. Siehe [Übersicht](https://docs.adobe.com/content/help/de-DE/launch/using/overview.html) im Benutzerhandbuch zu Adobe Experience Platform Launch.
* **Listen-Prop:** eine Einstellung, die eine typische Traffic-Variable konvertiert, um mehrere Werte im selben Treffer zu unterstützen. Jede benutzerspezifische Traffic-Variable kann eine Listen-Prop werden, wenn die Einstellung aktiviert ist. Siehe [Prop](../implement/vars/page-vars/prop.md) im Benutzerhandbuch zu Implementierungen.
* **Listenvariable:** eine separate Variable, die von Konversionsvariablen getrennt ist. Listenvariablen unterstützen mehrere Werte im selben Treffer und Variablenwerte werden bei einem Besuch beibehalten, ähnlich wie Konversionsvariablen. Ein Unternehmen kann nur drei Listenvariablen verwenden. Siehe [Liste](/help/implement/vars/page-vars/list.md) im Benutzerhandbuch zu Implementierungen.
* **Anmeldeunternehmen:** eine Sammlung von Report Suites, die von Ihrer Organisation verwendet werden. Einige Organisationen verfügen über mehrere Anmeldeunternehmen, die jeweils für verschiedene Teile der Organisation relevant sind.
* **Marketing-Kanal:** eine Funktion in Adobe Analytics, die Treffer nach der Ankunft auf Ihrer Site kategorisiert. Die zur Kategorisierung von Treffern verwendete Logik kann mithilfe von Marketing-Kanal-Verarbeitungsregeln angepasst werden. Siehe [Erste Schritte mit Marketing-Kanälen](/help/components/c-marketing-channels/c-getting-started-mchannel.md) im Benutzerhandbuch zu Komponenten.
* **Metrik:** ein Komponententyp, der quantitative Daten enthält. Metrikwerte enthalten in der Regel Zahlen wie Seitenansichten, Besuche und Umsatz. Eine Dimension bildet normalerweise ihr Gegenstück.
* **Multi-Suite-Tagging:** die Vorgehensweise, denselben Treffer an mehrere Report Suites zu senden. Mit der Einführung in Virtual Report Suites ist diese Vorgehensweise weitgehend nicht mehr erforderlich. Die meisten Multi-Suite-Tagging-Bemühungen unterstützen eine globale Report Suite.
* **Normalisierung:** eine Möglichkeit, eine Visualisierung zu organisieren, bei der alle Metriken in gleiche Proportionen umgewandelt werden, sodass Trends leichter verglichen werden können.
* **Vorfälle:** ein Metriktyp, der anzeigt, in wie vielen Treffern ein Dimensionselement festgelegt oder beibehalten wurde. Weitere Informationen finden Sie unter der Metrik [Vorfälle](/help/components/metrics/occurrences.md) im Komponenten-Benutzerhandbuch.
* **Omniture:** wird nicht mehr als Begriff verwendet. Unternehmen, das im Besitz von Adobe Analytics war, bevor es 2009 von Adobe übernommen wurde.
* **Pfade:** Siehe „Fluss“.
* **Seitenansicht:** ein Treffertyp, der die Seitenansichten erhöht. Weitere Informationen finden Sie unter der Metrik [Seitenansichten](/help/components/metrics/page-views.md) im Komponenten-Benutzerhandbuch. Siehe auch „Treffer“.
* **Persistenz:** ein abstraktes Konzept für Konversionsvariablen, das die Verknüpfung zwischen einem Variablenwert und einem Ereignis bei separaten Treffern ermöglicht. Siehe auch „Gültigkeit“.
* **Primärer Server-Aufruf:** Alternativname für Bildanforderungen oder Treffer, der hauptsächlich im Zusammenhang mit Multi-Suite-Tagging und Abrechnung verwendet wird. Wenn derselbe Treffer an mehrere Report Suites gesendet wird, handelt es sich bei der ersten Report Suite um einen primären Server-Aufruf und bei den anderen um sekundäre Server-Aufrufe. Diese Regel gilt für alle Treffertypen, einschließlich Seitenansicht und Linktracking. Siehe auch „Sekundäre Server-Aufrufe“.
* **Verarbeitungsregeln:** kann sich auf Folgendes beziehen:
   * Verarbeitungsregeln, um die Datenerfassung mithilfe bestimmter Regeln in der Admin Console zu ändern. Siehe [Verarbeitungsregeln](/help/admin/admin/c-processing-rules/processing-rules.md) im Administratorhandbuch.
   * Marketing-Kanal-Verarbeitungsregeln, ein Regelsatz, der bestimmt, zu welchem Marketing-Kanal ein Treffer gehört. Siehe [Marketing-Kanal-Verarbeitungsregeln](/help/admin/admin/marketing-channels-admin.md) im Administratorhandbuch.
* **Prop:** Siehe „Traffic-Variable“.
* **Rangbericht:** ein Berichtsformat, das normalerweise einer Dimension mit einer Metrik folgt. Mit diesem Berichtstyp können Sie die wichtigsten Elemente anzeigen, wie z. B. die am häufigsten angezeigten Seiten Ihrer Site. Siehe auch „Trend-Bericht“.
* **Echtzeit:** zeigt konfigurierte Variablen an, sobald sie mit wenig bis gar keiner Latenz erfasst werden. Siehe [Echtzeitberichte](/help/admin/admin/realtime/realtime.md) im Administratorhandbuch.
* **Report Suite:** ein übergeordneter Container, an den Sie Daten senden. Alle Berichte in Adobe Analytics verweisen auf eine Report Suite.
* **Rollierender Datumsbereich:** ein Typ des relativen Datumsbereichs, der sich im Zeitverlauf ändert. Ein Bericht mit den letzten sieben Tagen kann beispielsweise als rollierender Datumsbereich betrachtet werden. Siehe auch „Statischer Datumsbereich“.
* **RSID:** Abkürzung für Report Suite-ID. Eine Report Suite verfügt sowohl über einen benutzerfreundlichen Namen als auch über eine Report Suite-ID.
* **s.t():** der Name der Funktion in einer AppMeasurement-Bibliothek, die eine Bildanforderung für die Seitenansicht sendet. Einige AppMeasurement-Bibliotheken verwenden stattdessen `s.track()`. Siehe [t](../implement/vars/functions/t-method.md) im Benutzerhandbuch zu Implementierungen.
* **s<span>.</span>tl():** der Name der Funktion in einer AppMeasurement-Bibliothek, die eine Bildanforderung für das Linktracking sendet. Einige AppMeasurement-Bibliotheken verwenden stattdessen `s.trackLink()`. Siehe [tl](../implement/vars/functions/tl-method.md) im Benutzerhandbuch zu Implementierungen.
* **s_code.js:** der Name der JavaScript-Datei, die in alten Versionen von Adobe Analytics verwendet wird. Der aktuelle Name der verwendeten JavaScript-Datei ist „AppMeasurement.js“.
* **Satellite:** wird nicht mehr als Begriff verwendet. Der frühere Produktname für Dynamic Tag Management.
* **Sekundärer Server-Aufruf:** Alternativname für Bildanforderungen oder Treffer, der hauptsächlich im Zusammenhang mit Multi-Suite-Tagging und Abrechnung verwendet wird. Wenn derselbe Treffer an mehrere Report Suites gesendet wird, sind alle Report Suites nach dem ersten aufgelisteten Aufruf sekundäre Server-Aufrufe. Siehe auch „Primäre Server-Aufrufe“.
* **Segment:** Hiermit können Sie sich auf eine bestimmte Untergruppe Ihrer Daten konzentrieren. Siehe [Segmentierung](/help/components/segmentation/seg-overview.md) im Benutzerhandbuch zu Komponenten.
* **Segment-Container:** der Teil eines Segments, der bestimmt, wie viele Daten eingehen sollen. Container können auf Seitenansicht, Besuch oder Besucher basieren. Siehe [Segmentierung](/help/components/segmentation/seg-overview.md) im Benutzerhandbuch zu Komponenten.
* **Serialisierung:** Siehe „Ereignis-Serialisierung“.
* **Server-Aufruf:** Alternativname für eine Bildanforderung oder einen Treffer, der hauptsächlich im Zusammenhang mit der Abrechnung verwendet wird.
* **Einzelzugriff:** ein Besuch, bei dem eine Dimension nur einen eindeutigen Wert aufwies. Der Besuch kann mehrere Treffer aufweisen, solange nicht mehrere eindeutige Werte vorhanden sind. Weitere Informationen finden Sie unter der Metrik [Einzelzugriff](/help/components/metrics/single-access.md) im Komponenten-Benutzerhandbuch. Siehe auch „Absprung“.
* **SiteCatalyst:** wird nicht mehr als Begriff verwendet. Der frühere Produktname für Adobe Analytics.
* **Lösungs-Design-Dokument:** Auch als Lösungs-Design-Referenz (Solution Design Reference, SDR) bezeichnet. Ein internes Dokument, das von einem Unternehmen verwaltet wird und in dem die Verwendung benutzerspezifischer Variablen sowie die zum Ausfüllen verwendete Logik erläutert werden. Siehe [Lösungsdesigndokument erstellen](/help/implement/prepare/solution-design.md) im Benutzerhandbuch zu Implementierungen.
* **Subrelation:** wird nicht mehr als Begriff verwendet; durch Dimensionsaufschlüsselungen ersetzt. In früheren Versionen von Adobe Analytics boten Subrelationen die Möglichkeit, Konversionsvariablen aufzuschlüsseln. Siehe [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md) im Benutzerhandbuch zu Analysen.
* **Erfolgsereignis:** eine verfolgte Aktion, die ein Anwender ausgeführt hat. Ihr Unternehmen legt fest, welche Ereignisse verfolgt werden und welche Erfolgsereignisvariablen Sie für das Tracking verwenden. Siehe [Benutzerspezifische Ereignisse](/help/components/metrics/custom-events.md) im Benutzerhandbuch zu Komponenten.
* **Unterstützter Anwender:** Siehe „Support-Beauftragter“.
* **Traffic-Variable:** Auch als „Props“ bezeichnet. Speichert einen benutzerspezifischen Wert für einen einzelnen Treffer. In früheren Versionen von Adobe Analytics wurden Props eindeutige Werte zugewiesen. Durch Verbesserungen der Plattform sind benutzerspezifische Traffic-Variablen jedoch heute weitgehend unnötig. Adobe empfiehlt in den meisten Fällen die Verwendung benutzerspezifischer Konversionsvariablen (eVars). Weitere Informationen finden Sie unter der Dimension [Prop](/help/components/dimensions/prop.md) im Komponenten-Benutzerhandbuch.
* **Trend-Bericht:** ein Berichtsformat, das normalerweise mehrere Datumsbereiche mit einer Metrik anzeigt. Mit diesem Berichtstyp können Sie die Leistung einer Metrik im Laufe der Zeit anzeigen. Siehe auch „Rangbericht“.
* **Unique Visitor**: stellt die Anzahl eindeutiger Einzelanwender dar, die Ihre Site besucht haben. Ein einzelner Unique Visitor kann mehrere Besuche aufweisen. Weitere Informationen finden Sie unter der Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md) im Komponenten-Benutzerhandbuch.
* **Virtual Report Suite:** ein virtueller Daten-Container, der auf eine normale Report Suite verweist und die Datenveredelung ermöglicht. Daten werden nicht an eine Virtual Report Suite gesendet. Stattdessen werden sie an eine normale Report Suite gesendet und eine Virtual Report Suite nutzt diese erfassten Daten. Siehe [Virtual Report Suites](/help/components/vrs/vrs-about.md) im Benutzerhandbuch zu Komponenten.
* **Besuch:** stellt die Anzahl der eindeutigen Sitzungen dar, die auf Ihrer Site stattgefunden haben. Weitere Informationen finden Sie unter der Metrik [Besuche](/help/components/metrics/visits.md) im Komponenten-Benutzerhandbuch.
* **VISTA-Regel:** benutzerspezifische Logik, die von Adobe auf Anforderung eines Kunden erstellt wurde, um Daten Server-seitig zu kopieren, zu analysieren oder zu filtern. VISTA-Regeln verursachen in der Regel zusätzliche Kosten. Siehe auch „Verarbeitungsregeln“.
* **Webbeacon:** Siehe „Bildanforderung“.
