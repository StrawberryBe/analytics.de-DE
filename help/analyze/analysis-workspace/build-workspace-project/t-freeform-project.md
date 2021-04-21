---
description: Erstellen Sie ein Projekt und fügen Sie dem Freiform-Bedienfeld Komponenten (Dimensionen, Metriken, Segmente, Datumsbereiche) hinzu.
keywords: Analysis Workspace
title: Workspace-Projekt erstellen
feature: Grundlagen zu Reports & Analysen
uuid: c1def77a-a76e-4699-9feb-1ede5b70b7ba
translation-type: tm+mt
source-git-commit: cddf2a76ca36914f133379959b7cbb5246bdd695
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 99%

---


# Workspace-Projekt erstellen

Erstellen Sie ein Projekt und fügen Sie dem Freiform-Bedienfeld Komponenten (Dimensionen, Metriken, Segmente, Datumsbereiche) hinzu.

In diesem Beitrag werden die Elemente der Benutzeroberfläche von Analysis Workspace erläutert und Sie erfahren, wie ein Projekt erstellt wird.

## Erstellen Sie ein Projekt

1. Legen Sie die Benutzerberechtigung zum Erstellen und Kuratieren von Projekten fest.

   Damit Sie ein Projekt in Analysis Workspace erstellen oder kuratieren können, müssen die Administratoren Sie zuerst zu einer Gruppe hinzufügen, für die die Berechtigung zum **[!UICONTROL Erstellen/Kuratieren von Projekten in Analysis Workspace]** aktiviert ist, oder zu einer Benutzergruppe mit **[!UICONTROL Zugriff auf alle Berichte]**. (**[!UICONTROL Admin]** > **[!UICONTROL User Management]** > [Gruppen](https://docs.adobe.com/content/help/de-DE/analytics/admin/user-product-management/user-groups/groups.html)).

1. Klicken Sie in [!DNL Experience Cloud] auf **[!UICONTROL Analytics]** > **[!UICONTROL Workspace]**.

   ![](assets/analysis_workspace_menu.png)

   Geben Sie alternativ einen Schrägstrich (/) ein, um die Berichtssuche zu öffnen, und geben Sie *`workspace`* ein.

   ![](assets/analysis-app-search.png)

1. Klicken Sie auf **[!UICONTROL Neues Projekt erstellen]**.

   Für die Erstellung eines Projekts gibt es folgende Ausgangspunkte:

* Ein leeres Projekt (Standard). Eine Anleitung finden Sie unten.
* Eine Standardvorlage. Diese Vorlagen wurden von Adobe erstellt und können sofort verwendet werden. Eine Anleitung finden Sie unter [Vorlagen](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md).
* Eine benutzerdefinierte Vorlage. Diese Vorlagen werden von Benutzern mit Administratorrechten erstellt. Eine Anleitung finden Sie unter [Vorlagen](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md).

   ![](assets/start_modal.png)

1. Um ein Projekt aus einem leeren Projekt zu erstellen, klicken Sie auf **[!UICONTROL Leeres Projekt]**.

   * Klicken Sie anschließend auf **[!UICONTROL Erstellen]** oder
   * einfach auf **[!UICONTROL Eingabe]**.

   Ein leeres Projekt wird angezeigt, das einen Freiformbereich und eine Datentabellenvisualisierung enthält.

   ![](assets/fa_project_new.png)

   >[!NOTE]
   >
   >Manchmal wird beim Laden eines Projekts (oder beim Umschalten auf eine Report Suite) die Meldung „Inkompatible Report Suite“ angezeigt, wenn nicht alle Komponenten (Metriken/Dimensionen) des Projekts in der Report Suite enthalten sind. Sie können eine Liste der nicht kompatiblen Komponenten anzeigen und wissen somit, warum Sie die Meldung erhalten.

<table id="table_3989E45D9D4241CBB2E58B29DA257B2F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/analysis-workspace-components.md"  > Komponenten</a> </td> 
   <td colname="col2"> <p>Dimensionen, Metriken, Segmente und Datumsbereiche, die Sie in Projekte ziehen können </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md"  > Visualisierungen</a> </td> 
   <td colname="col2"> <p>Elemente, die Sie in den Bereich oder die Projektbereiche der Benutzeroberfläche ziehen können </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md"  >Freiform-Bedienfeld</a> </td> 
   <td colname="col2"> <p>Die Arbeitsfläche bzw. der Workspace, in dem Sie mit Analysis Workspace interagieren </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Speichern Sie Ihr Projekt. Vergeben Sie einen Namen für das Projekt, geben Sie eine Beschreibung an (optional, aber hilfreich) und taggen Sie das Projekt (optional). Klicken Sie dann auf **[!UICONTROL Projekt speichern]**.

   ![](assets/save_project.png)

1. Sie können eine Visualisierung oder ein Bedienfeld nun per Rechtsklick kopieren und das kopierte Element dann an einer anderen Stelle innerhalb des Projekts oder in ein anderes Projekt einfügen.

   Mithilfe dieser Funktion können Sie Bausteine – vordefinierte Visualisierungen/Bedienfelder – erstellen und diese in andere Projekte kopieren, wodurch Ihnen ein schnellerer Start mit Ihren unternehmensspezifischen Daten ermöglicht wird.

   >[!NOTE]
   >
   >Die internen Links beziehen sich nach dem Kopieren/Speichern nun auf das Projekt, in dem sie sich befinden, nicht auf das Originalprojekt, aus dem sie kopiert wurden.

## Komponenten und Visualisierungen hinzufügen {#task_CDAC9B3007BE4A3790AFAD3746D669B1}

1. Erstellen Sie Ihr Projekt durch Ziehen von *`components`* und *`visualizations`* in das Projekt.

   **Komponenten**

   Die Komponenten-Symbolleiste zeigt suchbare Dimensionen, Metriken, Segmente und Datumsbereiche an, die Sie häufig verwenden.

<table id="table_4626163E26DE46CB86391868BBA3AD32"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Komponente </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Dimensionen (orange) </td> 
   <td colname="col2"> <p>Werden auf der Projektebene angewendet </p> <p><img  src="assets/dimensions.png" id="image_353BAF1A7AC04C7DB5F5CDFDE7614402" align="left" placement="break" width="300px" /> </p> <p>Prop#, eVar# und event# werden an die Namen der Dimensionen angehängt. Daraufhin können Sie nach diesen Zahlen suchen. Beispiel: „Interne Kampagne“ wird in der linken Schiene als „Interne Kampagne (evar2)“ angezeigt. </p> <p> Beachten Sie, dass die Zahlen für prop, eVar und Ereignisse nicht in der Tabelle angezeigt werden (damit die Titel kurz gehalten werden). </p> <p>Es gibt eine standardmäßige Sortierreihenfolge für einige Out-of-the-Box-Dimensionen, wenn diese in eine Freiformtabelle gezogen oder in der linken Schiene angezeigt werden. Wenn zum Beispiel „Stunde des Tages“ in einer Tabelle abgelegt oder in der linken Schiene angezeigt wird, ist die Sortierreihenfolge aufsteigend von 0:00 Uhr bis 23:00 Uhr. Sie haben auch die Möglichkeit, nach einer Metrikspalte zu sortieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metriken (grün) </td> 
   <td colname="col2"> <p>Werden auf der Projektebene angewendet. </p> <p><img  src="assets/metrics.png" id="image_7C874C72992E414CBEE6B90CEF7B9F3C" /> </p> <p> <span class="term">Vorkommen</span> ist die Standardmetrik für die Datentabelle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Segmente (blau) </td> 
   <td colname="col2"> <p>Können per Drag-and-Drop nur auf Bereichsebene angewendet werden, Sie können jedoch Inline-Segmente in der Datentabelle erstellen. </p> <p><img  src="assets/segments.png" id="image_5674B18BC3AB47A2B1FEE584E0FBF47C" /> </p> <p>Weitere Informationen finden Sie unter <a href="/help/analyze/analysis-workspace/components/t-freeform-project-segment.md"  > Segmente</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Datumsbereiche und Granularitäten (violett) </td> 
   <td colname="col2"> <p>Können per Drag-and-Drop nur auf Bereichsebene angewendet werden. Sie können ein Projekt aus dem Kalender erstellen, wenn Sie einen Datumsbereich konfigurieren. </p> <p><img  src="assets/date-ranges.png" id="image_A1750DA921234AD0BB02166865EB8FCC" /> </p> </td> 
  </tr> 
 </tbody> 
</table>

**[Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)**

Der Bereich [!UICONTROL Visualisierungen] enthält standardmäßige Analytics-Graphen, Ringdiagramme, Datentabellen, [Kohorten](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md)-Tabellen, Venn-Diagramme usw. Sie können mehrere Visualisierungen per Drag-and-Drop in Ihrem Projekt platzieren.

![Schritt Ergebnis](assets/visualizations.png)

![](assets/fa_full_panel.png)

1. Schritt

## Daten mit dem Kontextmenü per Rechtsklick individuell anpassen {#concept_8117C300F21843B99F4E1B9AB7B11B6F}

Im Kontextmenü (Rechtsklick) können Sie die folgenden Aktionen ausführen (abhängig von der in der Tabelle ausgewählten Zelle).

![Schritt Ergebnis](assets/fa_data_table_actions.png)

<table id="table_0F84CC5B604D4D41BD0C9668DF525929"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Aktion </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/calendar-date-ranges/time-comparison.md"  > Spalte mit Zeitraum hinzufügen</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/calendar-date-ranges/time-comparison.md"  > Zeiträume vergleichen</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>In die Zwischenablage kopieren </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Auswahl löschen </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/components/c-alerts/intellligent-alerts.md"  > Warnhinweis aus Auswahl erstellen</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md"  > Aufschlüsselung</a> 
    <ul id="ul_18C83B8514AD4C1C86C071AA8402CB5C"> 
     <li id="li_6CA84ED293EA4940A7495DA9D9121264">Dimensionen </li> 
     <li id="li_EA16EE017B2E4A6998918706938A21BF">Metriken </li> 
     <li id="li_0405D339CD01405DB508A7D8D1A976B4">Segmente </li> 
     <li id="li_819CE81C552F49BB9C1B83ED3B42C5F7">Zeit </li> 
    </ul> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md"  > Visualisieren</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/curate-share/download-send.md"  > Als CSV herunterladen</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/home.md"  > Trend-Auswahl</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/t-freeform-project-segment.md"  > Segment aus Auswahl erstellen</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md"  > In Segmentvergleich ausführen</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nur ausgewählte Zeilen anzeigen </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alle Zeilen anzeigen </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

Informationen zum Kopieren und Auswählen von Zeilen finden Sie unter [Tastatur- und Mausinteraktionen in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md).
