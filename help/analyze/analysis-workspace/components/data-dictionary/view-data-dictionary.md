---
description: Das Datenwörterbuch in Analysis Workspace ermöglicht es Benutzenden, die verschiedenen Komponenten in Analysis Workspace zu katalogisieren und im Auge zu behalten, einschließlich ihres Verwendungszwecks, welche genehmigt sind, welche Duplikate sind usw.
title: Datenwörterbuch anzeigen
feature: Components
role: User, Admin
exl-id: 68f68ea4-f0a6-4937-bf8f-aecfa28572bb
source-git-commit: a6805f0944570bee265d5db9a159ae24e0694837
workflow-type: ht
source-wordcount: '348'
ht-degree: 100%

---

# Komponenteninformationen im Datenwörterbuch anzeigen

Mit dem Datenwörterbuch können Sie Informationen über eine Komponente anzeigen, einschließlich der Komponentenbeschreibung, ähnlicher Komponenten, anderer Komponenten, mit denen eine Komponente häufig verwendet wird, und mehr.

So zeigen Sie Informationen zu einer Komponente im Datenwörterbuch an:

1. Wechseln Sie zum Analysis Workspace-Projekt, das die Komponente enthält, die Sie anzeigen möchten.

1. Wählen Sie das Symbol [!UICONTROL **Datenwörterbuch**] in der linken Leiste von Analysis Workspace. (Alternative Möglichkeiten für den Zugriff auf das Datenwörterbuch sind unter „Zugriff auf das Datenwörterbuch“ in [Datenwörterbuch – Überblick](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) beschrieben.)

   Das Fenster „Datenwörterbuch“ wird angezeigt.

   ![data-dictionary.png](assets/data-dictionary.png)

   <!--double-check this screenshot. I mocked the admin view up a bit to get rid of the Dictionary health tab.-->

1. Vergewissern Sie sich, dass die Report Suite, die die Komponente enthält, die Sie ansehen möchten, im Dropdown-Menü ausgewählt ist. Standardmäßig wird die Report Suite angezeigt, in der Sie sich bereits befinden.

1. (Optional) Geben Sie im Suchfeld den Namen der Komponente ein, die Sie anzeigen möchten.

   Der Komponententyp kann sowohl durch Farbe als auch durch ein Symbol identifiziert werden. **Dimensionen** ![Dimensionsymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) sind orange, **Segmente** ![Segmentsymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) sind blau, **Datumsbereiche** ![Datumsbereichsymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) sind violett und **Metriken** ![Metriksymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg) sind grün. Das Adobe-Symbol zeigt entweder eine Vorlage für berechnete Metriken oder eine Segmentvorlage an und das Taschenrechnersymbol ![Taschenrechnersymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg) zeigt eine berechnete Metrik an, die von einer Analytics-Administratorin bzw. einem -Administrator in Ihrer Organisation erstellt wurde.

{{dd-filter-criteria}}

1. (Optional) Wählen Sie das Symbol **Sortieren** Symbol ![Komponenten sortieren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg) aus und wählen Sie dann eine der folgenden Filteroptionen, um die Liste der Komponenten zu sortieren:

   {{components-sort-options}}

1. Wählen Sie aus der Komponentenliste die Komponente aus, die Sie anzeigen möchten.

   Es werden die folgenden Informationen über die Komponente angezeigt:

   {{dd-component-information}}

1. (Optional) Ziehen Sie eine Komponente aus dem Datenwörterbuch in Analysis Workspace.
