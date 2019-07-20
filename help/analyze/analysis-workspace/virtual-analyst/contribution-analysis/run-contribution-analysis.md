---
description: 'null '
seo-description: 'null '
seo-title: Ausführen einer Beitragsanalyse
title: Ausführen einer Beitragsanalyse
uuid: 5282 a 5 f 9-0771-4974-93 cb -335204 bde 114
translation-type: tm+mt
source-git-commit: 8b2feced9fd503395d06dc12c8e5d7985ca89161

---


# Ausführen einer Beitragsanalyse

Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. Damit soll dem Benutzer geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysieren viel schneller zu identifizieren.

## Ausführen einer Beitragsanalyse {#section_7D2C5E48A5664727941DF4C90976D9DC}

Es gibt zwei Möglichkeiten, die Beitragsanalyse in einem Projekt aufzurufen:

* In einer Freiform-Tabelle mit täglicher Granularität klicken Sie mit der rechten Maustaste auf eine beliebige Zeile und wählen dann **[!UICONTROL Beitragsanalyse durchführen aus]**. Sie können die Analyse sogar für Zeilen durchführen, die nicht als anormal gekennzeichnet sind.

   >[!NOTE]
   >
   >Die Beitragsanalyse wird derzeit nur mit täglicher Granularität unterstützt.

   ![](assets/run_ca.png)

* Zeigen Sie in einem Liniendiagramm auf einen anomalen Datenpunkt im Diagramm. Klicken Sie auf den Link **[!UICONTROL Analysieren], der erscheint.**

   ![](assets/contribution-analysis.png)

1. (Optional) Nachdem Sie in einem Liniendiagramm oder einer Tabelle auf **[!UICONTROL Beitragsanalyse durchführen]** geklickt haben, können Sie die Analyse weiter eingrenzen (und damit beschleunigen), indem Sie [Dimensionen ausschließen](../../../../analyze/analysis-workspace/virtual-analyst/contribution-analysis/run-contribution-analysis.md#section_F6932F4BF74544B5872164E7B1E0C6FC).

1. Warten Sie, während Ihre Beitragsanalyse geladen wird. Dieser Vorgang kann je nach der Größe Ihrer Report Suite und der Anzahl Ihrer Dimensionen einige Zeit in Anspruch nehmen. Die Beitragsanalyse erfolgt anhand der obersten 50.000 Elemente pro Dimension.
1. Anschließend lädt der Analysis Workspace ein neues Beitragsanalyse-Bedienfeld direkt in dieses Projekt. Wenn Sie die Beitragsanalyse schon früher in Reports &amp; Analytics genutzt haben, werden Ihnen etliche Bereiche vertraut vorkommen:

   * Eine Visualisierung, die die Anzahl der **Besuche** an diesem Tag anzeigt.
   * Eine monatliche **Besuchstrendlinie** für den Kontext.
   * **Oberste Elemente**, die zu dieser Anomalie beigetragen haben, sortiert nach der [Beitragsbewertung](https://marketing.adobe.com/resources/help/en_US/analytics/contribution/ca_contribution_score.html), plus der fraglichen Metrik, und eine Metrik namens Unique Visitors, um die Metrik hinsichtlich der Größe in einen Kontext zu setzen.

   * Die Tabelle [Generierte Segmente](https://marketing.adobe.com/resources/help/en_US/analytics/contribution/ca_workflow_premium.html) (Wichtigste Element-Cluster) gibt die Zugehörigkeiten der obersten Elemente basierend auf der Beitragsbewertung, den ungewöhnlichen Vorkommen und dem gesamten prozentualen Beitrag zu der anormalen Metrik an. Dies wird dann als Zielgruppensegment (Beitragssegment 1, Beitragssegment 2 usw.) erfasst. Wenn Sie auf die Infoschaltfläche („i“) klicken, sehen Sie eine Ansicht mit der Definition des jeweiligen Segments inklusive der obersten Elemente, aus denen dieses besteht:

      ![](assets/auto_segment.png)

1. Da die Beitragsanalyse nun Bestandteil des Analysis Workspace ist, haben Sie über das Kontextmenü einer Tabelle Zugriff auf eine Reihe zugehöriger Funktionen, mit denen Sie Ihre Analysen noch aussagekräftiger gestalten können, beispielsweise:

   * [Aufschlüsseln der einzelnen Dimensionselemente nach einer anderen Dimension](../../../../analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md#task_B594DA2476E84DFDA8279E831F0BD9C4)
   * [Anzeigen von Trends für mindestens eine Zeile](../../../../analyze/analysis-workspace/analysis-workspace-features.md#section_34930C967C104C2B9092BA8DCF2BF81A)
   * [Hinzufügen neuer Visualisierungen](../../../../analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#concept_09242627629147A88A68F1506954C276)
   * [Erstellen von Warnhinweisen](/help/components/c-alerts/intellligent-alerts.md)
   * [Erstellen oder Vergleichen von Segmenten](../../../../analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md#concept_74FAC1C6D0204F9190A110B0D9005793)

>[!NOTE]
>
>Wir heben die Anomalie hervor, die mit einem blauen Punkt in der Beitragsanalyse und den mit ihm verknüpften intelligenten Warnhinweisprojekten analysiert wird. Dadurch ist die gerade analysierte Anomalie leichter zu erkennen.

## Exclude dimensions from Contribution Analysis {#section_F6932F4BF74544B5872164E7B1E0C6FC}

Es kann von Zeit zu Zeit erforderlich sein, einige Dimensionen bei der Beitragsanalyse auszuschließen. Hier ein Beispiel: Sie sind nicht an Dimensionen interessiert, die mit Browsern oder Hardware in Zusammenhang stehen, und möchten die Analyse beschleunigen, indem Sie die entsprechenden Dimensionen entfernen.

1. Nachdem Sie auf **[!UICONTROL Beitragsanalyse durchführen]** (oder in einem Liniendiagramm auf **[!UICONTROL Analysieren]) geklickt haben, wird der Bereich** Ausgeschlossene Dimensionen] angezeigt.**[!UICONTROL **

1. Just drag any unwanted dimensions into the **[!UICONTROL Excluded Dimensions]** panel, then save the list by clicking **[!UICONTROL Set as Default]**. Alternativ können Sie auch auf **[!UICONTROL Alle löschen]klicken, um neue Dimensionen auszuwählen, die Sie ausschließen möchten.**

   ![](assets/exclude_dimensions.png)

1. Nachdem Sie Dimensionen hinzugefügt haben, die ausgeschlossen werden sollen, klicken Sie wieder auf **[!UICONTROL Beitragsanalyse durchführen].**
1. Wenn Sie die Liste mit ausgeschlossenen Dimensionen verändern müssen, doppelklicken Sie einfach auf „Dimensionen“. Die Liste mit ausgeschlossenen Dimensionen wird dann angezeigt:

   ![](assets/excluded-dimensions.png)

1. Löschen Sie einfach alle nicht erforderlichen Dimensionen, indem Sie auf das x-Symbol neben den einzelnen Dimensionen klicken. Speichern Sie dann die Liste, indem Sie auf **[!UICONTROL Als Standard festlegen klicken]**.

