---
description: Das Datenwörterbuch in Analysis Workspace ermöglicht es Benutzenden, die verschiedenen Komponenten in Analysis Workspace zu katalogisieren und im Auge zu behalten, einschließlich ihres Verwendungszwecks, welche genehmigt sind, welche Duplikate sind usw.
title: Einträge im Datenwörterbuch bearbeiten
feature: Components
role: Admin
exl-id: 4f15cad2-596e-41c3-89aa-4456d8e94fa0
source-git-commit: 631f84794203cb0a1154d68149c9d64d7247ecd3
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 70%

---

# Bearbeiten von Komponenteneinträgen im Datenwörterbuch

Analytics-Admins können Komponenteneinträge im Datenwörterbuch für eine bestimmte Report Suite bearbeiten. Alle vorgenommenen Änderungen sind für alle Benutzenden der Report Suite sichtbar.

Bearbeiten einer Komponente im Datenwörterbuch:

1. Wechseln Sie zum Analysis Workspace-Projekt, das die zu bearbeitende Komponente enthält.

1. Wählen Sie das Symbol **Datenwörterbuch** in der linken Leiste von Analysis Workspace. (Alternative Möglichkeiten für den Zugriff auf das Datenwörterbuch sind unter „Zugriff auf das Datenwörterbuch“ in [Datenwörterbuch – Überblick](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) beschrieben.)

   Das Fenster „Datenwörterbuch“ wird angezeigt.

   ![Adminansicht des Datenwörterbuchs](assets/data-dictionary-admin.png)

1. Stellen Sie sicher, dass im Dropdown-Menü die richtige Report Suite ausgewählt ist. Standardmäßig wird die Report Suite angezeigt, in der Sie sich bereits befinden.

1. (Optional) Geben Sie im Suchfeld den Namen der Komponente ein, die Sie bearbeiten möchten.

   Der Komponententyp kann sowohl durch Farbe als auch durch Symbol identifiziert werden. **Dimensionen** ![Symbol &quot;Dimension&quot;](assets/dimension-icon.png) orange sind, **Segmente** ![Segmentsymbol](assets/segment-icon.png) blau sind, **Datumsbereiche** ![Symbol für Datumsbereich](assets/date-range-icon.png) violett sind und **Metriken** ![Metriksymbol](assets/default-metric-icon.png) sind grün. Das Symbol Adobe ![Symbol &quot;Adobe&quot;](assets/default-calc-metric-icon.png) gibt entweder eine Vorlage für berechnete Metriken oder eine Segmentvorlage an und das Symbol für den Rechner ![Symbol &quot;Rechner&quot;](assets/calculated-metric-icon-created.png) eine berechnete Metrik angezeigt, die von einem Analytics-Administrator in Ihrer Organisation erstellt wurde.

{{dd-filter-criteria}}

1. (Optional) Wählen Sie die **Sortieren** icon ![Symbol &quot;Komponenten sortieren&quot;](assets/component-sort-icon.png)und wählen Sie eine der folgenden Filteroptionen aus, um die Liste der Komponenten zu sortieren:

   {{components-sort-options}}

1. Wählen Sie aus der Komponentenliste die Komponente aus, die Sie bearbeiten möchten.

1. Wählen Sie das Symbol **Bearbeiten** ![Datenwörterbuch bearbeiten](assets/data-dictionary-edit-icon.png) neben dem Komponentennamen.

1. Bearbeiten Sie eine der folgenden Informationen zur Komponente:

   {{dd-component-information}}

1. Klicken Sie auf das Symbol **Speichern** ![Datenwörterbuch speichern](assets/data-dictionary-save-icon.png), um Ihre Änderungen zu speichern.
