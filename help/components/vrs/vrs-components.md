---
description: Virtual Report Suites können kuratiert werden, um Komponenten einzuschließen und auszuschließen.in Analyse Workspace.
title: Zusammenstellung der Virtual Report Suite-Komponenten
uuid: 6c6a4071-22ad-4e8c-b1ed-140b2aa04f76
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Zusammenstellung der Virtual Report Suite-Komponenten

Virtual Report Suites können kuratiert werden, um Komponenten einzuschließen und auszuschließen.in Analyse Workspace.

>[!NOTE]Die Änderungen betreffen die Komponenten, die Administratoren und Benutzer ohne diese Rolle in kuratierten Workspace-Projekten und kuratierten Virtual Report Suites (VRSs) anzeigen können. Zuvor konnte jeder nicht kuratierte Komponenten sehen, indem er auf **[!UICONTROL Show all Components]**. The [updated curation experience](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/curate-projects-vrs.html) allows for more fine-grained control over which components are visible.

So ermöglichen Sie die Kuratierung von Komponenten:

1. Öffnen von **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Virtual Report Suites]** > **[!UICONTROL Create new virtual report suite]**.
1. Klicken Sie nach dem Definieren der **[!UICONTROL Settings]** Registerkarte auf die **[!UICONTROL Components]** Registerkarte.

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Enable Customization of Virtual Report Suite Components]**:

   ![](assets/vrs-enable.png)

   >[!NOTE]
   >
   >Bei Aktivierung der Komponentenanpassung ist die Virtual Report Suite **nur über Analysis Workspace** zugänglich, nicht aber über Folgendes:

   * [!UICONTROL Reports & Analytics]
   * [!UICONTROL Ad Hoc Analysis]
   * [!UICONTROL Data Warehouse]
   * [!UICONTROL Report Builder]
   * Analytics-Reporting-API
   Nach der Aktivierung können Sie die Komponenten, die Sie in die Virtual Report Suite aufnehmen möchten, hinzufügen, indem Sie die entsprechenden Komponenten aus der Spalte &quot;Ausgeschlossene Komponenten&quot;in die Spalte &quot;Einbezogene Komponenten&quot;ziehen. Folgende Komponenten können einbezogen und ausgeschlossen werden:

   * Dimensionen
   * Metriken
   * Segmente
   * Datumsbereiche
   >[!NOTE]
   >
   >Kuratierte Komponenten (Segmente, berechnete Metriken, Datumsbereiche) müssen nicht *freigegeben* werden. Für die Virtual Report Suite kuratierte Komponenten sind in Analysis Workspace stets sichtbar, auch wenn sie nicht freigegeben werden.

1. Additionally, you can filter or search the components and add the entire filtered selection to the included column by clicking **[!UICONTROL Add All]**.

   ![](assets/vrs-add-all.png)

## Umbenannte Komponenten {#section_0F7CD9F684FE4765BC00A2AFED56550E}

Sie können die Anzeigenamen der eingeschlossenen Komponenten ändern, die für die Virtual Report Suite spezifisch sind. Wenn Sie z. B. den Seitennamen in die Virtual Report Suite aufnehmen möchten, ihn aber in einen benutzerfreundlicheren Kontext umbenennen möchten, können Sie ihn in App-Bildschirme ändern. Der neue Name wird im Arbeitsbereich für Analysen immer dann angezeigt, wenn diese Virtual Report Suite verwendet wird.

![](assets/vrs-rename-component.png)

Klicken Sie im Arbeitsbereich für Analyse auf das Informationssymbol für eine beliebige Komponente, um den Originalnamen der umbenannten Komponente anzuzeigen:

![](assets/vrs-aw-renamed.png)

## Komponentengruppen  {#section_483BEC76F49E46ADAAA03F0A12E48426}

Verwenden Sie Komponentengruppen, um Ihrer Virtual Report Suite Massenkomponenten hinzuzufügen. Wenn Sie z. B. einen Standardsatz von Komponenten importieren möchten, die für die mobile App-Analyse spezifisch sind, wählen Sie die Gruppe der mobilen App aus. Ein entsprechender Satz von Dimensionen und Metriken (bereits umbenannt) wird automatisch der Virtual Report Suite Included Liste hinzugefügt.

![](assets/vrs-comp-grp.png)

## Workspace-Verhalten {#section_6C32F8B642804C0097FCB14E21028D4A}

Weitere Informationen zum Kuratieren in Analysis Workspace finden Sie unter [Kuratieren und Freigeben von Projekten](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/curate.html).
