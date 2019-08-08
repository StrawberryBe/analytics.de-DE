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
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Integrieren des Integrate-Moduls{#including-the-integrate-module}

Der Integrationscode erfordert, dass das Integrate-Modul in Ihrer Adobe Analytics-Bereitstellung vorhanden ist.

Wenn Sie das Integrate-Modul noch nicht Teil Ihrer Bereitstellung haben, führen Sie abhängig vom Typ der Implementierung die folgenden Schritte aus.

## Für appmeasurement v 1.0 + {#section-f28d090bf2404cabaae34cd9c66fc575}

1. Dekomprimieren Sie die ZIP-Datei appmeasurement, die Sie von **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL codemanager heruntergeladen]** haben.

1. Öffnen Sie die Datei mit dem Namen [!DNL AppMeasurement_Module_Integrate.js].
1. Kopieren Sie den Inhalt dieser Datei und fügen Sie sie in Ihre primäre [!DNL AppMeasurement.js] Datei ein.

   >[!NOTE]
   >
   >Fügen Sie es direkt vor dem Kommentar "DO NOT ALTER ANYTHING BELOW THIS LINE" in die Datei ein.

## Für Legacy-Code (H-Code) {#section-bba8ad8c715e4f97883e7de3269f681a}

1. Laden Sie das Integrate-Modul aus dem Bereich "Ressourcen" in der Data Connectors-Benutzeroberfläche (auf der Registerkarte Support) herunter.

   ![](assets/h_code.png)

1. Kopieren Sie den Inhalt dieser Datei und fügen Sie sie in Ihre [!DNL s_code] Datei ein.

   >[!NOTE]
   >
   >Fügen Sie es direkt vor dem Kommentar "DO NOT ALTER ANYTHING BELOW THIS LINE" in die Datei ein.

