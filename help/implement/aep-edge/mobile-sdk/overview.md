---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK
description: Verwenden Sie die Mobile SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
source-git-commit: e6b40881a543b43c03b612c7e7b0d9bd09f44c0d
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 20%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK

Mit dem Adobe Experience Platform Mobile SDK können Sie die Experience Cloud-Lösungen und -Services von Adobe in Ihren Mobile Apps nutzen. Es ist für Android™, iOS und verschiedene plattformübergreifende Entwicklungs-Frameworks verfügbar. Die Konfiguration erfolgt über die Datenerfassung von Adobe Experience Platform.
>[!IMPORTANT]
>
>Eine Adobe Analytics-Erweiterung ist ebenfalls in der Datenerfassung von Adobe Experience Platform verfügbar. Wenn Sie diese Erweiterung installieren, nutzen Sie weder XDM noch das Edge-Netzwerk.

## Adobe Experience Platform SDK

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Adobe Analytics mithilfe des Workflows für die Analytics-Erweiterung](../../assets/mobilesdk-annotated.png)

|<div style="width:20px"></div>| Aufgabe | Weitere Informationen | |-| —|—| | 1 | Stellen Sie sicher, dass **Report Suite definiert haben**. | [Report Suite Manager](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Einrichten von Schemata und Datensätzen**. Um die Datenerfassung für die Verwendung in allen Anwendungen zu standardisieren, die Adobe Experience Platform nutzen, hat Adobe den offenen und öffentlich dokumentierten Standard Experience-Datenmodell (XDM) erstellt. | [Einrichten von Schemata und Datensätzen](https://developer.adobe.com/client-sdks/documentation/getting-started/set-up-schemas-and-datasets/) | | 3 | **Konfigurieren eines Datenspeichers**. Ein Datastream stellt die serverseitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar. | [Konfigurieren eines Datenspeichers](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 4 | **Hinzufügen eines Adobe Analytics-Dienstes** in Ihren Datastream. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden. | [Hinzufügen des Adobe Analytics-Dienstes zu einem Datenspeicher](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 5 | **Erstellen einer mobilen Eigenschaft**. Eine Eigenschaft ist ein Container, den Sie mit Erweiterungen, Regeln, Datenelementen und Bibliotheken füllen. | [Einrichten einer mobilen Eigenschaft](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/) | | 6 | **Installieren der Adobe Experience Platform Edge Network-Erweiterung** in der mobilen Tag-Eigenschaft und konfigurieren Sie den Datastream in der Erweiterung. | [Adobe Experience Platform Edge Network](https://developer.adobe.com/client-sdks/documentation/edge-network/) | | 7 | **Verwenden des Codes in Ihrer App** , um die erforderlichen Erweiterungen zu registrieren und Ihre Tag-Konfiguration zu laden. | [Einrichten der Konfiguration](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration) | | 8 | **Implementieren und Testen von Funktionen** Verwenden Sie eine Kombination aus den Datenelementen, Regeln, zusätzlichen Erweiterungen und SDK-API-Aufrufen des Tags in Ihrer App. Datenerfassung und Erlebnisse für Ihre Mobile App in Inspect validieren und debuggen. | [Beispielanwendung verwenden](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application) | | 9 | **Mobile-App-Implementierung erweitern und validieren** bevor sie in die Produktion verschoben wird. | |


## Adobe Analytics-Erweiterung.

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Adobe Analytics mithilfe des Workflows für die Analytics-Erweiterung](../../assets/mobilesdk-analytics-annotated.png)

|<div style="width:20px"></div> | Aufgabe | Weitere Informationen | |-| —|—| | 1 | Stellen Sie sicher, dass **Report Suite definiert haben**. | [Report Suite Manager](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Erstellen einer mobilen Eigenschaft**. Eine Eigenschaft ist ein Container, den Sie mit Erweiterungen, Regeln, Datenelementen und Bibliotheken füllen. | [Einrichten einer mobilen Eigenschaft](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/) | | 3 | **Installieren der Adobe Analytics-Erweiterung** in der mobilen Tag-Eigenschaft und konfigurieren Sie die Erweiterung so, dass sie auf Ihre Report Suite verweist. | [Adobe Analytics-Erweiterung für mobile Eigenschaft](https://developer.adobe.com/client-sdks/documentation/adobe-analytics/) | | 4 | **Verwenden des Codes in Ihrer App** , um die erforderlichen Erweiterungen zu registrieren und Ihre Tag-Konfiguration zu laden. | [Einrichten der Konfiguration](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration) | | 5 | **Implementieren und Testen von Funktionen** Verwenden Sie eine Kombination aus den Datenelementen, Regeln, zusätzlichen Erweiterungen und SDK-API-Aufrufen des Tags in Ihrer App. Datenerfassung und Erlebnisse für Ihre Mobile App in Inspect validieren und debuggen. | [Beispielanwendung verwenden](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application) | | 6 | **Mobile-App-Implementierung erweitern und validieren** bevor sie in die Produktion verschoben wird. | |

## Zusätzliche Ressourcen

- [Dokumentation zu Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#)

- [Mobile-SDKs – Dokumentation](https://developer.adobe.com/client-sdks/documentation/)



