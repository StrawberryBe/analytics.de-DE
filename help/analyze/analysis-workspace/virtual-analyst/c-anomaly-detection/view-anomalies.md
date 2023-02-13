---
description: Sie können Anomalien in einer Tabelle oder einem Liniendiagramm anzeigen.
title: Anomalien in Analysis Workspace anzeigen
feature: Anomaly Detection
role: User, Admin
exl-id: 32edc7f4-c9b9-472a-b328-246ea5b54d07
source-git-commit: bc56f3567d2285d063ef35f316e22699bdcf151d
workflow-type: ht
source-wordcount: '467'
ht-degree: 100%

---

# Anomalien in Analysis Workspace anzeigen

Sie können Anomalien in einer Tabelle oder einem Liniendiagramm anzeigen.

## Anzeigen von Anomalien in einer Tabelle {#section_869A87B92B574A38B017A980ED8A29C5}

Sie können Anomalien in einer Freiformtabelle für Zeitreihen anzeigen.

1. Wählen Sie das Symbol für die Spalteneinstellungen in der Spaltenüberschrift aus und stellen Sie sicher, dass die Option [!UICONTROL **Anomalien**] in der Optionsliste ausgewählt ist. Weitere Informationen finden Sie unter [Spalteneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md).

1. Klicken Sie auf eine Stelle außerhalb des Einstellungsmenü, um die aktualisierte Tabelle anzuzeigen.

   ![](assets/anomaly_detected.png)

1. Anomalien werden in der Tabelle wie folgt angezeigt:

   In der oberen rechten Ecke jeder Zeile, in der eine Datenanomalie erkannt wird, wird ein **dunkelgraues Dreieck** angezeigt.

   Die farbige **senkrechte Linie** in jeder Zeile zeigt den erwarteten Wert an. Im farbig **schattierten Bereich** in jeder Zeile wird der tatsächliche Wert angezeigt. Der Vergleich der Linie (erwarteter Wert) mit dem schattierten Bereich (tatsächlicher Wert) bestimmt, ob eine Anomalie vorliegt. (Eine Anomalie wird auf der Basis fortschrittlicher statistischer Verfahren erkannt, die im Abschnitt [In der Anomalieerkennung verwendete statistische Verfahren](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) beschrieben werden.)

1. Wählen Sie das graue Dreieck in der oberen rechten Ecke einer Zeile aus, um Details über die Anomalie zu erfahren. Angezeigt wird das Ausmaß (in Prozent), in dem der tatsächliche Wert über oder unter dem erwarteten Wert liegt.

## Darstellen von Anomalien in einem Liniendiagramm {#section_7C1192AFDB4345A8A2CCFB3AE0C47D82}

Anomalien können ausschließlich in Liniendiagrammen visuell dargestellt werden.

So stellen Sie Anomalien in einem Liniendiagramm dar:

1. Wählen Sie in der Visualisierungskopfzeile das Einstellungssymbol aus und achten Sie darauf, dass die Option [!UICONTROL **Anomalien anzeigen**] in der Optionsliste ausgewählt ist. Weitere Informationen finden Sie im Abschnitt [Linie](/help/analyze/analysis-workspace/visualizations/line.md).

1. (Optional) Damit das Konfidenzintervall das Diagramm skalieren kann, wählen Sie das Einstellungssymbol in der Visualisierungskopfzeile und dann die Option **[!UICONTROL Anomalien können auf der Y-Achse skaliert werden]** aus.

   Diese Option ist nicht standardmäßig aktiviert, da das Diagramm dadurch unübersichtlicher werden kann.

1. Klicken Sie auf eine Stelle außerhalb des Einstellungsmenü, um das aktualisierte Liniendiagramm anzuzeigen.

   ![](assets/anomaly_linechart.png)

   Anomalien werden im Liniendiagramm wie folgt dargestellt:

   Ein **weißer Punkt** auf der Linie bedeutet, dass an dieser Stelle eine Datenanomalie erkannt wurde. (Eine Anomalie wird auf der Basis fortschrittlicher statistischer Verfahren erkannt, die im Abschnitt [In der Anomalieerkennung verwendete statistische Verfahren](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) beschrieben werden.)

   Der **hell schattierte Bereich** ist das Konfidenzband bzw. der erwartete Bereich, in dem Werte auftreten sollten. Jeder Wert, der außerhalb dieses erwarteten Bereichs liegt, ist eine Anomalie.

   Wenn das Liniendiagramm mehrere Metriken enthält, werden nur die Anomalien angezeigt. Bewegen Sie in diesem Fall den Mauszeiger über jede einzelne Anomalie, damit das Konfidenzband für diese Metrik eingeblendet wird.

   Die **gepunktete Linie** ist der erwartete Wert.

1. Durch Anklicken einer Anomalie (weißer Punkt) werden die folgenden Informationen angezeigt:

   * Das Datum, an dem die Anomalie auftrat

   * Der Rohdatenwert der Anomalie

   * Der Prozentwert über oder unter dem erwarteten Wert, der durch eine durchgezogene grüne Linie dargestellt wird.

   * Der Link „Analysieren“ zum Starten der [Beitragsanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md).





