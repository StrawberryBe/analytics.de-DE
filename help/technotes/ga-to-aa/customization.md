---
title: Berichtsanpassung in Adobe Analytics
description: Erfahren Sie, wie Sie Berichte in Adobe Analytics anpassen können.
translation-type: tm+mt
source-git-commit: 6fc8145d9a94427ec942d55776b6029f7dd6f79c
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 78%

---


# Berichte anpassen

Auf Plattformen von Drittanbietern wie Google Analytics stehen verschiedene Anpassungsoptionen zur Verfügung. Mit diesen Anpassungen können Anwender Dashboards, benutzerspezifische Berichte, gespeicherte Berichte und benutzerdefinierte Warnungen erstellen. Da Analysis Workspace seinen Anwendern das Erstellen von Berichten auf einer leeren Arbeitsfläche ermöglicht, sind die meisten Anpassungen direkt in das Tool integriert.

Diese Seite geht davon aus, dass der Benutzer über grundlegende Kenntnisse in der Verwendung von [!UICONTROL Analysis Workspace] verfügt. Siehe [Basisbericht in Analysis Workspace für GA-Anwender erstellen](reports/create-report.md), wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Dashboards

Die [!UICONTROL Analysis Workspace]-Architektur ist ähnlich wie das Konzept der Dashboard-Widgets aufgebaut. Projekte in [!UICONTROL Analysis Workspace] sind ungefähr äquivalent zu Dashboards in Google Analytics. Visualisierungen in [!UICONTROL Analysis Workspace] sind die ungefähr äquivalente Entsprechung von Widgets in Google Analytics.

### Hinzufügen von Inhalten zu einem Projekt

1. Klicken Sie auf das Symbol [!UICONTROL Visualisierungen] links und ziehen Sie die gewünschte Visualisierung in den Arbeitsbereich.
2. Klicken Sie auf das Symbol [!UICONTROL Komponenten] links und ziehen Sie die gewünschten Dimensionen und Metriken in die Visualisierung, um sie mit Daten zu füllen.
3. Verschieben Sie die Kanten der Visualisierung, um die Größe zu ändern, und ziehen Sie den Titel der Visualisierung, um sie zu verschieben.

Alle Google Analytics-Widgets stehen unter [!UICONTROL Analysis Workspace] zur Verfügung:

* Das **Metrik-Widget** entspricht ungefähr der Visualisierung der Zusammenfassungsnummer.
* Das **Timeline-Widget** entspricht ungefähr der Linienvisualisierung.
* Das **Geomap-Widget** entspricht ungefähr der Kartenvisualisierung.
* Das **Tabellen-Widget** entspricht ungefähr der Freiformtabellen-Visualisierung.
* Das **Kreis-Widget** entspricht ungefähr der Ringvisualisierung.
* Das **Balken-Widget** entspricht ungefähr der Balkenvisualisierung.

[!UICONTROL Analysis Workspace enthält viele weitere Visualisierungsoptionen, um die Daten so darzustellen, wie es für Ihre Berichtsanforderungen am besten geeignet ist. ] Weitere Informationen finden Sie unter [Visualisierungen in Analysis Workspace](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) im Benutzerhandbuch zu Analysen.

### Freigeben von Projekten

Nachdem Sie die Inhalte zu einem Projekt hinzugefügt haben, können Sie es freigeben.

* Um das Projekt für Ihre Kollegen freizugeben, gehen Sie zu **[!UICONTROL Freigeben > Projekt freigeben]**. Empfänger sind andere Anwender in Ihrer Organisation mit Adobe Analytics-Konten.
* Um Ihr Projekt über einen Link freizugeben, gehen Sie zu **[!UICONTROL Freigeben > Projektlink abrufen]**. Beachten Sie, dass hierfür in Ihrem Unternehmen weiterhin eine Anmeldung bei Adobe Analytics erforderlich ist.

### Exportieren von Projekten

Zusätzlich zu PDF führt [!UICONTROL Analysis Workspace] einen CSV-Export durch.

1. Klicken Sie auf *[!UICONTROL Freigeben]* > *[!UICONTROL Datei jetzt senden]*, um ein modales Fenster zu öffnen.
2. Geben Sie den Dateityp und die Empfänger an.
3. Klicken Sie auf [!UICONTROL Jetzt senden].

## Benutzerspezifische Berichte

Beim Erstellen eines benutzerspezifischen Berichts in Google Analytics ähneln die erforderlichen Felder dem Workflow beim Erstellen einer Visualisierung in Workspace. Dimensions-, Metrik- und Filterdefinitionen der beiden Plattformen sind sich ähnlich. In Analysis Workspace werden Dimensionen und Metriken nicht aus einer Liste ausgewählt, sondern in eine Freiformtabelle gezogen.

### Berechnete Metriken in benutzerspezifischen Berichten

Benutzerspezifische Berichte sind einer der wenigen Bereiche in Google Analytics, in denen berechnete Metriken verwendet werden können. Da Analysis Workspace wie eine Arbeitsfläche funktioniert, funktionieren berechnete Metriken rückwirkend und in jedem Kontext.

So erstellen Sie eine errechnete Metrik:

1. Klicken Sie auf das Symbol **+**[!UICONTROL  neben der Metrikliste, um den Generator für berechnete Metriken zu öffnen].
2. Geben Sie für die berechnete Metrik einen Namen und ein Format an.
3. Ziehen Sie Metrikkomponenten in den Definitionsbereich und verwenden Sie die Dropdown-Listen zwischen den einzelnen Komponenten, um einen Operator zu bestimmen.
4. Sobald die berechnete Metrik die gewünschte Formel enthält, klicken Sie auf „Speichern“, um zu Ihrem Arbeitsbereich zurückzukehren.
5. Ziehen Sie die neu definierte berechnete Metrik in den Arbeitsbereich.

   Weitere Informationen zu [berechneten Metriken](/help/components/c-calcmetrics/cm-overview.md) finden Sie im Benutzerhandbuch zu Komponenten.

## Benutzerspezifische Warnungen

Warnungen sind auf beiden Plattformen verfügbar. Verwenden Sie in Adobe Analytics das Navigationsmenü in der Kopfzeile und gehen Sie zu *[!UICONTROL Komponenten]* > *[!UICONTROL Warnhinweise]*. Weitere Informationen finden Sie unter [Intelligente Warnungen](/help/components/c-alerts/intellligent-alerts.md) im Benutzerhandbuch zu Komponenten.
