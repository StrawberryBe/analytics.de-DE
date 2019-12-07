---
description: Beschreibt die Schritte, die beim Anwenden von Filtern bei Fallout-Berichten durchgeführt werden müssen.
title: Fallout-Bericht mit dem Anforderungs-Assistenten filtern
topic: Report builder
uuid: 269e900e-23bd-48d8-9bac-69e3167a9c18
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Fallout-Bericht mit dem Anforderungs-Assistenten filtern

Beschreibt die Schritte, die beim Anwenden von Filtern bei Fallout-Berichten durchgeführt werden müssen.

Dieses Beispiel zeigt einen Fallout-Bericht für Seiten.

1. In Adobe Report Builder, click **[!UICONTROL Create]** to open the Request Wizard.
1. Wählen Sie die richtige Report Suite aus.
1. In the tree view on the left, select **[!UICONTROL Paths]** &gt; **[!UICONTROL Page]** &gt; **[!UICONTROL Page Fallout]**.

   ![](assets/page_fallout.png)

1. Konfigurieren Sie die entsprechenden [Datumsbereiche](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md).
1. Klicken Sie auf **[!UICONTROL Weiter]**.
1. In Step 2 of the Wizard, under **[!UICONTROL Row Labels]**, click the **[!UICONTROL Define Checkpoints]** link. (Im Gegensatz zu Pfadberichten, bei denen ein Muster bereits angewendet wird, müssen Sie bei einem Fallout-Bericht stets Pfadelemente definieren.)

   ![](assets/define_checkpoints.png)

1. Select the **[!UICONTROL Filter]** option.

1. In the **[!UICONTROL Define Site Section Fallout Checkpoints]** dialog, define checkpoints from a range of cells or from a list. Klicken Sie anschließend auf **[!UICONTROL OK]**.
1. Entscheiden Sie, ob Sie aus einem Zellenbereich oder einer Liste auswählen möchten.
1. If you select from a list, click **[!UICONTROL Add]** to select checkpoints to add to the fallout path. Sie können zwischen 3 und 8 Checkpoints definieren. (Suchen Sie nach verfügbaren Elementen, indem Sie auf **[!UICONTROL Weitere Informationen klicken]**.)

   For more information on refining the filter, see [Filter Dimensions](/help/analyze/report-builder/layout/c-filter-dimensions/filter-dimensions.md). 1. Move **[!UICONTROL Available Elements]** from the left column to the right by selecting them and clicking the orange arrow.
1. Click **[!UICONTROL OK]** three times, then click **[!UICONTROL Finish]**.

   Der Bericht sollte jetzt aktualisiert werden.
