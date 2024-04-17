---
description: Konfigurieren Sie das Cloud-Importkonto und den Speicherort, an den Classification-Daten hochgeladen werden können.
keywords: Analysis Workspace
title: Standorte-Manager
feature: Classifications
exl-id: ace70568-220a-44e8-8e5f-f73002b9e2a2
source-git-commit: 7b293c962428c7b8fac62a9f70ce62a0fe8f0cea
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 1%

---

# Standorte-Manager

Mit dem Locations Manager können Sie Konten und Standorte anzeigen, erstellen, bearbeiten oder löschen. Diese können für einen der folgenden Zwecke verwendet werden:

* Exportieren von Dateien mithilfe von [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md)
* Exportieren von Berichten mithilfe von [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Importieren von Schemata mit [Klassifizierungssätze](/help/components/classifications/sets/overview.md)

## Anzeigen, Filtern und Suchen von Standorten

Mit dem Standort-Manager können Sie alle von Ihnen erstellten Standorte anzeigen. Systemadministratoren können von allen Benutzern erstellte Standorte anzeigen.

1. Um auf den Locations Manager in Adobe Analytics zuzugreifen, wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]**.

1. (Bedingt) Wenn Sie Systemadministrator sind, können Sie die [!UICONTROL **Anzeigen von Standorten für alle Benutzer**] -Option zum Anzeigen von Orten, die von allen Benutzern in Ihrer Organisation erstellt wurden. <!-- Maybe add a screenshot? This is new functionality -->

1. Filtern oder durchsuchen Sie die Liste der Standorte:

   * **Filter:** Wählen Sie das Symbol Filter aus, um die Liste der Standorte zu filtern.

     Sie können Standorte nach **[!UICONTROL Location Type]**, **[!UICONTROL Konto]** oder **[!UICONTROL Erstellt von]**.

     ![Standortfilter](assets/locations-filters.png)

   * **Suchen:** Geben Sie im Suchfeld den Namen des Standorts ein, den Sie anzeigen möchten. Die Ergebnisse werden bei der Eingabe gefiltert. Die folgenden Spalten werden durchsucht: **Ortsname**, **Location Type**, **Konto**, und **Erstellt von**.

1. (Optional) Wenn Sie mehr als 1.000 Standorte haben, werden nur die ersten 1.000 angezeigt. Auswählen [!UICONTROL **Mehr laden**] , um 1.000 weitere Standorte zu laden.

## Spalten im Locations Manager konfigurieren

Die folgenden Spalten sind im Locations Manager verfügbar. Um die in der Tabelle angezeigten Spalten anzupassen, wählen Sie die **Tabelle anpassen** icon ![Symbol &quot;Tabelle anpassen&quot;](assets/customize-table-icon.png).

* **[!UICONTROL Ortsname]**: Der Standortname. Wählen Sie das 3-Punkt-Menü neben einem Ortsnamen aus, um [Speicherort bearbeiten](/help/components/locations/configure-import-locations.md) oder löschen Sie sie.
* **[!UICONTROL Standorttyp]**: Der Kontotyp, der mit dem Standort verknüpft ist.
* **[!UICONTROL Konto]**: Das spezifische Konto, das mit dem Standort verknüpft ist.
* **Anwendung**: Der Anwendungstyp, mit dem der Speicherort verwendet werden kann (z. B. Daten-Feeds, Data Warehouse oder Classification-Sets).
* **[!UICONTROL Zuletzt verwendet]**: Das Datum, an dem der Standort zuletzt verwendet wurde.
* **[!UICONTROL Erstellt von]**: Der Benutzer, der den Standort erstellt hat.
* **[!UICONTROL Erstellungsdatum]**: Das Datum, an dem der Speicherort erstellt wurde.

## Erstellen und Verwalten von Standorten

Sie können Speicherorte erstellen, bearbeiten und löschen.

### Erstellen eines Standorts

Informationen zum Erstellen eines Standorts finden Sie unter [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md).

<!-- Do I need to add some steps here about how to create a location and then assign that location to be used with DF, DW, or Classifications sets? Need to hear back from Ron and team whether we are including this functionality -->

### Speicherort bearbeiten

Informationen zum Bearbeiten eines Standorts finden Sie unter [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md).

### Löschen eines Speicherorts

>[!IMPORTANT]
>
>Wenn ein Speicherort gelöscht wird, schlagen alle Daten-Feed-Dateien, Data Warehouse-Berichte oder Classification-Set-Schemata, die mit dem gelöschten Speicherort verknüpft sind, bei der nächsten Verwendung fehl.
>
>Wenn Sie einen Ort löschen, sollten Sie [Bearbeiten Ihrer Daten-Feeds](/help/export/analytics-data-feed/create-feed.md), [Data Warehouse-Berichte](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), und [Classification-Sets-Schemata](/help/components/classifications/sets/manage/schema.md) , um einen funktionierenden Standort zu verwenden.

So löschen Sie einen Speicherort:

1. Wählen Sie das Menü mit 3 Punkten im [!UICONTROL **Ortsname**] -Spalte für den Ort, den Sie löschen möchten.

1. Wählen Sie [!UICONTROL **Löschen**] aus.

## Konten bearbeiten

1. Um Konten im Locations Manager in Adobe Analytics zu bearbeiten, wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Standortkonten**] Registerkarte.

1. (Bedingt) Wenn Sie Systemadministrator sind, können Sie die [!UICONTROL **Anzeigen von Konten für alle Benutzer**] -Option zum Anzeigen von Orten, die von allen Benutzern in Ihrer Organisation erstellt wurden. <!-- Maybe add a screenshot? This is new functionality -->


1. Auswählen [!UICONTROL **Details anzeigen**] auf dem Konto, das Sie bearbeiten möchten.

1. Nehmen Sie die gewünschten Änderungen vor und wählen Sie dann [!UICONTROL **Speichern**].

## Kontoschlüssel anzeigen

Nachdem Sie ein Konto erstellt haben, können Sie alle zugehörigen Kontoschlüssel für dieses Konto anzeigen. Möglicherweise müssen Sie diese Informationen einsehen, wenn Sie die Konfiguration des Kontos mit Ihrem Cloud-Anbieter bei der [ursprünglich das Konto konfiguriert hat](/help/components/locations/configure-import-accounts.md).

So zeigen Sie Schlüssel an, die mit einem Exportkonto verknüpft sind:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Standortkonten**] Registerkarte.

1. Wählen Sie das 3-Punkt-Symbol für das Konto aus, das Sie bearbeiten möchten, und wählen Sie dann [!UICONTROL **Kontoschlüssel**].

## Löschen von Konten

1. Wählen Sie in Adobe Analytics **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Standortkonten**] Registerkarte.

1. Wählen Sie das 3-Punkt-Symbol für das Konto aus, das Sie bearbeiten möchten, und wählen Sie dann [!UICONTROL **Konto löschen**]
