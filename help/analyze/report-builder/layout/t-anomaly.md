---
description: Schritte zum Erstellen einer Fehlererkennungsanforderung in ReportBuilder.
title: Konfigurieren einer Anomalieerkennungsanforderung
topic: Report builder
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Konfigurieren einer Anomalieerkennungsanforderung

Schritte zum Erstellen einer Anomalieerkennungsanforderung in ReportBuilder.

1. Wählen Sie einen Trendbericht aus, z. B. einen Bericht für **Site-Metriken** &gt; **[!UICONTROL Traffic.]**
1. Wählen Sie im Menü [!UICONTROL Granularität anwenden]**den Eintrag[!UICONTROL Tag]**.

   >[!NOTE]
   >
   >The [!UICONTROL Anomaly Detection] menu is available only when you select Day granularity. Die Daten der letzten 30 Tage werden unabhängig vom gewählten Datumsbereich als Schulungszeitraum für statistische Daten verwendet.

1. After configuring date ranges, click **[!UICONTROL Next]**.

   Schritt Ergebnis 1. On the Request Wizard: Step 2 of 2, add a metric, such as **[!UICONTROL Visits]**.

   Schritt Ergebnis 1. For the added metric, click the **[!UICONTROL None]** link.

   ![Schritt Ergebnis](assets/anomaly_select.png)

1. Select **[!UICONTROL Anomaly Detection]** &gt; **[!UICONTROL `<selection>`]**.

   ![Schritt-Info](assets/anomaly_visit.png)

   Wenn Sie eine dieser Optionen wählen, erstellt das System für die Anomalieerkennung Kopien der ursprünglichen Metrik. Beispielsweise wird für die Besuchsmetrik der Gruppe [!UICONTROL Metrik] eine Metrik für die Untergrenze von Besuchen hinzugefügt.
1. Click **[!UICONTROL Finish]** and select the cell for output to Excel.

   See [Anomaly Detection](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) for definitions.
