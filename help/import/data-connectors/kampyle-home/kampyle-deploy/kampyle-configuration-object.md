---
description: Nach Abschluss des Integrationsassistenten müssen Sie das Integrationskonfigurationsobjekt für Ihre Webeigenschaft bereitstellen.
seo-description: Nach Abschluss des Integrationsassistenten müssen Sie das Integrationskonfigurationsobjekt für Ihre Webeigenschaft bereitstellen.
seo-title: Implementierungskonfigurationsobjekt bereitstellen
solution: Analytics
title: Implementierungskonfigurationsobjekt bereitstellen
uuid: e 951 c 864-2914-4324-9 f 03-5069 d 4 f 75 d 99
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Implementierungskonfigurationsobjekt bereitstellen{#deploy-the-integration-configuration-object}

Nach Abschluss des Integrationsassistenten müssen Sie das Integrationskonfigurationsobjekt für Ihre Webeigenschaft bereitstellen.

In vielen Fällen ist es am einfachsten, das Integrationskonfigurationsobjekt bereitzustellen, indem Sie es mit Ihrem Adobe Analytics-Bereitstellungscode integrieren.

>[!NOTE]
>
>Wenn Sie Adobe Analytics mit Adobe tagmanager oder dynamischem Tag-Management bereitstellen, können Sie das Integrationskonfigurationsobjekt einfach über dieses Tool hinzufügen.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Ressourcen]** &gt; **[!UICONTROL Support]** der Integration.
1. Laden Sie die Ressource **[!UICONTROL Kampyle Integration Code (JS)]** herunter und speichern Sie sie. Der Code sieht wie folgt aus:

   ```
   /* Kampyle:  Integration configuration settings */
     window.k_sc_param = { "version":1.1 }
   ```

1. Stellen Sie den Code mit einer der folgenden Methoden bereit:

       | ** Sie verwenden Adobe tagmanager oder dynamisches Tag-Management.** | Verwenden Sie die Oberfläche für Tag-Management, um den Code hinzuzufügen. |
    |—|—|
    | ** In allen anderen Fällen** | Stellen Sie den Code für die Unternehmensressource bereit, die für die Aktualisierung Ihres Adobe Analytics-Bereitstellungscodes zuständig ist. |
   
