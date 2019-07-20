---
title: Erstellen einer Analytics-Eigenschaft im Start
seo-title: Erstellen einer Adobe Analytics-Eigenschaft in Adobe Experience Platform Launch
description: Erstellen Sie mithilfe des Adobe Experience Platform Launch einen Bereich, um die Art der Datenerfassung anzupassen.
seo-description: Erstellen Sie mithilfe des Adobe Experience Platform Launch einen Bereich zur Anpassung der Daten in Adobe Analytics.
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Erstellen einer Analytics-Eigenschaft in Adobe Experience Platform Launch

Adobe Experience Platform Launch ist das Tool, mit dem Sie Experience Cloud-Lösungen in Ihre Website integrieren können (einschließlich Analytics). Diese Seite erläutert insbesondere, wie ein Start-Administrator eine einfache konfigurierte Adobe Analytics-Implementierung erhalten kann.

## Voraussetzungen

[Erstellen Sie eine Report Suite](../../admin/admin-console/create-report-suite.md): Erstellen Sie ein Silo für die zu erfassenden Analytics-Daten.

## Erstellen Sie eine Eigenschaft und installieren Sie wichtige Erweiterungen.

Eigenschaften sind übergeordnete Container, die Sie zur Verwaltung von Tags verwenden. Mit Erweiterungen können Sie produktspezifische Tags installieren und konfigurieren.

1. Go to [launch.adobe.com](https://launch.adobe.com) and log in if prompted.
1. Klicken Sie auf "Neue Eigenschaft" .
1. Geben Sie Ihrer Eigenschaft einen Namen, z. B. den Titel Ihrer Website, und geben Sie die Domäne ein, auf der Sie Analytics implementieren möchten. Klicken Sie auf „Speichern“.
1. Klicken Sie auf die neu erstellte Eigenschaft, um deren Einstellungen einzugeben.
1. Klicken Sie auf die Registerkarte Erweiterungen und dann auf Katalog.
1. Suchen Sie nach dem Identitätsdienst und klicken Sie auf Installieren.
1. Alle Einstellungen, einschließlich der Experience Cloud-Organisations-ID, sollten bereits ausgefüllt sein. Klicken Sie auf „Speichern“.
1. Suchen Sie im erweiterten Katalog nach Adobe Analytics und klicken Sie auf Installieren.

## Datenelemente für Adobe Analytics erstellen

Datenelemente sind Verweise auf bestimmte Teile Ihrer Site, um Variablenwerte zu erfassen.

1. Go to [launch.adobe.com](https://launch.adobe.com) and log in if prompted.
2. Klicken Sie auf die Starteigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte Datenelemente und dann auf Neues Datenelement erstellen.
4. Geben Sie dem Datenelement die folgenden Einstellungen:
   * Name: Seitenname
   * Erweiterung: Core
   * Datenelementtyp: Javascript-Variable
   * Path to variable: `window.document.title`
      > [!NOTE] Hinweis: Dies ist ein Beispielwert für den Einstieg. Wenn Ihr Unternehmen einen besseren Wert für den Seitennamen definiert, z. B. einen Datenschichtwert, können Sie ihn hier eingeben.
   * Aktivierter Text aktiviert
   * Dauer: Seitenansicht
5. Klicken Sie auf „Speichern“.

## Erstellen von Regeln für Adobe Analytics

Regeln ordnen Datenelemente den Analytics-Variablenwerten zu und bestimmen, wann diese Werte an die Server von Adobe gesendet werden.

1. Go to [launch.adobe.com](https://launch.adobe.com) and log in if prompted.
1. Klicken Sie auf die Starteigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Click Create New Rule and name it `Global Rule`.
1. Klicken Sie neben Ereignissen auf Hinzufügen und geben Sie die folgenden Einstellungen ein:
   * Erweiterung: Core
   * Ereignistyp: Bibliothek geladen (Seitenanfang)
   * Name: Core - Bibliothek geladen (Seitenanfang)
   * Reihenfolge: 50
1. Klicken Sie auf Änderungen beibehalten.
1. Klicken Sie unter "Aktionen" auf" Hinzufügen" und geben Sie die folgenden Einstellungen ein:
   * Erweiterung: Adobe Analytics
   * Aktionstyp: Variablen festlegen
   * Page Name: click the container icon, and select the `Page Name` data element.
   * Campaign: Query parameter with a value of `cid`
1. Klicken Sie auf Änderungen beibehalten.
1. Klicken Sie auf das Pluszeichen neben Aktionen, um eine weitere Aktion hinzuzufügen, und geben Sie die folgenden Einstellungen ein:
   * Erweiterung: Adobe Analytics
   * Aktionstyp: Beacon senden
   * Name: Adobe Analytics - Beacon senden
   * Verfolgung: s. t ()
1. Klicken Sie auf Änderungen beibehalten.
1. Stellen Sie sicher, dass das Ereignis und zwei Aktionen festgelegt sind, und klicken Sie dann auf Speichern.

## Dokumentation und zusätzliche Ressourcen

* [Dokumentation zur Adobe Analytics-Erweiterung](https://docs.adobelaunch.com/extension-reference/web/adobe-analytics-extension): Vollständige Dokumentation speziell für die Adobe Analytics-Erweiterung in Adobe Experience Platform Launch.
* [Erste Schritte mit Start](https://docs.adobelaunch.com/getting-started): Vollständige Dokumentation für Launch, einschließlich detaillierter Einführungsschritte
* [Adobe Experience Platform Launch youtube channel](https://www.youtube.com/channel/UCa84ntcvYhPArOBsZIRE2Jw/videos?view=0&shelf_id=0&sort=dd): Erfahren Sie, wie Sie mit Videos starten.

## Nächste Schritte

[Implementieren Sie Ihre Analytics-Implementierung in Ihrer dev-Umgebung](deploy-dev.md): Analytics-Code in einer Testumgebung abrufen.
