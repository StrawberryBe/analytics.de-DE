---
title: Berichtanpassung in Adobe Analytics
description: Informationen zum Anpassen von Berichten in Adobe Analytics
translation-type: tm+mt
source-git-commit: a5f612ba5e8446a56bc2bd252a8781e8ab1de403

---


# Berichte anpassen

Bei Plattformen von Drittanbietern, wie Google Analytics, stehen verschiedene Anpassungsoptionen zur Verfügung. Diese Anpassungen ermöglichen es einem Benutzer, Dashboards, benutzerspezifische Berichte, gespeicherte Berichte und benutzerdefinierte Warnungen zu erstellen. Da der Analysis Workspace Benutzern das Erstellen von Berichten aus einer leeren Arbeitsfläche erlaubt, werden die meisten Anpassungen direkt in das Tool integriert.

Diese Seite geht davon aus, dass der Benutzer über grundlegende Kenntnisse zur Verwendung des Analysis Workspace verfügt. See [Create a basic report in Analysis Workspace for Google Analytics users](reports/create-report.md) if you are not yet familiar with the tool in Adobe Analytics.

## Dashboards

Die Architektur des Analysis Workspace ähnelt dem Konzept der Dashboard-Widgets. Projekte im Analysis Workspace sind die gleichen wie Dashboards in Google Analytics. Visualisierungen im Analysis Workspace sind die ungefähren Entsprechungen für Widgets in Google Analytics.

### Hinzufügen von Inhalten zu einem Projekt

1. Klicken Sie auf das Symbol Visualisierungen links und ziehen Sie die gewünschte Visualisierung auf die Arbeitsfläche.
2. Klicken Sie links auf das Symbol Komponenten und ziehen Sie die gewünschten Dimensionen und Metriken auf die Visualisierung, um sie mit Daten zu füllen.
3. Ziehen Sie die Kanten der Visualisierung, um sie zu ändern, und ziehen Sie den Titel der Visualisierung, um sie zu verschieben.

Alle Google Analytics-Widgets sind im Analysis Workspace verfügbar:

* The **Metric widget** is approximately equal to the Summary Number visualization.
* The **Timeline widget** is approximately equal to the Line visualization.
* The **Geomap widget** is approximately equal to the Map visualization.
* The **Table widget** is approximately equal to the Freeform Table visualization.
* The **Pie widget** is approximately equal to the Donut visualization.
* The **Bar widget** is approximately equal to the Bar visualization.

Der Analysis Workspace enthält viele weitere Visualisierungsoptionen, um Daten so zu präsentieren, dass sie Ihren Berichtsanforderungen optimal entsprechen. See [Visualizations in Analysis Workspace](../../analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) in the Analyze User Guide for more information.

### Freigeben von Projekten

Sobald Sie dem Projekt Inhalt hinzugefügt haben, können Sie ihn freigeben.

* Um das Projekt für Ihre Kollegen freizugeben, gehen Sie zum Freigeben &gt; Projekt freigeben. Empfänger sind andere Benutzer in Ihrem Unternehmen, die über Adobe Analytics-Konten verfügen.
* Um Ihr Projekt über einen Link freizugeben, wählen Sie "Freigeben" &gt;" Projektverknüpfung abrufen" . Beachten Sie, dass in Ihrem Unternehmen noch eine Anmeldung bei Adobe Analytics erforderlich ist.

### Exportieren von Projekten

Zusätzlich zu PDF bietet Analysis Workspace einen CSV-Export.

1. Click *[!UICONTROL Share]* &gt; *[!UICONTROL Send File Now]*, which opens a modal window.
2. Geben Sie den Dateityp und die Empfänger an.
3. Click [!UICONTROL Send Now].

## Benutzerspezifische Berichte

Beim Erstellen eines benutzerspezifischen Berichts in Google Analytics sind die erforderlichen Felder ähnlich wie der Arbeitsablauf beim Erstellen einer Visualisierung im Arbeitsbereich. Dimensionen, Metriken und Filterdefinitionen sind zwischen Plattformen ähnlich. Anstatt Dimensionen und Metriken aus einer Liste auszuwählen, werden Dimensionen und Metriken in Analysis Workspace in eine Freiform-Tabelle gezogen.

### Berechnete Metriken in benutzerspezifischen Berichten

Benutzerspezifische Berichte sind eines der wenigen Bereiche in Google Analytics, die die Verwendung berechneter Metriken ermöglichen. Da Analysis Workspace wie eine Arbeitsfläche funktioniert, funktionieren berechnete Metriken rückwirkend und in jedem beliebigen Kontext.

So erstellen Sie eine errechnete Metrik:

1. Click the **+** icon near the metric list to open the Calculated Metric Builder.
2. Geben Sie Ihrer errechneten Metrik einen Namen und geben Sie ein Format an.
3. Ziehen Sie Metrikkomponenten in den Definitionsbereich und verwenden Sie die Dropdown-Listen zwischen den einzelnen Komponenten, um einen Operator zu bestimmen.
4. Sobald die berechnete Metrik die gewünschte Formel enthält, klicken Sie auf Speichern, um zu Ihrer Arbeitsfläche zurückzukehren.
5. Ziehen Sie die neu definierte berechnete Metrik auf die Arbeitsfläche.

   Learn more about [Calculated Metrics](../../components/c-variables/c-metrics/calculated-metric.md) in the Components user guide.

## Benutzerspezifische Warnhinweise

Warnungen sind auf beiden Plattformen verfügbar. In Adobe Analytics, use the header navigation menu and go to *[!UICONTROL Components]* &gt; *[!UICONTROL Alerts]*. See [Intelligent Alerts](../../components/c-alerts/intellligent-alerts.md) in the Components User Guide for more information.
