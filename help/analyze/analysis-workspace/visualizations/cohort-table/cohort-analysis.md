---
keywords: Analysis Workspace
title: Was ist eine Kohortenanalyse?
topic: Reports and analytics
uuid: 39a83f3a-15d1-41d7-bcdd-50c22aed8f1c
translation-type: tm+mt
source-git-commit: 99232c5bce94cfc55b9f01080555cb8e545442e9

---


# Was ist eine Kohortenanalyse?

Eine *`cohort`* ist eine Personengruppe mit gemeinsamen Merkmalen innerhalb eines vorgegebenen Zeitraums. Die Kohortenanalyse ist z. B. dann nützlich, wenn Sie wissen möchten, wie eine Kohorte mit einer Marke interagiert. Sie können problemlos Trend-Änderungen offenlegen und entsprechend reagieren. (Erläuterungen zur Kohortenanalyse sind im Internet verfügbar, z. B. unter [Cohort Analysis 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

Nachdem Sie einen Kohortenbericht erstellt haben, können Sie seine Komponenten (bestimmte Dimensionen, Metriken und Segmente) kuratieren und den Kohortenbericht dann für andere freigeben. See [Curate and Share](/help/analyze/analysis-workspace/curate-share/curate.md).

Beispiele für die Nutzung einer Kohortenanalyse:

* Starten Sie Kampagnen, die eine gewünschte Aktion auslösen sollen.
* Verschiebt das Marketingbudget genau zum richtigen Zeitpunkt im Kundenlebenszyklus.
* Erkennen Sie, wann eine Testversion oder ein Angebot beendet werden soll, um den Wert zu maximieren.
* Erhalten Sie Ideen für A/B-Tests in Bereichen wie Preisgestaltung, Aktualisierungspfad usw.
* Ansicht eines Berichts zur Kohorte-Analyse in einem Bericht zur geführten Analyse.

Die Analyse der Kohorte steht allen Analytics-Kunden mit Zugriffsrechten auf den Analyse Workspace zur Verfügung.

[Kohortenanalyse auf YouTube](https://www.youtube.com/watch?v=kqOIYrvV-co&index=45&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (4:36)

>[!IMPORTANT]
>
>Die Kohortenanalyse unterstützt keine berechneten Metriken.

## Funktionen der Kohortenanalyse

Im Januar 2019 veröffentlichte Adobe eine neue und deutlich verbesserte Version der Kohortenanalyse. Sie erhalten damit eine sehr viel feinere Steuerung der Kohorten, die Sie erstellen. Die folgenden Erweiterungen wurden vorgestellt:

### Bindungstabelle

Ein Bindungskohortenbericht gibt Besucherdaten aus: Jede Datenzelle zeigt die Roh- und Prozentanzahl der Besucher in der Kohorte, die die Aktion während dieses Zeitraums ausgeführt haben. Sie können bis zu 3 Kennzahlen und bis zu 10 Segmente einschließen.

![](assets/retention-report.png)

### Abwanderungstabelle

Eine Abwanderungskohorte ist die Umkehrung einer Bindungstabelle und zeigt Besucher, die abgewandert sind oder die Rückkehrkriterien für Ihre Kohorte im Laufe der Zeit nie erfüllt haben. Sie können bis zu 3 Kennzahlen und bis zu 10 Segmente einschließen.

![](assets/churn-report.png)

### Rollierende Berechnung

Ermöglicht es Ihnen, die Bindung oder die Abwanderung auf Grundlage der vorherigen Spalte und nicht der Aufnahmespalte zu berechnen.

![](assets/cohort-rolling-calculation.png)

### Latenztabelle

Misst die Zeit, die vor und nach dem Aufnahmeereignis verstrichen ist. Ein hervorragendes Tool für die Vor- und Nachanalyse. Die Spalte &quot;Einbezogen&quot;befindet sich in der Mitte der Tabelle und die Zeiträume vor und nach dem Einschluss-Ereignis werden auf beiden Seiten angezeigt.

![](assets/cohort-latency.png)

### Angepasste Dimensionskohorte

Erstellen Sie Kohorten auf Grundlage einer ausgewählten Dimension und nicht auf Grundlage zeitbasierter Kohorten, die Standardeinstellung sind. Verwenden Sie Dimensionen wie Marketing-Kanal, Kampagne, Produkt, Seite, Region oder andere Dimensionen in Adobe Analytics, um zu zeigen, wie sich die Bindung je nach den verschiedenen Werten dieser Dimensionen ändert.

![](assets/cohort-customizable-cohort-row.png)

Anweisungen zum Einrichten und Durchführen eines Kohortenberichts finden Sie unter  [Konfigurieren eines Kohortenanalyseberichts](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).

