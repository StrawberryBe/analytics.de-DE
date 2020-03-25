---
description: Diese Hilfeseite enthält empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Die Tools sollten in der Reihenfolge, in der sie aufgelistet sind, berücksichtigt werden. Wenn ein bestimmtes Werkzeug nicht den Anforderungen entspricht, gehen Sie zum nächsten zur Prüfung.
title: Welches Adobe Analytics-Tool sollte ich verwenden?
uuid: 1179e49d-3cfc-4abd-a8eb-35c5ae380c16
translation-type: tm+mt
source-git-commit: f7125e6845a653ca3d4dd3f1313d1b39f564459c

---


# Welches Adobe Analytics-Tool sollte ich verwenden?

Diese Hilfeseite enthält empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Die Tools sollten in der Reihenfolge, in der sie aufgelistet sind, berücksichtigt werden. Wenn ein bestimmtes Werkzeug nicht den Anforderungen entspricht, gehen Sie zum nächsten zur Prüfung.

Weitere Informationen zu Adobe Analytics-Produktvergleichen finden Sie [hier](/help/admin/c-analytics-product-comparison/analytics-product-comparison.md).

## Adobe Analytics-Berichtsoberflächen {#section_8265460EBB47405AB19A3B2B0729C8A4}

**[Analysis Workspace](/help/analyze/analysis-workspace/analysis-workspace-features.md)**sollte die bevorzugte Benutzeroberfläche für alle Berichts- und Analyseaufgaben sein. Adobe investiert weiterhin in dieses Produkt und gibt monatlich Updates dafür heraus. Können Sie eine Aufgabe nicht mit Analysis Workspace durchführen, versuchen Sie eine der unten stehenden Oberflächen.**

**[Reports &amp; Analytics](/help/analyze/reports-analytics/overview/report-overview.md)**sollte verwendet werden:

* Von Einsteigern, die auf eine vorkonfigurierte Berichterstellung zugreifen müssen, in der einfacher navigiert werden kann.
* Steigerung und Konfidenz der Zielgruppe (Analytics for Zielgruppe/A4T).
* So greifen Sie auf Echtzeitdaten in der Benutzeroberfläche zu.
* So richten Sie Kalendereinstellungen ein.
* So richten Sie Zielgruppen ein.
* Ansicht Bot Berichte.
* Für den Zugriff auf eindeutige Video-Visualisierungen von gleichzeitigem Viewer, Videotagesabschnitt und Viewer-Drop-off.
* So nutzen Sie Veröffentlichungs-Listen im geplanten Berichte.

**[Mobile Services](https://docs.adobe.com/content/help/en/mobile-services/using/home.html)**sollte verwendet werden:

* Wenn eine Silo-Ansicht mit Daten zur mobilen App gewünscht wird.
* So verwalten Sie die Implementierung Ihres Mobile App SDK.
* Zur Einrichtung mobiler Anzeigen wie In-App-Nachrichten, Push-Nachrichten und Standort-Targeting.
* Wenn mehr interaktive Visualisierungen für App-Daten gewünscht werden (Sunburst).
* Zur Visualisierung von Sehenswürdigkeiten auf einer Karte.
* Für Lebensdauerwertmetriken.

**[Ad Hoc Analysis](/help/analyze/ad-hoc-analysis/adhoc-home.md)**sollte verwendet werden:

* So exportieren Sie 50.000 Datenzeilen
* Wenn eine tabulatorische Organisation der Projektarbeit gewünscht wird.
* Zur Verwendung des Site-Analyse-Berichts (3D-Pfadsetzungsbericht).

**[Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html)**sollte verwendet werden:

* Als flexibelste Analytics-Tool-Option (bis zur Analyse auf Trefferebene auf Besucher-Ebene).
* Zur Erstellung eines Multi-Kanal-Datensatzes mit Online- und Offline-Interaktionen von CRM über POS bis Web.
* Für erweiterte Zuordnung (regelbasierte und algorithmische Modelle).
* Zur Vorhersage, statistischen Modellierung (Tendenzauswertung, Clustering, Korrelationen usw.).
* Für Latenzzeit Analyse (Zeit vor/seit einem Ereignis).
* Zur Identifizierung und zum Export komplexer Segmente in die Adobe Experience Cloud.

## Importieren von Daten in Adobe Analytics {#section_B42B998D6E3E4357B024AEFA4EC69A23}

**[Classifications](/help/components/c-classifications2/c-classifications.md)**sollte verwendet werden:

* Wenn Metadaten vorhanden sind, die Sie mit einem Erfassungswert (eVar, prop, Marketing-Kanal) verknüpfen möchten
* Optionen:

   * Rule Builder: verwenden, wenn für eine Variable vorhersehbare formatierte Werte erfasst werden, z. B. durch Trennzeichen getrennte Werte. Mit diesem Ansatz können Sie Regeln einmalig festlegen und weitgehend &quot;Set-it and vergiss-it&quot;.
   * Browser-Importtool: verwenden, wenn Sie nicht über vorhersagbare Werte oder über eine begrenzte Liste von Werten verfügen, die eine einmalige Aktualisierung erfordern. Bei diesem Ansatz ist eine fortlaufende Überwachung der Klassifizierungen auf neue Werte nötig.

**[Data Sources](/help/import/c-data-sources/datasrc-home.md)**sollte verwendet werden:

* Wenn Offline-Daten vorliegen, die dauerhaft in Adobe Analytics geschrieben werden sollen
* Optionen:

   * Zusammenfassung: einfache Datenuploads nach Tag oder begrenzten Dimensionen
   * Transaktions-ID: Datenuploads, die einen Online-Endpunkt mit Offlinedaten verbinden und importierte Daten vollständig einem Online-Schnappschuss des Besuchers zuordnen (z. B. online abgeschlossene Bestellungen und offline zurückgegebene )
   * Volle Verarbeitung: Datenquellen mit Zeitstempel, die so verarbeitet werden, als ob es sich um einen von Adobe-Servern erfassten Treffer handelte. D.h. Daten werden direkt in die Besucher-Reise eingefügt.

**[Data Connectors](https://www.adobeexchange.com/experiencecloud.html)(ehemals Genesis)**sollte verwendet werden:

* Wenn Sie mit einem Drittanbieter interagieren, der eine unterstützte Verbindung mit Adobe Analytics aufgebaut hat. Data Connectors integrieren Daten auf Zusammenfassungsebene in Adobe Analytics in der Regel dauerhaft und automatisch, und zwar regelmäßig.

Die **[Data Insertion API](https://marketing.adobe.com/developer/documentation/data-insertion/c-data-insertion-api)**sollte verwendet werden:

* Wenn Sie Daten in Adobe Analytics laden und den Adobe AppMeasurement- oder mobilen SDK-Code nicht nutzen können.

**[Kundenattribute](/help/components/c-variables/dimensionslist/reports-customer-attributes.md)**sollten verwendet werden:

* Wenn Sie Daten von Unternehmenskunden in einer CRM-Datenbank (Customer Relationship Management) erfassen und die Daten in die Experience Cloud hochladen möchten.
* Wenn Sie CRM-Daten für eine tiefere Analyse in Analytics oder als Targeting-Kriterien in Adobe Zielgruppe verwenden möchten.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)**sollte verwendet werden:

* Wenn Sie Daten zur Adobe Audience Manager-Audience (AAM) wie demografische Informationen (z. B. Geschlecht oder Einkommensstufe), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten oder Daten zu Anzeigenimpressionen in einen beliebigen Analytics-Arbeitsablauf integrieren möchten.
* Wenn hochgeladene CRM-Daten zeitbasiert sein sollen, da diese Integration neue Informationen an Analytics-Treffer sendet.

## Exportieren von Daten aus Adobe Analytics {#section_901C06ABF2014E92B2952906723DF235}

**[Report Builder](/help/analyze/report-builder/home.md)**sollte verwendet werden:

* Wenn die benutzerdefinierten Layoutoptionen von Workspace eingeschränkt sind (alles ist in ReportBuilder möglich, innerhalb der Grenzen von Excel).
* Zur lockeren Verknüpfung von Benutzereingaben oder Offline-Datenquellen (Impressionen, Kosten) mit Adobe-Daten. Eine dauerhaftere Lösung zum Einbinden von Daten ist Data Sources (siehe Importieren von Daten in Analytics).
* Zum Zusammenführen von Daten aus verschiedenen dimensionalen Berichten (z. B. zusammen mit dem Bericht zu Promo-Impressionen und dem Bericht zu &quot;Klick-zu-Konversion&quot;).
* Für Report Suite-übergreifende Ansichten.
* Wenn Automatisierung durch Zeitplanung gewünscht wird (XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)**sollte verwendet werden:

* Für den Zugriff auf Variablen, die ansonsten in der Benutzeroberfläche verborgen sind: IP-Adresse, Experience Cloud ID, Analytics-Besucher-ID, Seiten-URL
* So greifen Sie auf granulärere Daten als die Benutzeroberfläche zu (denormalisierte Tabellendaten-Ansicht)
* So laden Sie Daten in einem für die Pivot-Tabelleneingabe geeigneten Format herunter
* Wenn der Kunde Adobe-Daten in ein Visualisierungstool für Daten von Drittanbietern eingeben möchte (leicht zusammengefasst und nicht auf Trefferebene)
* Für den Zugriff auf alle eindeutigen Dimensionswerte, wenn in Adobe Analytics ein geringer Datenverkehr für Sie vorliegt

**[Analytics-Daten-Feed](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)**sollte verwendet werden:

* Zur Nutzung des granulärsten Datenfeeds, den wir bereitstellen können (Besucher-ID, Treffer).
* Wenn der Kunde Adobe-Daten in einer clientseitigen Datenbank speichern möchte, können wir diese auf möglichst granularer Ebene senden.
* Wenn der Kunde ein Business Intelligence-Tool (BI) entwickeln oder Adobe-Daten auf Trefferebene in ein Tool eines Drittanbieters eingeben möchte.

**[Reporting-APIs](https://marketing.adobe.com/developer/get-started/introduction/c-introduction)**sollten verwendet werden, wenn die anderen Visualisierungsoptionen Ihren Anforderungen nicht gerecht werden. Die 3 API-Optionen umfassen:

* **Vollständig verarbeitet**: wenn Sie umfangreiche Daten (einschließlich Besuche, Besucher und Segmente) benötigen. Dies sind typische zusammengefasste Daten der Analytics-Benutzeroberfläche, die innerhalb von etwa 30-90 Minuten verfügbar sind. Kann über ReportBuilder verwendet werden.
* **Echtzeit**: wenn Sie einige Metriken und Dimensionen mit einer Wartezeit von Sekunden Ansicht haben möchten. Dies sind begrenzte, teilweise verarbeitete, zusammenfassende Daten, die innerhalb von etwa 30 Sekunden verfügbar sind. Umfasst eindeutige Algorithmen der beliebtesten, Gewinner und Verlierer. Kann über ReportBuilder verwendet werden.
* **[!UICONTROL Live Stream]**: wenn Sie einen Stream teilweise verarbeiteter Analytics-Daten auf Trefferebene innerhalb von Sekunden nach der Erfassung benötigen. Hierbei handelt es sich um teilweise verarbeitete Daten, die innerhalb von etwa 30 Sekunden verfügbar sind. Nur für Analytics Premium verfügbar. Erfordert eine Möglichkeit, die Daten zu visualisieren, in der Regel durch eine Interaktion mit Engineering Services.

## Individuelle Lösungen {#section_4A212F26A15947599DFB0399A0440CB6}

Engineering Services sollten in folgenden Fällen verwendet werden:

* Die anderen Adobe-Tools entsprechen nicht Ihren Anforderungen.
* Sie möchten ein benutzerdefiniertes Erlebnis.
* Sie wollen eine vollautomatisierte Lösung.
* Sie möchten viele Geräte erreichen.
* Sie haben mehrere Datenquellen.
* Sie haben komplexe Daten-ETL (Extract-Transform-Load) Anforderungen.
* Sie möchten ein benutzerdefiniertes Branding.
* Du willst visualisieren [!UICONTROL Analytics Live Stream].
