---
description: Schritte zum Erstellen einer grundlegenden Report Builder-Datenanforderung.
title: Datenanforderung erstellen
feature: Report Builder
role: User, Admin
exl-id: 21d552a0-7a58-4217-ba8a-7c87eb4757f6
source-git-commit: d2e4a6eed54fa8b3e080b162a5e841fc2f5a0e59
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 100%

---

# Report Builder-Datenanforderung erstellen

Schritte zum Erstellen einer grundlegenden Datenanforderung.

1. Klicken Sie in Excel auf **[!UICONTROL Erstellen]**.
1. Wählen Sie im Fenster [!UICONTROL Anforderungs-Assistent: Schritt 1] eine [Report Suite](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).
1. (Optional) Wählen Sie ein Segment, auf das Sie die Anforderung anwenden möchten. Wenn Sie eines oder mehrere Segmente ausgewählt haben, werden diese an den Anfang der Liste verschoben.

   Report Builder verwendet Segmente auf dieselbe Weise wie Adobe Analytics. Weitere Informationen finden Sie im [Analytics-Segmentierungshandbuch](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=de).
1. Wählen Sie einen [Berichtstyp](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md) aus.
1. Definieren Sie einen [Datumsbereich](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md) und eine [Granularität](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md) für den Bericht.
1. Klicken Sie auf **[!UICONTROL Weiter]**.
1. Geben Sie im Fenster [Layout – Anforderungs-Assistent: Schritt 2](/help/analyze/report-builder/layout/layout.md) ein Layout an:

   | Element | Beschreibung |
   |---|---|
   | Pivot-Layout | Stellt ein Zeilen-, Spalten- und Metrik-Raster für das Layout zur Verfügung, das Excel-Standardtabellen ähnelt. Mithilfe dieses Layouts können Sie Aufschlüsselungsanforderungen innerhalb der ursprünglichen Anforderung hinzufügen. |
   | Benutzerdefiniertes Layout | Gleicht im Wesentlichen dem [!UICONTROL Pivot-Layout], Sie können jedoch festlegen, an welcher Position des Arbeitsblatts sich die einzelnen Elemente des Rasters befinden sollen. Dieses Layout bietet die Flexibilität, die von früheren Versionen bekannt ist. |

1. Doppelklicken Sie auf der Registerkarte [!UICONTROL Metriken] auf Metriken, um sie dem Raster [!UICONTROL Metriken] hinzuzufügen (wahlweise können Sie die Metriken auch in das Raster ziehen).
1. Doppelklicken Sie auf der Registerkarte [!UICONTROL Dimensionen] auf Dimensionen, um sie dem Raster [!UICONTROL Zeilenbezeichnungen] hinzuzufügen.

   Die in Schritt 2 verfügbaren [Dimensionen](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/layout/filter-dimenson/filter-dimensions.html?lang=de) hängen davon ab, welchen Basisbericht Sie in Schritt 1 gewählt haben und wie Ihre Report Suite konfiguriert ist. Die Dimensionen sind Elemente, die korrelieren, Unterbeziehungen herstellen oder eine Classification der im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 1] ausgewählten Berichtstypmetrik darstellen. Wenn Sie in Schritt 2 mehr als eine Dimension hinzufügen, wird dadurch eine Aufschlüsselung der Datenanforderung erreicht.

   Siehe [Metriken und Dimensionen hinzufügen](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) für weitere Informationen.
