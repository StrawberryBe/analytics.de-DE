---
title: Was ist eine Kohortenanalyse?
description: Erfahren Sie mehr über die Analyse von Kohorten in Analysis Workspace
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 50%

---


# What is [!UICONTROL Cohort Analysis]?

Eine *`cohort`* ist eine Personengruppe mit gemeinsamen Merkmalen innerhalb eines vorgegebenen Zeitraums. [!UICONTROL Die Kohortenanalyse ist z. B. dann nützlich, wenn Sie wissen möchten, wie eine Kohorte mit einer Marke interagiert. ] Sie können problemlos Trend-Änderungen offenlegen und entsprechend reagieren. (Explanations of [!UICONTROL Cohort Analysis] are available on the web, such as at [Cohort Analysis 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

Nachdem Sie einen Kohortenbericht erstellt haben, können Sie dessen Komponenten (bestimmte Dimensionen, Metriken und Segmente) kuratieren und den Kohortenbericht dann für andere freigeben. Weitere Informationen finden Sie unter [Kuratieren und freigeben](/help/analyze/analysis-workspace/curate-share/curate.md).

Examples of what you can do with [!UICONTROL Cohort Analysis]:

* Starten Sie Kampagnen, die dafür ausgelegt sind, eine erwünschte Aktion anzuregen.
* Erhöhen Sie das Marketingbudget genau zum richtigen Zeitpunkt im Kundenlebenszyklus.
* Erkennen Sie, wann eine Testversion oder ein Angebot beendet werden soll, um den Wert zu maximieren.
* Gewinnen Sie Ideen für A/B-Tests in Bereichen wie Preisstruktur, Upgradepfad usw.
* View a [!UICONTROL Cohort Analysis] report within a Guided Analysis report.

[!UICONTROL Die Analyse] der Kohorte steht allen Adobe Analytics-Kunden mit Zugriffsrechten auf [!UICONTROL Analysis Workspace]zur Verfügung.

[Kohortenanalyse auf YouTube](https://www.youtube.com/watch?v=kqOIYrvV-co&amp;index=45&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (4:36)

>[!IMPORTANT]
>
>[!UICONTROL Kohortenanalyse]
>
>unterstützt keine nicht segmentfähigen Metriken (einschließlich berechneter Metriken), Nicht-Ganzzahlmetriken (z. B. Umsatz) oder Vorfälle. Nur Metriken, die in Segmenten verwendet werden können, können in
>[!UICONTROL Kohorte-Analyse], und sie können jeweils nur um 1 inkrementiert werden.

## Funktionen der Kohortenanalyse

Die folgenden Funktionen ermöglichen eine Feinabstimmung der Steuerung der erstellten Kohorten:

### [!UICONTROL Bindungstabelle]

A [!UICONTROL Retention] cohort report returns visitors: each data cell shows the raw number and percentage of visitors in the cohort who did the action during that time period. Sie können bis zu 3 Kennzahlen und bis zu 10 Segmente einschließen.

![](assets/retention-report.png)

### [!UICONTROL Abwanderungstabelle]

A [!UICONTROL Churn] cohort is the inverse of a retention table and shows the visitors who fell out or never met the return criteria for your cohort over time. Sie können bis zu 3 Kennzahlen und bis zu 10 Segmente einschließen.

![](assets/churn-report.png)

### [!UICONTROL Rollierende Berechnung]

Ermöglicht es Ihnen, die Bindung oder die Abwanderung auf Grundlage der vorherigen Spalte und nicht der Aufnahmespalte zu berechnen.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latenztabelle]

Misst die Zeit, die vor und nach dem Aufnahmeereignis verstrichen ist. Ein hervorragendes Tool für die Vor- und Nachanalyse. The **[!UICONTROL Included]** column is in the center of the table and time periods before and after the inclusion event are shown on both sides.

![](assets/cohort-latency.png)

### [!UICONTROL Angepasste Dimensionskohorte]

Erstellen Sie Kohorten auf Grundlage einer ausgewählten Dimension und nicht auf Grundlage zeitbasierter Kohorten, die Standardeinstellung sind. Use dimensions such as [!UICONTROL marketing channel], [!UICONTROL campaign], [!UICONTROL product], [!UICONTROL page], [!UICONTROL region], or any other dimension in Adobe Analytics to show how retention changes based on the different values of these dimensions.

![](assets/cohort-customizable-cohort-row.png)

Anweisungen zum Einrichten und Durchführen eines Kohortenberichts finden Sie unter [Konfigurieren eines Kohortenanalyseberichts](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).

