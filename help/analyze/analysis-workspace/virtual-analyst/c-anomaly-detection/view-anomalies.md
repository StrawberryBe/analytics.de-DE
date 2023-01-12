---
description: Sie können Anomalien in einer Tabelle oder einem Liniendiagramm anzeigen.
title: Anomalien in Analysis Workspace anzeigen
feature: Anomaly Detection
role: User, Admin
exl-id: 32edc7f4-c9b9-472a-b328-246ea5b54d07
source-git-commit: bc56f3567d2285d063ef35f316e22699bdcf151d
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 16%

---

# Anomalien in Analysis Workspace anzeigen

Sie können Anomalien in einer Tabelle oder einem Liniendiagramm anzeigen.

## Anzeigen von Anomalien in einer Tabelle {#section_869A87B92B574A38B017A980ED8A29C5}

Sie können Anomalien in einer Freiformtabelle für Zeitreihen anzeigen.

1. Wählen Sie das Symbol für die Spalteneinstellungen in der Spaltenüberschrift aus und stellen Sie sicher, dass die [!UICONTROL **Anomalien**] in der Optionsliste ausgewählt ist. Weitere Informationen finden Sie unter [Spalteneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md).

1. Klicken Sie im Einstellungsmenü weg, um die aktualisierte Tabelle anzuzeigen.

   ![](assets/anomaly_detected.png)

1. Die Tabelle zeigt Anomalien wie folgt:

   A **dunkelgraues Dreieck** in der oberen rechten Ecke jeder Zeile angezeigt, in der eine Datenanomalie erkannt wird.

   Die Farben **vertikale Linie** in jeder Zeile gibt den erwarteten Wert an. Die Farben **schattierter Bereich** in jeder Zeile gibt den tatsächlichen Wert an. Wie sich die Linie (erwarteter Wert) mit dem schattierten Bereich (tatsächlicher Wert) vergleicht, bestimmt, ob eine Anomalie vorliegt. (Eine Beobachtung wird aufgrund der fortgeschrittenen statistischen Verfahren, die unter [In der Anomalieerkennung verwendete statistische Verfahren](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md).

1. Wählen Sie das graue Dreieck in der oberen rechten Ecke einer Zeile aus, um Details zur Anomalie anzuzeigen. Dies zeigt das Ausmaß (in Prozent), in dem der tatsächliche Wert über oder unter dem erwarteten Wert abweicht.

## Anzeigen von Anomalien in einem Liniendiagramm {#section_7C1192AFDB4345A8A2CCFB3AE0C47D82}

Liniendiagramme sind die einzige Visualisierung, mit der Sie Anomalien anzeigen können.

So zeigen Sie Anomalien in einem Liniendiagramm an:

1. Wählen Sie das Einstellungssymbol in der Visualisierungskopfzeile aus und stellen Sie sicher, dass die [!UICONTROL **Anomalien anzeigen**] in der Optionsliste ausgewählt ist. Weitere Informationen finden Sie unter [Linie](/help/analyze/analysis-workspace/visualizations/line.md).

1. (Optional) Damit das Konfidenzintervall das Diagramm skalieren kann, wählen Sie das Einstellungssymbol in der Visualisierungskopfzeile und dann die Option aus. **[!UICONTROL Anomalien können auf der Y-Achse skaliert werden]**.

   Diese Option ist standardmäßig nicht aktiviert, da sie das Diagramm manchmal weniger lesbar machen kann.

1. Klicken Sie im Einstellungsmenü weg, um das aktualisierte Liniendiagramm anzuzeigen.

   ![](assets/anomaly_linechart.png)

   Anomalien werden im Liniendiagramm wie folgt dargestellt:

   A **weißer Punkt** wird immer dann in der Zeile angezeigt, wenn eine Datenanomalie erkannt wird. (Eine Beobachtung wird aufgrund der fortgeschrittenen statistischen Verfahren, die unter [In der Anomalieerkennung verwendete statistische Verfahren](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md).

   Die **hellschattierter Bereich** ist das Konfidenzband bzw. der erwartete Bereich, in dem Werte auftreten sollten. Jeder Wert, der außerhalb dieses erwarteten Bereichs liegt, ist eine Anomalie.

   Wenn das Liniendiagramm mehrere Metriken enthält, werden nur die Anomalien angezeigt und Sie müssen den Mauszeiger über jede Anomalie bewegen, um das Konfidenzband für diese Metrik anzuzeigen.

   Die **gepunktete Linie** ist der genaue erwartete Wert.

1. Klicken Sie auf eine Anomalie (weißer Punkt), um die folgenden Informationen anzuzeigen:

   * Das Datum, an dem die Anomalie aufgetreten ist

   * Der Rohdatenwert der Anomalie

   * Der Prozentwert über oder unter dem erwarteten Wert, der durch eine durchgezogene grüne Linie dargestellt wird.

   * Der Link „Analysieren“ zum Starten der [Beitragsanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md).





