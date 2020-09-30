---
title: Analytics-Eigenschaft in Launch erstellen
description: Erstellen Sie mit Adobe Experience Platform Launch einen Bereich zur Anpassung der Datenerfassung.
translation-type: tm+mt
source-git-commit: 56ca9fa36db9d7dd126808280ba17f29f4b787d9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Analytics-Eigenschaft in Adobe Experience Platform Launch erstellen

Adobe Experience Platform Launch ist das Tool, mit dem Sie Experience Cloud-Lösungen auf Ihrer Website integrieren können (einschließlich Analytics). Auf dieser Seite wird speziell erläutert, wie ein Launch-Administrator eine grundlegende Adobe Analytics-Implementierung ordnungsgemäß konfigurieren kann.

## Voraussetzungen

[Report Suite erstellen](/help/admin/admin-console/create-report-suite.md): Erstellen eines Silos für zu erfassende Analytics-Daten.

## Eigenschaften erstellen und wichtige Erweiterungen installieren

Eigenschaften sind übergreifende Container, die Sie zum Verwalten von Tags verwenden. Mit Erweiterungen können Sie produktspezifische Tags installieren und konfigurieren.

1. Wechseln Sie zu [launch.adobe.com](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Click **[!UICONTROL New Property]**.
1. Geben Sie Ihrer Eigenschaft einen Namen, z. B. den Titel Ihrer Website, und geben Sie die Domäne ein, auf der Sie Analytics implementieren möchten. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Klicken Sie auf die neu erstellte Eigenschaft, um deren Einstellungen einzugeben.
1. Click the **[!UICONTROL Extensions]** tab, then click **[!UICONTROL Catalog]**.
1. Locate Identity Service, then click **[!UICONTROL Install]**.
1. Alle Einstellungen, einschließlich Experience Cloud-Organisations-ID, sollten bereits ausgefüllt sein. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Back in the extensions catalog, locate Adobe Analytics and click **[!UICONTROL Install]**.

## Datenelemente für Adobe Analytics erstellen

Datenelemente sind Verweise auf bestimmte Teile Ihrer Website zur Erfassung von Variablenwerten.

1. Wechseln Sie zu [launch.adobe.com](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf die Launch-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Click the **[!UICONTROL Data Elements]** tab, then click **[!UICONTROL Create New Data Element]**.
1. Legen Sie für das Datenelement die folgenden Einstellungen fest:

   * Name: Seitenname
   * Erweiterung: Core
   * Datenelementtyp: JavaScript-Variable
   * Pfad zur Variable: `window.document.title`

      >[!NOTE]
      >
      >Dies ist ein Beispielwert für die ersten Schritte. Wenn Ihr Unternehmen einen besseren Wert für den Seitennamen definiert, z. B. einen Datenschichtwert, können Sie ihn hier eingeben.
   * Markierter Text
   * Dauer: Seitenansicht
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Regeln für Adobe Analytics erstellen

Regeln ordnen Datenelemente Analytics-Variablenwerten zu und bestimmen, wann diese Werte an die Adobe-Server gesendet werden.

1. Wechseln Sie zu [launch.adobe.com](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf die Launch-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Click **[!UICONTROL Create New Rule]** and name it `Global Rule`.
1. Click **[!UICONTROL Add]** next to events, and enter the following settings:
   * Erweiterung: Core
   * Ereignistyp: Bibliothek geladen (Seitenanfang)
   * Name: Core - Bibliothek geladen (Seitenanfang)
   * Bestellung: 50
1. Klicken Sie auf **[!UICONTROL Änderungen beibehalten]**.
1. Under **[!UICONTROL Actions]**, click **[!UICONTROL Add]**, and enter the following settings:
   * Erweiterung: Adobe Analytics
   * Aktionstyp: Variablen festlegen
   * Seitenname: Klicken Sie auf das Container-Symbol und wählen Sie das `Page Name`-Datenelement aus
   * Kampagne: Abfrageparameter mit dem Wert `cid`
1. Klicken Sie auf **[!UICONTROL Änderungen beibehalten]**.
1. Klicken Sie auf das Pluszeichen neben „Aktionen“, um eine weitere Aktion hinzuzufügen, und geben Sie die folgenden Einstellungen ein:
   * Erweiterung: Adobe Analytics
   * Aktionstyp: Beacon senden
   * Name: Adobe Analytics - Beacon senden
   * Tracking: s.t()
1. Klicken Sie auf **[!UICONTROL Änderungen beibehalten]**.
1. Verify that you have the event and two actions set, then click **[!UICONTROL Save]**.

## Dokumentation und zusätzliche Ressourcen

* [Dokumentation zu Adobe Analytics-Erweiterungen](https://docs.adobelaunch.com/extension-reference/web/adobe-analytics-extension): Vollständige Dokumentation speziell für die Adobe Analytics-Erweiterung in Adobe Experience Platform Launch.
* [Erste Schritte mit Launch](https://docs.adobelaunch.com/getting-started): Vollständige Dokumentation für den Start, einschließlich einer ausführlicheren Anleitung für die ersten Schritte.
* [Adobe Experience Platform Launch Kanal](https://experienceleague.adobe.com/?tag=Launch#recommended/solutions/experience-platform): Einführung in Videos

## Nächste Schritte

[Stellen Sie Ihre Analytics-Implementierung in Ihrer Entwicklungsumgebung bereit](deploy-dev.md): Analytics-Code in einer Testumgebung verwenden.
