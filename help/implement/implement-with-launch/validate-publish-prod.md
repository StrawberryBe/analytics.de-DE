---
title: Bereitstellen von Adobe Analytics in einer dev-Umgebung
seo-title: Bereitstellen von Adobe Analytics in einer dev-Umgebung
description: Erfahren Sie, wie Sie Adobe Analytics starten, um Adobe Analytics in Ihrer Entwicklungsumgebung bereitzustellen.
seo-description: Erfahren Sie, wie Sie Adobe Analytics starten, um Adobe Analytics in Ihrer Entwicklungsumgebung bereitzustellen.
translation-type: tm+mt
source-git-commit: d195fb85711f58383577bf1d7b4da4078b909427

---


# Validieren einer Entwicklungsimplementierung und Veröffentlichen in der Produktion

Sobald Ihre Adobe Experience Platform Launch Library an die Produktion gesendet wird, kann Ihre Organisation mit Adobe Analytics beginnen, einfache Berichte abzurufen.

## Voraussetzungen

[Implementieren Sie Ihre Analytics-Implementierung in Ihrer dev-Umgebung](deploy-dev.md): Eine Analytics-Implementierung muss in Ihrer Entwicklungsumgebung veröffentlicht werden, damit diese Seite verfolgt werden kann.

## Validieren der dev-Implementierung mit dem Experience Cloud-Debugger

Der Experience Cloud-Debugger ist ein Chrome-Plugin, das alle auf einer Seite vorhandenen Experience Cloud-Tags anzeigt.

1. Open [Chrome Web Browser](https://www.google.com/chrome/) and go to [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) on the Chrome Web Store to install the extension.
2. Navigieren Sie zu Ihrer Website, auf der Sie Starten aktiviert haben.
3. Klicken Sie oben rechts in Chrome auf das Symbol für das Adobe Experience Cloud-Debugger.
4. Wenn alles ordnungsgemäß implementiert ist, sollten Sie Inhalte in Adobe Analytics, Adobe Experience Platform Launch und dem Adobe Experience Cloud Besucher-ID-Dienst anzeigen:

![debugger][assets/debugger.png]

## Implementierung der dev-Implementierung auf Staging/prod

Sobald Sie die Daten überprüft haben, können Sie Ihre Implementierung auf die Live-Version Ihrer Site übertragen.

1. Go to [Adobe Experience Platform Launch](https://launch.adobe.com) and log in if prompted.
2. Klicken Sie auf die Starteigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte Veröffentlichung und suchen Sie in der Spalte "Entwicklung" nach Ihrer Bibliothek.
4. Klicken Sie auf die Dropdown-Liste in der Bibliothek und wählen Sie dann zur Genehmigung senden. Klicken Sie im modalen Fenster auf Senden.
5. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek (jetzt in der Spalte "Gesendet" ) und wählen Sie" Für Staging erstellen" aus.
6. Nach einigen Minuten wird das gelbe hellgrüne Licht in der Bibliothek grün, was einen erfolgreichen Aufbau anzeigt.
7. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek und wählen Sie "Zur Veröffentlichung genehmigen" .
8. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek (jetzt in der Spalte Genehmigung) und wählen Sie dann "In Produktion erstellen" und" Veröffentlichen" .
9. Rufen Sie die Registerkarte Umgebungen auf, klicken Sie auf Produktionsumgebung.
10. Kopieren Sie den Produktions- und Fußzeilencode und stellen Sie ihn Ihren Website-Inhabern zur Verfügung. Fordern Sie an, diesen Code in der Produktionsumgebung Ihrer Site zu implementieren.

## Validieren der Produktionsimplementierung

Vergewissern Sie sich, dass Sie Daten zur Live-Version Ihrer Site anzeigen und beginnen Sie mit der offiziellen Datenerfassung für Adobe Analytics.

1. Sobald Sie von Ihren Website-Inhabern bestätigt haben, dass sie den Startcode in die Produktion verschoben haben, navigieren Sie in Chrome zur Homepage Ihrer Website und öffnen Sie den Adobe Experience Cloud-Debugger.
2. Wenn alles funktioniert, sollten Sie in Ihrer dev-Umgebung ähnliche Daten zu Ihren Tests sehen. An dieser Stelle erfassen Sie Daten auf Ihrer Site und können jetzt mit Adobe Analytics für die Berichterstellung beginnen.

## Fehlerbehebung 

**Im Debugger werden keine Daten angezeigt.**

Öffnen Sie auf Ihrer Site die Entwicklerkonsole des Browsers (normalerweise F 12). Betrachten Sie den Quellcode der Seite und stellen Sie sicher, dass Folgendes erfüllt ist:

* Die Konsole gibt es keine javascript-Fehler. Arbeiten Sie mit den Website-Eigentümern Ihrer Organisation zusammen, um sicherzustellen, dass alle JS-Fehler aufgelöst werden.
* Header code is properly implemented: Make sure the header code is inside the `<head>` tag, and that the file exists.
* Appmeasurement-Bibliothek vorhanden: Navigieren Sie direkt zur JS-Quelle, um sicherzustellen, dass die JS-Datei Code enthält. Wenn dies nicht der Fall ist, stellen Sie sicher, dass jede Umgebung erstellt wird und dass die Bibliothek in der entsprechenden Umgebung veröffentlicht wird.
* Störungen von Plug-plugins: Einige Chrome-Plugins können verhindern, dass Bildanforderungen ausgelöst werden. Deaktivieren Sie alle Plugins, die das Senden von Daten an die Server von Adobe verhindern könnten.

## Nächste Schritte

Nachdem eine einfache Implementierung eingerichtet wurde, kann Ihre Rolle in Ihrer Organisation beeinflussen, welchen Pfad Sie mehr über die folgenden Punkte erfahren möchten:

* [Erstellen Sie ein Dokument für das Lösungsdesign](../prepare/solution-design.md): Planen Sie die Verwendung benutzerdefinierter Variablen und schließen Sie diese dann in Ihre Implementierung ein.
* [Erste Schritte mit Analysis Workspace](../../analyze/analysis-workspace/home.md): Dive Right into Adobe Analytics using the tool's flagship capabilities.
