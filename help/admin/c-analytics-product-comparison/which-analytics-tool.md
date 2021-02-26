---
description: Diese Hilfeseite enthält empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Die Tools sollten in der Reihenfolge der Liste verwendet werden. Wenn ein bestimmtes Tool Ihren Anforderungen nicht gerecht wird, wählen Sie stattdessen das nächste in der Liste aus.
title: Welches Adobe Analytics-Tool sollte ich verwenden?
uuid: 1179e49d-3cfc-4abd-a8eb-35c5ae380c16
translation-type: tm+mt
source-git-commit: f2db5f611952ee315c84f925d038c539da110e38
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 100%

---


# Welches Adobe Analytics-Tool sollte ich verwenden?

Diese Hilfeseite enthält empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Die Tools sollten in der Reihenfolge der Liste verwendet werden. Wenn ein bestimmtes Tool Ihren Anforderungen nicht gerecht wird, wählen Sie stattdessen das nächste in der Liste aus.

Weitere Informationen zu Adobe Analytics-Produktvergleichen finden Sie  [hier](/help/admin/c-analytics-product-comparison/analytics-product-comparison.md).

## Adobe Analytics-Berichtsoberflächen {#user-interfaces}

**[Analysis Workspace](/help/analyze/analysis-workspace/home.md)** sollte die bevorzugte Benutzeroberfläche für alle Berichts- und Analyseaufgaben sein. Adobe investiert weiterhin in dieses Produkt und gibt monatlich Updates dafür heraus. Können Sie eine Aufgabe nicht mit Analysis Workspace durchführen, versuchen Sie eine der unten stehenden Oberflächen.**

**[Reports &amp; Analytics](/help/analyze/reports-analytics/overview/report-overview.md)** sollte verwendet werden:

* Von Einsteigern, die auf eine vorkonfigurierte Berichterstellung zugreifen müssen, in der einfacher navigiert werden kann.
* Für den Zugriff auf Echtzeitdaten in der Benutzeroberfläche
* Zum Einrichten von Kalenderereignissen
* Zum Einrichten von Zielen
* Zum Anzeigen von Bot-Berichten
* Für den Zugriff auf eindeutige Videovisualisierungen von Videotagesabschnitten und Zuschauerrückgängen.
* Zur Nutzung von Veröffentlichungslisten für terminierte Berichte

**[Data Workbench](https://docs.adobe.com/content/help/de-DE/data-workbench/using/home.html)** sollte verwendet werden:

* Als flexibelste Analyseoption (bis hin zur Analyse auf Besucher-/Trefferebene).
* Für die Erstellung eines Mehrkanal-Datensatzes der Online- und Offline-Interaktionen von CRM über POS bis Web.
* Für erweiterte Attribution (regelbasierte und Algorithmus-Modelle).
* Für prädiktive statistische Modellierung (Tendenzauswertung, Clustering, Korrelationen usw.).
* Für die Latenzanalyse (Zeit vor/seit einem Ereignis).
* Für die Identifikation und den Export komplexer Segmente in Adobe Experience Cloud.

## Importieren von Daten in Adobe Analytics   {#import}

**[Classifications](/help/components/classifications/c-classifications.md)** sollte verwendet werden:

* Wenn Metadaten vorliegen, die Sie einem Erfassungswert (eVar, prop, Marketingkanal) zuweisen möchten.
* Optionen:

   * Rule Builder: verwenden, wenn für eine Variable Werte in einem vorhersagbaren Format erfasst werden, z. B. durch Trennzeichen getrennte Werte. Mit diesem Ansatz können Sie Regeln einmal erstellen, ohne sich später weiter damit beschäftigen zu müssen.
   * Browser-Importtool: verwenden, wenn Sie nicht über vorhersagbare Werte oder über eine begrenzte Liste von Werten verfügen, die eine einmalige Aktualisierung erfordern. Bei diesem Ansatz ist eine fortlaufende Überwachung der Klassifizierungen auf neue Werte nötig.

**[Data Sources](/help/import/c-data-sources/datasrc-home.md)** sollte verwendet werden:

* Wenn Offline-Daten vorliegen, die dauerhaft in Adobe Analytics geschrieben werden sollen.
* Optionen:

   * Zusammenfassung: einfache Datenuploads nach Tag oder anhand von begrenzten Dimensionen.
   * Transaktions-ID: Datenuploads, die einen Online-Endpunkt mit Offlinedaten verknüpfen und importierte Daten vollständig einem online erstellten Besucher-Schnappschuss zuordnen (z. B. online abgeschlossene Bestellungen, die offline zurückgegeben werden).
   * Volle Verarbeitung: Datenquellen mit Zeitstempel, verarbeitet, als ob es sich dabei um einen von Adobe-Servern abgerufenen Treffer handeln würde. D. h. die Daten werden direkt in die Visitor Journey eingefügt.

**[Data Connectors](https://www.adobeexchange.com/experiencecloud.html)** sollten verwendet werden:

* Wenn Sie mit einem Drittanbieter interagieren, der eine unterstützte Schnittstelle für Adobe Analytics erstellt hat. Data Connectors übernimmt meist zusammengefasste Daten automatisch, dauerhaft und wiederholt in Adobe Analytics.

Die **[Data Insertion API](/help/import/c-data-insertion-api/c-data-insertion-api.md)** sollte verwendet werden:

* Wenn Sie Daten in Adobe Analytics laden und den Adobe AppMeasurement- oder mobilen SDK-Code nicht nutzen können.

**[Bulk-Dateneinfüge-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)**

* Die Data Insertion-API und Bulk Data Insertion-API sind beides Methoden, um Server-seitige Sammlungsdaten an Adobe Analytics zu senden. Aufrufe der Data Insertion-API erfolgen jeweils für ein Ereignis. Die Bulk Data Insertion-API akzeptiert Dateien mit Ereignisdaten im CSV-Format, wobei ein Ereignis pro Zeile angegeben wird. Wenn Sie an einer neuen Implementierung der Server-seitigen Sammlung arbeiten, empfehlen wir die Verwendung der Bulk Data Insertion-API.

**[Kundenattribute](https://docs.adobe.com/content/help/de-DE/core-services/interface/customer-attributes/attributes.html)** sollten verwendet werden:

* Wenn Sie Unternehmenskundendaten in einer Datenbank für Customer Relationship Management (CRM) speichern und die Daten in die Experience Cloud hochladen möchten.
* Wenn Sie CRM-Daten für tiefgreifende Analysen in Analytics oder als Targeting-Kriterien in Adobe Target verwenden möchten.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)** sollte verwendet werden:

* Wenn Sie Zielgruppendaten des Adobe Audience Manager (AAM) – wie beispielsweise demografische Daten (z. B. Geschlecht oder Verdienstniveau), psychografische Daten (z. B. Interessen und Hobbys), CRM-Daten oder Ad-Impression-Daten – in einen beliebigen Analytics-Workflow einbetten möchten.
* Wenn Sie möchten, dass hochgeladene CRM-Daten zeitbasiert sind, da diese Integration für jeden Treffer Daten an Analytics übermittelt.

## Exportieren von Daten aus Adobe Analytics   {#export}

**[Report Builder](/help/analyze/report-builder/home.md)** sollte verwendet werden:

* Wenn die individuellen Layoutoptionen von Workspace zu sehr einschränken (in Report Builder sind sämtliche Optionen möglich, die Excel bietet).
* Zur lockeren Verknüpfung von Benutzereingaben oder Offline-Datenquellen (Impressionen, Kosten) mit Adobe-Daten. Eine dauerhaftere Lösung für das Einbinden von Daten ist Data Sources (siehe „Importieren von Daten in Analytics“).
* Zum Zusammenführen von Daten aus verschiedenen dimensionalen Berichten (z. B. Kombination eines Berichts über Promo-Impressionen mit einem Bericht über den Klick-zu-Konversion-Verlauf bei einer Promo).
* Zum Zusammenführen von Daten aus verschiedenen Report Suites, entweder durch Zusammenfassen oder durch paralleles Anzeigen in derselben Tabelle.
* Wenn bei der Planung Automatisierung gewünscht wird (XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)** sollte verwendet werden:

* Für den Zugriff auf Variablen, die ansonsten in der Benutzeroberfläche verborgen sind: IP-Adresse, Experience Cloud ID, Analytics-Besucher-ID, Seiten-URL.
* Für den Zugriff auf granularere Daten als jene in der Benutzeroberfläche (denormalisierte Tabellenansicht).
* Für den Download von Daten in einem für die Pivot-Tabellen-Eingabe geeigneten Format.
* Wenn der Kunde Adobe-Daten in ein Drittanbieter-Tool für die Datenvisualisierung eingeben möchte (leicht zusammengefasst und nicht auf Trefferebene).
* Für den Zugriff auf alle eindeutigen Dimensionselemente, wenn in Adobe Analytics ein geringer Datenverkehr für Sie vorliegt.

**[Analytics-Daten-Feed](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)** sollte verwendet werden:

* Zur Nutzung des granularsten Daten-Feeds, der möglich ist (Besucher-ID, Treffer).
* Wenn der Kunde Adobe-Dateien in einer clientseitigen Datenbank und so granular wie möglich speichern möchte.
* Wenn der Kunde ein Business Intelligence-Tool entwickeln oder Adobe-Daten auf Trefferebene in ein Drittanbieter-Tool importieren möchte.

**[Reporting-APIs](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)** sollten verwendet werden, wenn die anderen Visualisierungsoptionen Ihren Anforderungen nicht gerecht werden. Die 3 API-Optionen sind:

* **Vollständig verarbeitet:** Wenn Sie umfangreiche Daten präsentieren möchten (einschließlich Besuchen, Besuchern und Segmenten). Dabei handelt es sich üblicherweise um in der Analytics-Benutzeroberfläche zusammengefasste Daten, die innerhalb von etwa 30–90 Minuten verfügbar sind. Die Verwendung ist überall im Report Builder möglich.
* **Echtzeit:** Wenn Sie einige Metriken und Dimensionen mit nur wenigen Sekunden Latenz anzeigen möchten. Hierbei handelt es sich um begrenzte, teilweise verarbeitete, zusammengefasste Daten, die innerhalb von etwa 30 Sekunden verfügbar sind. Umfasst eindeutige Algorithmen für die beliebtesten Elemente, Gewinner und Verlierer. Die Verwendung ist überall im Report Builder möglich.
* **[!UICONTROL Livestream]**: Wenn Sie einen Stream mit teilweise verarbeiteten Analytics-Daten auf Trefferebene innerhalb von Sekunden nach deren Erfassung benötigen. Hierbei handelt es sich um teilweise verarbeitete Daten, die innerhalb von etwa 30 Sekunden verfügbar sind. Nur für Analytics Premium verfügbar. Benötigt eine Option zur Visualisierung der Daten, üblicherweise mithilfe von Engineering Services.

## Individuelle Lösungen {#custom-solutions}

Engineering Services sollten in folgenden Fällen verwendet werden:

* Die anderen Adobe-Tools entsprechen nicht Ihren Anforderungen.
* Sie benötigen ein individuelles Erlebnis.
* Sie benötigen eine vollständig automatisierte Lösung.
* Sie möchten viele Geräte erreichen.
* Sie verfügen über mehrere Datenquellen.
* Sie haben komplizierte Daten-ETL-Anforderungen (Anforderungen für Extraktion, Transformation und Laden).
* Sie benötigen individuelles Branding.
* Sie möchten [!UICONTROL Analytics-Live-Stream] visualisieren.
