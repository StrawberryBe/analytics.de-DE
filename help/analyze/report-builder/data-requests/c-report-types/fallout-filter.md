---
description: Beschreibt die Schritte, die beim Anwenden von Filtern bei Fallout-Berichten durchgeführt werden müssen.
seo-description: Beschreibt die Schritte, die beim Anwenden von Filtern bei Fallout-Berichten durchgeführt werden müssen.
seo-title: Einen Fallout-Bericht mit dem Anforderungs-Assistenten filtern
solution: Analytics
title: Einen Fallout-Bericht mit dem Anforderungs-Assistenten filtern
topic: ReportBuilder
uuid: 269 e 900 e -23 bd -48 d 8-9 bac -69 e 3167 a 9 c 18
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Einen Fallout-Bericht mit dem Anforderungs-Assistenten filtern

Beschreibt die Schritte, die beim Anwenden von Filtern bei Fallout-Berichten durchgeführt werden müssen.

Dieses Beispiel zeigt einen Fallout-Bericht für Seiten.

1. In Adobe Report Builder, click **[!UICONTROL Create]** to open the Request Wizard.
1. Wählen Sie die richtige Report Suite aus.
1. In the tree view on the left, select **[!UICONTROL Paths]** &gt; **[!UICONTROL Page]** &gt; **[!UICONTROL Page Fallout]**.

   ![](assets/page_fallout.png)

1. Configure the appropriate [date ranges](../../../../analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md).
1. Click **[!UICONTROL Next]**.
1. In Step 2 of the Wizard, under **[!UICONTROL Row Labels]**, click the **[!UICONTROL Define Checkpoints]** link. (Im Gegensatz zu Pfadberichten, bei denen ein Muster bereits angewendet wird, müssen Sie bei einem Fallout-Bericht stets Pfadelemente definieren.)

   ![](assets/define_checkpoints.png)

1. Select the **[!UICONTROL Filter]** option.

1. In the **[!UICONTROL Define Site Section Fallout Checkpoints]** dialog, define checkpoints from a range of cells or from a list. Klicken Sie anschließend auf **[!UICONTROL OK]**.
1. Entscheiden Sie, ob Sie aus einem Zellenbereich oder einer Liste auswählen möchten.
1. If you select from a list, click **[!UICONTROL Add]** to select checkpoints to add to the fallout path. Sie können zwischen 3 und 8 Checkpoints definieren. (Suchen Sie nach verfügbaren Elementen, indem Sie auf **[!UICONTROL Weitere Informationen klicken]**.)

   For more information on refining the filter, see [Filter Dimensions](../../../../analyze/report-builder/layout/c-filter-dimensions/filter-dimensions.md#concept_9C0518E2CF604AADA97DDBB1B4ECAAF8). 1. Move **[!UICONTROL Available Elements]** from the left column to the right by selecting them and clicking the orange arrow.
1. Click **[!UICONTROL OK]** three times, then click **[!UICONTROL Finish]**.

   Der Bericht sollte jetzt aktualisiert werden.