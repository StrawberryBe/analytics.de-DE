---
title: Auswirkungen an Benutzer kommunizieren
description: Erfahren Sie, wie Sie die Wirkung eines Ereignisses in Ihrem Unternehmen effektiv kommunizieren können.
translation-type: tm+mt
source-git-commit: 022d9cbfdae11d7efe1efb7fe503f4fdaa785be1

---


# Auswirkungen des Ereignisses auf Benutzer kommunizieren

Wenn Sie Daten haben, die von einem Ereignis [](overview.md)betroffen sind, ist es wichtig, dieses Ereignis den Benutzern in Ihrer Organisation mitzuteilen.

* Entwickeln Sie einen allgemeinen Haftungsausschluss, den Sie zur Konsistenz in der Kommunikation verwenden können.
* Fortlaufende Kommunikation mit Analytics-Benutzern und wichtigen Interessenvertretern während und nach dem Ereignis
* Fügen Sie eine Kalendererinnerung für nachfolgende Meilensteine ein, z. B. für den folgenden Monat oder das folgende Jahr. Diese Mitteilung in der Zukunft soll Benutzer, die Berichte anzeigen, daran erinnern, wie sich die Berichte über Monate oder über Jahre auswirken.

In Adobe Analytics gibt es in den folgenden Abschnitten verschiedene Möglichkeiten zur Kommunikation mit Benutzern in Ihrem Unternehmen. Sie können auch andere Methoden außerhalb von Adobe Analytics verwenden, z. B. E-Mail, um mit Benutzern zu kommunizieren.

## Kommunikation über Bedienfeld- oder Visualisierungsbeschreibungen

Wenn Sie ein Workspace-Projekt verwenden, das von Benutzern in Ihrem Unternehmen gemeinsam genutzt wird, können Sie die Auswirkungen eines Ereignisses über Bedienfeld- oder Visualisierungsbeschreibungen kommunizieren. Klicken Sie mit der rechten Maustaste auf einen Bereich oder eine Visualisierungskopfzeile und wählen Sie **[!UICONTROL Edit description]**.

![Bereichsbeschreibung](assets/panel_description.png)

## Kommunikation über Textvisualisierungen

Sie können die Auswirkungen eines Ereignisses auch über spezielle Textvisualisierungen kommunizieren. See [Text visualizations](/help/analyze/analysis-workspace/visualizations/text.md) in the Analyze user guide.

![Textvisualisierung](assets/text_visualization.png)

## Hinzufügen benutzerdefinierter Kalender-Ereignis zu Trends in Workspace

Für jede Trendvisualisierung in Workspace können Sie eine Reihe hinzufügen, die Ihren betroffenen Datumsbereich darstellt.

1. Erstellen Sie eine berechnete Metrik mit dem Segment &quot;Betroffene Tage&quot;, indem Sie bestimmte Daten in der Analyse [ausschließen](segments.md).
1. Hinzufügen Sie die gewünschte Metrik in die Arbeitsfläche für berechnete Metriken.

   ![Metrik](assets/calcmetric_event.png)

1. Hinzufügen einen Titel und eine Beschreibung, die die Benutzer über die Auswirkungen informieren. Sie können diese Metrik bei Bedarf auch als Kalenderanmerkung taggen.

   ![Titel und Beschreibung](assets/calcmetric_title_description.png)

1. Fügen Sie in einer Freiformtabelle die Dimension &quot;Tag&quot;hinzu. Hinzufügen Sie &quot;Besuche&quot;und Ihre berechnete Metrik als Spalten nebeneinander an.

   ![Freiformtabelle](assets/calcmetric_freeform.png)

1. Klicken Sie auf das Zahnradsymbol für die Spalteneinstellungen für die errechnete Metrik und aktivieren Sie **[!UICONTROL Interpret zero as no value]**.

   ![Einstellungen für berechnete Metriken](assets/calcmetric_zero_no_value.png)

1. Hinzufügen einer Linienvisualisierung. Betroffene Tage werden mit einer anderen Farbe dargestellt. Benutzer können auch auf das Symbol &quot;Info&quot;in der berechneten Metrik klicken, um weitere Informationen zu erhalten.

   ![Infosymbol](assets/calcmetric_infoicon.png)

## Kalendereinstellungen in Reports &amp; Analysen verwenden

Wenn Sie Reports &amp; Analysen verwenden, können Sie mithilfe eines [Kalenderberichts](/help/components/t-calendar-event.md) die betroffenen Ereignis in einem beliebigen Trendbericht hervorheben. Diese Methode gilt nicht für Analyse Workspace.

1. Navigieren Sie zu **[!UICONTROL Components]** > **[!UICONTROL Calendar events]**.
2. Geben Sie den gewünschten Titel, den Datumsbereich und den Notiztext ein.
3. Klicken Sie auf **[!UICONTROL Save]**.

![Kalender-Ereignis](assets/exclude_calendar_event.png)
