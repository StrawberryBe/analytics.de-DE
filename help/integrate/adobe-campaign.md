---
description: Erfahren Sie, wie Sie die Adobe Campaign Standard-Berichterstellung in Adobe Analytics aktivieren
title: Wie integriere ich Adobe Campaign Standard Reporting in Adobe Analytics?
feature: Campaign Integration
exl-id: 63bae5ee-f94d-43fa-87ce-6380236745d6
source-git-commit: 0a039668af52a0e5433f9b0c4e643db566b95702
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 68%

---

# Adobe Campaign Standard Reporting

Weitere Informationen zum Konfigurieren dieser Integrationen finden Sie in der [Adobe Campaign-Dokumentation](https://helpx.adobe.com/de/campaign/standard/integrating/using/about-campaign-analytics-integration.html)

>[!IMPORTANT]
>Dieser Artikel gilt für Adobe Campaign **Standard** nur Berichterstellung. Siehe [here](https://experienceleague.adobe.com/docs/analytics/integration/analytics-to-campaign-classic.html?lang=en) zum Hinzufügen von Adobe Campaign **Classic** Berichterstellung.

Diese Integration zwischen Adobe Analytics und Adobe Campaign Standard:

* können Sie Ihre KPI (Key Performance Indicator)-Daten aus Adobe Campaign Standard in Adobe Analytics freigeben.
* werden Verfolgungsformeln mit Adobe Analytics-Parametern erweitert.
* wird unter **[!UICONTROL Analytics]** > **[!UICONTROL Berichte]** > **[!UICONTROL Adobe Campaign]** ein neuer Bericht hinzugefügt.
* werden 5 neue Adobe Campaign-Klassifizierungen hinzugefügt.
* werden 9 neue Adobe Campaign-Metriken hinzugefügt.
* werden 6 neue Adobe Campaign-Dimensionen hinzugefügt.
* Synchronisiert Daten alle 15 Minuten mit Analytics über eine automatisch bereitgestellte Datenquelle.

## Schritt 1. Adobe Campaign Standard Reporting aktivieren {#section_C685EF10505045708A6536BB13F6CD58}

Um Campaign Standard-Daten in Analytics anzeigen zu können, müssen Sie zunächst die Kampagnenberichterstellung im Report Suite Manager aktivieren.

1. Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **`<select report suite>`** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Berichterstellung für Adobe Campaign]** .
1. Klicken Sie auf **[!UICONTROL Berichterstellung für Campaign aktivieren]**.

   ![](assets/enable-campaign.png)

## Schritt 2. Anzeigen von Adobe Campaign-Berichten {#section_9C18A29F3CC54BD4AC5EA96417F17B33}

Durch die Integration zwischen Adobe Campaign Standard und Adobe Analytics wird die folgende Berichtsnummer unter **[!UICONTROL Analytics]** > **[!UICONTROL Berichte]** hinzugefügt.

* **[!UICONTROL Ausgeführte Adobe Campaign-Bereitstellungs-ID]**: Zeigt Daten zu aus Adobe Campaign importierten E-Mails an, die von Adobe Campaign gesendet wurden. |

## Schritt 3. Verwenden von Klassifizierungen in Adobe Campaign {#section_74A28AF3F4CA4091943789DE4D8B2B63}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **`<select report suite>`** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Adobe Campaign Classifications]**

Nach der Aktivierung der Report Suite für Adobe Campaign sind die folgenden Klassifizierungen verfügbar:

| Klassifizierung | Beschreibung |
| --- | --- |
| [!UICONTROL Bereitstellungs-ID] | Interner Versandname, den Sie in Campaign sehen |
| [!UICONTROL Versandtitel] | Versand in Campaign - Individuelle Bereitstellung/wiederkehrende Bereitstellung/Transaktionsbereitstellung |
| [!UICONTROL Kampagnen-ID] | Interner Kampagnenname, den Sie in Campaign sehen |
| [!UICONTROL Kampagnenbezeichnung] | Campaign in Adobe Campaign |
| [!UICONTROL Bezeichnung der ausgeführten Bereitstellung] | Liste der jeweils ausgeführten Sendungen |

## In Adobe Analytics verfügbare Adobe Campaign Standard-Dimensionen und -Metriken {#section_F33385C9660644AF84172EC39601469B}

Die folgenden **Metriken** sind in Campaign der Adobe Analytics Report Suites verfügbar:

* Adobe Campaign – Gesendet
* Adobe Campaign – Geöffnet
* Adobe Campaign – Geklickt
* Adobe Campaign – Geliefert
* Adobe Campaign – Einzelöffnung
* Adobe Campaign – Einzelklick
* Adobe Campaign – Abonnement beendet
* Adobe Campaign – Rücksendungen insgesamt
* Adobe Campaign – Instanzen für ID der ausgeführten Bereitstellung

Die folgenden **Dimensionen** sind in Campaign der Adobe Analytics Report Suites verfügbar:

| Name der Dimension | Definition |
| --- | --- |
| Kampagnen-ID | ID aller Kampagnen, für die während der Dauer KPIs gesendet wurden. |
| Kampagnenbezeichnung | Bezeichnungen der Kampagnen-IDs |
| Bereitstellungs-ID | ID aller Bereitstellungen, für die während der Dauer KPIs gesendet wurden. Beinhaltet zudem die IDs von Master-Bereitstellungen für periodische Bereitstellungen und Transaktionsbereitstellungen. Beispiel: Eine periodische Bereitstellung DM1 wurde geplant und DM2, DM3, DM4 und DM5 waren untergeordnete Bereitstellungen der periodischen Bereitstellung.  Die Bereitstellungs-ID zeigt Ergebnisse für alle Bereitstellungen von DM1 bis DM5 an. |
| Versandtitel | Bezeichnungen der Bereitstellungs-IDs |
| ID der ausgeführten Bereitstellung | IDs von nur ausgeführten Bereitstellungen. Keine ID einer periodischen/transaktionsbezogenen Master-Bereitstellung. Beispiel: Eine periodische Bereitstellung DM1 wurde geplant und DM2, DM3, DM4 und DM5 waren untergeordnete Bereitstellungen der periodischen Bereitstellung. Die ausgeführte Bereitstellungs-ID zeigt Ergebnisse für alle Bereitstellungen von DM2 bis DM5 an – dies sind die tatsächlich ausgeführten Bereitstellungen. |
| Bezeichnung der ausgeführten Bereitstellung | Bezeichnungen der ausgeführten Bereitstellungs-IDs |
