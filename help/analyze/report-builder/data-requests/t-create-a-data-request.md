---
description: Schritte zum Erstellen einer grundlegenden Reportbuilder-Datenanforderung.
seo-description: Schritte zum Erstellen einer grundlegenden Reportbuilder-Datenanforderung.
seo-title: Erstellen einer Reportbuilder-Datenanforderung
solution: Analytics
title: Datenanforderung erstellen
topic: ReportBuilder
uuid: 5 d 0151 f 1-e 23 d -43 eb -84 a 4-96 ae 6 a 3 a 564
translation-type: tm+mt
source-git-commit: 65b3c25288060b1b6d0b9590a8fdca4087f416a0

---


# Erstellen einer Reportbuilder-Datenanforderung

Schritte zum Erstellen einer grundlegenden Datenanforderung.

1. In Excel, click **[!UICONTROL Create]**.
1. In the [!UICONTROL Request Wizard: Step 1] window, select a [report suite](../../../analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md#task_59444416F6F042D1998217AE91580913).
1. (Optional) Wählen Sie ein Segment, auf das Sie die Anforderung anwenden möchten. Wenn Sie eines oder mehrere Segmente ausgewählt haben, werden diese an Anfang der Liste verschoben.

   ReportBuilder verwendet Segmente auf dieselbe Weise wie Adobe Analytics. Weitere Informationen finden Sie im [Analytics-Segmentierungshandbuch](https://marketing.adobe.com/resources/help/en_US/analytics/segment/). 1. (Optional) Select a [publishing list](../../../analyze/report-builder/data-requests/allow-publishing-list-overrides.md#concept_BCB19A20DC4B4B8D984F9670EE018D8C) to use for distribution.
1. Select a [report type](../../../analyze/report-builder/data-requests/c-report-types/select-report-types.md#concept_C711B27E6FB64C18AC564EE142FC7EFC).
1. Specify a [date range](../../../analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md) and report [granularity](../../../analyze/report-builder/data-requests/configuring-report-dates/granularity.md#concept_A13CBA2962E24FF882456135431B7ADB).
1. Click **[!UICONTROL Next]**.
1. In the [Layout - Request Wizard Step 2](../../../analyze/report-builder/layout/layout.md#concept_D66E1C2217E24E1F837AC064C61919DB) window, specify a layout:

   | Element | Beschreibung |
   |---|---|
   | Pivot-Layout | Stellt ein Zeilen-, Spalten- und Metrik-Raster für das Layout zur Verfügung, das Excel-Standardtabellen ähnelt. Mithilfe dieses Layouts können Sie Aufschlüsselungsanforderungen innerhalb der ursprünglichen Anforderung hinzufügen. |
   | Benutzerdefiniertes Layout | Gleicht im Wesentlichen dem [!UICONTROL Pivot-Layout], Sie können jedoch festlegen, an welcher Position des Arbeitsblatts sich die einzelnen Elemente des Rasters befinden sollen. Dieses Layout bietet die Flexibilität, die von früheren Versionen bekannt ist. |

1. Doppelklicken Sie auf der Registerkarte [!UICONTROL Metriken] auf Metriken, um sie dem Raster [!UICONTROL Metriken] hinzuzufügen (wahlweise können Sie die Metriken auch in das Raster ziehen).
1. Doppelklicken Sie auf der Registerkarte [!UICONTROL Dimensionen] auf Dimensionen, um sie dem Raster [!UICONTROL Zeilenbezeichnungen] hinzuzufügen.

   Die in Schritt 2 verfügbaren [Dimensionen](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=dimensions) hängen davon ab, welchen Basisbericht Sie in Schritt 1 gewählt haben und wie Ihre Report Suite konfiguriert ist. Die Dimensionen sind Elemente, die korrelieren, Unterbeziehungen herstellen oder eine Classification der im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 1] ausgewählten Berichtstypmetrik darstellen. Wenn Sie in Schritt 2 mehr als eine Dimension hinzufügen, wird dadurch eine Aufschlüsselung der Datenanforderung erreicht.

   Siehe [Metriken und Dimensionen hinzufügen](../../../analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md#task_E3F520C020F64C5A96DC5C96FEF71FC4) für weitere Informationen.