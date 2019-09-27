---
description: Zeigt Ihnen die Bereiche Ihrer Site, die Ihre Kunden am häufigsten aufrufen. Siteabschnitte können kategorienähnliche Produktgruppen enthalten, die Sie definieren. Sie können beispielsweise eine Seitengruppe „Kameras“ oder „Computer“ usw. einrichten. Daten für den Bericht „Konversionssitebereiche“ werden aus dem Bericht „Sitebereiche“ in der Traffic-Gruppe importiert, welcher seine Daten aus der Kanalvariablen im Trackingcode erhält. Mithilfe dieses Berichts können Sie die stärkste Auswirkung bestimmter Einheiten in unterschiedlichen Sitebereichen auf die Site-Statistik identifizieren.
seo-description: Zeigt Ihnen die Bereiche Ihrer Site, die Ihre Kunden am häufigsten aufrufen. Siteabschnitte können kategorienähnliche Produktgruppen enthalten, die Sie definieren. Sie können beispielsweise eine Seitengruppe „Kameras“ oder „Computer“ usw. einrichten. Daten für den Bericht „Konversionssitebereiche“ werden aus dem Bericht „Sitebereiche“ in der Traffic-Gruppe importiert, welcher seine Daten aus der Kanalvariablen im Trackingcode erhält. Mithilfe dieses Berichts können Sie die stärkste Auswirkung bestimmter Einheiten in unterschiedlichen Sitebereichen auf die Site-Statistik identifizieren.
seo-title: Sitebereiche
solution: Analytics
title: Sitebereiche
topic: Berichte
uuid: 6839c566-f88f-4979-9cf5-52a77c0b0416
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Sitebereiche

Zeigt Ihnen die Bereiche Ihrer Site, die Ihre Kunden am häufigsten aufrufen. Siteabschnitte können kategorienähnliche Produktgruppen enthalten, die Sie definieren. Sie können beispielsweise eine Seitengruppe „Kameras“ oder „Computer“ usw. einrichten. Daten für den Bericht „Konversionssitebereiche“ werden aus dem Bericht „Sitebereiche“ in der Traffic-Gruppe importiert, welcher seine Daten aus der Kanalvariablen im Trackingcode erhält. Mithilfe dieses Berichts können Sie die stärkste Auswirkung bestimmter Einheiten in unterschiedlichen Sitebereichen auf die Site-Statistik identifizieren.

* Dieser Bericht listet Daten direkt aus der auf Ihrer Website implementierten Variablen „[s.channel](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_channel.html)“ auf.
* Der Bericht kann sowohl als Trendansicht als auch als Rangansicht angezeigt werden.
* In diesem Bericht können bestimmte Zeileneinträge mit einem Suchfilter ermittelt werden.
* Sie können Classifications zum Umbenennen und Konsolidieren von Zeileneinträgen in diesem Bericht verwenden.
* Korrelationen können in den Admin Tools mit jeder beliebigen Traffic-Variablen erstellt werden.
* Dieser Bericht kann die folgenden Metriken verwenden:

   * **Seitenansichten**: Gibt an, wie oft die Variable [„pageName“](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_pagename.html) oder URL definiert wurde (als Standardmetrik festgelegt).

   * **Alle Pfadsetzungsmetriken**: Besuche, durchschnittliche Klicktiefe, durchschnittliche Besuchszeit pro Seite, Einstiege, Ausstiege, Neuladungen und Einzelzugriffe.
   * Je nach Report Suite-Einstellungen Ihrer Organisation kann die Erfassung von Unique Visitors pro Tag, Woche, Monat oder Quartal für den Bericht aktiviert werden.
   * **Alle E-Commerce-Standardmetriken**: Umsatz, Bestellungen, Einheiten, Warenkorb, Warenkorbansichten, Checkouts, Zusätze zum Warenkorb und Entnahmen aus Warenkorb.
   * **Alle benutzerspezifischen Ereignisse**: Ereignisse 1-80 und Ereignisse 81-100 bei H22-Code oder höher.

Alle Konversionsereignisse im [!UICONTROL Sitebereichsbericht] verwenden die letzte Zuordnung. Sie sehen die Konversion auf die Seiten aufgeteilt, die in Ihrer Implementierung keine Erfolgsereignisse enthalten. Das unterscheidet sich vom [Seitenbericht](../../../components/c-variables/dimensionslist/reports-pages.md#concept_0219136EA25745B58434D0C7E751D7D5), bei dem eine lineare Zuordnung verwendet wird.

**Produktspezifische Informationen**

<table id="table_525FDF95C8ED4BF2A1E25BE2DA971EFB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Schnittstelle </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Reports and Analytics </td> 
   <td colname="col2"> <p> <span class="uicontrol">„Site-Content“</span> &gt; <span class="uicontrol">„Sitebereiche“</span> </p> <p>Abgesehen von Korrelationen kann dieser Bericht die folgenden Aufschlüsselungen verwenden: </p> 
    <ul id="ul_9CD009D89B134C53807332E3C88D3C44"> 
     <li id="li_566417EB074D425C9A1F4FB28AA7FAB4"> 
      <ul id="ul_3795C7AAE6DA4B7E96FCDC7F3211DFBB"> 
       <li id="li_50B295E961724CFB83D222DE9B4C7FF2">Alle klassifizierten Berichte, die auf diesem Bericht basieren </li> 
       <li id="li_697682892D8841BC8120BEC0E1AE9753"> <span class="wintitle"> Bericht zu Trackingcodes</span> </li> 
       <li id="li_F6D893FCBA7A4B3EB04715833CA41022">  Berichte zu <span class="wintitle">Produkten</span> und <span class="wintitle">Kategorien</span> </li> 
       <li id="li_9F379E61DB4F4753AE1FFFC8F9C17347"> <span class="wintitle"> Bericht zur Kundenloyalität</span> </li> 
       <li id="li_64A6A06F9265410ABB425DA4AF50C440">Alle Konversionsvariablen mit voller Subrelation </li> 
       <li id="li_907DDFCC35AB48EEA5B169B4A2598FB1"> <span class="wintitle"> Erst- und Letztkontakt von Marketingkanälen</span> </li> 
       <li id="li_B08A0DCB40154152AF1033B7629A5B5A">  Bericht <span class="uicontrol">Target</span> &gt; <span class="uicontrol">Kampagnen</span> (wenn aktiviert) </li> 
       <li id="li_6D4E65DD6E2B49C9A8C12181D23F185A">Zeit pro Besuch </li> 
       <li id="li_C6D3AD5A534243A8A6E17C663FEBA6BA">Sitebereiche </li> 
       <li id="li_E1F46EED5CE2425D83200A2FCB686EE5">Entrypages </li> 
       <li id="li_1201EE0EBF13476C9A9525E0700F30F3">Die meisten Berichte zu Traffic-Quellen </li> 
       <li id="li_563E07858FB1473BB22C2B191E8BE620">Besuchnummer </li> 
       <li id="li_1CAD77ABA6A2454282A4DA7E88C047E8">Viele Besucherprofilberichte </li> 
       <li id="li_D3A04E4CD8EC4646AAB90BF19F0AFA8A">Alle Konversionsvariablen und Listenvariablen </li> 
       <li id="li_01C194CE0F3E4C0694A34B4C6697F385">Die Erfassung von Besuchen und Unique Visitors pro Tag, Woche, Monat oder Quartal ist verfügbar. </li> 
      </ul> </li> 
    </ul> <p>Dieser Bericht kann Segmente verwenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ad Hoc Analysis  </td> 
   <td colname="col2"> 
    <ul id="ul_DFF9BFC01FC1424B8905C2D2C0EFD156"> 
     <li id="li_65FDF1C165C84F729E0EE84FF671B5E4">Ad Hoc Analysis können den Bericht „Site-Abschnitte“ nach fast allen anderen Berichten der Marketing-Bericht-Oberfläche aufschlüsseln. </li> 
     <li id="li_2159DE10C52D40AA89E4C934FC184641">Zusätzlich zu allen bereits erwähnten Ereignissen können alle Konversionen und Traffic-Metriken genutzt und für alle Konversionsmetriken können unterschiedliche Zuordnungen verwendet werden. </li> 
     <li id="li_3A23C6286D314B5D814612469F4F77C5">Dieser Bericht kann mehrere hochgradig erweiterte Segmente nutzen. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

