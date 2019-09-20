---
description: Fügen Sie bei der manuellen Bereitstellung des Dynamic Tag Managements in Adobe Analytics AppMeasurement-Code ein.
keywords: Dynamisches Tag-Management;Verknüpfte Konten;Konten;Code bearbeiten;AppMeasurement;AppMeasurement-Code
seo-description: Fügen Sie bei der manuellen Bereitstellung des Dynamic Tag Managements in Adobe Analytics AppMeasurement-Code ein.
seo-title: Grundlegenden AppMeasurement-Code einfügen
solution: Experience Cloud, Analytics, Target, Dynamisches Tag-Management
title: Grundlegenden AppMeasurement-Code einfügen
uuid: 3f83fbb1-3ed5-4e45-888a-0a183aac1a90
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Grundlegenden AppMeasurement-Code einfügen

Fügen Sie bei der manuellen Bereitstellung des Dynamic Tag Managements in Adobe Analytics AppMeasurement-Code ein.

1. Erweitern Sie auf der Seite [!DNL Adobe Analytics] den Abschnitt **Allgemein** und klicken Sie dann auf **[!UICONTROL Editor öffnen]**.
1. Unzip the [!DNL AppMeasurement_JavaScript*.zip] file you downloaded in [deploy Adobe Analytics](../../../implement/c-implement-with-dtm/t-analytics-deploy.md#task_3A00639CADF14C9C844F962222077E4E).

   Sollten Sie sich für eine benutzerdefinierte Bibliothek entscheiden, wird beim Öffnen des Fensters bereits die aktuellste Codeversion angezeigt. Die zip-Datei muss nicht aus der Admin Console heruntergeladen werden.
1. Open [!DNL AppMeasurement.js] in a text editor.
1. Copy and paste the contents into the **[!UICONTROL Edit Code]** window.

   ![](assets/edit-code.png)

1. Adobe recommends adding the following code above the *`Do Not Alter Anything Below This Line`*:

   ```
   var s_account="INSERT-RSID-HERE"
   var s=s_gi(s_account)
   ```

   >[!IMPORTANT]
   >
   >If you add this code, it is recommended that you also select the **[!UICONTROL Set report suites using custom code below]** checkbox in the overall library settings.

1. Click **[!UICONTROL Save and Close]**.

   Wenn Sie das Media-Modul, Integrate-Modul oder Implementation-Plug-ins verwenden, können Sie diese ebenfalls in den Codeabschnitt kopieren. Der verwaltete Code im Dynamic Tag Management kann genauso wie die JavaScript-Datei in einer normalen Implementierung konfiguriert werden.

