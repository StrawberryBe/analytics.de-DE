---
description: 'null'
title: Ausführen einer Beitragsanalyse
uuid: 5282a5f9-0771-4974-93cb-335204bde114
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Ausführen einer Beitragsanalyse

Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. Damit soll dem Benutzer geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysieren viel schneller zu identifizieren.

## Ausführen einer Beitragsanalyse {#section_7D2C5E48A5664727941DF4C90976D9DC}

Es gibt zwei Möglichkeiten, die Beitragsanalyse in einem Projekt aufzurufen:

* In a freeform table with daily granularity, right-click any row and select **[!UICONTROL Run Contribution Analysis]**. Sie können die Analyse sogar für Zeilen durchführen, die nicht als anormal gekennzeichnet sind.

   >[!NOTE]
   >
   >Hinweis: Beitragsanalyse wird derzeit nur mit täglicher Granularität unterstützt.

   ![](assets/run_ca.png)

* Zeigen Sie in einem Liniendiagramm auf einen anomalen Datenpunkt im Diagramm. Click the **[!UICONTROL Analyze]** link that appears.

   ![](assets/contribution-analysis.png)

1. (Optional) After you have clicked **[!UICONTROL Run Contribution Analysis]** in either the line chart or a table, you can narrow the scope of (and thus speed up) the analysis by [excluding dimensions](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/run-contribution-analysis.md#section_F6932F4BF74544B5872164E7B1E0C6FC).

1. Warten Sie, während Ihre Beitragsanalyse geladen wird. Dieser Vorgang kann je nach der Größe Ihrer Report Suite und der Anzahl Ihrer Dimensionen einige Zeit in Anspruch nehmen. Die Beitragsanalyse erfolgt anhand der obersten 50.000 Elemente pro Dimension.
1. Anschließend lädt der Analysis Workspace ein neues Beitragsanalyse-Bedienfeld direkt in dieses Projekt. Wenn Sie die Beitragsanalyse schon früher in Reports &amp; Analytics genutzt haben, werden Ihnen etliche Bereiche vertraut vorkommen:

   * Eine Visualisierung, die die Anzahl der **Besuche** an diesem Tag anzeigt.
   * Eine monatliche **Besuchstrendlinie** für den Kontext.
   * **Oberste Elemente**, die zu dieser Anomalie beigetragen haben, sortiert nach der [Beitragsbewertung](https://marketing.adobe.com/resources/help/de_DE/analytics/contribution/ca_contribution_score.html), plus der fraglichen Metrik, und eine Metrik namens Unique Visitors, um die Metrik hinsichtlich der Größe in einen Kontext zu setzen.

   * Die Tabelle [Generierte Segmente](https://marketing.adobe.com/resources/help/de_DE/analytics/contribution/ca_workflow_premium.html) (Wichtigste Element-Cluster) gibt die Zugehörigkeiten der obersten Elemente basierend auf der Beitragsbewertung, den ungewöhnlichen Vorkommen und dem gesamten prozentualen Beitrag zu der anormalen Metrik an. Dies wird dann als Zielgruppensegment (Beitragssegment 1, Beitragssegment 2 usw.) erfasst. Wenn Sie auf die Infoschaltfläche („i“) klicken, sehen Sie eine Ansicht mit der Definition des jeweiligen Segments inklusive der obersten Elemente, aus denen dieses besteht:

      ![](assets/auto_segment.png)

1. Da die Beitragsanalyse nun Bestandteil des Analysis Workspace ist, haben Sie über das Kontextmenü einer Tabelle Zugriff auf eine Reihe zugehöriger Funktionen, mit denen Sie Ihre Analysen noch aussagekräftiger gestalten können, beispielsweise:

   * [Aufschlüsseln der einzelnen Dimensionselemente nach einer anderen Dimension](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)
   * [Anzeigen von Trends für mindestens eine Zeile](/help/analyze/analysis-workspace/analysis-workspace-features.md#section_34930C967C104C2B9092BA8DCF2BF81A)
   * [Hinzufügen neuer Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)
   * [Erstellen von Warnhinweisen](/help/components/c-alerts/intellligent-alerts.md)
   * [Erstellen oder Vergleichen von Segmenten](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

>[!NOTE] Hinweis: Die analysierte Anomalie wird durch einen blauen Punkt in der Beitragsanalyse und in den verknüpften intelligenten Benachrichtigungsprojekten markiert. Dadurch ist die gerade analysierte Anomalie leichter zu erkennen.

## Ausschluss von Dimensionen aus einer Beitragsanalyse {#section_F6932F4BF74544B5872164E7B1E0C6FC}

Es kann von Zeit zu Zeit erforderlich sein, einige Dimensionen bei der Beitragsanalyse auszuschließen. Hier ein Beispiel: Sie sind nicht an Dimensionen interessiert, die mit Browsern oder Hardware in Zusammenhang stehen, und möchten die Analyse beschleunigen, indem Sie die entsprechenden Dimensionen entfernen.

1. Nachdem Sie auf **[!UICONTROL Run Contribution Analysis]** (oder **[!UICONTROL Analyze]** in einem Liniendiagramm) geklickt haben, wird das **[!UICONTROL Excluded Dimensions]** Bedienfeld angezeigt.

1. Ziehen Sie einfach alle unerwünschten Dimensionen in das **[!UICONTROL Excluded Dimensions]** Bedienfeld und speichern Sie die Liste, indem Sie auf **[!UICONTROL Set as Default]**. Or, click **[!UICONTROL Clear All]** to start over with selecting dimensions to exclude.

   ![](assets/exclude_dimensions.png)

1. After you have added dimensions to exclude (or chosen not to), click **[!UICONTROL Run Contribution Analysis]** again.
1. Wenn Sie die Liste mit ausgeschlossenen Dimensionen verändern müssen, doppelklicken Sie einfach auf „Dimensionen“. Die Liste mit ausgeschlossenen Dimensionen wird dann angezeigt:

   ![](assets/excluded-dimensions.png)

1. Just delete any unwanted dimensions by clicking the x next to them, then save the list by clicking **[!UICONTROL Set as Default]**.

