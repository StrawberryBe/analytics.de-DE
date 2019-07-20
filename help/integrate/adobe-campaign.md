---
description: 'null '
seo-description: 'null '
seo-title: Adobe Campaign-Berichterstellung
title: Adobe Campaign-Berichterstellung
uuid: 0919 ae 9 f -84 eb -43 a 5-8282-6 cd 6 dec 63 dc 1
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Adobe Campaign-Berichterstellung

Weitere Informationen zum Konfigurieren dieser Integrationen finden Sie in der [Adobe Campaign-Dokumentation](https://helpx.adobe.com/campaign/standard/integrating/using/about-campaign-analytics-integration.html)

Mithilfe dieser Integration zwischen Adobe Analytics und Adobe Campaign

* können Sie Ihre KPI (Key Performance Indicator)-Daten aus Adobe Campaign Standard in Adobe Analytics freigeben.
* werden Verfolgungsformeln mit Adobe Analytics-Parametern erweitert.
* Adds a new report under  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Reports]** &gt; **[!UICONTROL Adobe Campaign.]**
* werden 5 neue Adobe Campaign-Klassifizierungen hinzugefügt.
* werden 10 neue Adobe Campaign-Metriken hinzugefügt.
* werden 6 neue Adobe Campaign-Dimensionen hinzugefügt.
* werden Daten alle 15 Minuten mit Analytics synchronisiert.

## Schritt 1. Aktivieren der Berichterstellung für Adobe Campaign {#section_C685EF10505045708A6536BB13F6CD58}

Wenn Sie Campaign-Daten in Analytics anzeigen möchten, müssen Sie zunächst Campaign-Berichte aktivieren.

1. Navigate to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL <select report suite>]** &gt; **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Adobe Campaign]** &gt; **[!UICONTROL Adobe Campaign Reporting]** .
1. Klicken Sie auf **[!UICONTROL Berichterstellung für Campaign aktivieren]**.

   ![](assets/enable-campaign.png)

## Schritt 2: Anzeigen von Adobe Campaign-Berichten {#section_9C18A29F3CC54BD4AC5EA96417F17B33}

The integration between Adobe Campaign Standard and Adobe Analytics adds the following report under  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Reports]**

<table id="table_3627F40DC90646A7B5E217A88B6FD630"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Bericht </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Campaign – ID der ausgeführten Bereitstellung </p> </td> 
   <td colname="col2"> <p>Zeigt aus Adobe Campaign importierte Daten über E-Mails an, die in Adobe Campaign gesendet wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Schritt 3. Adobe Campaign Classifications {#section_74A28AF3F4CA4091943789DE4D8B2B63}

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL <select report suite>]** &gt; **[!UICONTROL Einstellungen bearbeiten]** &gt; **[!UICONTROL Adobe Campaign]** &gt; **[!UICONTROL Adobe Campaign Classifications]**

Nach der Aktivierung der Report Suite für Adobe Campaign sind die folgenden Klassifizierungen verfügbar:

* Bereitstellungs-ID (in Campaign angezeigter, interner Bereitstellungsname)
* Bereitstellungsbeschriftung ((Bereitstellung in Kampagne - Individuelle Auslieferung/Wiederkehrende Auslieferung/Transaktionsbereitstellung)
* Kampagnen-ID (in Campaign angezeigter, interner Kampagnenname)
* Bereitstellungsbezeichnung (Campaign in Adobe Campaign)
* Ausgeführte Bereitstellungsbezeichnung (Liste der individuellen ausgeführten Bereitstellungen)

## In Adobe Analytics verfügbare Adobe Campaign-Dimensionen und -Metriken {#section_F33385C9660644AF84172EC39601469B}

Die folgenden **Metriken** sind in Campaign der Adobe Analytics Report Suites verfügbar:

* Adobe Campaign – Gesendet
* Adobe Campaign – Geöffnet
* Adobe Campaign – Geklickt
* Adobe Campaign – Verarbeitet
* Adobe Campaign – Geliefert
* Adobe Campaign – Einmalige Öffnung
* Adobe Campaign – Einmaliger Klick
* Adobe Campaign – Abonnement beendet
* Adobe Campaign – Rücksendungen insgesamt
* Adobe Campaign – Instanzen für ID der ausgeführten Bereitstellung

Die folgenden **Dimensionen** sind in Campaign der Adobe Analytics Report Suites verfügbar:

| Name der Dimension | Definition |
|--- |--- |
| Kampagnen-ID | ID aller Kampagnen, für die während der Dauer KPIs gesendet wurden |
| Kampagnenbezeichnung | Bezeichnungen der Kampagnen-IDs |
| Bereitstellungs-ID | ID aller Bereitstellungen, für die während der Dauer KPIs gesendet wurden. Beinhaltet zudem die IDs von Master-Bereitstellungen für periodische Bereitstellungen und Transaktionsbereitstellungen. Beispiel: Eine periodische Bereitstellung DM1 wurde geplant und DM2, DM3, DM4 und DM5 waren untergeordnete Bereitstellungen der periodischen Bereitstellung.  Die Bereitstellungs-ID zeigt Ergebnisse für alle Bereitstellungen von DM1 bis DM5 an. |
| Bereitstellungsbezeichnung | Bezeichnungen der Bereitstellungs-IDs |
| Ausgeführte Bereitstellungs-ID | IDs von nur ausgeführten Bereitstellungen. Keine ID einer periodischen/transaktionsbezogenen Master-Bereitstellung. Beispiel: Eine periodische Bereitstellung DM1 wurde geplant und DM2, DM3, DM4 und DM5 waren untergeordnete Bereitstellungen der periodischen Bereitstellung. Die ausgeführte Bereitstellungs-ID zeigt Ergebnisse für alle Bereitstellungen von DM2 bis DM5 an – dies sind die tatsächlich ausgeführten Bereitstellungen. |
| Bezeichnung der ausgeführten Bereitstellung | Bezeichnungen der ausgeführten Bereitstellungs-IDs |
