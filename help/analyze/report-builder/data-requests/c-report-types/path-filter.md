---
description: Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.
seo-description: Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.
seo-title: Pfadberichte mithilfe des Anforderungs-Assistenten filtern
solution: Analytics
title: Pfadberichte mithilfe des Anforderungs-Assistenten filtern
topic: ReportBuilder
uuid: 9 b 22 d 5 b 5-7 ae 8-49 a 2-90 ae -0 c 1075562 bbe
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Pfadberichte mithilfe des Anforderungs-Assistenten filtern

Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.

In diesem Beispiel werden Pfade für Sitebereiche verwendet.

1. In Adobe Report Builder, click **[!UICONTROL Create]** to open the Request Wizard.
1. Wählen Sie die richtige Report Suite aus.
1. In the tree view on the left, select **[!UICONTROL Paths]** &gt; **[!UICONTROL Site Sections]** &gt; **[!UICONTROL Site Section Paths]**.

   ![](assets/site_section_path_1.png)

1. Legen Sie die entsprechenden Werte für das Datum fest.
1. Click **[!UICONTROL Next]**.
1. In Step 2 of the Wizard, under **[!UICONTROL Row Labels]**, click the **[!UICONTROL Top 1-10 (pattern applied)]** link. In einem Pfadbericht wird ein Muster standardmäßig angewendet.

   ![](assets/site_section_path_2.png)

1. Select the **[!UICONTROL Filter]** option.

   ![](assets/filter_option.png)

1. In the **[!UICONTROL Define 'Site Section Paths' Path Pattern]** dialog, you can specify
   1. den Startrang des ersten Berichts 
   1. die Anzahl der Einträge, die in diesem Bericht angezeigt werden sollen 
1. Click **[!UICONTROL Edit]** to define a path pattern.
1. If you want a custom pattern, drag and drop any **[!UICONTROL Pattern Objects]** from the list on the left into the **[!UICONTROL Pattern Build Canvas]** on the right.

   ![](assets/custom_pattern.png)

1. You can also select a predefined pattern from the **[!UICONTROL Select a Pattern]** drop-down list and modify it. Folgende Muster stehen zur Verfügung:

   ![](assets/select_a_pattern.png)

   Einige dieser Muster sind ReportBuilder-spezifisch: Einstiegspfadmuster für nächstes Element, Einstiegspfadmuster für vorheriges Element, Muster für nächstes Element.
1. So bearbeiten Sie ein vordefiniertes Muster: 
   1. Wählen Sie es aus. Wählen Sie zum Beispiel das **[!UICONTROL Muster für Ausstiegssite aus]**: ![](assets/exited_site_pattern.png)

   1. Nun definieren Sie den Sitebereichspfad, dem der Benutzer vor dem Ausstieg folgt. Klicken Sie auf **[!UICONTROL Bestimmte Elemente: 0 ausgewählt]**. Sie können diesen Pfad durch Auswahl aus einem Zellenbereich (wenn Sie eine vorhandene Anforderung bearbeiten) oder durch Auswahl aus einer Bereichsliste definieren.
   1. To select from a range of cells from a previous request, select **[!UICONTROL From range of cells]** and click the cell selector icon. Wählen Sie dann aus dem Bericht die Zellen aus. ![](assets/choose_site_section_paths.png)

   1. To select from a list of site sections, select **[!UICONTROL From list]** and click **[!UICONTROL Add]**.
   1. Move elements from the **[!UICONTROL Available Elements]** column to the **[!UICONTROL Selected Elements]** column by selecting them and clicking the orange arrow. Klicken Sie anschließend auf **[!UICONTROL OK]**. ![](assets/move_site_section_elements.png)

   1. To save the pattern you just established, click **[!UICONTROL Save]**.
   1. Click **[!UICONTROL OK]** three times and then click **[!UICONTROL Finish]**. Die gefilterte Pfadanforderung wird nun generiert.
