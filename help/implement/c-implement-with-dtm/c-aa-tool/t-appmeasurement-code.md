---
description: Fügen Sie bei der manuellen Bereitstellung des Dynamic Tag Managements in Adobe Analytics AppMeasurement-Code ein.
keywords: Dynamic Tag Management;verknüpfte Konten;Konten verknüpfen;Code bearbeiten;AppMeasurement;AppMeasurement-Code
seo-description: Fügen Sie bei der manuellen Bereitstellung des Dynamic Tag Managements in Adobe Analytics AppMeasurement-Code ein.
seo-title: Grundlegenden AppMeasurement-Code einfügen
solution: Experience Cloud, Analytics, Target, Dynamic Tag Management
title: Grundlegenden AppMeasurement-Code einfügen
uuid: 3f83fbb1-3ed5-4e45-888a-0a183aac1a90
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Grundlegenden AppMeasurement-Code einfügen

Fügen Sie bei der manuellen Bereitstellung des Dynamic Tag Managements in Adobe Analytics AppMeasurement-Code ein.

1. Erweitern Sie auf der Seite [!DNL Adobe Analytics] den Abschnitt **[!UICONTROL Allgemein]** und klicken Sie dann auf **[!UICONTROL Editor öffnen]**.
1. Extrahieren Sie die Datei [!DNL AppMeasurement_JavaScript*.zip], die Sie im Abschnitt [Adobe Analytics bereitstellen](../../../implement/c-implement-with-dtm/t-analytics-deploy.md#task_3A00639CADF14C9C844F962222077E4E) heruntergeladen haben.

   Sollten Sie sich für eine benutzerdefinierte Bibliothek entscheiden, wird beim Öffnen des Fensters bereits die aktuellste Codeversion angezeigt. Die zip-Datei muss nicht aus der Admin Console heruntergeladen werden.
1. Öffnen Sie [!DNL AppMeasurement.js] in einem Texteditor.
1. Kopieren Sie die Inhalte und fügen Sie sie im Fenster **[!UICONTROL Code bearbeiten]** ein.

   ![](assets/edit-code.png)

1. Adobe empfiehlt, folgenden Code über *`Do Not Alter Anything Below This Line`*:

   ```
   var s_account="INSERT-RSID-HERE"
   var s=s_gi(s_account)
   ```

   >[!IMPORTANT]
   >
   >Sollten Sie diesen Code hinzufügen, wird empfohlen, auch das Kontrollkästchen **[!UICONTROL Report Suites mithilfe eines benutzerspezifischen Codes unten festlegen]** in den Gesamteinstellungen der Bibliothek zu aktivieren.

1. Klicken Sie auf **[!UICONTROL Speichern und schließen]**.

   Wenn Sie das Media-Modul, Integrate-Modul oder Implementation-Plug-ins verwenden, können Sie diese ebenfalls in den Codeabschnitt kopieren. Der verwaltete Code im Dynamic Tag Management kann genauso wie die JavaScript-Datei in einer normalen Implementierung konfiguriert werden.

