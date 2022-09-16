---
title: Auswirkungen an Benutzer kommunizieren
description: Erfahren Sie, wie Sie die Wirkung eines Ereignisses in Ihrer Organisation effektiv kommunizieren können.
exl-id: 9ba83f3f-2eea-44c2-80b2-a0a9111d51cf
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 3%

---

# Auswirkungen von Ereignissen an Benutzer kommunizieren

Wenn Sie Daten haben [von einem Ereignis beeinflusst](overview.md)ist es wichtig, dieses Ereignis Benutzern in Ihrer Organisation mitzuteilen.

* Entwickeln eines allgemeinen Haftungsausschlusses, den Sie für die Konsistenz in der Kommunikation verwenden können
* Bereitstellung laufender Kommunikation für Analytics-Benutzer und wichtige Interessengruppen während und nach der Veranstaltung
* Fügen Sie eine Kalendererinnerung für nachfolgende Meilensteine ein, z. B. für den folgenden Monat oder das folgende Jahr. Diese Mitteilung in der Zukunft hilft Benutzern, die Berichte anzeigen, daran zu erinnern, wie sich diese in Monatsberichten oder Jahresberichten auswirken.

Die folgenden Abschnitte in Adobe Analytics zeigen verschiedene Möglichkeiten, mit Benutzern in Ihrem Unternehmen zu kommunizieren. Sie können auch andere Methoden außerhalb von Adobe Analytics verwenden, z. B. E-Mail, um mit Benutzern zu kommunizieren.

## Kommunikation über Bedienfeld- oder Visualisierungsbeschreibungen

Wenn Sie ein Workspace-Projekt unter Benutzern in Ihrer Organisation freigegeben haben, können Sie die Auswirkungen eines Ereignisses über Bedienfeld- oder Visualisierungsbeschreibungen kommunizieren. Klicken Sie mit der rechten Maustaste auf einen Bereich oder eine Visualisierungsheader und wählen Sie **[!UICONTROL Beschreibung bearbeiten]**.

![Bedienfeldbeschreibung](assets/panel_description.png)

## Kommunikation über Textvisualisierungen

Sie können die Auswirkungen eines Ereignisses auch über spezielle Textvisualisierungen kommunizieren. Siehe [Textvisualisierungen](/help/analyze/analysis-workspace/visualizations/text.md) im Benutzerhandbuch zu Analysen.

![Textvisualisierung](assets/text_visualization.png)

## Hinzufügen benutzerdefinierter Kalenderereignisse zu Trends in Workspace

Für jede Trend-Visualisierung in Workspace können Sie eine Reihe hinzufügen, die Ihren betroffenen Datumsbereich darstellt.

1. Erstellen Sie eine berechnete Metrik mit dem Segment &quot;Betroffene Tage&quot;, indem Sie Folgendes ausführen [Ausschließen spezifischer Daten in der Analyse](segments.md).
1. Fügen Sie die gewünschte Metrik der Arbeitsfläche für berechnete Metriken hinzu.

   ![Metrik](assets/calcmetric_event.png)

1. Fügen Sie einen Titel und eine Beschreibung hinzu, die Benutzer über die Auswirkungen informieren. Sie können diese Metrik bei Bedarf auch als Kalenderanmerkung taggen.

   ![Titel und Beschreibung](assets/calcmetric_title_description.png)

1. Fügen Sie in einer Freiformtabelle die Dimension &quot;Tag&quot;hinzu. Fügen Sie &quot;Besuche&quot;und Ihre berechnete Metrik als Spalten nebeneinander hinzu.

   ![Freiformtabelle](assets/calcmetric_freeform.png)

1. Klicken Sie auf das Zahnradsymbol für die Spalteneinstellungen für die berechnete Metrik und aktivieren Sie **[!UICONTROL Null als keinen Wert auffassen]**.

   ![Einstellungen für berechnete Metriken](assets/calcmetric_zero_no_value.png)

1. Fügen Sie eine Linienvisualisierung hinzu. Betroffene Tage werden mit einer anderen Farbe dargestellt. Benutzer können auch auf das Symbol &quot;Info&quot;in der berechneten Metrik klicken, um weitere Informationen zu erhalten.

   ![Info-Symbol](assets/calcmetric_infoicon.png)

## Kalenderereignisse in Reports &amp; Analytics verwenden

Wenn Sie Reports &amp; Analytics verwenden, können Sie eine [Kalenderereignis](/help/components/t-calendar-event.md) , um die betroffenen Tage in allen Trendberichten hervorzuheben. Diese Methode gilt nicht für Analysis Workspace.

1. Navigieren Sie zu **[!UICONTROL Komponenten]** > **[!UICONTROL Alle Komponenten]** > **[!UICONTROL Kalenderereignisse]**.
2. Geben Sie den gewünschten Titel, den Datumsbereich und den Text für Anmerkungen ein.
3. Klicken Sie auf **[!UICONTROL Speichern]**.

![Kalenderereignis](assets/exclude_calendar_event.png)
