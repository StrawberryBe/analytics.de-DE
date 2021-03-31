---
description: Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.
title: Pfadbericht mit dem Anforderungs-Assistenten filtern
uuid: 9b22d5b5-7ae8-49a2-90ae-0c1075562bbe
feature: Report Builder
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 99%

---


# Pfadbericht mit dem Anforderungs-Assistenten filtern

Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.

In diesem Beispiel werden Pfade für Sitebereiche verwendet.

1. Klicken Sie in Adobe Report Builder auf **[!UICONTROL Erstellen]**, um den Anforderungs-Assistenten zu öffnen.
1. Wählen Sie die richtige Report Suite aus.
1. Wählen Sie in der Baumansicht auf der linken Seite **[!UICONTROL Pfade]** > **[!UICONTROL Sitebereich]** > **[!UICONTROL Pfade für Sitebereich]** aus.

   ![](assets/site_section_path_1.png)

1. Legen Sie die entsprechenden Werte für das Datum fest.
1. Klicken Sie auf **[!UICONTROL Weiter]**.
1. Klicken Sie in Schritt 2 des Assistenten unter **[!UICONTROL Zeilenbezeichnungen]** auf den Link **[!UICONTROL Erste 1-10 (Muster angewendet)]**. In einem Pfadbericht wird ein Muster standardmäßig angewendet.

   ![](assets/site_section_path_2.png)

1. Wählen Sie die **[!UICONTROL Filter]**-Option.

   ![](assets/filter_option.png)

1. Im Dialogfeld **[!UICONTROL Pfadmuster für „Pfade für Sitebereiche“ definieren]**, können Sie Folgendes festlegen:
   1. den Startrang des ersten Berichts
   1. die Anzahl der Einträge, die in diesem Bericht angezeigt werden sollen
1. Klicken Sie auf **[!UICONTROL Bearbeiten]**, um ein Pfadmuster zu definieren.
1. Für ein benutzerdefiniertes Muster verschieben Sie beliebige **[!UICONTROL Musterobjekte]** per Drag-and-drop aus der Liste auf der linken Seite in die **[!UICONTROL Pfadmuster-Arbeitsfläche]** auf der rechten Seite.

   ![](assets/custom_pattern.png)

1. Sie können auch aus der Dropdown-Liste **[!UICONTROL Ein Muster auswählen]** ein vordefiniertes Muster auswählen und es anpassen. Folgende Muster stehen zur Verfügung:

   ![](assets/select_a_pattern.png)

   Einige dieser Muster sind Report Builder-spezifisch: Einstiegspfadmuster für nächstes Element, Einstiegspfadmuster für vorheriges Element, Muster für nächstes Element.
1. So bearbeiten Sie ein vordefiniertes Muster:
   1. Wählen Sie es aus. Wählen Sie zum Beispiel das **[!UICONTROL Muster für Ausstiegssite]** aus: ![](assets/exited_site_pattern.png)

   1. Nun definieren Sie den Sitebereichspfad, dem der Benutzer vor dem Ausstieg folgt. Klicken Sie auf **[!UICONTROL Bestimmte Elemente: 0 ausgewählt]**. Sie können diesen Pfad durch Auswahl aus einem Zellenbereich (wenn Sie eine vorhandene Anforderung bearbeiten) oder durch Auswahl aus einer Bereichsliste definieren.
   1. Um aus einem Zellenbereich einer vorherigen Anforderung auszuwählen, wählen Sie **[!UICONTROL Aus Zellenbereich]** und klicken Sie auf das Symbol für die Zellenauswahl. Wählen Sie dann aus dem Bericht die Zellen aus. ![](assets/choose_site_section_paths.png)

   1. Um aus einer Liste mit Sitebereichen auszuwählen, wählen Sie **[!UICONTROL Aus Liste]** aus und klicken Sie auf **[!UICONTROL Hinzufügen]**.
   1. Verschieben Sie Elemente aus der Spalte **[!UICONTROL Verfügbare Elemente]** in die Spalte **[!UICONTROL Ausgewählte Elemente]**, indem Sie sie auswählen und auf den orangefarbenen Pfeil klicken. Klicken Sie anschließend auf **[!UICONTROL OK]**. ![](assets/move_site_section_elements.png)

   1. Um das eben erstellte Muster zu speichern, klicken Sie auf **[!UICONTROL Speichern]**.
   1. Klicken Sie dreimal auf **[!UICONTROL OK]** und anschließend auf **[!UICONTROL Fertigstellen]**. Die gefilterte Pfadanforderung wird nun generiert.
