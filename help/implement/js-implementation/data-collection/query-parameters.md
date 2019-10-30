---
description: In den folgenden Tabellen werden die Abfrageparameter aufgeführt, die den Wert für jede Analytics-Variable enthalten, die zur Datenerfassung gesendet werden.
keywords: Analytics-Implementierung
seo-description: In den folgenden Tabellen werden die Abfrageparameter aufgeführt, die den Wert für jede Analytics-Variable enthalten, die zur Datenerfassung gesendet werden.
seo-title: Datenerfassungs-Abfrageparameter
solution: Analytics
title: Datenerfassungs-Abfrageparameter
topic: Entwickler und Implementierung
uuid: 4d5af486-df27-42fe-bb9c-28938dddf2b2
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Datenerfassungs-Abfrageparameter

In den folgenden Tabellen werden die Abfrageparameter aufgeführt, die den Wert für jede Analytics-Variable enthalten, die zur Datenerfassung gesendet werden.

Diese Informationen können für das Debugging mit [Packet-Analyzern](../../../implement/impl-testing/packet-monitor.md#concept_490DF35E06D44234A91B5FC57C0BF258), beim manuellen Erstellen von Bildanforderungen oder bei der Verwendung von [dynamischen Variablen](../../../implement/js-implementation/c-variables/dynvars-overview.md#concept_B016789733A94070A9EAB209EEC05262) genutzt werden.

<table id="table_5442E15BF0AE4BDA92DDADD1C08F7C13"> 
 <thead> 
  <tr> 
   <th class="entry"> Parameter </th> 
   <th class="entry"> Analytics-Variable </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> aamlh </td> 
   <td colname="col2"> Keine </td> 
   <td colname="col3"> Keine </td> 
   <td colname="col4"> Audience Manager-Standorthinweis (in Experience Cloud Shared Profile-Integration verwendet) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> aamb </td> 
   <td colname="col2"> Keine </td> 
   <td colname="col3"> Keine </td> 
   <td colname="col4"> Audience Manager-Blob (in Experience Cloud Shared Profile-Integration verwendet) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> aid </td> 
   <td colname="col2"> Keine </td> 
   <td colname="col3"> Keine </td> 
   <td colname="col4"> Analytics-Besucher-ID </td> 
  </tr> 
  <tr> 
   <td> AQB </td> 
   <td> Keine </td> 
   <td> Keine </td> 
   <td> Zeigt den Anfang einer Bildanforderung an. </td> 
  </tr> 
  <tr> 
   <td> AQE </td> 
   <td> Keine </td> 
   <td> Keine </td> 
   <td> Zeigt das Ende einer Bildanforderung an (was beutet, dass die Anforderung nicht abgeschnitten wurde) </td> 
  </tr> 
  <tr> 
   <td> bh </td> 
   <td> Keine </td> 
   <td> Besucherprofil | Technologie | Browser-Fensterhöhe </td> 
   <td> Browser-Fensterhöhe (in Pixel) </td> 
  </tr> 
  <tr> 
   <td> bw </td> 
   <td> Keine </td> 
   <td> Besucherprofil | Technologie | Browser-Fensterbreite </td> 
   <td> Browser-Fensterbreite (in Pixel) </td> 
  </tr> 
  <tr> 
   <td> c </td> 
   <td> Keine </td> 
   <td> Besucherprofil | Technologie | Bildschirmfarbtiefen </td> 
   <td> Farbqualität (in Bit) </td> 
  </tr> 
  <tr> 
   <td> </td><td><p></p></td><td><p></p></td><td><p></p><p><code> &lt;my.a&gt;red&lt;/my.a&gt; </code></p><p></p><p><code> &lt;my&gt;&lt;a&gt;red&lt;/a&gt;&lt;/my&gt; </code></p><p><code> my.a = red </code></p><p><code> c.&my.a=red </code></p></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td><code> D </code></td><td></td><td></td><td><p></p></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td><p><code> t </code></p><code>
      dd/mm/yyyy&amp;nbsp;hh:mm:ss&amp;nbsp;D&amp;nbsp;OFFSET 
    </code><p><code> 0-6 </code><code> OFFSET </code></p><code>
      offset&amp;nbsp;from&amp;nbsp;GMT&amp;nbsp;in&amp;nbsp;hours&amp;nbsp;*&amp;nbsp;60&amp;nbsp;*&amp;nbsp;-&amp;nbsp;1 
    </code><p></p><code>
      23/09/2016&amp;nbsp;14:00:00&amp;nbsp;1&amp;nbsp;420 
    </code></td></tr><tr><td><code> ts </code></td><td><p></p></td><td></td><td><p></p></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td><p></p></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td><p></p></td></tr></tbody></table>

