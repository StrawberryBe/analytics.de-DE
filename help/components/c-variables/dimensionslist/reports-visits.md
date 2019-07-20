---
description: Zeigt die Anzahl der Besuche auf Ihrer gesamten Website während eines angegebenen Zeitraums an.
seo-description: Zeigt die Anzahl der Besuche auf Ihrer gesamten Website während eines angegebenen Zeitraums an.
seo-title: Besuchen
solution: Analytics
title: Besuchen
topic: 'Berichte    '
uuid: ff 65 bddf-fb 65-4 cf 0-8 aae -4 ab 59 c 2 bb 0 a 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Besuche

Zeigt die Anzahl der Besuche auf Ihrer gesamten Website während eines angegebenen Zeitraums an.

**Berichteigenschaften**

* Ein Besuch ist als Sequenz zusammenhängender Seitenansichten ohne 30-minütige Unterbrechung oder als bis zu 12 Stunden andauernde Aktivität definiert.
* Nach Ablauf eines Besuchs wird für eine anschließende Bildanforderung ein neuer Besuch gestartet.
* Für einen Besucher wird in der Regel mindestens ein Besuch (wahrscheinlich eher mehrere) verzeichnet.
* Ein Besuch wird mit der ersten Bildanforderung eingeleitet, die von einem neuen Besucher oder von einem vorhandenen Benutzer stammt, dessen Besuch abgelaufen war. Damit wird die Entrypage bezeichnet.
* Die letzte Bildanforderung vor Ablauf eines Besuchs gilt das Ende eines Besuchs. Damit wird die Exitpage bezeichnet.

   Siehe [Berichte zu Einstiegen und Ausstiegen](../../../components/c-variables/dimensionslist/reports-entries-exits.md#concept_C4AED2C1D62E43A48ACAA837327FCCF2).
* Stündliche Aufschlüsselungen basieren auf der Zeitzone der Report Suite.
* Der Bericht enthält keine Zeileneinträge. Sie können ihn nur in der Trendansicht anzeigen.
* Eine Granularität wie Stunde, Tag, Woche, Monat, Quartal und Jahr kann angewendet werden. Die Verfügbarkeit dieser Granularitätseinstellungen hängt vom Datumsbereich der Berichterstellung ab.

Siehe [Besuchsmetrik](../../../components/c-variables/c-metrics/metrics-visit.md#concept_9DA4D9EF8B964755BAC57378AD37911E), um weitere Informationen zur Verarbeitung dieser Metrik in Experience Cloud zu erhalten.

**Produktspezifische Berichtinformationen**

<table id="table_3138CA443CAC4F55838216E8B8786EE2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Produkt </th> 
   <th colname="col2" class="entry"> Navigation </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Reports &amp; Analytics </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol">„Sitemetriken“</span> &gt; <span class="uicontrol">„Besuche“</span> </p> <p>Sie können einen <span class="wintitle">„Besuche“-Bericht</span> auf einer ausgewählten Seite ausführen. Besuche, die über Mitternacht hinausgehen, werden sowohl für den Tag gezählt, an dem der Besuch begann, als auch für den Tag, an dem er endete. In der Gesamtsumme für den speziellen Datumsbereich werden Doppelzählungen jedoch dedupliziert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ad Hoc Analysis </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol">„Berichte“</span> &gt; <span class="uicontrol">„Sitemetriken“</span> &gt; <span class="uicontrol">„Besuche“</span> </p> 
    <ul id="ul_73FEE02C129041D6A63F2DB07676960F"> 
     <li id="li_CC3BB22DE97941EB8032BE4421FFC173"> Sie können jedes Element in diesem Bericht nach nahezu jedem anderen Bericht und beliebigen Variablen aufschlüsseln, sodass Sie Aufschlüsselungen jeder Granularität sehen können. </li> 
     <li id="li_D53D480D73264D47945C9E1202B7BD4F">Besuche, die über Mitternacht hinausgehen, werden sowohl für den Tag gezählt, an dem der Besuch begann, als auch für den Tag, an dem er endete. In der Gesamtsumme für den speziellen Datumsbereich werden Doppelzählungen jedoch abgezogen (dedupliziert). </li> 
     <li id="li_B8BCC584F95B407DB87F5EA57CC88F62">Sie können in diesem Bericht alle Konversions- und Traffic-Metriken sowie unterschiedliche Zuordnungen für alle Konversionsmetriken verwenden. </li> 
     <li id="li_0F342D3DCFF44ABAB79BD0F9E7F43E1E">Dieser Bericht kann mehrere hochgradig erweiterte Segmente nutzen. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

