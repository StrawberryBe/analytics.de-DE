---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK
description: Verwenden Sie die Mobile SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
exl-id: 516e9a1e-caa7-4f8a-ab8c-6404e9242ccb
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 6%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK

Mit dem Adobe Experience Platform Mobile SDK können Sie die Experience Cloud-Lösungen und -Dienste von Adobe in Ihren mobilen Apps nutzen. Es ist für Android, iOS und verschiedene plattformübergreifende Entwicklungs-Frameworks verfügbar. Die Konfiguration erfolgt über die Adobe Experience Platform-Datenerfassung.

So senden Sie Daten mit dem Mobile SDK an Adobe Experience Edge:

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection).
2. Wählen Sie die gewünschte Eigenschaft aus der Liste aus oder [Einrichten einer mobilen Eigenschaft](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).
3. Navigieren Sie zur Registerkarte Erweiterungen und installieren Sie die [Identität für Edge Network](https://aep-sdks.gitbook.io/docs/foundation-extensions/identity-for-edge-network) -Erweiterung.
4. Installieren Sie die [Adobe Experience Platform Edge Network](https://aep-sdks.gitbook.io/docs/foundation-extensions/experience-platform-extension).
5. [Konfigurieren eines Datenspeichers](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams)hinzugefügt, indem Adobe Analytics als Dienst hinzugefügt wird, der auf die gewünschte Report Suite verweist.
6. [SDK installieren](https://aep-sdks.gitbook.io/docs/getting-started/get-the-sdk) in Ihrer mobilen App.

>[!IMPORTANT]
>
>Eine Adobe Analytics-Erweiterung ist auch in der Adobe Experience Platform-Datenerfassung verfügbar. Wenn Sie diese Erweiterung installieren, nutzen Sie weder XDM noch das Edge-Netzwerk.
