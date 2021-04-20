---
description: 'Schritte zum Erstellen einer Anomalieerkennungsanforderung in Report Builder. '
title: Konfigurieren einer Anomalieerkennungsanforderung
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 98%

---


# Konfigurieren einer Anomalieerkennungsanforderung

Schritte zum Erstellen einer Anomalieerkennungsanforderung in Report Builder.

1. Wählen Sie einen Trendbericht aus, z. B. einen Bericht für **[!UICONTROL Site-Metriken]** > **[!UICONTROL Traffic]**.
1. Wählen Sie im Menü [!UICONTROL Granularität anwenden] den Eintrag **[!UICONTROL Tag]**.

   >[!NOTE]
   >
   >Das Menü [!UICONTROL Anomalieerkennung] ist nur verfügbar, wenn Sie als Granularität „Tag“ auswählen. Die Daten der letzten 30 Tage werden unabhängig vom gewählten Datumsbereich als Schulungszeitraum für statistische Daten verwendet.

1. Nach dem Konfigurieren der Datumsbereiche klicken Sie auf **[!UICONTROL Weiter]**.

   Schritt Ergebnis 1. Im Anforderungs-Assistenten, Schritt 2 von 2, fügen Sie eine Metrik hinzu, z. B. **[!UICONTROL Besuche]**.

   Schritt Ergebnis 1. Klicken Sie für die hinzugefügte Metrik auf den Link **[!UICONTROL Keine]**.

   ![Schritt Ergebnis](assets/anomaly_select.png)

1. Wählen Sie **[!UICONTROL Anomalieerkennung]** > **[!UICONTROL `<selection>`]** aus.

   ![Schritt-Info](assets/anomaly_visit.png)

   Wenn Sie eine dieser Optionen wählen, erstellt das System für die Anomalieerkennung Kopien der ursprünglichen Metrik. Beispielsweise wird für die Besuchsmetrik der Gruppe [!UICONTROL Metrik] eine Metrik für die Untergrenze von Besuchen hinzugefügt.
1. Klicken Sie auf **[!UICONTROL Fertigstellen]** und wählen Sie eine Zelle für die Ausgabe in Excel.

   Siehe [Anomalieerkennung](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) für Definitionen.
