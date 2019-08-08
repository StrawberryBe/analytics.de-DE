---
description: Nach Abschluss des Integrationsassistenten müssen Sie den Integrationscode in Ihrem Adobe Analytics-Bereitstellungscode (s_ code) bereitstellen.
seo-description: Nach Abschluss des Integrationsassistenten müssen Sie den Integrationscode in Ihrem Adobe Analytics-Bereitstellungscode (s_ code) bereitstellen.
seo-title: Bereitstellen des Integrationscodes
title: Bereitstellen des Integrationscodes
uuid: b 3 fbda 0 b -4 ed 3-4967-84 ee -6 c 66564606 e 7
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Bereitstellen des Integrationscodes{#deploying-the-integration-code}

Nach Abschluss des Integrationsassistenten müssen Sie den Integrationscode in Ihrem Adobe Analytics-Bereitstellungscode (s_ code) bereitstellen.

>[!NOTE]
>
>Wenn Sie Adobe Analytics mit Adobe tagmanager oder dynamischem Tag-Management bereitgestellt haben, können Sie den Integrationscode problemlos mit einem dieser Werkzeuge hinzufügen.

1. Rufen Sie die **[!UICONTROL Registerkarte Support]** auf und laden Sie die `integration code v2_0_1` Ressource aus dem Ressourcenbereich der Integration herunter und speichern Sie sie.

1. Falls zutreffend, nehmen Sie gegebenenfalls erforderliche Änderungen am Code vor. Weitere Informationen finden Sie unter [Integrationscode ändern](../../demandbase-home/demandbase-deploying/demandbase-deploying-integration-code.md#concept-2e9e56282c9940d78e879aa45f70d855).
1. Integrieren Sie das Integrate-Modul, wenn es noch nicht in Ihrem Adobe Analytics-Bereitstellungscode vorhanden ist. Weitere Informationen finden Sie unter [Integrieren des Integrate-Moduls](../../demandbase-home/demandbase-deploying/demandbase-including-integrate-module.md#concept-2cc81dff010a4da89b097a59476f8b6e).
1. Stellen Sie den Code mit einer der folgenden Methoden bereit:

   * Verwenden Sie zum Hinzufügen des Codes Adobe tagmanager oder Dynamisches Tag-Management.
   * Oder stellen Sie den Code für die Unternehmensressource bereit, die für die Aktualisierung Ihres Adobe Analytics-Bereitstellungscodes zuständig ist.

>[!IMPORTANT]
>
>Stellen Sie sicher, dass Sie die Bereitstellung für diese Integration in einer Entwicklungs-/Staging-Umgebung testen, bevor Sie sie in einer Produktionsumgebung bereitstellen.

