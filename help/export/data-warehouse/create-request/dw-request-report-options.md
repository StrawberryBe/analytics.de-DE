---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anforderung erstellen.
title: Berichtsoptionen für eine Data Warehouse-Anforderung konfigurieren
feature: Data Warehouse
source-git-commit: 42c95198a4d4389308c78c312b5bb37572350cc1
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 16%

---

# Berichtsoptionen für eine Data Warehouse-Anforderung konfigurieren

{{release-limited-testing}}

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Im Folgenden wird beschrieben, wie Sie Berichtsoptionen für die Anforderung konfigurieren.

Informationen zum Erstellen einer Anforderung sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

So konfigurieren Sie Berichtsoptionen für eine Data Warehouse-Anforderung:

1. Erstellen einer Anforderung in Adobe Analytics durch Auswahl von **[!UICONTROL Instrumente]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**].

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite Neue Data Warehouse-Anforderung die [!UICONTROL **Berichtsoptionen**] Registerkarte.

   ![Berichtsziel-Tab](assets/dw-report-options.png) <!-- update screenshot to include Sort by metrics -->

1. Füllen Sie die folgenden Felder aus:

   | Option | Funktion |
   |---------|----------|
   | Dateiname | Gibt den Bericht an. |
   | Datumsbereich des Berichts an Dateinamen anhängen | Fügt den Datumsbereich zum Namen der Berichtsdatei hinzu. <p>Wenn Sie beispielsweise Daten vom 1. Mai 2024 bis zum 7. Mai 2024 anfordern, enthält der Dateiname den Datumsbereich 20240501 - 20240507.</p> |
   | CSV | Stellt Berichte im CSV-Dateiformat zur Anzeige von Daten in einer Tabelle bereit. |
   | Tableau (TDE) | Ermöglicht die Berichterstellung im Tableau-Datenextraktion-Dateiformat (TDE), mit dem Daten visualisiert und zusätzliche Daten in Tableau erfasst werden können. |
   | Bericht als komprimierte Datei senden (ZIP) | Stellt Berichte im komprimierten ZIP-Dateiformat bereit. Wir empfehlen, diese Option zu aktivieren, wenn E-Mails als [Berichtsziel](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). |
   | Anzahl der Zeilen in der Tabelle | Die Anzahl der Zeilen, die in den Bericht aufgenommen werden können. Verwenden Sie 0, um alle Zeilen einzuschließen (dies ist die Standardauswahl). <!-- when would you want to limit the rows? To improve performance? Do we have recommendations? --> |
   | Kommentare | Fügen Sie alle Kommentare hinzu, die Sie in den Bericht aufnehmen möchten. Kommentare werden zu Beginn des Berichts angezeigt. |
   | Nach Metriken sortieren | Bietet nach Rang geordnet Detailberichte in Data Warehouse, die nach absteigendem Metrikwert sortiert sind. Die Sortierung nach Metrik erleichtert die Interpretation von Data Warehouse-Berichten und den Vergleich mit anderen Ansichten von Analytics-Aufschlüsselungsberichten.<p>Weitere Informationen finden Sie unter [Nach Metrik sortieren](/help/export/data-warehouse/sorting-by-metric.md).</p> |
   | Manifestdatei senden | Enthält Metadaten zu den im Bericht enthaltenen Dateien.<!-- What kind of metadata is included in the manifest file? --> |
   | Digitale Signaturdatei senden | Ermöglicht Empfängern des Berichts zu überprüfen, ob die Datei von Adobe stammt und nicht verändert wurde. |
   | Leere Datei senden, wenn keine Daten im Bericht vorhanden sind | Sendet einen Bericht auch dann, wenn der Bericht keine Daten enthält. |

   {style="table-layout:auto"}

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der [!UICONTROL **Planungsoptionen**] Registerkarte. Weitere Informationen finden Sie unter [Planungsoptionen für Data Warehouse-Anfragen konfigurieren](/help/export/data-warehouse/create-request/dw-request-scheduling.md).