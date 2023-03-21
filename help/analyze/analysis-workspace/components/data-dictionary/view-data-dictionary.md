---
description: Das Datenwörterbuch in Analysis Workspace ermöglicht es Benutzenden, die verschiedenen Komponenten in Analysis Workspace zu katalogisieren und im Auge zu behalten, einschließlich ihres Verwendungszwecks, welche genehmigt sind, welche Duplikate sind usw.
title: Datenwörterbuch anzeigen
feature: Components
role: User, Admin
source-git-commit: 5d83d2621ee5eee7dbbc2af3793a9e1d3de0f97b
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 58%

---

# Komponenteninformationen im Datenwörterbuch anzeigen

{{release-limited-testing}}

Mit dem Datenwörterbuch können Sie Informationen über eine Komponente anzeigen, einschließlich der Komponentenbeschreibung, ähnlicher Komponenten, anderer Komponenten, mit denen eine Komponente häufig verwendet wird, und mehr.

So zeigen Sie Informationen zu einer Komponente im Datenwörterbuch an:

1. Wechseln Sie zum Analysis Workspace-Projekt, das die Komponente enthält, die Sie anzeigen möchten.

1. Wählen Sie das Symbol [!UICONTROL **Datenwörterbuch**] in der linken Leiste von Analysis Workspace. (Alternative Möglichkeiten für den Zugriff auf das Datenwörterbuch sind unter „Zugriff auf das Datenwörterbuch“ in [Datenwörterbuch – Überblick](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) beschrieben.)

   Das Fenster „Datenwörterbuch“ wird angezeigt.

   ![data-dictionary.png](assets/data-dictionary.png)

   <!--double-check this screenshot. I mocked the admin view up a bit to get rid of the Dictionary health tab.-->

1. Vergewissern Sie sich, dass die Report Suite, die die Komponente enthält, die Sie ansehen möchten, im Dropdown-Menü ausgewählt ist. Standardmäßig wird die Report Suite angezeigt, in der Sie sich bereits befinden.

1. (Optional) Geben Sie im Suchfeld den Namen der Komponente ein, die Sie anzeigen möchten.

   Neben den Komponentennamen werden Symbole angezeigt, die den Komponententyp angeben:

   | Symbol | Bedeutung |
   |---------|----------|
   | ![Symbol &quot;Dimension&quot;](assets/dimension-icon.png) | Gibt einen **Dimension**. Dimensionen werden durch Adobe bereitgestellt. Vorhandene Dimensionen können nicht geändert werden und neue Dimensionen können nicht erstellt werden. |
   | ![Metriksymbol](assets/default-metric-icon.png) | Gibt einen **Standardmetrik** (nicht berechnet). Standardmetriken werden von Adobe bereitgestellt und können nicht geändert werden. |
   | ![Symbol &quot;Adobe&quot;](assets/default-calc-metric-icon.png) | Gibt einen **Vorlage für berechnete Metriken** oder **Segmentvorlage**. Diese Komponenten werden von Adobe bereitgestellt und können nicht geändert werden. |
   | ![Symbol &quot;Rechner&quot;](assets/calculated-metric-icon-created.png) | Gibt einen **berechnete Metrik** wurde von einem Analytics-Administrator in Ihrem Unternehmen erstellt. |
   | ![Segmentsymbol](assets/segment-icon.png) | Gibt einen **Segment**. Hierbei kann es sich um von Adobe bereitgestellte oder von einem Analytics-Administrator in Ihrem Unternehmen erstellte Segmente handeln. |
   | ![Symbol für Datumsbereich](assets/date-range-icon.png) | Gibt einen **Datumsbereich**. Dabei kann es sich um Datumsbereiche handeln, die von Adobe bereitgestellt oder von einem Analytics-Administrator in Ihrem Unternehmen erstellt werden. |

{{dd-filter-criteria}}

1. Wählen Sie aus der Komponentenliste die Komponente aus, die Sie anzeigen möchten.

   Es werden die folgenden Informationen über die Komponente angezeigt:

   {{dd-component-information}}

1. (Optional) Ziehen Sie eine Komponente aus dem Datenwörterbuch in Analysis Workspace.