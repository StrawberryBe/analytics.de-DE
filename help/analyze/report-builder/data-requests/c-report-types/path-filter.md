---
description: Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.
title: Pfadbericht mit dem Anforderungs-Assistenten filtern
feature: Report Builder
role: User, Admin
exl-id: 085351b3-4d9c-45cf-b2a8-379f05932b26
source-git-commit: d218d07ec16e981d7e148092b91fbbd5711e840f
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 62%

---

# Pfadbericht mit dem Anforderungs-Assistenten filtern

Beschreibt die Schritte, die beim Anwenden von Filtern bei Pfadsetzungsberichten durchgeführt werden müssen.

In diesem Beispiel werden Pfade für Sitebereiche verwendet.

1. Klicken Sie in Adobe Report Builder auf **[!UICONTROL Erstellen]**, um den Anforderungs-Assistenten zu öffnen.
1. Wählen Sie die richtige Report Suite aus.
1. Wählen Sie in der Baumansicht auf der linken Seite **[!UICONTROL Pfade]** > **[!UICONTROL Sitebereich]** > **[!UICONTROL Pfade für Sitebereich]** aus.

   ![Screenshot mit ausgewählten Sitebereichspfaden.](assets/site_section_path_1.png)

1. Legen Sie die entsprechenden Werte für das Datum fest.

1. Klicken Sie auf **[!UICONTROL Weiter]**.

1. Klicken Sie in Schritt 2 des Assistenten unter **[!UICONTROL Zeilenbezeichnungen]** auf den Link **[!UICONTROL Erste 1-10 (Muster angewendet)]**. In einem Pfadbericht wird ein Muster standardmäßig angewendet.

   ![Screenshot mit dem Standardpfadmuster.](assets/site_section_path_2.png)

1. Wählen Sie die **[!UICONTROL Filter]**-Option.

   ![Screenshot, in dem die Option Filter hervorgehoben wird.](assets/filter_option.png)

1. Im Dialogfeld **[!UICONTROL Pfadmuster für „Pfade für Sitebereiche“ definieren]**, können Sie Folgendes festlegen:
   * Der Startrang des ersten Berichts.
   * Die Anzahl der Einträge, die in diesem Bericht angezeigt werden sollen.
1. Klicken Sie auf **[!UICONTROL Bearbeiten]**, um ein Pfadmuster zu definieren.

1. Für ein benutzerdefiniertes Muster verschieben Sie beliebige **[!UICONTROL Musterobjekte]** per Drag-and-drop aus der Liste auf der linken Seite in die **[!UICONTROL Pfadmuster-Arbeitsfläche]** auf der rechten Seite.

   ![](assets/custom_pattern.png)

1. Sie können auch aus der Dropdown-Liste **[!UICONTROL Ein Muster auswählen]** ein vordefiniertes Muster auswählen und es anpassen. Folgende Muster stehen zur Verfügung:

   ![](assets/select_a_pattern.png)

   Einige dieser Muster beziehen sich speziell auf den Report Builder: &quot;Muster für nächstes Element des Einstiegspfads&quot;, &quot;Muster für vorheriges Element des Ausstiegspfads&quot;, &quot;Muster für nächstes Element&quot;.

## So bearbeiten Sie ein vordefiniertes Muster

Sie können ein vordefiniertes Muster nach Auswahl eines Musters bearbeiten.

1. Wählen Sie ausgehend von den obigen Schritten das Muster aus. Wählen Sie zum Beispiel das **[!UICONTROL Muster für Ausstiegssite]** aus:

   ![Screenshot, der das ausgewählte Muster hervorhebt.](assets/exited_site_pattern.png)

1. Definieren Sie den Sitebereichspfad, dem der Benutzer vor dem Beenden folgt. Klicken Sie auf **[!UICONTROL Bestimmte Elemente: 0 ausgewählt]**. Sie können diesen Pfad durch Auswahl aus einem Zellenbereich definieren, wenn Sie eine vorhandene Anforderung bearbeiten, oder durch Auswahl aus einer Bereichsliste.

1. Um aus einem Zellenbereich einer vorherigen Anforderung auszuwählen, wählen Sie **[!UICONTROL Aus Zellenbereich]** und klicken Sie auf das Symbol für die Zellenauswahl. Wählen Sie dann aus dem Bericht die Zellen aus.

   ![Screenshot mit den Optionen zur Auswahl aus einem Zellenbereich oder aus einer Liste.](assets/choose_site_section_paths.png)

1. Um aus einer Liste mit Sitebereichen auszuwählen, wählen Sie **[!UICONTROL Aus Liste]** aus und klicken Sie auf **[!UICONTROL Hinzufügen]**.

1. Verschieben Sie Elemente aus der Spalte **[!UICONTROL Verfügbare Elemente]** in die Spalte **[!UICONTROL Ausgewählte Elemente]**, indem Sie sie auswählen und auf den orangefarbenen Pfeil klicken. Klicken Sie anschließend auf **[!UICONTROL OK]**.

   ![Screenshot mit den verfügbaren Elementen und den ausgewählten Elementen](assets/move_site_section_elements.png)

1. Um das eben erstellte Muster zu speichern, klicken Sie auf **[!UICONTROL Speichern]**.

1. Klicks **[!UICONTROL OK]** dreimal und klicken Sie dann auf **[!UICONTROL Beenden]** , um den gefilterten Pfad zu generieren.
