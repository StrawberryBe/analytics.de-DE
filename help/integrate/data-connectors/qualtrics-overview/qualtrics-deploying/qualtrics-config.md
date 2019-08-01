---
description: Nach Abschluss des Integrationsassistenten müssen Sie die Integration für jede Qualtrics-Umfrage aktivieren, die Sie verbinden möchten.
seo-description: Nach Abschluss des Integrationsassistenten müssen Sie die Integration für jede Qualtrics-Umfrage aktivieren, die Sie verbinden möchten.
seo-title: Aktivieren der Integration in Qualtrics Research Suite
solution: Analytics
subtopic: Qualtrics
title: Aktivieren der Integration in Qualtrics Research Suite
topic: Data Connectors
uuid: 2 cc 6 fa 4 a-d 17 e -4560-bd 5 b -1790851 d 6274
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Enabling the Integration in Qualtrics Research Suite{#enabling-the-integration-in-qualtrics-research-suite}

Nach Abschluss des Integrationsassistenten müssen Sie die Integration für jede Qualtrics-Umfrage aktivieren, die Sie verbinden möchten.

1. Melden Sie sich bei der Qualtrics Research Suite an.
1. On the **[!UICONTROL My Surveys]** tab, click the **[!UICONTROL Edit]** button for the survey that you want to integrate.
1. Click the **[!UICONTROL Advanced Options]** menu and select **[!UICONTROL Adobe Analytics]**. (Wenn diese Option nicht angezeigt wird, bitten Sie Ihren Administrator, die erforderlichen Berechtigungen zu erhalten.)

   ![](assets/advanced_options.png)

1. Select the Adobe Analytics Configuration, then click **[!UICONTROL Save]**. Wenn keine Konfigurationen verfügbar sind, haben Sie den Adobe Integration-Assistenten wahrscheinlich noch nicht abgeschlossen.
   1. The **[!UICONTROL Include Partial Responses]** checkbox can be used to indicate that you’d like to capture data into Adobe Analytics after each partial survey screen is completed. Wenn diese Option nicht aktiviert ist, werden Daten nur für vollständig abgeschlossene Umfragen übertragen.
   1. The **[!UICONTROL Send Timestamp With Beacon]** checkbox should be used only when integrating with a Report Suite that is configured to receive time-stamped data (not common).
   ![](assets/integration_config.png)

