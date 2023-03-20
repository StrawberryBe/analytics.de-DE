---
description: Das Datenwörterbuch in Analysis Workspace ermöglicht es Benutzenden, die verschiedenen Komponenten in Analysis Workspace zu katalogisieren und im Auge zu behalten, einschließlich ihres Verwendungszwecks, welche genehmigt sind, welche Duplikate sind usw.
title: Einträge im Datenwörterbuch bearbeiten
feature: Components
role: Admin
source-git-commit: 8edd7b1b90e2ac3137bea734e5a0f1cb8004e743
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 63%

---

# Bearbeiten von Komponenteneinträgen im Datenwörterbuch

{{release-limited-testing}}

Analytics-Admins können Komponenteneinträge im Datenwörterbuch für eine bestimmte Report Suite bearbeiten. Alle vorgenommenen Änderungen sind für alle Benutzenden der Report Suite sichtbar.

Bearbeiten einer Komponente im Datenwörterbuch:

1. Wechseln Sie zum Analysis Workspace-Projekt, das die zu bearbeitende Komponente enthält.

1. Wählen Sie das Symbol **Datenwörterbuch** in der linken Leiste von Analysis Workspace. (Alternative Möglichkeiten für den Zugriff auf das Datenwörterbuch sind unter „Zugriff auf das Datenwörterbuch“ in [Datenwörterbuch – Überblick](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) beschrieben.)

   Das Fenster „Datenwörterbuch“ wird angezeigt.

   ![Adminansicht des Datenwörterbuchs](assets/data-dictionary-admin.png)

1. Stellen Sie sicher, dass im Dropdown-Menü die richtige Report Suite ausgewählt ist. Standardmäßig wird die Report Suite angezeigt, in der Sie sich bereits befinden.

1. (Optional) Geben Sie im Suchfeld den Namen der Komponente ein, die Sie bearbeiten möchten.

   Neben den Komponentennamen werden Symbole angezeigt, die den Komponententyp angeben:

   | Symbol | Bedeutung |
   |---------|----------|
   | ![Symbol &quot;Dimension&quot;](assets/dimension-icon.png) | Gibt einen **Dimension**. Dimensionen werden durch Adobe bereitgestellt. Vorhandene Dimensionen können nicht geändert werden und neue Dimensionen können nicht erstellt werden. |
   | ![Metriksymbol](assets/default-metric-icon.png) | Gibt einen **Standardmetrik** (nicht berechnet). Standardmetriken werden von Adobe bereitgestellt und können nicht geändert werden. |
   | ![Symbol &quot;Adobe&quot;](assets/default-calc-metric-icon.png) | Gibt einen **Vorlage für berechnete Metriken**. Hierbei handelt es sich um berechnete Metriken, die von Adobe bereitgestellt werden und nicht geändert werden können. |
   | ![Symbol &quot;Rechner&quot;](assets/calculated-metric-icon-created.png) | Gibt einen **berechnete Metrik** wurde von einem Analytics-Administrator in Ihrem Unternehmen erstellt. <!-- Delete all the comments... Components with this icon can be modified by an Analytics administrator. New calculated metrics can be created by an Analytics administrator, as described in [Metrics](/help/analyze/analysis-workspace/components/apply-create-metrics.md). --> |
   | ![Segmentsymbol](assets/segment-icon.png) | Gibt einen **Segment**. Hierbei kann es sich um von Adobe bereitgestellte oder von einem Analytics-Administrator in Ihrem Unternehmen erstellte Segmente handeln.<!-- Segments that were created byComponents with this icon can be modified by an Analytics administrator, as described in [Edit component entries in the Data Dictionary](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md). New calculated metrics can also be created by an Analytics administrator, as described in [Metrics](/help/analyze/analysis-workspace/components/apply-create-metrics.md). --> |
   | ![Symbol für Datumsbereich](assets/date-range-icon.png) | Gibt einen **Datumsbereich**. Dabei kann es sich um Datumsbereiche handeln, die von Adobe bereitgestellt oder von einem Analytics-Administrator in Ihrem Unternehmen erstellt werden. <!-- Components with this icon can be modified by an Analytics administrator. New date ranges can also be created by an Analytics administrator, as described in [Create custom date ranges](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md). --> |

{{dd-filter-criteria}}

1. Wählen Sie aus der Komponentenliste die Komponente aus, die Sie bearbeiten möchten.

1. Wählen Sie das Symbol **Bearbeiten** ![Datenwörterbuch bearbeiten](assets/data-dictionary-edit-icon.png) neben dem Komponentennamen.

1. Bearbeiten Sie eine der folgenden Informationen zur Komponente:

   {{dd-component-information}}

1. Klicken Sie auf das Symbol **Speichern** ![Datenwörterbuch speichern](assets/data-dictionary-save-icon.png), um Ihre Änderungen zu speichern.
