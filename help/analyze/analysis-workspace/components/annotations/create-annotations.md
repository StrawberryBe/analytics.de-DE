---
title: Anmerkungen erstellen
description: Erstellen von Anmerkungen in Workspace.
role: User, Admin
source-git-commit: f8a928782b4c4916f5ff2042cb72941d76f57d7d
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 5%

---


# Anmerkungen erstellen

>[!NOTE]
>
>Diese Funktion wird derzeit nur eingeschränkt getestet.

1. Um Anmerkungen zu erstellen, haben Sie vier Möglichkeiten:

   * Navigieren Sie zu [!UICONTROL Analytics] > [!UICONTROL Komponenten] > [!UICONTROL Anmerkung]. Die Seite &quot;Anmerkungs-Manager&quot;wird geöffnet. Klicken [!UICONTROL Neue Anmerkung erstellen] und der Anmerkungs-Builder geöffnet wird oder

   * Klicken Sie mit der rechten Maustaste auf einen Punkt auf einer Tabelle oder einem Liniendiagramm. Der Anmerkungs-Builder wird geöffnet oder

   * Wechseln Sie in Workspace zu [!UICONTROL Komponenten] > [!UICONTROL Anmerkung erstellen].

   * Verwenden Sie diesen Hotkey, um den Anmerkungs-Builder zu öffnen:
      * (PC) `ctrl` `shift` + o
      * (Mac) `shift` + `command` + o

1. Füllen Sie die Builder-Elemente aus.

   ![](assets/ann-builder.png)

   | Element | Beschreibung |
   | --- | --- |
   | [!UICONTROL Anrede/Titel] | Benennen Sie die Anmerkung, z. B. &quot;Gedenktag&quot; |
   | [!UICONTROL Beschreibung] | (Optional) Geben Sie eine Beschreibung für die Anmerkung ein, z. B. &quot;Feiertage in den USA&quot;. |
   | [!UICONTROL Tags] | (Optional) Organisieren Sie Anmerkungen, indem Sie ein Tag erstellen oder anwenden. |
   | [!UICONTROL Anwendungsdatum] | Wählen Sie das Datum oder den Datumsbereich aus, das bzw. der vorhanden sein muss, damit die Anmerkung sichtbar ist. |
   | [!UICONTROL Farbe] | Wenden Sie eine Farbe auf die Anmerkung an. Die Anmerkung wird im Projekt mit der ausgewählten Farbe angezeigt. Mit Farbe können Sie Anmerkungen kategorisieren, z. B. Feiertage, externe Ereignisse, Tracking-Probleme usw. |
   | [!UICONTROL Anwendungsbereich] | (Optional) Ziehen Sie die Metriken, mit denen die Anmerkung Trigger wird, per Drag-and-Drop. Ziehen Sie dann alle Dimensionen oder Segmente, die als Filter fungieren (d. h., dass die Anmerkung sichtbar ist) per Drag-and-Drop in den Arbeitsbereich. Wenn Sie keinen Bereich angeben, gilt die Anmerkung für alle Ihre Daten.<ul><li>**[!UICONTROL Jede dieser Metriken ist vorhanden]**: Ziehen Sie bis zu 10 Metriken in den Arbeitsbereich, um die angezeigte Anmerkung Trigger.</li><li>**[!UICONTROL Mit all diesen Filtern]**: Ziehen Sie bis zu 10 Dimensionen oder Segmente in den Arbeitsbereich, die gefiltert werden, wenn die Anmerkung angezeigt wird.</li></ul><p>Anwendungsbeispiele: Ein eVar hat die Erfassung von Daten für einen bestimmten Datumsbereich eingestellt. Ziehen Sie das eVar in die **[!UICONTROL Jede dieser Metriken ist vorhanden]** angezeigt. Oder [!UICONTROL Besuche] -Metrik meldet keine Daten - folgen Sie demselben Prozess. |
   | [!UICONTROL Auf alle Report Suites anwenden] | Standardmäßig gilt die Anmerkung für die ursprüngliche Report Suite. Wenn Sie dieses Kontrollkästchen aktivieren, können Sie die Anmerkung für alle Report Suites im Unternehmen gelten lassen. |
   | [!UICONTROL Auf alle Projekte anwenden] | Standardmäßig gilt die Anmerkung für das aktuelle Projekt. Wenn Sie dieses Kontrollkästchen aktivieren, können Sie die Anmerkung auf alle Projekte anwenden, deren Inhaber Sie sind. |

1. Klicken Sie auf [!UICONTROL Speichern].