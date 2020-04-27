---
description: Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.
title: Pfadbericht mit dem Anforderungs-Assistenten filtern
topic: Report builder
uuid: 9b22d5b5-7ae8-49a2-90ae-0c1075562bbe
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Pfadbericht mit dem Anforderungs-Assistenten filtern

Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.

In diesem Beispiel werden Pfade für Sitebereiche verwendet.

1. In Adobe Report Builder, click **[!UICONTROL Create]** to open the Request Wizard.
1. Wählen Sie die richtige Report Suite aus.
1. Wählen Sie in der Ansicht auf der linken Seite **[!UICONTROL Paths]** > **[!UICONTROL Site Sections]** > **[!UICONTROL Site Section Paths]**.

   ![](assets/site_section_path_1.png)

1. Legen Sie die entsprechenden Werte für das Datum fest.
1. Klicken Sie auf **[!UICONTROL Next]**.
1. Klicken Sie in Schritt 2 des Assistenten unter **[!UICONTROL Row Labels]** dem Link **[!UICONTROL Top 1-10 (pattern applied)]** . In einem Pfadbericht wird ein Muster standardmäßig angewendet.

   ![](assets/site_section_path_2.png)

1. Wählen Sie die Option **[!UICONTROL Filter]** aus.

   ![](assets/filter_option.png)

1. Im **[!UICONTROL Define 'Site Section Paths' Path Pattern]** Dialogfeld können Sie
   1. den Startrang des ersten Berichts
   1. die Anzahl der Einträge, die in diesem Bericht angezeigt werden sollen
1. Click **[!UICONTROL Edit]** to define a path pattern.
1. If you want a custom pattern, drag and drop any **[!UICONTROL Pattern Objects]** from the list on the left into the **[!UICONTROL Pattern Build Canvas]** on the right.

   ![](assets/custom_pattern.png)

1. You can also select a predefined pattern from the **[!UICONTROL Select a Pattern]** drop-down list and modify it. Folgende Muster stehen zur Verfügung:

   ![](assets/select_a_pattern.png)

   Einige dieser Muster sind Report Builder-spezifisch: Einstiegspfadmuster für nächstes Element, Einstiegspfadmuster für vorheriges Element, Muster für nächstes Element.
1. So bearbeiten Sie ein vordefiniertes Muster:
   1. Wählen Sie es aus. Wählen Sie beispielsweise **[!UICONTROL Exited Site Pattern]**: ![](assets/exited_site_pattern.png)

   1. Nun definieren Sie den Sitebereichspfad, dem der Benutzer vor dem Ausstieg folgt. Klicken Sie auf **[!UICONTROL Specific Item(s): 0 selected]**. Sie können diesen Pfad durch Auswahl aus einem Zellenbereich (wenn Sie eine vorhandene Anforderung bearbeiten) oder durch Auswahl aus einer Bereichsliste definieren.
   1. To select from a range of cells from a previous request, select **[!UICONTROL From range of cells]** and click the cell selector icon. Wählen Sie dann aus dem Bericht die Zellen aus. ![](assets/choose_site_section_paths.png)

   1. To select from a list of site sections, select **[!UICONTROL From list]** and click **[!UICONTROL Add]**.
   1. Move elements from the **[!UICONTROL Available Elements]** column to the **[!UICONTROL Selected Elements]** column by selecting them and clicking the orange arrow. Klicken **[!UICONTROL OK]**. ![](assets/move_site_section_elements.png)

   1. To save the pattern you just established, click **[!UICONTROL Save]**.
   1. Click **[!UICONTROL OK]** three times and then click **[!UICONTROL Finish]**. Die gefilterte Pfadanforderung wird nun generiert.
