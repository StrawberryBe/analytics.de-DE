---
description: Fügen Sie bei der manuellen Bereitstellung des Dynamic Tag Managements in Adobe Analytics AppMeasurement-Code ein.
keywords: Dynamic Tag Management;linked accounts;linking accounts;edit code;appmeasurement;appmeasurement code
solution: Experience Cloud,Analytics,Target
title: Grundlegenden AppMeasurement-Code einfügen
uuid: 3f83fbb1-3ed5-4e45-888a-0a183aac1a90
translation-type: tm+mt
source-git-commit: a4542164031fc9f181dfdc471a1d54b5056b1223
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 100%

---


# Grundlegenden AppMeasurement-Code einfügen

Fügen Sie bei der manuellen Bereitstellung des Dynamic Tag Managements in Adobe Analytics AppMeasurement-Code ein.

1. Erweitern Sie auf der Seite [!DNL Adobe Analytics] den Abschnitt **[!UICONTROL Allgemein]** und klicken Sie dann auf **[!UICONTROL Editor öffnen]**.
1. Extrahieren Sie die Datei [!DNL AppMeasurement_JavaScript*.zip], die Sie im Abschnitt [Adobe Analytics bereitstellen](/help/implement/other/dtm/t-analytics-deploy.md) heruntergeladen haben.

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

   Wenn Sie das Medienmodul, das Integrationsmodul oder Implementation-Plug-ins verwenden, können Sie diese ebenfalls in den Code-Abschnitt kopieren. Der verwaltete Code im Dynamic Tag Management kann genauso wie die JavaScript-Datei in einer normalen Implementierung konfiguriert werden.

