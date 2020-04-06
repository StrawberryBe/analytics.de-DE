---
description: 'null'
title: Ausführen einer Beitragsanalyse
uuid: 5282a5f9-0771-4974-93cb-335204bde114
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Ausführen einer Beitragsanalyse

Bei der Contribution-Analyse handelt es sich um einen intensiven maschinellen Lernprozess, mit dem Beitragszahler entdeckt werden können, die zu einer festgestellten Anomalie in Adobe Analytics beitragen. Ziel ist es, den Anwender bei der Suche nach Schwerpunktbereichen oder Möglichkeiten für zusätzliche Analysen wesentlich schneller zu unterstützen, als dies sonst möglich wäre.

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

1. Warten Sie, während Ihre Beitragsleistung geladen wird. Dies kann je nach Größe Ihrer Report Suite und der Anzahl der Dimensionen eine erhebliche Zeit in Anspruch nehmen. Die Analyse &quot;Beitrag&quot;führt die Analyse der 50.000 wichtigsten Elemente pro Dimension durch.
1. Der Arbeitsbereich für Analysen lädt dann direkt in dieses Projekt einen neuen Bereich für die Analyse von Beiträgen. Sie werden eine Menge vertrauter Bedienfelder bemerken, wenn Sie zuvor in Reports &amp; Analysen die Analyse von Contribution verwendet haben:

   * Eine Visualisierung, die die Anzahl der **Besuche** an diesem Tag anzeigt.
   * Eine monatliche Trendlinie **für Besuche** für den Kontext.
   * **Top-Elemente** , die zu dieser Anomalie beigetragen haben, sortiert nach dem [Beitragswert](https://marketing.adobe.com/resources/help/de_DE/analytics/contribution/ca_contribution_score.html), der fraglichen Metrik und einer Metrik zu individuellen Besuchern, um die Metrik aus der Größenperspektive in den Kontext zu setzen.

   * Die Tabelle &quot; [Generierte Segmente](https://marketing.adobe.com/resources/help/de_DE/analytics/contribution/ca_workflow_premium.html) &quot;(Top-Elementzähler) identifiziert Zuordnungen der wichtigsten Elemente basierend auf der Beitragsbewertung, den Anomalievorkommen und dem Gesamtprozentsatz, der zur abweichenden Metrik beiträgt. Dies wird dann als Audience-Segment (Beitragssegment 1, Beitragssegment 2 usw.) erfasst. Durch Klicken auf die Info-Schaltfläche (&quot;i&quot;) erhalten Sie eine Ansicht der Definition der einzelnen Autosegmente, einschließlich der wichtigsten Elemente, aus denen das Segment besteht:

      ![](assets/auto_segment.png)

1. Da Beitragsfunktionen jetzt zum Arbeitsbereich für Analysen gehören, können Sie eine Reihe von Funktionen aus dem Kontextmenü einer Tabelle nutzen, um Ihre Analyse noch aussagekräftiger zu gestalten, z. B.:

   * [Aufschlüsseln der einzelnen Dimensionselemente nach einer anderen Dimension](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)
   * [Anzeigen von Trends für mindestens eine Zeile](/help/analyze/analysis-workspace/analysis-workspace-features.md#section_34930C967C104C2B9092BA8DCF2BF81A)
   * [Hinzufügen neuer Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)
   * [Erstellen von Warnhinweisen](/help/components/c-alerts/intellligent-alerts.md)
   * [Erstellen oder Vergleichen von Segmenten](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

>[!NOTE] Hinweis: Die analysierte Anomalie wird durch einen blauen Punkt in der Beitragsanalyse und in den verknüpften intelligenten Benachrichtigungsprojekten markiert. Dadurch ist die gerade analysierte Anomalie leichter zu erkennen.

## Ausschluss von Dimensionen aus einer Beitragsanalyse {#section_F6932F4BF74544B5872164E7B1E0C6FC}

Es kann vorkommen, dass Sie einige Dimensionen aus der Beitragsanalyse ausschließen möchten. So sind Sie z.B. mit Browser- oder Hardware-bezogenen Dimensionen nicht vertraut und möchten die Analyse durch Entfernen beschleunigen.

1. Nachdem Sie auf **[!UICONTROL Run Contribution Analysis]** (oder **[!UICONTROL Analyze]** in einem Liniendiagramm) geklickt haben, wird das **[!UICONTROL Excluded Dimensions]** Bedienfeld angezeigt.

1. Ziehen Sie einfach alle unerwünschten Dimensionen in das **[!UICONTROL Excluded Dimensions]** Bedienfeld und speichern Sie dann die Liste, indem Sie auf klicken **[!UICONTROL Set as Default]**. Or, click **[!UICONTROL Clear All]** to start over with selecting dimensions to exclude.

   ![](assets/exclude_dimensions.png)

1. After you have added dimensions to exclude (or chosen not to), click **[!UICONTROL Run Contribution Analysis]** again.
1. Wenn Sie die Liste mit ausgeschlossenen Dimensionen verändern müssen, doppelklicken Sie einfach auf „Dimensionen“. Die Liste mit ausgeschlossenen Dimensionen wird dann angezeigt:

   ![](assets/excluded-dimensions.png)

1. Just delete any unwanted dimensions by clicking the x next to them, then save the list by clicking **[!UICONTROL Set as Default]**.

