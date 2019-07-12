---
title: Zielgruppenberichte in Adobe Analytics
description: Erfahren Sie, wie Sie mit dem Analysis Workspace zielgruppenbasierte Berichte erstellen.
translation-type: tm+mt
source-git-commit: 71899840dd5b401c6892b6ad5088d4a32fd07042

---


# Zielgruppenberichte

Zielgruppenberichte zeigen Informationen zu den Typen der Personen an, die Ihre Site besuchen.

Diese Seite geht davon aus, dass der Benutzer über grundlegende Kenntnisse zur Verwendung des Analysis Workspace verfügt. See [Create a basic report in Analysis Workspace for Google Analytics users](create-report.md) if you are not yet familiar with the tool in Adobe Analytics.

## Aktive Benutzer

Aktive Benutzer zeigen die Gesamtzahl der Benutzer auf Ihrer Site in den vorherigen, siebten, 14 oder 28 Tagen an. Obwohl Adobe nicht über die genaue Berechnung in Google Analytics verfügt, können Sie die Metrik &quot;Unique Visitors&quot; verwenden, um eine deduplizierte Anzahl von Benutzern auf Ihrer Site basierend auf dem ausgewählten Datumsbereich zu sehen.

So erhalten Sie ein Liniendiagramm mit individuellen Besuchern:

1. Klicken Sie auf das Symbol Visualisierungen links und ziehen Sie die Linienvisualisierung auf den Arbeitsbereich oberhalb der leeren Freiform-Tabelle.
2. Click the Components icon on the left, then drag the **Unique Visitors** metric into the smaller space labeled &#39;Drop a Metric here&#39;.
3. If different granularity is desired, drag the desired date range (e.g. **Day**, **Week**, **Month**, etc.) über dem vorhandenen Datumsüberschriften-Header.

See [Unique Visitors](../../../components/c-variables/c-metrics/metrics-unique-visitors.md) in the Components user guide for details on how Adobe calculates unique visitors.

## Lebenszeitwert

Lebenszeitwert ist eine Funktion, die für beide Plattformen zusätzliche spezialisierte Implementierungen erfordert. Adobe empfiehlt die Zusammenarbeit mit einem Implementierungsberater, um diese Daten abzurufen.

## Kohortenanalyse

Die Kohortenanalyse zeigt an, wie oft dieselben Benutzer zu Ihrer Site zurückkehren.

So erstellen Sie eine Kohortentabelle:

1. Klicken Sie auf das Symbol Visualisierung links und ziehen Sie die Kohortentabellenvisualisierung auf die Arbeitsfläche.
2. Click the Components icon on the left, then drag the **Visits** metric onto both the Inclusion Criteria and Return Criteria.
3. Klicken Sie auf Erstellen.

See [Cohort Analysis](../../../analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) in the Analysis Workspace user guide for details on additional customizations to the cohort visualization.

## Zielgruppen

Für den Zielgruppenbericht in Google Analytics ist die Einrichtung von Zielgruppen erforderlich. Zielgruppen erfordern außerdem die Konfiguration in Adobe über Adobe Audience Manager. Weitere Informationen finden Sie im Benutzerhandbuch zu Audience Manager.

## Benutzer-Explorer

Der Benutzerexplorer-Bericht ermöglicht es Analysten, einzelne Besuche über anonymierte ids anzuzeigen. Adobe nimmt die Backend-Bezeichner außerhalb von Datenfeeds nicht auf, die Rohdatenexporte auf Trefferebene darstellen.

* Wenn diese Daten im Analysis Workspace gewünscht werden, ist es möglich, mit einem Implementierungsberater zusammenzuarbeiten, um den anonymen Cookie-Cookie-Wert in eine evar zu übergeben. Beachten Sie, dass dies nur bei kleineren Implementierungen möglich ist, die aus weniger als 1 Million individuellen Besuchern pro Monat bestehen.
* If this data is desired within data feeds, the concatenated columns `visid_high` and `visid_low` are the most common way to identify unique visitors. Learn more about [Data Feeds](../../../export/analytics-data-feed/c-getstarted/data-feed-overview.md) in the Export user guide.

## Berichte zu demografischen und Interessensgebieten

Demografische Daten und Interessensdaten liefern Informationen über Alter, Geschlecht und Interessen von Site-Benutzern. Diese Daten werden von Google über ihre Site-übergreifenden Verfolgungsfähigkeiten erfasst.

Demografische und Interessensdaten werden nicht automatisch von Adobe erfasst. Wenn Ihr Unternehmen diese Daten jedoch abruft, können Sie Kundenattribute verwenden, eine Funktion auf der Adobe Experience Cloud-Plattform. Sie ermöglicht die vollständige Kontrolle über die Organisation von Daten nach Attributen und ist nicht nur auf demografische Elemente oder Interessen beschränkt.

Weitere Informationen finden Sie in der Hilfe zu Kundenattributen.

## Geo - Sprache

Der Geo-Sprachenbericht zeigt den Site-Traffic nach der Spracheinstellung im Browser des Besuchers an.

So erstellen Sie einen Sprachenbericht:

1. In the Components menu, locate the **Language** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Language](../../../components/c-variables/dimensionslist/reports-languages.md) dimension in the Components user guide for more information.

## Geo - Standort

Der geografische Standort-Bericht bietet eine weltweltliche Kartenansicht, die Daten nach Land unterteilt.

So erstellen Sie einen geografischen Standort-Bericht:

1. Klicken Sie auf das Symbol Visualisierungen links und ziehen Sie die Map-Visualisierung auf den Arbeitsbereich oberhalb der leeren Freiform-Tabelle.
2. Click the Components icon on the left, then drag the **Unique Visitors** metric into the space labeled &#39;Add Metric&#39;.
3. Klicken Sie auf Erstellen.

Wenn die Tabelle zusätzlich zur Map ebenfalls gewünscht wird:

1. In the Components menu, locate the **Countries** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See [Geosegmentation](../../../components/c-variables/dimensionslist/reports-geosegmentation.md) dimensions in the Components user guide for more information.

## Verhalten - neue im Vergleich zu zurückkehrenden

Der neue und zurückkehrende Bericht bietet eine vereinfachte Ansicht der ersten Sitzungen (neue Besuche) und nachfolgende Sitzungen (rückkehrende Besuche).

So erstellen Sie einen neuen und rückkehrenden Besuchsbericht:

1. In the components menu, locate the **First Time Visits** segment and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;. Note that **First Time Visits** is a segment, while Workspace typically uses dimensions to represent rows.
2. Locate the **Return Visits** segment and drag it on top of the Segments row header. Dadurch wird das Segment als Dimension unterhalb der Erstbesuche hinzugefügt, was einen einfachen Vergleich ermöglicht.
3. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

Wenn ein Liniendiagramm ebenfalls gewünscht wird:

1. Klicken Sie links auf das Visualisierungssymbol und ziehen Sie eine Linienvisualisierung auf den Arbeitsbereich oberhalb der Freiformtabelle.
2. Klicken Sie bei gedrückter Strg-Taste (Windows) bzw. Befehlstaste (Mac) auf jede Zeile in der Freiform-Tabelle, um sie zu markieren. Dadurch können beide Trends in der Visualisierung angezeigt werden.
3. Klicken Sie auf den kleinen runden Punkt in der oberen linken Ecke der Linienvisualisierung und klicken Sie dann auf das Kontrollkästchen &quot;Auswahl sperren&quot; .

## Verhalten - Häufigkeit und Neuigkeit

The frequency &amp; recency report is approximately equal to the **Visit Number** dimension in Analysis Workspace.

1. In the components menu, locate the **Visit Number** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Visit Number](../../../components/c-variables/dimensionslist/reports-visitor-number.md) dimension in the Components user guide for more information.

## Verhalten - Interaktion

The engagement report is approximately equal to the **Time Spent per Visit - Bucketed** dimension.

1. In the components menu, locate the **Time Spent per Visit - Bucketed** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Time Spent per Visit](../../../components/c-variables/dimensionslist/reports-time-spent-per-visit.md) dimension in the Components user guide for more information.

## Technologie - Browser und Betriebssystem

Im Browser- und Betriebssystembericht sind mehrere primäre Dimensionen verfügbar.

* The **Browser** primary dimension is also available in Analysis Workspace as a dimension.
* The **Operating System** primary dimension is also available in Analysis Workspace as a dimension.
* The **Screen Resolution** primary dimension is available in Analysis Workspace as the **Monitor Resolution** dimension.
* The **Screen Colors** primary dimension is available in Analysis Workspace as the **Color Depth** dimension.
* The **Flash Version** primary dimension is not available in Adobe Analytics, however this data can be collected by an eVar if wanted.

1. Suchen Sie im Komponentenmenü die gewünschte Dimension oben und ziehen Sie sie auf den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot; .
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

Weitere Informationen zu ihrer jeweiligen Dimension finden Sie auf den folgenden Seiten im Benutzerhandbuch für Komponenten:

* [Browser](../../../components/c-variables/dimensionslist/reports-browsers.md)
* [Betriebssystem](../../../components/c-variables/dimensionslist/reports-operating-system.md)
* [Bildschirmauflösung](../../../components/c-variables/dimensionslist/reports-technology.md)
* [Farbtiefe](../../../components/c-variables/dimensionslist/reports-color-depth.md)

## Technologie - Netzwerk

The network report is approximately equal to the **Domain** dimension.

1. In the components menu, locate the **Domain** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Domain](../../../components/c-variables/dimensionslist/reports-domains.md) dimension in the Components user guide for more information.

## Mobil - Übersicht

The mobile overview report is approximately equal to the **Mobile Device Type** dimension. Beachten Sie, dass der Wert &quot;Sonstige&quot; dem Desktop-Traffic entspricht.

1. In the components menu, locate the **Mobile Device Type** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Mobile Device Type](../../../components/c-variables/dimensionslist/reports-device-types.md) dimension in the Components user guide for more information.

## Mobil - Geräte

The mobile devices report is approximately equal to the **Mobile Device** dimension.

1. In the components menu, locate the **Mobile Device** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Mobile Device](../../../components/c-variables/dimensionslist/reports-devices.md) dimension in the Components user guide for more information.

## Benutzerspezifisch

Benutzerspezifische Berichte werden pro Implementierung definiert. Arbeiten Sie mit dem Analytics-Administrator und/oder Implementation Consultant Ihres Unternehmens zusammen, um diese Berichte zu interpretieren. Typically an organization maintains a [Solution Design Document](../../../implement/prepare/solution-design.md) to keep track of custom variable values and how they are populated.

## Benchmarking

Anhand von Vergleichsberichten können Sie erkennen, wie Facetten Ihrer Daten im Vergleich zu den Durchschnittswerten der Branche stehen. Adobe gibt derzeit keine Vergleichsdaten zwischen seinen Kunden frei.

## Benutzerfluss

Der Flussbericht ist auf beiden Plattformen verfügbar. So erstellen Sie einen Flussbericht:

1. Klicken Sie links auf das Visualisierungssymbol und ziehen Sie eine Flussvisualisierung auf den Arbeitsbereich oberhalb der Freiformtabelle.
2. Locate the **Pages** dimension, then click the Arrow icon to reveal page values. Dimensionswerte sind gelb farbig.
3. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den Bereich mit der Bezeichnung &quot;Dimension oder Element&quot; in der Mitte.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um die Flüsse auf die nachfolgenden oder vorherigen Seiten zu erweitern. Verwenden Sie das Rechtsklick-Menü, um Spalten zu erweitern oder zu minimieren. Innerhalb desselben Flussberichts können auch unterschiedliche Dimensionen verwendet werden.
