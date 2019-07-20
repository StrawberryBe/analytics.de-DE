---
description: Sie können Anomalien in einer Tabelle oder einem Liniendiagramm anzeigen.
seo-description: Sie können Anomalien in einer Tabelle oder einem Liniendiagramm anzeigen.
seo-title: Anomalien im Analysis Workspace anzeigen
title: Anomalien im Analysis Workspace anzeigen
uuid: 270 a 7 ea 9-6485-4 c 83-8220-5 a 2200 bd 7200
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Anomalien im Analysis Workspace anzeigen

Sie können Anomalien in einer Tabelle oder einem Liniendiagramm anzeigen.

## View anomalies in a table {#section_869A87B92B574A38B017A980ED8A29C5}

In einer Zeitreihen-Freiform-Tabelle wird nun jede Zeile automatisch mit einem dunkelgrauen Ausrufezeichen versehen, in der eine Datenanomalie erkannt wurde.

![](assets/anomaly_detected.png)

Die senkrechte graue Linie in jeder Zeile zeigt an, wo der erwartete Wert stehen sollte. Wenn Sie den Mauszeiger über ein Ausrufezeichen bewegen, wird angezeigt, wie weit die Anomalie vom erwarteten Wert abweicht (in + oder - %).

## View anomalies in a line chart {#section_7C1192AFDB4345A8A2CCFB3AE0C47D82}

Das Liniendiagramm zeigt die abnormen Werte (weiße Punkte) in einem hellgrünen Konfidenzband an. 

Wenn Sie auf einen weißen Punkt klicken, wird dieser grün und es wird Ihnen Folgendes angezeigt:

* Das Datum, an dem die Anomalie auftrat
* Der Rohdatenwert der Anomalie
* Der Prozentwert über oder unter dem erwarteten Wert, der durch eine durchgezogene grüne Linie dargestellt wird.
* Der Link „Analysieren“ zum Starten der [Beitragsanalyse](../../../../analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md).

![](assets/anomaly_linechart.png)

Wenn das Liniendiagramm mehrere Metriken enthält, werden nur die Anomalien angezeigt und Sie müssen den Mauszeiger über die einzelnen Metriken bewegen, damit das Konfidenzband für diese Metrik eingeblendet wird.

Der Vertrauensbereich der Anomalieerkennung skaliert nicht automatisch die Y-Achse einer Visualisierung, um das Diagramm nach Möglichkeit lesbarer zu machen.

Sie können festlegen, dass der Vertrauensbereich das Diagramm skaliert. Klicken Sie einfach auf das Symbol „Einstellungen“ (Zahnrad) und aktivieren Sie die Option **[!UICONTROL Anomalieerkennung erlauben, um die Y-Achse zu skalieren]**.

![](assets/scale-y-axis.png)

