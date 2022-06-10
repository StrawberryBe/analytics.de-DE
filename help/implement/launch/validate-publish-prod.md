---
title: Entwicklungsimplementierung validieren und in der Produktion veröffentlichen
description: Hier erfahren Sie, wie Sie Tags in Adobe Experience Platform verwenden, um Adobe Analytics in Ihrer Produktionsumgebung bereitzustellen.
feature: Launch Implementation
exl-id: 2f5bcfee-d75e-4dac-bea9-91c6cc545173
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 83%

---

# Entwicklungsimplementierung validieren und in der Produktion veröffentlichen

Sobald Ihre Tag-Bibliothek in die Produktion verschoben wurde, kann Ihr Unternehmen Adobe Analytics verwenden, um grundlegende Berichte abzurufen.

## Voraussetzungen

[Stellen Sie Ihre Analytics-Implementierung in Ihrer Entwicklungsumgebung bereit](deploy-dev.md): Eine Analytics-Implementierung muss in Ihrer Entwicklungsumgebung veröffentlicht werden, um dieser Seite zu folgen.

## Überprüfung der Dev-Implementierung mit dem Experience Cloud-Debugger

Der Experience Cloud-Debugger ist eine Erweiterung, die alle Experience Cloud-Tags anzeigt, die auf einer Seite vorhanden sind.

1. Installieren Sie die Erweiterung für [Chrome](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob) oder [Firefox](https://addons.mozilla.org/de/firefox/addon/adobe-experience-platform-dbg/).
2. Navigieren Sie zu Ihrer Entwicklungs-Website, auf der Sie Tags implementiert haben.
3. Klicken Sie in Ihrem Browser auf das Adobe Experience Cloud-Debugger-Symbol.
4. Wenn alles ordnungsgemäß implementiert ist, sollten Sie Inhalte in Adobe Analytics, Tags und den Besucher-ID-Service von Adobe Experience Cloud sehen.

## Bereitstellen der Dev-Implementierung für Staging/Produktion.

Nachdem Sie überprüft haben, ob Daten für Sie sichtbar sind, können Sie Ihre Implementierung an die Live-Version Ihrer Site übertragen.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Publishing]** und suchen Sie die Bibliothek in der Spalte „Entwicklung“.
1. Klicken Sie in der Bibliothek auf das Dropdown-Menü und wählen Sie **[!UICONTROL Zur Genehmigung übermitteln]**. Klicken Sie im modalen Fenster auf **[!UICONTROL Senden]**.
1. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek (jetzt in der Spalte „Gesendet“) und wählen Sie **[!UICONTROL Für Staging erstellen]**.
1. Nach einigen Augenblicken wird das gelbe Licht der Bibliothek grün, was auf eine erfolgreiche Erstellung hinweist.
1. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek und wählen Sie **[!UICONTROL Für Publishing genehmigen]**.
1. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek (jetzt in der Spalte [!UICONTROL Genehmigt]) und wählen Sie **[!UICONTROL Erstellen und in Produktion veröffentlichen]**.
1. Klicken Sie auf der Registerkarte „Umgebungen“ auf **[!UICONTROL Produktionsumgebung]**.
1. Kopieren Sie den Produktions-Installationscode und stellen Sie ihn Ihren Website-Eigentümern zur Verfügung. Fordern Sie an, diesen Code in der Produktionsumgebung Ihrer Site zu implementieren.

## Überprüfen der Produktionsimplementierung

Vergewissern Sie sich, dass Sie Daten zur Live-Version Ihrer Site sehen, und beginnen Sie mit der offiziellen Datenerfassung für Adobe Analytics.

1. Nachdem Sie sich von Ihren Website-Verantwortlichen bestätigen haben lassen, dass diese den Tag-Code in die Produktion verschoben haben, navigieren Sie in Chrome zur Homepage Ihrer Website und öffnen Sie den [!UICONTROL Adobe Experience Cloud-Debugger].
2. Wenn alles funktioniert, sollten Sie ähnliche Daten wie Ihre Tests in Ihrer Entwicklungsumgebung sehen. Zu diesem Zeitpunkt erfassen Sie jetzt Daten auf Ihrer Site und können nun Adobe Analytics für die Berichterstellung verwenden.

## Fehlerbehebung

**Im Debugger werden keine Daten angezeigt.**

Öffnen Sie auf Ihrer Site die Entwicklerkonsole des Browsers (normalerweise F12). Sehen Sie sich den Quellcode der Seite an und stellen Sie sicher, dass Folgendes erfüllt ist:

* Es gibt keine JavaScript-Fehler in der Konsole. Wenden Sie sich an die Website-Inhaber Ihres Unternehmens, um sicherzustellen, dass alle JS-Fehler behoben sind.
* Der Kopfzeilencode ist ordnungsgemäß implementiert: Stellen Sie sicher, dass sich der Kopfzeilencode innerhalb des `<head>`-Tags befindet und dass die Datei vorhanden ist.
* AppMeasurement-Bibliothek vorhanden: Navigieren Sie direkt zur JS-Quelle, um sicherzustellen, dass die JS-Datei Code enthält. Ist dies nicht der Fall, stellen Sie sicher, dass jede Umgebung erstellt und die Bibliothek in der entsprechenden Umgebung veröffentlicht wurde.
* Erweiterungen abhören: Einige Erweiterungen, wie z. B. Anzeigensperren, können das Auslösen von Bildanforderungen verhindern. Deaktivieren Sie alle Erweiterungen, die verhindern könnten, dass Daten an Adobe gesendet werden.

## Nächste Schritte

Nachdem eine Basisimplementierung eingerichtet wurde, kann Ihre Rolle innerhalb Ihres Unternehmens beeinflussen, über welchen Pfad Sie mehr erfahren möchten:

* [Erstellen Sie ein Lösungsdesigndokument](../prepare/solution-design.md): Planen Sie, wie Sie benutzerdefinierte Variablen verwenden möchten, und schließen Sie sie dann in Ihre Implementierung ein
* [Erste Schritte mit Analysis Workspace](/help/analyze/analysis-workspace/home.md): Tauchen Sie mit der Flagship-Funktion des Tools direkt in Adobe Analytics ein.
