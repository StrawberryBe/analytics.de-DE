---
description: Der Integrationscode erfordert, dass das Integrate-Modul in Ihrer Adobe Analytics-Bereitstellung vorhanden ist.
seo-description: Der Integrationscode erfordert, dass das Integrate-Modul in Ihrer Adobe Analytics-Bereitstellung vorhanden ist.
seo-title: Integrieren des Integrate-Moduls
title: Integrieren des Integrate-Moduls
uuid: e 574 f 3 db -49 fa -4 f 72-bbcf-fd 98540 d 3198
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Including the Integrate Module{#including-the-integrate-module}

Der Integrationscode erfordert, dass das Integrate-Modul in Ihrer Adobe Analytics-Bereitstellung vorhanden ist.

Wenn Sie das Integrate-Modul noch nicht Teil Ihrer Bereitstellung haben, führen Sie abhängig vom Typ der Implementierung die folgenden Schritte aus.

## For AppMeasurement v1.0+ {#section-f28d090bf2404cabaae34cd9c66fc575}

1. Unzip the AppMeasurement zip file that you downloaded from **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL CodeManager]**.

1. Open the file named [!DNL AppMeasurement_Module_Integrate.js].
1. Copy and paste the contents of this file into your primary [!DNL AppMeasurement.js] file.

   >[!NOTE]
   >
   >Fügen Sie es direkt vor dem Kommentar "DO NOT ALTER ANYTHING BELOW THIS LINE" in die Datei ein.

## For Legacy Code (H-code) {#section-bba8ad8c715e4f97883e7de3269f681a}

1. Laden Sie das Integrate-Modul aus dem Bereich "Ressourcen" in der Data Connectors-Benutzeroberfläche (auf der Registerkarte Support) herunter.

   ![](assets/h_code.png)

1. Copy and paste the contents of that file into your [!DNL s_code] file.

   >[!NOTE]
   >
   >Fügen Sie es direkt vor dem Kommentar "DO NOT ALTER ANYTHING BELOW THIS LINE" in die Datei ein.

