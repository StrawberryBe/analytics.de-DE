---
title: Erstellen von Anmerkungen
description: Erstellen von Anmerkungen in Workspace.
role: User, Admin
feature: Annotations
exl-id: 3cf9a0fd-11c9-4375-8bbe-9551ba86f86d
source-git-commit: 20ab0e9728969c4cc11227a1255e41e3d1a1540f
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 100%

---

# Erstellen von Anmerkungen

1. Um Anmerkungen zu erstellen, haben Sie verschiedene Möglichkeiten zur Verfügung:

| Erstellungsmethode | Details |
| --- | --- |
| **Navigieren Sie zu [!UICONTROL Analytics] > [!UICONTROL Komponenten] > [!UICONTROL Anmerkung].** | Die Seite „Anmerkungsverwaltung“ wird geöffnet. Klicken Sie auf [!UICONTROL Neue Anmerkung erstellen], und der [!UICONTROL Anmerkungsgenerator] wird geöffnet. |
| **Klicken Sie mit der rechten Maustaste auf einen Punkt auf einer Tabelle.** | [!UICONTROL Der Anmerkungsgenerator] wird geöffnet. Beachten Sie, dass die auf diese Weise erstellten Anmerkungen standardmäßig nur in dem Projekt sichtbar sind, in dem sie erstellt wurden. Sie können sie aber für alle Projekte verfügbar machen. Beachten Sie, dass das Datum und ggf. Metriken usw. bereits ausgefüllt sind.<p>![](assets/annotate-table.png) |
| **Klicken Sie mit der rechten Maustaste auf einen Punkt in einem [!UICONTROL Linien] diagramm.** | Der [!UICONTROL Anmerkungsgenerator] wird geöffnet. Beachten Sie, dass die auf diese Weise erstellten Anmerkungen standardmäßig nur in dem Projekt sichtbar sind, in dem sie erstellt wurden. Sie können sie aber für alle Projekte verfügbar machen. Beachten Sie, dass das Datum und ggf. Metriken usw. bereits ausgefüllt sind.<p>![](assets/annotate-line.png) |
| **Wechseln Sie in Workspace zu [!UICONTROL Komponenten] > [!UICONTROL Anmerkung erstellen].** | Der [!UICONTROL Anmerkungsgenerator] wird geöffnet. |
| **Verwenden Sie dieses Tastenkürzel**, um den Anmerkungsgenerator zu öffnen: (PC) `ctrl` `shift` + o, (Mac) `shift` + `command` + o | Beachten Sie, dass Sie durch Verwendung des Tastenkürzels zur Erstellung einer Anmerkung eine eintägige Anmerkung für das aktuelle Datum ohne einen vorab ausgewählten Bereich (Kennzahlen oder Dimensionen) erstellen. |

{style=&quot;table-layout:auto&quot;}

1. Füllen Sie die Elemente des [!UICONTROL Anmerkungsgenerators] aus.

   ![](assets/ann-builder.png)

   | Element | Beschreibung |
   | --- | --- |
   | [!UICONTROL Projektspezifische Anmerkungen] | Standardmäßig gilt die Anmerkung für das aktuelle Projekt. Wenn Sie dieses Kontrollkästchen aktivieren, können Sie die Anmerkung in allen Projekten verfügbar machen, deren Inhaber Sie sind.<p> ![](assets/project-only.png) |
   | [!UICONTROL Titel] | Benennen Sie die Anmerkung, z. B. „Gedenktag“ |
   | [!UICONTROL Beschreibung] | (Optional) Geben Sie eine Beschreibung für die Anmerkung ein, z. B. „Feiertage in den USA“. |
   | [!UICONTROL Tags] | (Optional) Organisieren Sie Anmerkungen, indem Sie ein Tag erstellen oder anwenden. |
   | [!UICONTROL Anwendungsdatum] | Wählen Sie das Datum oder den Datumsbereich aus, das bzw. der vorhanden sein muss, damit die Anmerkung sichtbar ist. |
   | [!UICONTROL Farbe] | Wenden Sie eine Farbe auf die Anmerkung an. Die Anmerkung wird im Projekt mit der ausgewählten Farbe angezeigt. Mit Farben können Sie Anmerkungen kategorisieren, z. B. Feiertage, externe Ereignisse, Tracking-Probleme usw. |
   | [!UICONTROL Anwendungsbereich] | (Optional) Ziehen Sie die Metriken, von denen die Anmerkung ausgelöst werden soll, per Drag-and-Drop in das entsprechende Feld. Ziehen Sie dann alle Dimensionen oder Segmente, die als Filter fungieren (d. h. bei deren Anwendung die Anmerkung sichtbar bleiben soll) per Drag-and-Drop in das Feld. Wenn Sie keinen Bereich angeben, gilt die Anmerkung für alle Ihre Daten.<ul><li>**[!UICONTROL Eine dieser Metriken ist vorhanden]**: Ziehen Sie per Drag-and-Drop bis zu 10 Metriken in das Feld, die jeweils auslösen sollen, dass die Anmerkung angezeigt wird.</li><li>**[!UICONTROL Mit allen diesen Filtern]**: Ziehen Sie bis zu 10 Dimensionen oder Segmente per Drag-and-Drop in dieses Feld, nach denen gefiltert werden soll, wenn die Anmerkung angezeigt wird.</li></ul><p>Anwendungsbeispiele: Eine eVar hat die Erfassung von Daten für einen bestimmten Datumsbereich eingestellt. Ziehen Sie die eVar in das Dialogfeld **[!UICONTROL Eine dieser Metriken ist vorhanden]**. Oder die Metrik [!UICONTROL Besuche] meldet keine Daten – folgen Sie demselben Prozess.<p>**Hinweis:** Anmerkungen, die auf eine Komponente angewendet werden, die dann als Teil einer berechneten Kennzahl oder Segmentdefinition verwendet wird, übernehmen die Anmerkung NICHT automatisch. Die gewünschte berechnete Kennzahl muss auch dem Abschnitt „Umfang“ hinzugefügt werden, damit die Anmerkung angezeigt wird. Für jedes Segment, das Sie mit denselben Informationen versehen möchten, sollte jedoch eine neue Anmerkung erstellt werden.<p>Beispiel: Sie wenden eine Anmerkung auf [!UICONTROL Bestellungen] an einem bestimmten Tag an. Anschließend verwenden Sie [!UICONTROL Bestellungen] in einer berechneten Metrik für denselben Datumsbereich. Die neue berechnete Metrik zeigt die Anmerkung für Bestellungen nicht automatisch an. Die berechnete Metrik muss auch zum Bereich für den Umfang hinzugefügt werden, damit die Anmerkung angezeigt wird. |
   | [!UICONTROL Auf alle Report Suites anwenden] | Standardmäßig gilt die Anmerkung für die ursprüngliche Report Suite. Wenn Sie dieses Kontrollkästchen aktivieren, können Sie die Anmerkung für alle Report Suites im Unternehmen gelten lassen. |

   {style=&quot;table-layout:auto&quot;}

1. Klicken Sie auf **[!UICONTROL Speichern]**.
