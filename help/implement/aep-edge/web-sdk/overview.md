---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK
description: Verwenden Sie die Web SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
source-git-commit: e6b40881a543b43c03b612c7e7b0d9bd09f44c0d
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 24%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK

Sie können das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html) verwenden, um Daten an Adobe Analytics zu senden. Bei dieser Implementierungsmethode wird das [Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) in ein von Analytics verwendetes Format übersetzt.

Sie können Daten direkt mit dem Web SDK oder über die Web SDK-Erweiterung in Tags an Experience Edge senden.

## Web SDK

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Implementieren von Adobe Analytics mit dem Web SDK-Workflow](../../assets/websdk-annotated.png)

|<div style="width:20px"></div>| Aufgabe | Weitere Informationen | |-| —|—| | 1 | Stellen Sie sicher, dass **Report Suite definiert haben**. | [Report Suite Manager](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Einrichten von Schemata und Datensätzen**. Um die Datenerfassung für die Verwendung in allen Anwendungen zu standardisieren, die Adobe Experience Platform nutzen, hat Adobe den offenen und öffentlich dokumentierten Standard Experience-Datenmodell (XDM) erstellt. | [Übersicht über die Benutzeroberfläche von Schemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de) und [Übersicht über die Benutzeroberfläche von Datensätzen](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de) | | 3 | **Erstellen einer Datenschicht** um das Tracking der Daten auf Ihrer Website zu verwalten. | [Erstellen einer Datenschicht](../../prepare/data-layer.md) | | 4 | **Installieren der vordefinierten eigenständigen Version**. Sie können auf die Bibliothek verweisen (`alloy.js`) direkt auf Ihrer Seite platzieren oder herunterladen und in Ihrer eigenen Infrastruktur hosten. Alternativ können Sie das NPM-Paket verwenden. | [Installieren der vordefinierten eigenständigen Version](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-2%3A-installing-the-prebuilt-standalone-version) und [Verwenden des NPM-Pakets](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-3%3A-using-the-npm-package)| | 5 | **Konfigurieren eines Datenspeichers**. Ein Datastream stellt die serverseitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar. | [Konfigurieren eines Datenspeichers](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 6 | **Hinzufügen eines Adobe Analytics-Dienstes** in Ihren Datastream. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden. | [Hinzufügen des Adobe Analytics-Dienstes zu einem Datenspeicher](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 7 | **Web SDK konfigurieren**. Stellen Sie sicher, dass die Bibliothek, die Sie in Schritt 4 installiert haben, ordnungsgemäß mit der Datastraam-ID konfiguriert ist (ehemals Edge-Konfigurations-ID (`edgeConfigId`), Organisations-ID (`orgId`) und anderen verfügbaren Optionen. | [Web SDK konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) | | 8 | **Ausführen von Befehlen** und/oder **Ereignisse verfolgen**. Nachdem der Basis-Code auf Ihrer Webseite implementiert wurde, können Sie mit der Ausführung von Befehlen und Tracking-Ereignissen mit dem SDK beginnen. | [Ausführen von Befehlen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/executing-commands.html?lang=en) und [Ereignisse verfolgen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=en) | | 9 | **Implementierung erweitern und validieren** bevor sie in die Produktion verschoben wird. | |



## Web SDK-Erweiterung

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Implementieren von Adobe Analytics mithilfe des Workflows Web SDK-Erweiterung](../../assets/websdk-extension-annotated.png)

|<div style="width:20px"></div> | Aufgabe | Weitere Informationen | |-| —|—| | 1 | Stellen Sie sicher, dass **Report Suite definiert haben**. | [Report Suite Manager](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Einrichten von Schemata und Datensätzen**. Um die Datenerfassung für die Verwendung in allen Anwendungen zu standardisieren, die Adobe Experience Platform nutzen, hat Adobe den offenen und öffentlich dokumentierten Standard Experience-Datenmodell (XDM) erstellt. | [Übersicht über die Benutzeroberfläche von Schemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de) und [Übersicht über die Benutzeroberfläche von Datensätzen](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de) | | 3 | **Erstellen einer Datenschicht** um das Tracking der Daten auf Ihrer Website zu verwalten. | [Erstellen einer Datenschicht](../../prepare/data-layer.md) | | 4 | **Konfigurieren eines Datenspeichers**. Ein Datastream stellt die serverseitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar. | [Konfigurieren eines Datenspeichers](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 5 | **Hinzufügen eines Adobe Analytics-Dienstes** in Ihren Datastream. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden. | [Hinzufügen des Adobe Analytics-Dienstes zu einem Datenspeicher](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 6 | **Tag-Eigenschaft erstellen**. Eigenschaften sind übergreifende Container, die zum Verweisen auf Tag Management-Daten verwendet werden.| [Erstellen oder Konfigurieren einer Tag-Eigenschaft für das Web](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en#for-web) | | 7 | **Installieren und Konfigurieren der Web SDK-Erweiterung** in Ihrer Tag-Eigenschaft. Konfigurieren Sie die Web SDK-Erweiterung, um Daten an den in Schritt 4 konfigurierten Datastream zu senden. | [Übersicht über die Adobe Experience Platform Web SDK-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=en) | | 8 | **Iterieren, Validieren und Veröffentlichen** zur Produktion. Fügen Sie die Tag-Eigenschaft Ihrer Website hinzu. Verwenden Sie dann Datenelemente, Regeln usw., um Ihre Implementierung anzupassen. | [Veröffentlichungsübersicht](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=de) |



## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Dokumentation zum Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/web-sdk.html?lang=de)
