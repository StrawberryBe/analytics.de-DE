---
description: Beim Synchronisieren von Visualisierungen können Sie kontrollieren, welche Datentabelle oder Datenquelle zu einer Visualisierung gehört.
keywords: Analysis Workspace;Synchronize visualization with data source
title: Data Sources verwalten
translation-type: tm+mt
source-git-commit: 6eda9e3e5bd450213253a8181042c24c318c0300

---


# Data Sources verwalten

Beim Synchronisieren von Visualisierungen können Sie kontrollieren, welche Datentabelle oder Datenquelle zu einer Visualisierung gehört.

**Tipp:** Sie können erkennen, welche Visualisierungen mit der Farbe des Punkts neben dem Titel zusammenhängen. Übereinstimmende Farben bedeuten, dass Visualisierungen auf derselben Datenquelle basieren.

Durch die Verwaltung einer Datenquelle können Sie die Datenquelle anzeigen oder die Auswahl sperren. Diese Einstellungen bestimmen, wie sich die Visualisierung ändert (oder nicht ändert), wenn neue Daten eingehen.

1. [Erstellen Sie ein Projekt](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md) mit einer Datentabelle und einer [Visualisierung](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md).
1. Wählen Sie in der Datentabelle die Zellen (Datenquelle) aus, die Sie der Visualisierung zuordnen möchten.
1. In the visualization, click the dot next to the title to bring up the **[!UICONTROL Data Source]** dialog. Wählen Sie **[!UICONTROL Show Data Source]** oder **[!UICONTROL Lock Selection]**.

   ![](assets/manage-data-source.png)

   Beim Synchronisieren einer Visualisierung mit einer Tabellenzelle wird eine neue (ausgeblendete) Tabelle erstellt und die synchronisierte Visualisierung wird farblich kodiert.

| Element | Beschreibung |
|--- |--- |
| Verknüpfte Visualisierungen | Wenn Visualisierungen mit einer Freiform- oder Kohortentabelle verknüpft sind, öffnet sich über den Punkt oben links eine Liste der verbundenen Visualisierungen sowie ein Kontrollkästchen „Anzeigen“, über das die Tabelle angezeigt/ausgeblendet werden kann.  Wenn Sie den Mauszeiger darüber bewegen, wird die verknüpfte Visualisierung hervorgehoben. Wenn Sie darauf klicken, gelangen Sie dazu. |
| Datenquelle anzeigen | Hiermit können Sie die Datentabelle, die der Visualisierung entspricht, ein- bzw. ausblenden (durch Deaktivierung des Kontrollkästchens). |
| Auswahl sperren | Aktivieren Sie diese Einstellung, um die Visualisierung an den derzeit in der entsprechenden Datentabelle ausgewählten Daten zu sperren. Wählen Sie nach der Aktivierung aus:  <ul><li>**Ausgewählte Positionen**: Wählen Sie diese Option, wenn die Visualisierung an den Positionen, die in der entsprechenden Datentabelle ausgewählt sind, gesperrt bleiben soll. Diese Positionen werden weiterhin visualisiert, auch wenn sich die spezifischen Elemente an diesen Positionen ändern. Wählen Sie diese Option beispielsweise, wenn Sie die fünf wichtigsten Kampagnen in dieser Visualisierung jederzeit anzeigen möchten, unabhängig davon, welche Kampagnen in den ersten fünf angezeigt werden.</li> <li>**Ausgewählte Elemente**: Wählen Sie diese Option, wenn die Visualisierung für bestimmte Elemente, die derzeit in der entsprechenden Datentabelle ausgewählt sind, gesperrt bleiben soll. Diese Elemente werden weiterhin visualisiert, auch wenn sie ihre Rangfolge unter den Elementen in der Tabelle ändern. Wählen Sie diese Option beispielsweise, wenn Sie immer die gleichen fünf spezifischen Kampagnen in dieser Visualisierung anzeigen möchten, unabhängig davon, wo diese Kampagnen ihren Rang haben.</li></ul> |

Diese Architektur unterscheidet sich von der vorherigen darin, dass Analysis Workspace keine doppelte ausgeblendete Tabelle mehr erstellt, in der die gesperrte Auswahl für Sie gespeichert wird.  Die Datenquelle verweist nun auf die Tabelle, aus der Sie die Visualisierung erstellt haben.

**Anwendungsbeispiele:**

* Sie können eine Zusammenfassungs-Visualisierung erstellen und sie an einer Zelle in der Tabelle sperren, aus der Sie sie erstellt haben. Wenn Sie &quot;Datenquelle anzeigen&quot;aktivieren, wird genau angezeigt, woher diese Informationen in der Tabelle kommen. Die Quelldaten werden ausgegraut:

   ![](assets/data-source2.png)>
* Sie können viele Visualisierungen hinzufügen und sie aus verschiedenen Zellen in derselben Tabelle beziehen, wie hier gezeigt. Die Tabelle ist dieselbe wie im obigen Beispiel, die Quellzelle (und Metrik) ist jedoch anders:

   ![](assets/data-source3.png)>
* Sie können sehen, ob Visualisierungen mit einer Freiform- oder Kohortentabelle verbunden sind, indem Sie auf den oberen linken Punkt (Datenquelleneinstellungen) klicken. Wenn Sie den Mauszeiger darüber bewegen, wird die verknüpfte Visualisierung hervorgehoben. Wenn Sie darauf klicken, gelangen Sie dazu.

   ![](assets/linked-visualizations.png)>
