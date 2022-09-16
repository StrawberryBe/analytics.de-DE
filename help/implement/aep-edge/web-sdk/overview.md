---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK
description: Verwenden Sie die Web SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
exl-id: 97f8d650-247f-4386-b4d2-699f3dab0467
source-git-commit: 72b2497c5060f2309f2232a09e46166ac63da944
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 100%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK

Sie können das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html?lang=de) verwenden, um Daten an Adobe Analytics zu senden. Bei dieser Implementierungsmethode wird das [Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) in ein von Analytics verwendetes Format übersetzt.

## Einrichten

So richten Sie Analytics für den Empfang von XDM-Daten ein:

1. Installieren und [konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) Sie das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=de).

1. Stellen Sie sicher, dass die entsprechenden Report Suites den gewünschten Daten zugeordnet sind. XDM-Daten werden automatisch von Adobe Experience Edge in die Report Suite übertragen.
