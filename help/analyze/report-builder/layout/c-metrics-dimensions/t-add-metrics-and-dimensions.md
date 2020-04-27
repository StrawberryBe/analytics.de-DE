---
description: Schritte zum Hinzufügen von Metriken und Dimensionen zu einer Anforderung.
title: Metriken und Dimensionen hinzufügen
topic: Report builder
uuid: 588ce96b-3a2d-42b7-8a8e-7e6f448a0115
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Metriken und Dimensionen hinzufügen

Schritte zum Hinzufügen von Metriken und Dimensionen zu einer Anforderung.

1. [Erstellen Sie die Datenanforderung](/help/analyze/report-builder/data-requests/data-requests.md) auf der [!UICONTROL Request Wizard: Step 1]und klicken Sie auf **[!UICONTROL Next]**.
1. On the [!UICONTROL Request Wizard: Step 2], double-click metrics, or drag them to the desired position.

   ![Schritt-Info](assets/adding_metrics.png)

   When you add metrics, they are not removed from the [!UICONTROL Metrics] tab, because you can display metrics multiple times within a request. Beispielsweise kann die Zwischensumme einer Metrik neben jedem Wert angezeigt werden. Allerdings ändert sich die Liste der verfügbaren Metriken jedes Mal, wenn Sie eine Dimension hinzufügen oder entfernen.

   You can add only metrics to the [!UICONTROL Metrics] layout section. Metriken werden dem [!UICONTROL Column Label] Layout als [!UICONTROL Metric Header]. If you move a [!UICONTROL Metric Header] from [!UICONTROL Column Layout] to [!UICONTROL Row Layout], it is displayed there and is used as a metric as a breakdown.

   Beachten Sie, dass auf der Registerkarte „Metriken“ direkt über der Metrikenliste eine Suchleiste angezeigt wird.

   ![](assets/search_bar_metric.png)

   Beachten Sie:

   * Wenn Sie einen Suchbegriff eingeben, wird die Liste automatisch aktualisiert und es werden nur die Metriken angezeigt, deren Kennzeichnungen mit dem Suchbegriff übereinstimmen.
   * Die Treffer sind nicht von der Schreibweise abhängig. Sie entspricht einer Suche mit der Option „enthält“.
   * Suchen nach vollständigen Wörtern oder anderen speziellen Suchoptionen (beginnt mit, endet mit, UND, ODER usw.) werden nicht unterstützt.

      Der Suchbegriff wird gelöscht, wenn Sie den Anforderungs-Assistenten verlassen (z. B. durch Klicken auf „Beenden“ oder „Abbrechen“), Sie zu Schritt 1 des Anforderungs-Assistenten zurückkehren oder Sie die Metrikkategorie ändern.

      Der Suchbegriff wird in den folgenden Fällen nicht gelöscht:

   * Sie fügen ein Metrikelement aus der Liste per Drag-and-drop (oder Doppelklick) zum Metrikfeld „Pivot-Layout/Benutzerdefiniertes Layout“ hinzu.
   * Sie entfernen ein Metrikelement aus dem Metrikfeld „Pivot-Layout/Benutzerdefiniertes Layout“.
   * Sie klicken auf die Registerkarte „Dimension“ und kehren dann zur Registerkarte „Metrik“ zurück.
   * Sie rufen andere Unterformulare auf (modal oder amodal), bei denen Sie, wenn Sie sie verlassen, zu Schritt 2 des Anforderungs-Assistenten zurückkehren. Beispiele für diese Formulare:

      * Formulare für Dimensionsfilter
      * Formulare für die Datumsbereichformatierung
      * Formulare für Formatoptionen
      * Formulare für das Voranstellen/Anhängen von Text
      * Formulare für das Festlegen des Ausgabebereichs

1. (Optional) Um eine Anforderung nach Metrik zu sortieren, klicken Sie einfach auf die Metrikbezeichnung.
1. Dimensionen werden auf die gleiche Weise wie Metriken hinzugefügt.

On the [!UICONTROL Dimensions] tab, the system displays dimensions that break down or are a classification of any base report you select on Step 1, and on the configuration of the report suite. Wenn Sie eine Dimension auf dem Layoutraster ablegen, wird sie aus der Strukturansicht entfernt und eine Neuberechnung der Liste der verfügbaren Dimensionen durchgeführt.

The [!UICONTROL Date] dimension is added automatically. Available date dimensions change depending on the selected granularity from the [!UICONTROL Request Wizard: Step 1]. (Gültige Werte sind:

    * Stunde
    * Tag
    * Woche
    * Monat
    * Jahr
    * Datumsbereich (wenn keine Granularität angegeben ist)

1. Ändern Sie Metriken und Dimensionen, indem Sie [Formatoptionen](/help/analyze/report-builder/layout/t-format-display-headers.md) und Filter konfigurieren.
1. Klicken Sie auf **[!UICONTROL Finish]**.
In the following example, dimensions relate to the [!UICONTROL Page] metric. Hier erstellt die [!UICONTROL Referring Domain] Dimension einen Unterteilungsbericht zwischen [!UICONTROL Page] und [!UICONTROL Referring Domain]. Die Registerkarte [!UICONTROL Dimension] wird nur mit Dimensionen aktualisiert, die für einen Detailbericht verwenden können.

![](assets/page_pageview_02.png)
