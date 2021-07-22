---
title: Entwicklungsimplementierung validieren und in der Produktion veröffentlichen
description: Erfahren Sie, wie Sie mit Adobe Experience Platform-Tags Adobe Analytics in Ihrer Produktionsumgebung bereitstellen.
exl-id: 2f5bcfee-d75e-4dac-bea9-91c6cc545173
source-git-commit: 5368e808a862a3e320f5d079433db96ab79b45c8
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 64%

---

# Entwicklungsimplementierung validieren und in der Produktion veröffentlichen

Sobald Ihre Tag-Bibliothek in die Produktion verschoben wurde, kann Ihr Unternehmen mit der Verwendung von Adobe Analytics beginnen, um grundlegende Berichte abzurufen.

>[!NOTE]
>Adobe Experience Platform Launch wurde in Experience Platform als eine Suite von Datenerfassungstechnologien umbenannt. Infolgedessen wurden in der gesamten Produktdokumentation mehrere terminologische Änderungen eingeführt. Eine konsolidierte Übersicht der terminologischen Änderungen finden Sie im folgenden [Dokument](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en).

## Voraussetzungen

[Stellen Sie Ihre Analytics-Implementierung in Ihrer Entwicklungsumgebung bereit](deploy-dev.md): Eine Analytics-Implementierung muss in Ihrer Entwicklungsumgebung veröffentlicht werden, um dieser Seite zu folgen.

## Überprüfung der Dev-Implementierung mit dem Experience Cloud-Debugger

Der Experience Cloud-Debugger ist ein Chrome-Plug-in, das alle auf einer Seite vorhandenen Experience Cloud-Tags anzeigt.

1. Öffnen Sie den [Chrome-Webbrowser](https://www.google.com/intl/de/chrome/) und gehen Sie zu [Adobe Experience Cloud-Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) im Chrome Web Store, um die Erweiterung zu installieren.
2. Navigieren Sie zu Ihrer Entwicklungswebsite, auf der Sie Tags implementiert haben.
3. Klicken Sie oben rechts in Chrome auf das Symbol für den Adobe Experience Cloud-Debugger.
4. Wenn alles ordnungsgemäß implementiert ist, sollten Inhalte in Adobe Analytics, Tags und dem Adobe Experience Cloud-Besucher-ID-Dienst angezeigt werden:

![Debugger][assets/debugger.png]

## Bereitstellen der Dev-Implementierung für Staging/Produktion.

Nachdem Sie überprüft haben, dass Daten angezeigt werden, können Sie Ihre Implementierung an die Live-Version Ihrer Site übertragen.

1. Gehen Sie zu [experience.adobe.com](https://experience.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Wählen Sie **[!UICONTROL Launch/Data Collection]** aus.
1. Klicken Sie auf **[!UICONTROL Gehen Sie zu Launch/Data Collection]** und wählen Sie **[!UICONTROL Tags]** aus.
1. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Publishing]** und suchen Sie Ihre Bibliothek in der Spalte &quot;Entwicklung&quot;.
1. Klicken Sie in der Bibliothek auf das Dropdown-Menü und wählen Sie **[!UICONTROL Zur Genehmigung übermitteln]** aus. Klicken Sie im modalen Fenster auf **[!UICONTROL Submit]** .
1. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek (jetzt in der Spalte &quot;Gesendet&quot;) und wählen Sie **[!UICONTROL Build für Staging]** aus.
1. Nach einigen Augenblicken wird das gelbe Licht der Bibliothek grün, was auf eine erfolgreiche Erstellung hinweist.
1. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek und wählen Sie **[!UICONTROL Zur Veröffentlichung genehmigen]** aus.
1. Klicken Sie erneut auf das Dropdown-Menü der Bibliothek (jetzt in der Spalte [!UICONTROL Genehmigt] ) und wählen Sie **[!UICONTROL Erstellen und in Produktion veröffentlichen]** aus.
1. Klicken Sie auf der Registerkarte Umgebungen auf **[!UICONTROL Produktionsumgebung]**.
1. Kopieren Sie den Produktions-Kopf- und -Fußzeilencode und stellen Sie ihn Ihren Website-Inhabern zur Verfügung. Fordern Sie an, diesen Code in der Produktionsumgebung Ihrer Site zu implementieren.

## Überprüfen der Produktionsimplementierung

Vergewissern Sie sich, dass Sie Daten zur Live-Version Ihrer Site sehen, und beginnen Sie mit der offiziellen Datenerfassung für Adobe Analytics.

1. Nachdem Sie von Ihren Website-Eigentümern bestätigt haben, dass sie den Tag-Code in die Produktion gepusht haben, navigieren Sie zur Homepage Ihrer Website in Chrome und öffnen Sie den [!UICONTROL Adobe Experience Cloud-Debugger].
2. Wenn alles funktioniert, sollten Sie ähnliche Daten wie Ihre Tests in Ihrer Entwicklungsumgebung sehen. Zu diesem Zeitpunkt erfassen Sie jetzt Daten auf Ihrer Site und können nun Adobe Analytics für die Berichterstellung verwenden.

## Fehlerbehebung

**Im Debugger werden keine Daten angezeigt.**

Öffnen Sie auf Ihrer Site die Entwicklerkonsole des Browsers (normalerweise F12). Sehen Sie sich den Quellcode der Seite an und stellen Sie sicher, dass Folgendes erfüllt ist:

* Es gibt keine JavaScript-Fehler in der Konsole. Wenden Sie sich an die Website-Inhaber Ihres Unternehmens, um sicherzustellen, dass alle JS-Fehler behoben sind.
* Der Kopfzeilencode ist ordnungsgemäß implementiert: Stellen Sie sicher, dass sich der Kopfzeilencode innerhalb des `<head>`-Tags befindet und dass die Datei vorhanden ist.
* AppMeasurement-Bibliothek vorhanden: Navigieren Sie direkt zur JS-Quelle, um sicherzustellen, dass die JS-Datei Code enthält. Ist dies nicht der Fall, stellen Sie sicher, dass jede Umgebung erstellt und die Bibliothek in der entsprechenden Umgebung veröffentlicht wurde.
* Störende Plug-ins: Einige Chrome-Plug-ins können das Auslösen von Bildanforderungen verhindern. Deaktivieren Sie alle Plug-ins, die verhindern könnten, dass Daten an die Adobe-Server gesendet werden.

## Nächste Schritte

Nachdem eine Basisimplementierung eingerichtet wurde, kann Ihre Rolle innerhalb Ihres Unternehmens beeinflussen, über welchen Pfad Sie mehr erfahren möchten:

* [Erstellen Sie ein Lösungsdesigndokument](../prepare/solution-design.md): Planen Sie, wie Sie benutzerdefinierte Variablen verwenden möchten, und schließen Sie sie dann in Ihre Implementierung ein
* [Erste Schritte mit Analysis Workspace](/help/analyze/analysis-workspace/home.md): Tauchen Sie mit der Flagship-Funktion des Tools direkt in Adobe Analytics ein.
