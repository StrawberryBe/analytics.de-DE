---
description: Schritte zum Erstellen einer grundlegenden Report Builder-Datenanforderung.
title: Datenanforderung erstellen
topic: Report builder
uuid: 5d0151f1-e23d-43eb-84a4-96ae06c3a564
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Report Builder-Datenanforderung erstellen

Schritte zum Erstellen einer grundlegenden Datenanforderung.

1. In Excel, click **[!UICONTROL Create]**.
1. Wählen Sie im [!UICONTROL Request Wizard: Step 1] Fenster eine [Report Suite](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md)aus.
1. (Optional) Wählen Sie ein Segment, auf das Sie die Anforderung anwenden möchten. Wenn Sie eines oder mehrere Segmente ausgewählt haben, werden diese an den Anfang der Liste verschoben.

   Report Builder verwendet Segmente auf dieselbe Weise wie Adobe Analytics. Weitere Informationen finden Sie im [Analytics-Segmentierungshandbuch](https://marketing.adobe.com/resources/help/de_DE/analytics/segment/). 1. (Optional) Wählen Sie eine [Veröffentlichungsliste](/help/analyze/report-builder/data-requests/allow-publishing-list-overrides.md) für die Verteilung aus.
1. Wählen Sie einen [Berichtstyp](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md) aus.
1. Definieren Sie einen [Datumsbereich](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md) und eine [Granularität](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md) für den Bericht.
1. Klicken Sie auf **[!UICONTROL Next]**.
1. Geben Sie im Fenster [Layout – Anforderungs-Assistent: Schritt 2](/help/analyze/report-builder/layout/layout.md) ein Layout an:

   | Element | Beschreibung |
   |---|---|
   | Pivot-Layout | Stellt ein Zeilen-, Spalten- und Metrik-Raster für das Layout zur Verfügung, das Excel-Standardtabellen ähnelt. Mithilfe dieses Layouts können Sie Aufschlüsselungsanforderungen innerhalb der ursprünglichen Anforderung hinzufügen. |
   | Benutzerdefiniertes Layout | Provides most of the functionality of the [!UICONTROL Pivot Layout] but lets you choose where each item in the grid should be located in the spreadsheet. Dieses Layout bietet die Flexibilität, die von früheren Versionen bekannt ist. |

1. On the [!UICONTROL Metrics] tab, double-click (or drag) metrics in the tree to add them to the [!UICONTROL Metrics] grid.
1. On the [!UICONTROL Dimensions] tab, double-click (or drag) dimensions to the [!UICONTROL Row Labels] grid.

   Die in Schritt 2 verfügbaren [Dimensionen](https://marketing.adobe.com/resources/help/de_DE/reference/dimensions.html) hängen davon ab, welchen Basisbericht Sie in Schritt 1 gewählt haben und wie Ihre Report Suite konfiguriert ist. The dimensions are items that correlate, sub-relate, or are a classification of the original report type metric you selected on the [!UICONTROL Request Wizard: Step 1] window. Wenn Sie in Schritt 2 mehr als eine Dimension hinzufügen, wird dadurch eine Aufschlüsselung der Datenanforderung erreicht.

   Siehe [Metriken und Dimensionen hinzufügen](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) für weitere Informationen.
