---
title: Was ist Kohorte-Analyse und wie funktioniert sie?
description: Informieren Sie sich genauer über die Daten rund um Ihre Audience und unterteilen Sie mit der Kohorten-Analyse die zugehörigen Gruppen. Erfahren Sie mehr über die Analyse der Kohorte in Analysis Workspace.
translation-type: tm+mt
source-git-commit: c588087b949093152435967f62e43758e9e86208
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 89%

---


# Weitere Informationen zur [!UICONTROL Kohorte-Analyse] in Adobe Analytics

Eine *`cohort`* ist eine Personengruppe mit gemeinsamen Merkmalen innerhalb eines vorgegebenen Zeitraums. Die [!UICONTROL Kohortenanalyse] ist z. B. dann nützlich, wenn Sie wissen möchten, wie eine Kohorte mit einer Marke interagiert. Sie können problemlos Trend-Änderungen offenlegen und entsprechend reagieren. (Erläuterungen zur [!UICONTROL Kohortenanalyse] sind im Internet verfügbar, z. B. unter [Cohort Analysis 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

Nachdem Sie einen Kohortenbericht erstellt haben, können Sie dessen Komponenten (bestimmte Dimensionen, Metriken und Segmente) kuratieren und den Kohortenbericht dann für andere freigeben. Weitere Informationen finden Sie unter [Kuratieren und freigeben](/help/analyze/analysis-workspace/curate-share/curate.md).

Beispiele für die Nutzung einer [!UICONTROL Kohortenanalyse]:

* Starten Sie Kampagnen, die dafür ausgelegt sind, eine erwünschte Aktion anzuregen.
* Erhöhen Sie das Marketingbudget genau zum richtigen Zeitpunkt im Kundenlebenszyklus.
* Erkennen Sie, wann eine Testphase oder ein Angebot beendet werden sollte, um den Wert zu maximieren.
* Gewinnen Sie Ideen für A/B-Tests in Bereichen wie Preisstruktur, Upgrade-Pfad usw.
* Zeigen Sie einen [!UICONTROL Kohortenanalysebericht] mit einem angeleiteten Analysebericht an.

Die [!UICONTROL Kohortenanalyse] steht allen Adobe Analytics-Kunden mit Zugriffsrechten auf [!UICONTROL Analysis Workspace] zur Verfügung.

[Videoschulung](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/cohort-analysis/cohort-analysis-workspace.html)  zur Kohorte-Analyse (4:36)

>[!IMPORTANT]
>
>[!UICONTROL Kohortenanalyse]
>
>unterstützt keine nicht segmentierbaren Metriken (einschließlich berechneter Metriken), Nicht-Ganzzahlmetriken (z. B. Umsatz) oder Vorfälle. Nur Metriken, die in Segmenten verwendet werden können, können in der
>[!UICONTROL Kohortenanalyse] verwendet werden. Sie können jeweils nur um 1 inkrementiert werden.

## Funktionen der Kohortenanalyse

Die folgenden Fähigkeiten ermöglichen eine fein abgestimmte Kontrolle über die erstellten Kohorten:

### [!UICONTROL Bindungstabelle]

Ein [!UICONTROL Bindungskohortenbericht] gibt Besucherdaten aus: Jede Datenzelle zeigt die Roh- und Prozentanzahl der Besucher in der Kohorte, die die Aktion während dieses Zeitraums ausgeführt haben. Sie können bis zu 3 Metriken und bis zu 10 Segmente einschließen.

![](assets/retention-report.png)

### [!UICONTROL Abwanderungstabelle]

Eine [!UICONTROL Abwanderungskohorte] ist die Umkehrung einer Bindungstabelle und zeigt Besucher, die abgewandert sind oder die Rückkehrkriterien für Ihre Kohorte im Laufe der Zeit nie erfüllt haben. Sie können bis zu 3 Metriken und bis zu 10 Segmente einschließen.

![](assets/churn-report.png)

### [!UICONTROL Rollierende Berechnung]

Ermöglicht es Ihnen, die Bindung oder die Abwanderung auf Grundlage der vorherigen Spalte und nicht der Aufnahmespalte zu berechnen.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latenztabelle]

Misst die Zeit, die vor und nach dem Aufnahmeereignis verstrichen ist. Ein hervorragendes Tool für die Vor- und Nachanalyse. Die Spalte **[!UICONTROL Aufnahme]** befindet sich in der Mitte der Tabelle und die Zeiträume vor und nach dem Aufnahmeereignis werden auf beiden Seiten angezeigt.

![](assets/cohort-latency.png)

### [!UICONTROL Angepasste Dimensionskohorte]

Erstellen Sie Kohorten auf Grundlage einer ausgewählten Dimension und nicht auf Grundlage zeitbasierter Kohorten, die Standardeinstellung sind. Verwenden Sie Dimensionen wie [!UICONTROL Marketing-Kanal], [!UICONTROL Kampagne], [!UICONTROL Produkt], [!UICONTROL Seite], [!UICONTROL Region] oder jede andere Dimension in Adobe Analytics, um anzuzeigen, wie die Bindung sich basierend auf verschiedenen Werten dieser Dimensionen verändert.

![](assets/cohort-customizable-cohort-row.png)

Anweisungen zum Einrichten und Durchführen eines Kohortenberichts finden Sie unter  [Konfigurieren eines Kohortenanalyseberichts](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).

