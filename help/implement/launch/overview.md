---
title: Implementieren mithilfe von Tags in Adobe Experience Platform
description: Hier erfahren Sie, wie Sie Adobe Analytics mithilfe von Tags implementieren
feature: Launch Implementation
exl-id: 52990731-8a68-4779-ad42-6ec94b0aabd1
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 100%

---

# Implementieren mithilfe von Tags in Adobe Experience Platform

>[!NOTE]
>Adobe Experience Platform Launch wurde umbenannt und umfasst eine Suite von Datenerfassungstechnologien in Experience Platform. Infolgedessen wurden in der gesamten Produktdokumentation mehrere terminologische Änderungen vorgenommen. Eine Übersicht der terminologischen Änderungen finden Sie im folgenden [Dokument](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=de).

Während der gesamten Lebensdauer von Adobe Analytics hat Adobe verschiedene Methoden zur Implementierung von Code für die Datenerfassung auf Ihrer Website angeboten. Die derzeit von Adobe empfohlene Methode verwendet Tags in Adobe Experience Platform.

Tags in Adobe Experience Platform ist eine Tag-Management-Lösung, mit der Sie Analytics-Code bereitstellen und weitere Tagging-Vorgaben erfüllen können. Adobe bietet Integrationen mit anderen Lösungen und Produkten und ermöglicht die Bereitstellung von benutzerdefiniertem Code. Alle diese Aufgaben können ausgeführt werden, ohne dass Entwicklungsteams in Ihrer Organisation Code auf Ihrer Website aktualisieren müssen.

Alle Kunden mit einem aktiven Adobe Experience Cloud-Vertrag können Tags verwenden. Wenn Sie sich nicht sicher sind, ob Sie Zugriff haben, wenden Sie sich an einen Experience Cloud-Systemadministrator Ihres Unternehmens.

## Allgemeiner Workflow

Um eine Implementierung mithilfe von Tags durchzuführen, gehen Sie wie folgt vor:

1. **Zugriff auf Tags erhalten**: Sie können über einen Systemadministrator in Ihrem Unternehmen Zugriff auf Tags in Platform erhalten.
2. **Tag-Eigenschaft erstellen**: Eigenschaften sind übergreifende Container, die zum Verweisen auf Tag-Management-Daten verwendet werden.
3. **In einer Entwicklungsumgebung bereitstellen**: Verwenden Sie eine Umgebung, in der Sie die Entwicklung von Tags iterieren können.
4. **In Produktionsumgebung validieren und veröffentlichen**: Vergewissern Sie sich, dass alles funktioniert, und veröffentlichen Sie es dann live.

Erste Schritte finden Sie unter [Erstellen einer Analytics-Tag-Eigenschaft](create-analytics-property.md).

## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

* [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.
* [Adobe Analytics-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de): Verwenden Sie die Analytics-Erweiterung, um Daten an Adobe Analytics zu senden.
* [Implementierungsvariablen](../vars/overview.md): Legen Sie fest, welche Variablen Sie an Datenerfassungs-Server senden möchten.
