---
description: Beim Synchronisieren von Visualisierungen können Sie kontrollieren, welche Datentabelle oder Datenquelle zu einer Visualisierung gehört.
keywords: Analysis Workspace;Synchronisieren der Visualisierung mit der Datenquelle
title: Verwalten von Visualisierungsdatenquellen
feature: Visualizations
role: User, Admin
exl-id: 0500b27a-032e-4dc8-98b7-58519ef59368
source-git-commit: de1ddbed4d455b6d05059e367369eb575a747971
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 82%

---

# Verwalten von Visualisierungsdatenquellen

Beim Synchronisieren von Visualisierungen können Sie kontrollieren, welche Datentabelle oder Datenquelle zu einer Visualisierung gehört.

**Tipp:** Die Farbe des Punkts neben dem Titel gibt an, welche Visualisierungen zusammenhängen. Übereinstimmende Farben besagen, dass Visualisierungen auf derselben Datenquelle basieren.

Beim Verwalten von Datenquellen können Sie die Datenquelle anzeigen oder die Auswahl sperren. Diese Einstellungen legen fest, ob sich die Visualisierung ändert (oder nicht ändert), sobald neue Daten eingehen.

1. [Erstellen Sie ein Projekt](/help/analyze/analysis-workspace/home.md) mit einer Datentabelle und einer [Visualisierung](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md).
1. Wählen Sie in der Datentabelle die Zellen (Datenquelle) aus, die Sie der Visualisierung zuordnen möchten.
1. Klicken Sie in der Visualisierung auf den Punkt neben dem Titel, um das Dialogfeld **[!UICONTROL Datenquelle]** zu öffnen. Wählen Sie **[!UICONTROL Datenquelle anzeigen]** oder **[!UICONTROL Auswahl sperren]** aus.

   ![](assets/manage-data-source.png)

   Beim Synchronisieren einer Visualisierung mit einer Tabellenzelle wird eine neue (ausgeblendete) Tabelle erstellt und die synchronisierte Visualisierung mit dieser Tabelle farblich codiert.

## Einstellungen zur Datenquelle

Im Folgenden finden Sie ein Video zu diesen Einstellungen:

>[!VIDEO](https://video.tv.adobe.com/v/23729/?quality=12)

| Element | Beschreibung |
| --- | --- |
| Verknüpfte Visualisierungen | Wenn mit einer Freiform- oder Kohortentabelle verknüpfte Visualisierungen vorhanden sind, wird der Punkt oben links geöffnet, um die verbundenen Visualisierungen aufzulisten, und es wird ein Kontrollkästchen &quot;Anzeigen&quot;angezeigt, über das die Tabelle ein-/ausgeblendet werden kann. Wenn Sie die Maus über die verknüpfte Visualisierung bewegen, wird sie hervorgehoben. Wenn Sie darauf klicken, werden Sie dorthin geleitet. |
| Datenquelle anzeigen | Sie können die der Visualisierung entsprechende Datentabelle anzeigen (durch Aktivieren des Kontrollkästchens) oder ausblenden (durch Deaktivieren des Kontrollkästchens). |
| Auswahl sperren | Aktivieren Sie diese Einstellung, damit die Visualisierung mit den aktuell in der entsprechenden Datentabelle ausgewählten Daten verknüpft bleibt. Wenn Sie die Option aktiviert haben, können Sie Folgendes auswählen:<ul><li>**Ausgewählte Positionen**: Wählen Sie diese Option aus, damit die Visualisierung mit den Positionen verknüpft bleibt, die in der entsprechenden Datentabelle ausgewählt sind. Diese Positionen werden weiterhin visualisiert, auch wenn sich die spezifischen Elemente an diesen Positionen ändern. Wählen Sie diese Option aus, wenn Sie beispielsweise immer die fünf Kampagnennamen mit dem höchsten Wert in dieser Visualisierung zeigen möchten, egal um welche Kampagnennamen es sich handelt.</li><li>**Gewählte Elemente**: Wählen Sie diese Option aus, damit die Visualisierung mit genau den Elementen verknüpft bleibt, die aktuell in der entsprechenden Datentabelle ausgewählt sind. Diese Elemente werden weiterhin visualisiert, auch wenn sie ihren Rang unter den Elementen in der Tabelle ändern. Wählen Sie diese Option aus, wenn Sie z. B. immer die gleichen fünf Kampagnennamen in dieser Visualisierung zeigen möchten, egal welchen Rang diese Kampagnennamen einnehmen.</li></ul> |

Diese Architektur unterscheidet sich von der vorherigen darin, dass Analysis Workspace keine doppelte ausgeblendete Tabelle mehr erstellt, in der die gesperrte Auswahl für Sie gespeichert wird. Die Datenquelle verweist nun auf die Tabelle, aus der Sie die Visualisierung erstellt haben.

## Beispielhafte Anwendungsfälle

* Sie können eine Zusammenfassungsvisualisierung erstellen und mit einer Zelle in der Tabelle verknüpfen, aus der Sie sie erstellt haben. Wenn Sie „Datenquelle anzeigen“ aktivieren, wird angezeigt, wo genau die Informationen aus der Tabelle herkommen. Die Quelldaten sind ausgegraut:

  ![](assets/data-source2.png)>
* Sie können zahlreiche Visualisierungen hinzufügen und sie aus unterschiedlichen Zellen in derselben Tabelle beziehen, wie hier gezeigt wird. Es handelt sich um dieselbe Tabelle wie im Beispiel oben, allerdings ist die bezogene Zelle (und Metrik) anders:

  ![](assets/data-source3.png)>
* Sie können sehen, ob Visualisierungen mit einer Freiform- oder Kohortentabelle verbunden sind, indem Sie auf den Punkt oben links klicken (Datenquelleneinstellungen). Wenn Sie die Maus über die verknüpfte Visualisierung bewegen, wird sie hervorgehoben. Wenn Sie darauf klicken, werden Sie dorthin geleitet.

  ![](assets/linked-visualizations.png)>
