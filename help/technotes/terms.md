---
title: In Adobe Analytics verwendete Begriffe
description: Glossar für Adobe Analytics, das verwendete Begriffe definiert.
translation-type: tm+mt
source-git-commit: 5ca51ad6b967687004d9447964ed87b29077b330

---


# In Adobe Analytics verwendete Begriffe

Verwenden Sie dieses Glossar, um den Kontext vieler von Adobe Analytics verwendeter Begriffe zu verstehen.

* **Admin-Konsole:** Kann auf:
   * Legacy-Administrationstools, in denen Report Suite-Einstellungen in Adobe Analytics verwaltet werden. In früheren Versionen von Adobe Analytics wurden Benutzerberechtigungen ebenfalls hier verwaltet. See [Admin Tools](../admin/admin/c-admin-tools.md) in the Admin user guide.
   * Die Adobe Admin-Konsole, in der der Produktzugriff bereitgestellt und Benutzerberechtigungen verwaltet werden. See [Admin Console](../admin/admin-console/home.md) in the Admin user guide.
* **Zuordnung:** Wenn eine Konversionsvariable während eines Besuchs mehr als einen Wert erkennt, bestimmt die Zuweisungseinstellung der Variablen, welcher Wert beibehalten wird. See [Conversion variables](../admin/admin/conversion-var-admin/conversion-var-admin.md) in the Admin user guide.
* **Anomalie:** Mithilfe statistischer Modellierung erkannt, um unerwartete Trends in Daten automatisch zu finden. Das Modell analysiert Metriken und ermittelt Ober- und Untergrenze sowie eine erwartete Bandbreite von Werten. See [Anomaly Detection](../analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) in the Analyze user guide.
* **Appmeasurement:** Die Code-Bibliothek, mit der Daten erfasst und an Adobe gesendet werden. See the [Homepage](../implement/home.md) of the Implement user guide.
* **ASI-Slot:** Nicht mehr vorhanden. In früheren Versionen von Adobe Analytics stellte ASI-Slots einen temporären Report Suite-Container bereit, um segmentierte Daten anzuzeigen. In der aktuellen Version von Adobe Analytics können Segmente sofort auf jeden beliebigen Bericht angewendet werden.
* **Aufschlüsselung:** Sie können eine Dimension im Kontext einer anderen Dimension anzeigen. See [Break down dimensions](../analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md) in the Analyze user guide.
* **Abspringen:** Ein Besuch, der aus einem einzelnen Treffer besteht. See [Bounces](../components/c-variables/c-metrics/metrics-bounces.md) in the Components user guide. Siehe auch Einzelzugriff.
* **Berechnete Metrik:** Ermöglicht die Kombination vorhandener Metriken, statistische Funktionen und Formeln zur Verwendung in Berichten. See [Calculated metrics](../components/c-calcmetrics/cm-overview.md) in the Components user guide.
* **Kampagne:** Kann auf:
   * Die Kampagnenvariable, die die Dimension "Rückverfolgungscode" füllt. See [Page variables](../implement/js-implementation/c-variables/page-variables.md) in the Implement user guide.
   * Eine Standardklassifizierung der Rückverfolgungscode-Dimension; automatisch für alle Report Suites erstellt.
   * Adobe Campaign, Teil der Adobe Experience Cloud. More information on [Adobe.com](https://www.adobe.com/marketing/campaign.html).
* **Kanal:** Kann auf:
   * Die Kanalvariable, die die Dimension "Site-Abschnitte" füllt. See [Page variables](../implement/js-implementation/c-variables/page-variables.md) in the Implement user guide.
   * Marketingkanäle, eine Komponente, die Aufschluss darüber gibt, wie Benutzer zu Ihrer Site gelangen. See [Marketing Channels](../components/c-marketing-channels/c-overview.md) in the Components user guide.
* **Classification:** Eine Funktion in Adobe Analytics, die die Gruppierung von Dimensionswerten ermöglicht. See [Classifications](../components/c-classifications2/c-classifications.md) in the Components user guide.
* **Clickstream-Datenfeed:** Siehe Datenfeed.
* **Konversionsvariable:** Wird als evars bezeichnet. Speichert einen benutzerdefinierten Wert und behält den Variablenwert bei, bis er abläuft. See [Conversion variables](../components/c-variables/dimensionslist/reports-conversion.md) in the Components user guide.
* **Korrelation:** Nicht mehr als Begriff verwendet; durch Dimensionsaufschlüsselungen ersetzt. In früheren Versionen von Adobe Analytics haben Korrelationen die Möglichkeit, Traffic-Variablen aufzuschlüsseln. See [Break down dimensions](../analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md) in the Analyze user guide.
* **Aktuelle Daten:** Eine Option in einigen Berichten, die die Einbeziehung kürzlich erfasster Daten ermöglicht, die noch nicht vollständig verarbeitet wurden. See [Current data](../analyze/reports-analytics/current-data.md) in the Analyze user guide.
* **Benutzerspezifischer Link:** Ein Treffertyp, der Daten ohne Seitenansichten enthält. See the [s.tl() function](../implement/js-implementation/function-tl.md) in the Implement user guide. Siehe auch Treffer.
* **Kundenattribute:** Eine Experience Cloud-Funktion, die das Hochladen von Attributdaten ermöglicht. See [Customer attributes](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html) in the Core Services user guide.
* **Kundensupport-Stellvertreter:** Ein benannter Benutzer, der direkt mit dem Adobe-Kundendienst interagiert. See [Customer support delegates](https://helpx.adobe.com/experience-cloud/supported-users.html) in the Experience Cloud Knowledgebase.
* **Data Connectors:** Eine vollständige Entwicklungslösung, die es Dritten ermöglicht, das Hochladen von Daten in Adobe Analytics zu automatisieren. Kunden dieses Drittanbieters können mit einem Data Connector ihre Daten in Adobe Analytics anreichern. Die meisten Datenschnittstellen verwenden einen ähnlichen Arbeitsablauf, der in Data Sources verwendet wird. Siehe Data Connectors im Import-Benutzerhandbuch.
* **Datenfeed:** Ein Rohdatenexport, der jeden Treffer als Zeile und Variablen als separate Spalten auflistet. Wird am häufigsten zum Exportieren von Adobe Analytics-Daten in eine Drittanbieterdatenbank verwendet. See [Data feeds](../export/analytics-data-feed/c-getstarted/data-feed-overview.md) in the Export user guide.
* **Datenquellen:** Ermöglicht Benutzern das Hochladen von Daten aus einer Datei in Adobe Analytics. Die Datei wird normalerweise von einer FTP-Site abgerufen. See [Data Sources](../import/c-data-sources/datasrc-home.md) in the Import user guide.
* **Data Warehouse:** Eine Funktion in Adobe Analytics, mit der Sie größere Berichte anfordern können. See [Data Warehouse](../export/data-warehouse/data-warehouse.md) in the Export user guide.
* **Dimension:** Ein Komponententyp, der Variablenwerte enthält, z. B. Text. Beispiele sind Seitenname, Rückverfolgungscode oder Verweisende Domäne. Eine Metrik ist normalerweise ihr Gegenstück.
* **Dynamisches Tag-Management:** die bisherige Tag-Management-Lösung von Adobe. See [DTM implementation overview](../implement/c-implement-with-dtm/dtm-implementation-overview.md) in the Implement user guide. Adobe empfiehlt stattdessen das Starten von Adobe Experience Platform.
* **Ereignis-Serialisierung:** Der Vorgang der Implementierung von Messwerten, um die Sammlung doppelter Ereignisse zu verhindern. See [Event serialization](../implement/js-implementation/event-serialization.md) in the Implement user guide.
* **Evar:** Siehe Konversionsvariable.
* **Ereignis:** Siehe Erfolgsereignis.
* **Excelclient:** Wird nicht mehr als Begriff verwendet. Der Name des Vorgängers von Reportbuilder.
* **Ablauf:** Im Kontext einer Konversionsvariablen, wie lange der Wert auf dem Backend bleibt. Mit dieser Persistenz können Ereignisse mit Variablenwerten vor dem Treffertreffer des Ereignisses verknüpft werden. See [Conversion variables](../admin/admin/conversion-var-admin/conversion-var-admin.md) in the Admin user guide.
* **Fluss:** Eine Art Visualisierung im Analysis Workspace, die zeigt, welche Pfade Benutzer auf Ihrer Site eingeschlagen haben. See [Flow visualization](../analyze/analysis-workspace/visualizations/c-flow/flow.md) in the Analyze user guide.
* **Genesis:** Wird nicht mehr als Begriff verwendet. Der frühere Name von Data Connectors.
* **Globale Report Suite:** Ein offizieller Begriff, der einer Report Suite zugewiesen ist, die Treffer von mehreren Sites sammelt.
* **H-Code:** Ein Vorgänger zu appmeasurement. In früheren Versionen von Adobe Analytics wurden Codeversionen mit "H-Version" gemessen, z. B.H 24, H 23.1 usw.
* **Treffer:** Eine einzelne Bildanforderung, die an die Adobe-Datenerfassungsserver gesendet wird. Seitenansichten und benutzerspezifische Links können als Treffer bezeichnet werden.
* **Bildanforderung:** Ein transparentes 1 x 1 Pixel-Bild, das für die Kommunikation mit Adobe-Datenerfassungsservern verwendet wird. Eine Website fordert dieses unsichtbare Bild mit einer langen Abfragezeichenfolge mit Daten an. Adobe gibt das unsichtbare Bild zurück und analysiert die Abfragezeichenfolge.
* **Insight:** Kann auf:
   * Der frühere Name von Data Workbench.
   * Custom Insight, ein historischer Name für benutzerspezifische Traffic-Variablen.
* **KPI:** Abkürzung für Key Performance Indicator. Metriken, die einem Unternehmen helfen, dessen Leistung zu verstehen. Jede Organisation verfügt über verschiedene Kpis, die verschiedene Aspekte ihres Unternehmens messen. See [Create a solution design document](../implement/prepare/solution-design.md) in the Implement user guide.
* **Latenz:** Die Verzögerung zwischen der Erfassung von Daten und der Verfügbarkeit in Berichten. Typische Latenz in einer Report Suite beträgt 30 bis 90 Minuten. See [Latency](../technotes/latency.md) in the Technotes user guide.
* **Start:** Kurz für Adobe Experience Platform Launch, die aktuelle Implementierungslösung von Adobe. See [Overview](https://docs.adobe.com/content/help/en/launch/using/overview.html) in the Adobe Experience Platform Launch user guide.
* **Listen-Prop:** Eine Einstellung, die eine typische Traffic-Variable konvertiert, um mehrere Werte im selben Treffer zu unterstützen. Jede benutzerdefinierte Traffic-Variable kann zu einer Listeneigenschaftsvariablen werden, wenn die Einstellung aktiviert ist. See [Page variables](../implement/js-implementation/c-variables/page-variables.md) in the Implement user guide.
* **Listenvariable:** Eine eindeutige Variable, die zu Konversionsvariablen getrennt ist. Listenvariablen unterstützen mehrere Werte im selben Treffer und Variablenwerte werden bei einem Besuch beibehalten, ähnlich wie bei Konversionsvariablen. Für eine Organisation stehen nur drei Listenvariablen zur Verfügung. See [Page variables](../implement/js-implementation/c-variables/page-variables.md) in the Implement user guide.
* **Unternehmen anmelden:** Eine Sammlung von Report Suites, die von Ihrem Unternehmen verwendet werden. Einige Organisationen verfügen über mehrere Anmeldeunternehmen, die für verschiedene Teile ihrer Organisation gelten.
* **Metrik:** Ein Komponententyp, der quantitative Daten enthält. Metrikwerte enthalten typischerweise Zahlen wie Seitenansichten, Besuche und Umsatz. Eine Dimension ist normalerweise ihr Gegenstück.
* **Multi-Suite-Tagging:** Die Vorgehensweise, denselben Treffer an mehrere Report Suites zu senden. Mit der Einführung in Virtual Report Suites ist diese Vorgehensweise größtenteils nicht mehr erforderlich. Die meisten Multi-Suite-Tagging-Bemühungen unterstützen eine globale Report Suite.
* **Normalisierung:** Eine Möglichkeit, eine Visualisierung zu organisieren, die alle Metriken akzeptiert und diese zu gleichen Anteilen zwingt, was einen einfacheren Vergleich der Trends ermöglicht.
* **Omniture:** Wird nicht mehr als Begriff verwendet. Die Organisation, die Adobe Analytics im Besitz von Adobe im Jahr 2009 hatte.
* **Pfade:** Siehe Fluss.
* **Rangbericht:** Ein Berichtsformat, das normalerweise auf eine Dimension mit einer Metrik folgt. Mit diesem Berichtstyp können Sie die wichtigsten Elemente sehen, z. B. die am häufigsten angezeigten Seiten auf Ihrer Site. Siehe auch Trendbericht.
* **Echtzeit:** Zeigt konfigurierte Variablen an, sobald sie mit wenig Latenz erfasst werden. See [Real-time reports](../admin/admin/realtime/realtime.md) in the Admin user guide.
* **Report Suite:** Ein übergeordneter Container, an den Sie Daten senden. Alle Berichte in Adobe Analytics verweisen auf eine Report Suite.
* **RSID:** Abkürzung für Report Suite-ID. Eine Report Suite hat sowohl einen benutzerfreundlichen Namen als auch eine Report Suite-ID.
* **Seitenansicht:** Ein Treffertyp, der Seitenansichten inkrementiert. See [Page views](../components/c-variables/c-metrics/metrics-page-view.md) in the Components user guide. Siehe auch Treffer.
* **Verarbeitungsregeln:** Kann auf:
   * Verarbeitungsregeln, eine Methode zur Änderung der Datenerfassung mit bestimmten Regeln in der Admin-Konsole. See [Processing rules](../admin/admin/c-processing-rules/processing-rules.md) in the Admin user guide.
   * Marketingkanal-Verarbeitungsregeln, mit denen bestimmt wird, welcher Marketingkanal ein Treffer ist. See [Marketing channel processing rules](../admin/admin/marketing-channels-admin.md) in the Admin user guide.
* **Prop:** Siehe Traffic-Variable.
* **s. t ():** Der Name der Funktion in einer appmeasurement-Bibliothek, die eine Seitenansichtbildanforderung sendet. Some AppMeasurement libraries use `s.track()` instead. See [s.t()](../implement/js-implementation/function-t.md) in the Implement user guide.
* **s<span>.</span>tl ():** Der Name der Funktion in einer appmeasurement-Bibliothek, die eine Link-Tracking-Bildanforderung sendet. Some AppMeasurement libraries use `s.trackLink()` instead. See [s.tl()](../implement/js-implementation/function-tl.md) in the Implement user guide.
* **Satellite:** Wird nicht mehr als Begriff verwendet. Der frühere Produktname für das dynamische Tag-Management.
* **Segment:** Damit können Sie sich auf bestimmte Untergruppen Ihrer Daten konzentrieren. See [Segmentation](../components/c-segmentation/seg-overview.md) in the Components user guide.
* **Segmentbehälter:** Der Teil eines Segments, der festlegt, wie viele Daten eingebracht werden sollen. Behälter können auf Seitenansichten, Besuchen oder Besuchern basieren. See [Segmentation](../components/c-segmentation/seg-overview.md) in the Components user guide.
* **Serialisierung:** Siehe Ereignis-Serialisierung.
* **Server-Aufruf:** Alternativer Name für eine Bildanforderung oder einen Treffer, der hauptsächlich im Kontext der Abrechnung verwendet wird.
* **Einzelzugriff:** Ein Besuch, bei dem eine Dimension nur einen einzelnen eindeutigen Wert hatte. Der Besuch kann mehrere Treffer haben, solange es nicht mehrere eindeutige Werte gibt. See [Single access](../components/c-variables/c-metrics/metrics-single-access.md) in the Components user guide. Siehe auch Abspringen.
* **Sitecatalyst:** Wird nicht mehr als Begriff verwendet. Der frühere Produktname für Adobe Analytics.
* **Subrelation:** Nicht mehr als Begriff verwendet; durch Dimensionsaufschlüsselungen ersetzt. In früheren Versionen von Adobe Analytics konnten Subrelationen die Möglichkeit haben, Konversionsvariablen aufzuschlüsseln. See [Break down dimensions](../analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md) in the Analyze user guide.
* **Erfolgsereignis:** Eine verfolgte Aktion, die ein Benutzer durchgeführt hat. Ihr Unternehmen bestimmt, welche Ereignisse verfolgt werden sollen und welche Erfolgsereignisvariablen Sie zur Verfolgung verwenden. See [Custom events](../components/c-variables/c-metrics/metrics-custom.md) in the Components user guide.
* **Unterstützter Benutzer:** Siehe Kundensupport-Stellvertreter.
* **Traffic-Variable:** Wird als Props bezeichnet. Speichert einen benutzerdefinierten Wert für einen einzelnen Treffer. Frühere Versionen von Adobe Analytics geben props einen eindeutigen Wert, doch Verbesserungen der Plattform machen benutzerdefinierte Traffic-Variablen größtenteils überflüssig. Adobe empfiehlt in den meisten Fällen, benutzerdefinierte Konversionsvariablen (evars) zu verwenden. See [Custom traffic variables](../components/c-variables/dimensionslist/reports-custom-traffic.md) in the Components user guide.
* **Trendbericht:** Ein Berichtsformat, das in der Regel mehrere Datumsbereiche mit einer Metrik anzeigt. Mit diesem Berichtstyp können Sie sehen, wie eine Metrik im Laufe der Zeit läuft. Siehe auch Rangbericht.
* **Individueller Besucher**: Stellt die Anzahl der individuellen Personen dar, die Ihre Site besucht haben. Ein einzelner individueller Besucher kann mehrere Besuche haben. See [Unique visitor](../components/c-variables/c-metrics/metrics-unique-visitors.md) in the Components user guide.
* **Virtual Report Suite:** Ein virtueller Container mit Daten, der auf eine normale Report Suite verweist und die Datenverfeinerung zulässt. Daten werden nicht an eine Virtual Report Suite gesendet; Stattdessen werden Daten an eine normale Report Suite gesendet und eine Virtual Report Suite erstellt diese Daten. See [Virtual report suites](../components/vrs/vrs-about.md) in the Components user guide.
* **Besuch:** Stellt die Anzahl der eindeutigen Sitzungen dar, die auf Ihrer Site stattgefunden haben. See [Visits](../components/c-variables/c-metrics/metrics-visit.md) in the Components user guide.
* **VISTA-Regel:** Benutzerdefinierte Logik, die von Adobe auf Anfrage eines Kunden zum Kopieren, Analysieren oder Filtern von Daten erstellt wurde. VISTA-Regeln verursachen in der Regel zusätzliche Kosten. Siehe auch Verarbeitungsregeln.
* **Web-Beacon:** Siehe Bildanforderung.
