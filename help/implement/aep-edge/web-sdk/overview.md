---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK
description: Verwenden Sie die Web SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
source-git-commit: 6979736e1849d25af2141e0ab76a143605a90620
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 33%

---


# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK

Sie können die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html?lang=de) , um Daten an Adobe Analytics zu senden. Diese Implementierungsmethode funktioniert durch die Übersetzung der [Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) in ein von Analytics verwendetes Format.

## Einrichten

So richten Sie Analytics für den Empfang von XDM-Daten ein:

1. Installieren und [konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) Sie das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=de).

1. Stellen Sie sicher, dass die entsprechenden Report Suites den gewünschten Daten zugeordnet sind. XDM-Daten fließen automatisch von Adobe Experience Edge in die Report Suite.
