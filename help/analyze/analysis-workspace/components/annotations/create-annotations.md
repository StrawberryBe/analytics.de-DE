---
title: Anmerkungen erstellen
description: Erstellen von Anmerkungen in Workspace.
role: User, Admin
exl-id: 3cf9a0fd-11c9-4375-8bbe-9551ba86f86d
source-git-commit: 0bdf0a111f2b30dda7afe283709f073e549c5f17
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 3%

---

# Anmerkungen erstellen

>[!NOTE]
>
>Diese Funktion wird derzeit nur eingeschränkt getestet.

1. Um Anmerkungen zu erstellen, haben Sie mehrere Möglichkeiten, zu beginnen:

| Erstellungsmethode | Details |
| --- | --- |
| **Navigieren Sie zu [!UICONTROL Analytics] > [!UICONTROL Komponenten] > [!UICONTROL Anmerkung].** | Die Seite &quot;Anmerkungs-Manager&quot;wird geöffnet. Klicken [!UICONTROL Neue Anmerkung erstellen] und [!UICONTROL Anmerkungs-Builder] geöffnet. |
| **Klicken Sie mit der rechten Maustaste auf einen Punkt auf einer Tabelle.** | [!UICONTROL Der Anmerkungs-Builder] geöffnet. Beachten Sie, dass auf diese Weise erstellte Anmerkungen standardmäßig nur in dem Projekt sichtbar sind, in dem sie erstellt wurden. Sie können sie aber für alle Projekte verfügbar machen. Beachten Sie außerdem, dass die Daten und Metriken usw. bereits ausgefüllt wurden.<p>![](assets/annotate-table.png) |
| **Rechtsklicken auf einen Punkt in einem [!UICONTROL Linie] Diagramm.** | Die [!UICONTROL Anmerkungs-Builder] geöffnet. Beachten Sie, dass auf diese Weise erstellte Anmerkungen standardmäßig nur in dem Projekt sichtbar sind, in dem sie erstellt wurden. Sie können sie aber für alle Projekte verfügbar machen. Beachten Sie außerdem, dass die Daten und Metriken usw. bereits ausgefüllt wurden.<p>![](assets/annotate-line.png) |
| **Wechseln Sie in Workspace zu [!UICONTROL Komponenten] > [!UICONTROL Anmerkung erstellen].** | Die [!UICONTROL Anmerkungs-Builder] geöffnet. |
| **Verwenden Sie diesen Hotkey** , um den Anmerkungs-Builder zu öffnen: (PC) `ctrl` `shift` + o, (Mac) `shift` + `command` + o | Beachten Sie, dass Sie durch Verwendung des Hotkeys zur Erstellung einer Anmerkung eine eintägige Anmerkung für das aktuelle Datum erstellen, ohne dass ein vorab ausgewählter Bereich (Metriken oder Dimensionen) ausgewählt ist. |

1. Füllen Sie die [!UICONTROL Anmerkungs-Builder] -Elemente.

   ![](assets/ann-builder.png)

   | Element | Beschreibung |
   | --- | --- |
   | [!UICONTROL Anrede/Titel] | Benennen Sie die Anmerkung, z. B. &quot;Gedenktag&quot; |
   | [!UICONTROL Beschreibung] | (Optional) Geben Sie eine Beschreibung für die Anmerkung ein, z. B. &quot;Feiertage in den USA&quot;. |
   | [!UICONTROL Tags] | (Optional) Organisieren Sie Anmerkungen, indem Sie ein Tag erstellen oder anwenden. |
   | [!UICONTROL Anwendungsdatum] | Wählen Sie das Datum oder den Datumsbereich aus, das bzw. der vorhanden sein muss, damit die Anmerkung sichtbar ist. |
   | [!UICONTROL Farbe] | Wenden Sie eine Farbe auf die Anmerkung an. Die Anmerkung wird im Projekt mit der ausgewählten Farbe angezeigt. Mit Farbe können Sie Anmerkungen kategorisieren, z. B. Feiertage, externe Ereignisse, Tracking-Probleme usw. |
   | [!UICONTROL Anwendungsbereich] | (Optional) Ziehen Sie die Metriken, mit denen die Anmerkung Trigger wird, per Drag-and-Drop. Ziehen Sie dann alle Dimensionen oder Segmente, die als Filter fungieren (d. h., dass die Anmerkung sichtbar ist) per Drag-and-Drop in den Arbeitsbereich. Wenn Sie keinen Bereich angeben, gilt die Anmerkung für alle Ihre Daten.<ul><li>**[!UICONTROL Jede dieser Metriken ist vorhanden]**: Ziehen Sie bis zu 10 Metriken in den Arbeitsbereich, um die angezeigte Anmerkung Trigger.</li><li>**[!UICONTROL Mit all diesen Filtern]**: Ziehen Sie bis zu 10 Dimensionen oder Segmente in den Arbeitsbereich, die gefiltert werden, wenn die Anmerkung angezeigt wird.</li></ul><p>Anwendungsbeispiele: Ein eVar hat die Erfassung von Daten für einen bestimmten Datumsbereich eingestellt. Ziehen Sie das eVar in die **[!UICONTROL Jede dieser Metriken ist vorhanden]** angezeigt. Oder [!UICONTROL Besuche] -Metrik meldet keine Daten - folgen Sie demselben Prozess.<p>**Hinweis:** Anmerkungen, die auf eine Komponente angewendet werden, die dann als Teil einer berechneten Metrik oder Segmentdefinition verwendet wird, übernehmen die Anmerkung NICHT automatisch. Die gewünschte berechnete Metrik muss auch zum Bereich &quot;Perimeter&quot;hinzugefügt werden, damit die Anmerkung angezeigt wird. Für jedes Segment, das Sie mit denselben Informationen kommentieren möchten, sollte jedoch eine neue Anmerkung erstellt werden. Beispiel: Sie wenden eine Anmerkung auf [!UICONTROL Bestellungen] an einem bestimmten Tag. Anschließend verwenden Sie [!UICONTROL Bestellungen] in einer berechneten Metrik für denselben Datumsbereich. Die neue berechnete Metrik zeigt die Anmerkung für Bestellungen nicht automatisch an - für die berechnete Metrik muss eine neue Anmerkung erstellt werden. |
   | [!UICONTROL Auf alle Report Suites anwenden] | Standardmäßig gilt die Anmerkung für die ursprüngliche Report Suite. Wenn Sie dieses Kontrollkästchen aktivieren, können Sie die Anmerkung für alle Report Suites im Unternehmen gelten lassen. |
   | [!UICONTROL Auf alle Projekte anwenden] | Standardmäßig gilt die Anmerkung für das aktuelle Projekt. Wenn Sie dieses Kontrollkästchen aktivieren, können Sie die Anmerkung auf alle Projekte anwenden, deren Inhaber Sie sind. Beachten Sie, dass dieses Kontrollkästchen nur angezeigt wird, wenn Sie den Anmerkungs-Builder aus dem Anmerkungs-Builder starten? |

1. Klicken Sie auf **[!UICONTROL Speichern]**.
