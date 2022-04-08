---
title: Erstellen einer Analytics-Eigenschaft in Tags
description: Erstellen Sie mithilfe von Tags einen Bereich, um die Art der Datenerfassung anzupassen.
feature: Launch Implementation
exl-id: ffcd8e97-4d29-489e-bc2b-88805400dad5
source-git-commit: f4b495b11bcbd55bc8448f2c9c09268547fb9750
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Erstellen einer Tag-Eigenschaft in Adobe Analytics

Mit Tags in Adobe Experience Platform können Sie Experience Cloud-Lösungen auf Ihrer Website integrieren (einschließlich Analytics). Auf dieser Seite wird erläutert, wie ein Tag-Administrator eine grundlegende Adobe Analytics-Implementierung ordnungsgemäß konfigurieren kann.

## Voraussetzungen

[Report Suite erstellen](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Erstellen eines Silos für zu erfassende Analytics-Daten..

## Erstellen einer Tag-Eigenschaft und Installieren wichtiger Erweiterungen

Eigenschaften sind übergreifende Container, die Sie zum Verwalten von Tags verwenden. Mit Erweiterungen können Sie produktspezifische Tags installieren und konfigurieren.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf **[!UICONTROL Neue Eigenschaft]**.
1. Geben Sie Ihrer Eigenschaft einen Namen, z. B. den Titel Ihrer Website, und geben Sie die Domain ein, auf der Sie Analytics implementieren möchten. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Klicken Sie auf die neu erstellte Tag-Eigenschaft, um deren Einstellungen einzugeben.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Erweiterungen]** und dann auf **[!UICONTROL Katalog]**.
1. Suchen Sie nach „Experience Cloud-ID-Dienst“ und klicken Sie auf **[!UICONTROL Installieren]**.
1. Alle Einstellungen, einschließlich Experience Cloud-Organisations-ID, sollten bereits ausgefüllt sein. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Suchen Sie im Erweiterungskatalog nach Adobe Analytics und klicken Sie auf **[!UICONTROL Installieren]**.

Die vollständige Dokumentation finden Sie in der [Adobe Analytics-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de) für detailliertere Informationen.

## Datenelemente für Adobe Analytics erstellen

Datenelemente sind Verweise auf bestimmte Teile Ihrer Website zur Erfassung von Variablenwerten.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Datenelemente]** und dann auf **[!UICONTROL Datenelement hinzufügen]**.
1. Legen Sie für das Datenelement die folgenden Einstellungen fest:

   * Name: Seitenname
   * Erweiterung: Core
   * Datenelementtyp: JavaScript-Variable
   * JavaScript-Variablenname: `window.document.title`

      >[!NOTE]
      >
      >Dieser Wert dient als Beispiel für die ersten Schritte. Wenn Ihr Unternehmen einen besseren Wert für den Seitennamen definiert, z. B. einen Datenschichtwert, können Sie ihn hier eingeben.
   * Markierter Text
   * Speicherdauer: Keines
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Regeln für Adobe Analytics erstellen

Regeln ordnen Datenelemente Analytics-Variablenwerten zu und bestimmen, wann diese Werte an die Adobe-Server gesendet werden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Klicken Sie auf **[!UICONTROL Regeln]** Registerkarte und klicken Sie dann auf **[!UICONTROL Regel hinzufügen]**. Benennen Sie ihn `Global Rule`.
1. Klicken Sie neben „Ereignisse“ auf **[!UICONTROL Hinzufügen]** und geben Sie die folgenden Einstellungen ein:
   * Erweiterung: Core
   * Ereignistyp: Bibliothek geladen (Seitenanfang)
   * Name: Core - Bibliothek geladen (Seitenanfang)
1. Klicken Sie auf **[!UICONTROL Änderungen beibehalten]**.
1. Klicken Sie unter **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]** und geben Sie die folgenden Einstellungen ein:
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
1. Vergewissern Sie sich, dass das Ereignis und zwei Aktionen festgelegt sind, und klicken Sie auf **[!UICONTROL Speichern]**.

## Nächste Schritte

[Stellen Sie Ihre Analytics-Implementierung in Ihrer Entwicklungsumgebung bereit](deploy-dev.md): Analytics-Code in einer Testumgebung verwenden.
