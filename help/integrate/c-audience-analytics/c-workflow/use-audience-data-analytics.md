---
description: 'Sie können die AAM Zielgruppen-Dimensionen überall in Analytics nutzen. Die integrierten Segmente sind neue Analytics-Dimensionen namens „Zielgruppen-ID“ und „Zielgruppenname“. Diese können genau wie alle anderen von Analytics gesammelten Dimensionen gesammelt werden. In Daten-Feeds werden die Zielgruppen-IDs in der Spalte „mc_audiences“ gespeichert. Diese Dimensionen sind derzeit nicht in Data Workbench oder Livestream verfügbar. Nachfolgend finden Sie einige Beispiele dafür, wie die Zielgruppen-Dimensionen verwendet werden können '
seo-description: 'Sie können die AAM Zielgruppen-Dimensionen überall in Analytics nutzen. Die integrierten Segmente sind neue Analytics-Dimensionen namens „Zielgruppen-ID“ und „Zielgruppenname“. Diese können genau wie alle anderen von Analytics gesammelten Dimensionen gesammelt werden. In Daten-Feeds werden die Zielgruppen-IDs in der Spalte „mc_audiences“ gespeichert. Diese Dimensionen sind derzeit nicht in Data Workbench oder Livestream verfügbar. Nachfolgend finden Sie einige Beispiele dafür, wie die Zielgruppen-Dimensionen verwendet werden können '
seo-title: Zielgruppendaten in Analytics verwenden
solution: Experience Cloud
title: Zielgruppendaten in Analytics verwenden
uuid: 203925fb-f070-441c-813a-43099cb9b2b9
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Zielgruppendaten in Analytics verwenden

Sie können die AAM Zielgruppen-Dimensionen überall in Analytics nutzen. Die integrierten Segmente sind neue Analytics-Dimensionen namens „Zielgruppen-ID“ und „Zielgruppenname“. Diese können genau wie alle anderen von Analytics gesammelten Dimensionen gesammelt werden. In Daten-Feeds werden die Zielgruppen-IDs in der Spalte „mc_audiences“ gespeichert. Diese Dimensionen sind derzeit nicht in Data Workbench oder Livestream verfügbar. Nachfolgend finden Sie einige Beispiele dafür, wie die Zielgruppen-Dimensionen verwendet werden können:

## Analysis Workspace {#section_C70837499BEA4DED885B3486C9E02C68}

In Analysis Workspace erscheinen die AAM-Segmente als zwei Dimensionen.

1. Wechseln Sie zu **[!UICONTROL Arbeitsbereich]**.
1. Wählen Sie aus der Liste der **[!UICONTROL Dimensionen]** die Dimensionen **[!UICONTROL Zielgruppen-ID]** oder **Zielgruppenname[!UICONTROL aus]**. Der Name ist eine Anzeigeklassifikation der ID.

   ![](assets/aw-mcaudiences.png)

## Segmentvergleich {#section_E72B80B6470C42D4B9B19BE90E6070A2}

Der [Segmentvergleich](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/segment-comparison.html) findet die statistisch relevantesten Unterschiede zwischen zwei Segmenten. Audiences-Daten können im Segmentvergleich auf zwei Arten verwendet werden: 1) als die 2 Segmente, die verglichen werden, und 2) als Elemente in der Tabelle „Top-Dimensionselemente“.

1. Wechseln Sie zu **[!UICONTROL Arbeitsbereich]** und wählen Sie in der linken Schiene das Bedienfeld **Segmentvergleich]aus.[!UICONTROL **

1. Suchen Sie im Menü Komponente **nach[!UICONTROL Zielgruppenname].**

1. Öffnen Sie [!UICONTROL Zielgruppenname]. Daraufhin werden die damit verbundenen Dimensionselemente angezeigt.
1. Ziehen Sie die Zielgruppen, die Sie vergleichen möchten, in den Segmentvergleichsaufbau.
1. (Optional:) Sie können auch andere Dimensionselemente oder Segmente miteinbeziehen, es können bis zu zwei davon verglichen werden.
1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Die Dimensionen „Zielgruppen-ID“ und „Zielgruppen-Name“ werden automatisch in der Tabelle „Top-Dimensionselemente“ angezeigt, da sie zusätzliche Profildaten für die beiden verglichenen Segmente sind.

   ![](assets/aud-segcompare.png)

## Customer Journey (Fluss) in Analysis Workspace {#section_FC30E5795C9D4539838E30FE11FAEA6E}

AAM-Segmentdaten werden pro Treffer an Analytics weitergeleitet und stellen die Zugehörigkeit eines Besuchers zu Zielgruppen zu diesem Zeitpunkt dar. Das bedeutet, dass ein Besucher einem Segment zugehörig sein kann (z. B. „Bewusstsein“) und sich später für ein qualifizierteres Segment qualifizieren könnte (z. B. „Überlegung“). Sie können [Fluss](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/flow.html) in Analysis Workspace verwenden, um die Customer Journey eines Besuchers zwischen zwei Zielgruppen zu visualisieren.

1. Wechseln Sie zu **[!UICONTROL Arbeitsbereich]** und wählen Sie in der linken Schiene die Visualisierung **Fluss]aus.[!UICONTROL **

1. Ziehen Sie die Dimension [!UICONTROL Zielgruppenname] in den Flussaufbau.
1. Klicken Sie auf **[!UICONTROL Erstellen]**.
1. (Optional): Ziehen Sie eine beliebige weitere Dimension in die Flussvisualisierung, um einen [interdimensionalen Fluss](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/multi-dimensional-flow.html) zu erstellen.

![](assets/flow-aamaudiences.png)

Zielgruppen können außerdem für [Abgangsvisualisierungen](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/fallout_flow.html) verwendet werden.

## Venn-Visualisierung in Analysis Workspace {#section_E78AB764FB5047148B51DC1526B0DF89}

[Venn-Visualisierungen](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/venn.html) zeigen Überlappungen zwischen bis zu 3 Segmenten.

1. Wechseln Sie zu **[!UICONTROL Arbeitsbereich]** und wählen Sie in der linken Schiene die Visualisierung **Venn]aus.[!UICONTROL **

1. Suchen Sie nach [!UICONTROL Zielgruppenname] im Menü „Komponente“.
1. Öffnen Sie [!UICONTROL Zielgruppenname]. Daraufhin werden die damit verbundenen Dimensionselemente angezeigt.
1. Ziehen Sie die Zielgruppen, die Sie vergleichen möchten, in den Vennaufbau.
1. (Optional): Sie können auch andere Dimensionselemente oder Segmente miteinbeziehen; es können bis zu drei davon verglichen werden.
1. Klicken Sie auf **[!UICONTROL Erstellen]**.

![](assets/venn-viz.png)

## Segmentaufbau {#section_2AA81852A1404AB894472CA8959461B6}

Sie können die Zielgruppendimensionen zusammen mit den von Analytics erfassten Verhaltensinformationen in den Analytics-[Segmentaufbau](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html) eingeben.

1. Go to  **[!UICONTROL Components]** &gt; **[!UICONTROL Segments]** .
1. Klicken Sie auf **[!UICONTROL Hinzufügen], um ein neues Segment zu erstellen.**
1. Nachdem Sie das Segment benannt haben, ziehen Sie die Dimension [!UICONTROL Zielgruppenname] in das Bedienfeld „Dimensionen“.
1. (Optional): Fügen Sie ein weiteres Kriterium zum Segment hinzu.
1. Speichern Sie das Segment.

   ![](assets/aud-segbuilder.png)

## Reports &amp; Analysen und ReportBuilder {#section_04E8FD30F73344D7937AD3C6CD19E34A}

1. To view the Analytics report, go to  **[!UICONTROL Reports]** &gt; **[!UICONTROL Visitor Profile]** &gt; **[!UICONTROL Audience ID Reports]** .
1. Über diesen Ordner können Sie sowohl auf die Dimension „Zielgruppen-ID“ als auch auf die Dimension „Zielgruppenname“ zugreifen.

   ![](assets/mc-audiences.png)

