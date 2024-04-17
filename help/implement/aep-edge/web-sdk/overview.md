---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK
description: Verwenden Sie das Web SDK, um Daten an Adobe Analytics zu senden.
exl-id: 97f8d650-247f-4386-b4d2-699f3dab0467
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: d6c16d8841110e3382248f4c9ce3c2f2e32fe454
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 39%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK

Sie können das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/web-sdk/home.html) verwenden, um Daten an Adobe Analytics zu senden. Es gibt zwei Hauptmethoden zur Implementierung des Web SDK. Jede Methode verfügt über zwei Implementierungstypen:

| | **Migration von AppMeasurement** | **Implementierung des Web SDK bereinigen** |
| --- | --- | --- |
| **Tags verwenden** | [Migration von der Analytics-Erweiterung zur Web SDK-Erweiterung](analytics-extension-to-web-sdk.md) | [Senden von Daten an Adobe Analytics mithilfe der Web SDK-Erweiterung](web-sdk-tag-extension.md) |
| **JavaScript verwenden** | [Migration von AppMeasurement zur JavaScript-Bibliothek des Web SDK](appmeasurement-to-web-sdk.md) | [Senden von Daten an Adobe Analytics mithilfe der Web SDK-JavaScript-Bibliothek](web-sdk-javascript-library.md) |

Wenn Ihr Unternehmen eine neue Web SDK-Implementierung benötigt und in Zukunft Customer Journey Analytics verwenden möchte, empfiehlt Adobe eine saubere Web SDK-Implementierung unter Verwendung Ihres eigenen Schemas. Siehe [Daten über das Adobe Experience Platform Web SDK erfassen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) im Customer Journey Analytics-Benutzerhandbuch.

## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Adobe Experience Platform Web SDK-Dokumentation](https://experienceleague.adobe.com/docs/web-sdk.html?lang=de)
