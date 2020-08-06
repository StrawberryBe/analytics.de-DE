---
title: Analytics-Eigenschaft in Launch erstellen
description: Erstellen Sie mit Adobe Experience Platform Launch einen Bereich zur Anpassung der Datenerfassung.
translation-type: tm+mt
source-git-commit: 763c1b7405c1a1b3d6dbd685ce796911dd4ce78b
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 98%

---


# Analytics-Eigenschaft in Adobe Experience Platform Launch erstellen

Adobe Experience Platform Launch ist das Tool, mit dem Sie Experience Cloud-Lösungen auf Ihrer Website integrieren können (einschließlich Analytics). Auf dieser Seite wird speziell erläutert, wie ein Launch-Administrator eine grundlegende Adobe Analytics-Implementierung ordnungsgemäß konfigurieren kann.

## Voraussetzungen

[Report Suite erstellen](/help/admin/admin-console/create-report-suite.md): Erstellen eines Silos für zu erfassende Analytics-Daten.

## Eigenschaften erstellen und wichtige Erweiterungen installieren

Eigenschaften sind übergreifende Container, die Sie zum Verwalten von Tags verwenden. Mit Erweiterungen können Sie produktspezifische Tags installieren und konfigurieren.

1. Wechseln Sie zu [launch.adobe.com](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf „Neue Eigenschaft“.
1. Geben Sie Ihrer Eigenschaft einen Namen, z. B. den Titel Ihrer Website, und geben Sie die Domäne ein, auf der Sie Analytics implementieren möchten. Klicken Sie auf „Speichern“.
1. Klicken Sie auf die neu erstellte Eigenschaft, um deren Einstellungen einzugeben.
1. Klicken Sie auf die Registerkarte „Erweiterungen“ und dann auf „Katalog“.
1. Suchen Sie nach „Identitätsdienst“ und klicken Sie dann auf „Installieren“.
1. Alle Einstellungen, einschließlich Experience Cloud-Organisations-ID, sollten bereits ausgefüllt sein. Klicken Sie auf „Speichern“.
1. Suchen Sie im Erweiterungskatalog nach Adobe Analytics und klicken Sie auf Installieren.

## Datenelemente für Adobe Analytics erstellen

Datenelemente sind Verweise auf bestimmte Teile Ihrer Website zur Erfassung von Variablenwerten.

1. Wechseln Sie zu [launch.adobe.com](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf die Launch-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Klicken Sie auf die Registerkarte „Datenelemente“ und dann auf „Neues Datenelement erstellen“.
1. Legen Sie für das Datenelement die folgenden Einstellungen fest:

   * Name: Seitenname
   * Erweiterung: Core
   * Datenelementtyp: JavaScript-Variable
   * Pfad zur Variable: `window.document.title`

      >[!NOTE]
      >
      >Dies ist ein Beispielwert für den Einstieg. Wenn Ihr Unternehmen einen besseren Wert für den Seitennamen definiert, z. B. einen Datenschichtwert, können Sie ihn hier eingeben.
   * Markierter Text
   * Dauer: Seitenansicht
1. Klicken Sie auf „Speichern“.

## Regeln für Adobe Analytics erstellen

Regeln ordnen Datenelemente Analytics-Variablenwerten zu und bestimmen, wann diese Werte an die Adobe-Server gesendet werden.

1. Wechseln Sie zu [launch.adobe.com](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf die Launch-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Klicken Sie auf „Neue Regel erstellen“ und benennen Sie sie `Global Rule`.
1. Klicken Sie neben „Ereignisse“ auf „Hinzufügen“ und geben Sie die folgenden Einstellungen ein:
   * Erweiterung: Core
   * Ereignistyp: Bibliothek geladen (Seitenanfang)
   * Name: Core - Bibliothek geladen (Seitenanfang)
   * Bestellung: 50
1. Klicken Sie auf „Änderungen beibehalten“.
1. Klicken Sie unter „Aktionen“ auf „Hinzufügen“ und geben Sie die folgenden Einstellungen ein:
   * Erweiterung: Adobe Analytics
   * Aktionstyp: Variablen festlegen
   * Seitenname: Klicken Sie auf das Container-Symbol und wählen Sie das `Page Name`-Datenelement aus
   * Kampagne: Abfrageparameter mit dem Wert `cid`
1. Klicken Sie auf „Änderungen beibehalten“.
1. Klicken Sie auf das Pluszeichen neben „Aktionen“, um eine weitere Aktion hinzuzufügen, und geben Sie die folgenden Einstellungen ein:
   * Erweiterung: Adobe Analytics
   * Aktionstyp: Beacon senden
   * Name: Adobe Analytics - Beacon senden
   * Tracking: s.t()
1. Klicken Sie auf „Änderungen beibehalten“.
1. Vergewissern Sie sich, dass das Ereignis und zwei Aktionen festgelegt sind, und klicken Sie auf Speichern.

## Dokumentation und zusätzliche Ressourcen

* [Dokumentation zu Adobe Analytics-Erweiterungen](https://docs.adobelaunch.com/extension-reference/web/adobe-analytics-extension): Vollständige Dokumentation speziell für die Adobe Analytics-Erweiterung in Adobe Experience Platform Launch.
* [Erste Schritte mit Launch](https://docs.adobelaunch.com/getting-started): Vollständige Dokumentation für den Start, einschließlich einer ausführlicheren Anleitung für die ersten Schritte.
* [Adobe Experience Platform Launch-YouTube-Kanal](https://www.youtube.com/channel/UCa84ntcvYhPArOBsZIRE2Jw/videos?view=0&amp;shelf_id=0&amp;sort=dd): Lehrvideos zur Nutzung von Launch.

## Nächste Schritte

[Stellen Sie Ihre Analytics-Implementierung in Ihrer Entwicklungsumgebung bereit](deploy-dev.md): Analytics-Code in einer Testumgebung verwenden.
