---
description: Der Bericht "Links"enthält die Links, die auf der aktuellen Seite gefunden wurden. Es werden nicht alle Links gemeldet, die für diese Seite erfasst wurden.
title: Link-Bericht
topic: Activity map
uuid: 1e7ca5d8-d144-4a21-a2f9-e05bd3232c59
translation-type: tm+mt
source-git-commit: 6b27755178d156b1eaf159640d466bd84659983d

---


# Link-Bericht

Der Bericht &quot;Links&quot;enthält die Links, die auf der aktuellen Seite gefunden wurden. Es werden nicht alle Links gemeldet, die für diese Seite erfasst wurden.

Der Bericht &quot;Links auf Seite&quot;Angebot eine tabellarische Ansicht der Links. In einigen Fällen möchten Sie eventuell Link-Klicks (oder andere Metriken) in einer einzigen Ansicht nach Rang sortieren. Dadurch können Sie einen Link besser mit einem anderen vergleichen. Erstellen Sie den Bericht &quot;Links auf Seite&quot;, der eine Rangfolge aller Links auf der Seite (nach Link-ID), die Klickinformationen (# und %) und den Seitenbereich enthält. Klicken Sie in der Symbolleiste &quot;Aktivität&quot;auf die Schaltfläche &quot;Seitenbericht&quot;.

The **[!UICONTROL Links On Page]** report opens below the browser frame in the Activity Map dashboard.

## Standardmodus {#section_C8D2A1C07A2A4E3A8F84AC9240603FA7}

![](assets/links_in_page.png)

Im Standardmodus zeigt der Bericht &quot;Links auf Seite&quot;Link-Daten von einem Tag bis zu mehreren Tagen an, die über den gesamten Datumsbereich aggregiert wurden. Für jeden Link werden die folgenden Informationen angezeigt:

<table id="table_3DE41B2CFA644B70AF802A3123CE51D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Spalte </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Rang </td> 
   <td colname="col2"> Rang auf der Seite. Im Standardmodus bleibt der Rangwert gleich, unabhängig davon, auf welche Spalte Sie klicken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Link-ID </td> 
   <td colname="col2">The link's primary ID (for more information on how primary ID is defined by the <a href="/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md">New Link Tracking Methodology</a>) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Klicks </td> 
   <td colname="col2"> Die Anzahl der Rohdaten für einen bestimmten Link und der Prozentsatz der Gesamtklicks auf der Seite. Wenn der Benutzer eine andere Metrik in der Symbolleiste auswählt, wird der Link-Bericht stattdessen über diese Metrik berichtet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Region </td> 
   <td colname="col2"> Stellt die Region auf der Seite dar, auf der sich der Link befindet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sichtbarkeit </td> 
   <td colname="col2">Bezieht sich auf den Sichtbarkeitsstatus des Links. Es sind zwei Werte möglich: 
    <ul id="ul_BABCC0F64145407C9D439150A6898E6D">
     <li id="li_9AF0479BDCEB4A44A37292FAABFA83A5"><b>Ausgeblendet</b>: der Link befindet sich derzeit auf der Seite, für den Endbenutzer jedoch nicht sichtbar ist (z. B. ein Untermenü in einem Navigationsmenü, das nur sichtbar wird, wenn der Benutzer den Mauszeiger über dem übergeordneten Menü bewegt) </li>
     <li id="li_C6FA4EC27EDD4341AB9821E2B4BC9E60"><b>Angezeigt</b>: der Link wird derzeit auf der Seite angezeigt. Er kann jedoch unterhalb der Kante angezeigt werden: der Benutzer muss die Seite scrollen, um sie zu sehen. </li>
    </ul><p>Hinweis: Wenn ein Link auf „Verborgen“ gesetzt ist, werden keine Überlagerungen dafür angezeigt. </p></td> 
  </tr> 
 </tbody> 
</table>

**Daten filtern**

When you want to zero in on a specific link, you can search for a related term in the **[!UICONTROL Filter Data]** field. Nur die Links, die der Suche entsprechen, haben Überlagerungen. Ohne Filter werden die in den Einstellungen für die [Aktivität-Map angegebenen Überlagerungen angezeigt](/help/analyze/activity-map/activitymap-overlay-settings.md) .

## Livemodus {#section_AC1967217B5A4532ACB01D33636F6770}

Im Livemodus zeigt der Bericht „Links auf Seite“ die Trenddaten über mehrere Minuten an.

![](assets/links_on_page.png)

<table id="table_61D1FB0F02894055A1AB394DE4FE4742"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Spalte </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Rang </td> 
   <td colname="col2"> Rang auf der Seite. Bei einer Verlaufs- oder Blasenüberlagerung bleibt der Rangwert gleich, unabhängig davon, auf welche Spalte Sie klicken. Bei einer Gewinner-/Verlierer-Überlagerung ändert sich der Rangwert je nachdem, welche Links am meisten gewonnen/verloren haben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Link-ID </td> 
   <td colname="col2">Die primäre ID des Links. For more information on how the primary ID is defined by the New <a href="/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md"> Link Tracking Methodology</a>. </td>
  </tr> 
  <tr> 
   <td colname="col1"> Link-Klicks </td> 
   <td colname="col2"> Klicks insgesamt für den ausgewählten Zeitraum. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> % Änderung </td> 
   <td colname="col2"> % Änderung zwischen den Linkmetriken des aktuellen Zeitraums und den Linkmetriken des vorherigen Zeitraums. Negative prozentuale Veränderung wird in Rot, positive in Grün dargestellt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Trend </td> 
   <td colname="col2"> Ein Liniendiagramm für alle erfassten Zeiträume. Der aktuell ausgewählte Zeitraum wird durch eine grüne Markierung gekennzeichnet. Der Zeitraum, auf den der Mauszeiger bewegt wird, wird durch eine rote Markierung gekennzeichnet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Region </td> 
   <td colname="col2"> Stellt den Bereich auf der Seite dar, auf der sich der Link befindet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sichtbarkeit </td> 
   <td colname="col2">Bezieht sich auf den Sichtbarkeitsstatus des Links. Es sind zwei Werte möglich: 
    <ul id="ul_B10C55ED4D3C4CF99506DC467E2E7CFB">
     <li id="li_EA646722A51041CC9E62C56DEF92C81F">Ausgeblendet: ist derzeit auf der Seite, für Sie jedoch nicht sichtbar (z. B. ein Link, der nach dem Laden der Seite angezeigt wird). </li>
     <li id="li_F9543614C2894003AC9984A7404E2785">Angezeigt: wird derzeit auf der Seite angezeigt. Er kann jedoch unterhalb der Kante angezeigt werden: Sie müssten einen Bildlauf auf der Seite durchführen, um sie zu sehen. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

## Sortieren und Filtern {#section_4B8E8233C21247CAA70DAEC2156548AD}

Manchmal müssen Sie nur die Ergebnisse eines bestimmten Seitenbereichs analysieren (z. B. des linken Bereichs), um zu entscheiden, wie der Inhalt dieses bestimmten Bereichs der Webseite organisiert werden soll.

Zu diesem Zweck haben wir eine Sortier- und Filterfunktion für Links im Bericht &quot;Links auf Seite&quot;erstellt. Die Filterung ist über das Filterfeld verfügbar. Der Suchbegriff wird auf die Spalte &quot;Link-ID&quot;und &quot;Linkregion&quot;angewendet. Die Sortierung ist durch Klicken auf die Aufrufe (Rang, Link-ID, Klicks, Änderung im Zeitverlauf, Region, Sichtbarkeit) möglich und kann sowohl aufsteigend als auch absteigend sein. Überlagerungen verschwinden von der Website, wenn Links aus dem Bericht &quot;Links auf Seite&quot;herausgefiltert werden.
