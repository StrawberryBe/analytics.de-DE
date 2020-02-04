---
title: Übersicht über die Implementierung mit dem Start
description: Erfahren Sie, wie Sie Adobe Analytics mithilfe von Adobe Experience Platform Launch implementieren
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# Übersicht über die Implementierung mit dem Start

Während der gesamten Laufzeit von Adobe Analytics hat Adobe verschiedene Methoden zur Implementierung von Code für die Datenerfassung auf Ihrer Site angeboten. Die aktuelle Empfehlungsmethode von Adobe erfolgt über den Start der Adobe Experience Platform.

Launch ist eine Tag-Management-Lösung, mit der Sie Analytics-Code zusammen mit anderen Tagging-Anforderungen bereitstellen können. Adobe bietet Integrationen mit anderen Lösungen und Produkten und ermöglicht die Bereitstellung von benutzerspezifischem Code. Alle diese Aufgaben können ausgeführt werden, ohne dass Entwicklungsteams in Ihrem Unternehmen für die Aktualisierung von Code auf Ihrer Site eingesetzt werden müssen.

Alle Kunden mit einem aktiven Adobe Experience Cloud-Vertrag können Launch verwenden. Wenn Sie sich nicht sicher sind, ob Sie Zugriff haben, wenden Sie sich an einen Experience Cloud-Systemadministrator Ihres Unternehmens.

## Arbeitsablauf

Um eine Implementierung mit Launch auszuführen, gehen Sie wie folgt vor:

1. **Zugriff auf Start** erhalten: Sie können über einen Systemadministrator in Ihrem Unternehmen Zugriff auf Launch erhalten.
2. **Eigenschaft** erstellen: Eigenschaften sind übergreifende Behälter, die zum Verweisen auf Tag-Management-Daten verwendet werden.
3. **In einer Entwicklungsumgebung** bereitstellen: Sie haben eine Umgebung, in der Sie die Entwicklung von Tags durchlaufen können.
4. **Validieren und Veröffentlichen in der Produktion**: Vergewissern Sie sich, dass alles funktioniert, und veröffentlichen Sie es dann live.

Siehe [Erstellen einer Analytics-Eigenschaft in Adobe Experience Platform Launch](create-analytics-property.md) .

## Zusätzliche Ressourcen

Launch kann stark angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

* [Dokumentation](https://docs.adobe.com/content/help/en/launch/using/overview.html)starten: Erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.
* [Adobe Analytics-Erweiterung](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html): Verwenden Sie die Analytics-Erweiterung, um Daten an Adobe Analytics zu senden.
* [Implementierungsvariablen](../vars/overview.md): Legen Sie fest, welche Variablen Sie an Datenerfassungsserver senden möchten.
