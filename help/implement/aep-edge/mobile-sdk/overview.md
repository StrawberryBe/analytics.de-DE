---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK
description: Verwenden Sie die Mobile SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
exl-id: 516e9a1e-caa7-4f8a-ab8c-6404e9242ccb
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK

Mit dem Adobe Experience Platform Mobile SDK können Sie die Experience Cloud-Lösungen und -Services von Adobe in Ihren Mobile Apps nutzen. Es ist für Android, iOS und verschiedene plattformübergreifende Entwicklungs-Frameworks verfügbar. Die Konfiguration erfolgt über die Datenerfassung von Adobe Experience Platform.

So senden Sie Daten mit dem Mobile SDK an Adobe Experience Edge:

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) an.
2. Wählen Sie die gewünschte Eigenschaft aus der Liste aus oder [richten Sie eine Mobile-Eigenschaft ein](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).
3. Navigieren Sie zur Registerkarte „Erweiterungen“ und installieren Sie die Erweiterung [Identity for Edge Network](https://aep-sdks.gitbook.io/docs/foundation-extensions/identity-for-edge-network).
4. Installieren Sie [Adobe Experience Platform Edge Network](https://aep-sdks.gitbook.io/docs/foundation-extensions/experience-platform-extension).
5. [Konfigurieren Sie einen Datenstrom](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams) und fügen Sie Adobe Analytics als Service hinzu, der auf die gewünschte Report Suite verweist.
6. [Installieren Sie das SDK](https://aep-sdks.gitbook.io/docs/getting-started/get-the-sdk) in Ihrer Mobile App.

>[!IMPORTANT]
>
>Eine Adobe Analytics-Erweiterung ist ebenfalls in der Datenerfassung von Adobe Experience Platform verfügbar. Wenn Sie diese Erweiterung installieren, nutzen Sie weder XDM noch das Edge-Netzwerk.
