---
title: Übersicht über das Implementieren mit Launch
description: Erfahren Sie, wie Sie Adobe Analytics mithilfe von Adobe Experience Platform Launch implementieren
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 100%

---


# Übersicht über das Implementieren mit Launch

Während der gesamten Lebensdauer von Adobe Analytics hat Adobe verschiedene Methoden zur Implementierung von Code für die Datenerfassung auf Ihrer Website angeboten. Die derzeit von Adobe empfohlene Methode verwendet Adobe Experience Platform Launch.

Launch ist eine Tag-Management-Lösung, mit der Sie Analytics-Code zusammen mit anderen Tagging-Anforderungen bereitstellen können. Adobe bietet Integrationen mit anderen Lösungen und Produkten und ermöglicht die Bereitstellung von benutzerdefiniertem Code. Alle diese Aufgaben können ausgeführt werden, ohne dass Entwicklungsteams in Ihrer Organisation Code auf Ihrer Website aktualisieren müssen.

Alle Kunden mit einem aktiven Adobe Experience Cloud-Vertrag können Launch verwenden. Wenn Sie sich nicht sicher sind, ob Sie Zugriff haben, wenden Sie sich an einen Experience Cloud-Systemadministrator Ihres Unternehmens.

## Allgemeiner Workflow

Um eine Implementierung mit Launch auszuführen, gehen Sie wie folgt vor:

1. **Zugriff auf Launch erhalten**: Sie können über einen Systemadministrator in Ihrem Unternehmen Zugriff auf Launch erhalten.
2. **Eigenschaft erstellen**: Eigenschaften sind übergreifende Behälter, die zum Verweisen auf Tag-Management-Daten verwendet werden.
3. **In einer Entwicklungsumgebung bereitstellen**: Verwenden Sie eine Umgebung, in der Sie die Entwicklung von Tags iterieren können.
4. **In Produktionsumgebung validieren und veröffentlichen**: Vergewissern Sie sich, dass alles funktioniert, und veröffentlichen Sie es dann live.

Erste Schritte finden Sie unter [Analytics-Eigenschaft in Adobe Experience Platform Launch erstellen](create-analytics-property.md).

## Zusätzliche Ressourcen

Launch kann in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

* [Launch-Dokumentation](https://docs.adobe.com/content/help/de-DE/launch/using/overview.html): Erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.
* [Adobe Analytics-Erweiterung](https://docs.adobe.com/content/help/de-DE/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html): Verwenden Sie die Analytics-Erweiterung, um Daten an Adobe Analytics zu senden.
* [Implementierungsvariablen](../vars/overview.md): Legen Sie fest, welche Variablen Sie an Datenerfassungs-Server senden möchten.
