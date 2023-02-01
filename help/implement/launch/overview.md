---
title: Implementieren von Adobe Analytics mit der Analytics-Erweiterung
description: Erfahren Sie, wie Sie Adobe Analytics mithilfe von Tags und der Analytics-Erweiterung implementieren
feature: Launch Implementation
source-git-commit: 472faef9c6ef99d4e58f2f5a9a71ca8d058f0ee2
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 48%

---

# Implementieren von Adobe Analytics mit der Analytics-Erweiterung

Während der gesamten Lebensdauer von Adobe Analytics hat Adobe verschiedene Methoden zur Implementierung von Code für die Datenerfassung auf Ihrer Website angeboten. Die derzeit empfohlene Methode von Adobe erfolgt über -Tags in Adobe Experience Platform.

Tags in Adobe Experience Platform ist eine Tag-Management-Lösung, mit der Sie Analytics-Code bereitstellen und weitere Tagging-Vorgaben erfüllen können. Adobe bietet Integrationen mit anderen Lösungen und Produkten und ermöglicht die Bereitstellung von benutzerdefiniertem Code. Alle diese Aufgaben können ausgeführt werden, ohne dass Entwicklungsteams in Ihrer Organisation Code auf Ihrer Website aktualisieren müssen.

Alle Kunden mit einem aktiven Adobe Experience Cloud-Vertrag können Tags verwenden. Wenn Sie sich nicht sicher sind, ob Sie Zugriff haben, wenden Sie sich an einen Experience Cloud-Systemadministrator Ihres Unternehmens.

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Adobe Analytics mithilfe des Workflows für die Analytics-Erweiterung](../assets/analytics-extension-annotated.png)

| | Aufgabe | Weitere Informationen | |-| —|—| | 1 | Stellen Sie sicher, dass **Report Suite definiert haben**. | [Report Suite Manager](../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Erstellen einer Datenschicht** um das Tracking der Daten auf Ihrer Website zu verwalten. | [Erstellen einer Datenschicht](../prepare/data-layer.md) | | 3 | **Tag-Eigenschaft erstellen**. Eigenschaften sind übergreifende Container, die zum Verweisen auf Tag Management-Daten verwendet werden.| [Erstellen einer Adobe Analytics-Tag-Eigenschaft](../launch/create-analytics-property.md) | | 4 | **Installieren der Analytics-Erweiterung** in der Tag-Eigenschaft. Konfigurieren Sie die Analytics-Erweiterung, um Daten an Adobe Analytics zu senden. | [Übersicht über die Adobe Analytics-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=en) | | 5 | **In einer Entwicklungsumgebung bereitstellen**. Verwenden Sie eine Umgebung, in der Sie die Entwicklung von Tags iterieren können. | [Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen](./deploy-dev.md) | | 6 | **In der Produktion validieren und veröffentlichen**. Fügen Sie die Tag-Eigenschaft Ihrer Website hinzu. Verwenden Sie dann Datenelemente, Regeln usw., um Ihre Implementierung anzupassen.| [Entwicklungsimplementierung validieren und in der Produktion veröffentlichen](./validate-publish-prod.md) |

## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Implementierungsvariablen](../vars/overview.md): Legen Sie fest, welche Variablen Sie an Datenerfassungs-Server senden möchten.
