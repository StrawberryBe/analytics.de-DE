---
description: Schritte zum Erstellen einer Anomalieerkennungsanforderung in ReportBuilder.
seo-description: Schritte zum Erstellen einer Fehlererkennungsanforderung in ReportBuilder.
seo-title: Konfigurieren einer Fehlererkennungsanforderung
solution: Analytics
title: Konfigurieren einer Anomalieerkennungsanforderung
topic: ReportBuilder
uuid: 1 e 504 ff 9-df 88-4 fa 7-95 ea -1 ca 05 a 6 f 9 c 0 d
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Konfigurieren einer Anomalieerkennungsanforderung

Schritte zum Erstellen einer Anomalieerkennungsanforderung in ReportBuilder.

1. Wählen Sie einen Trendbericht aus, z. B. einen Bericht für **Site-Metriken** &gt; **[!UICONTROL Traffic.]**
1. Wählen Sie im Menü [!UICONTROL Granularität anwenden]**den Eintrag[!UICONTROL Tag]**.

   >[!NOTE]
   >
   >The [!UICONTROL Anomaly Detection] menu is available only when you select Day granularity. Die Daten der letzten 30 Tage werden unabhängig vom gewählten Datumsbereich als Schulungszeitraum für statistische Daten verwendet.

1. After configuring date ranges, click **[!UICONTROL Next]**.

   Schritt 1. On the Request Wizard: Step 2 of 2, add a metric, such as **[!UICONTROL Visits]**.

   Schritt 1. For the added metric, click the **[!UICONTROL None]** link.

   ![Schrittergebnis](assets/anomaly_select.png)

1. Select **[!UICONTROL Anomaly Detection]** &gt; **[!UICONTROL `<selection>`]**.

   ![Schritt-Info](assets/anomaly_visit.png)

   Wenn Sie eine dieser Optionen wählen, erstellt das System für die Anomalieerkennung Kopien der ursprünglichen Metrik. Beispielsweise wird für die Besuchsmetrik der Gruppe [!UICONTROL Metrik] eine Metrik für die Untergrenze von Besuchen hinzugefügt.
1. Click **[!UICONTROL Finish]** and select the cell for output to Excel.

   See [Anomaly Detection](../../../analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md#concept_9476D6C093334B1A8044AE63835BDBE7) for definitions.
