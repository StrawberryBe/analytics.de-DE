---
description: In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Datenfeeds berechnet werden.
keywords: Datenfeed;Auftrag;Metriken;Pre-Spalte;Post-Spalte;Bots;Datumsfilterung;Ereigniszeichenfolge;häufig;Formeln
seo-description: In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Datenfeeds berechnet werden.
seo-title: Berechnete Metriken
solution: Analytics
title: Berechnete Metriken
topic: Reports and Analytics
uuid: a45ea5bb-7c83-468f-b94a-63add78931d7
translation-type: tm+mt
source-git-commit: 2fc1a01aced4cf2b165b46353418fbee9b83bee5

---


# Berechnete Metriken

In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Datenfeeds berechnet werden.

<!--Meike, I commented out this heading because it contains no content, and I'm troubleshooting a dita error-Bob
## Pre vs. Post column {#section_19967AF2FD9D44D6A8EC30F77E71F2ED}
-->

## Bots {#section_06753B95800F47668AAF52E7227F27C8}

Bots werden aufgrund der für Ihre Report Suite definierten [Botregeln](https://marketing.adobe.com/resources/help/en_US/reference/bot_rules.html) aus den Datenfeeds ausgeschlossen.

## Datumsfilterung {#section_3BFF4F7EED1F4FA69EBF12BF98B347E8}

Schließen Sie Zeilen aus dem gewünschten Datumsbereich ein, indem Sie nach dem Feld `date_time` filtern. The `date_time` field is human readable (for example, `YYYY-MM-DD HH:MM:SS`) and is adjusted to the time zone of the report suite. For example, `date_time starts with "2013-12"` includes hits from December 2013.

## Ereigniszeichenfolge {#section_87B686512EFD4A6CA072165CB28A130A}

The event string in `event_list` and `post_event_list` contains a comma-delimited list of events, which may have a value and/or a unique ID. Es wird empfohlen, die gesamte Verarbeitung für `post_event_list` vorzunehmen, da diese bereits dedupliziert ist und Logik zur Entfernung doppelter Ereignisse mit derselben ID angewendet wird (siehe [Ereignis-Serialisierung](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_event_serialization.html)).

Weitere Informationen zur Ereignis-ID mithilfe der Namenszuordnung finden Sie in der Ereignisabfrage, die mit dem Datenfeed geliefert wird.

Weitere Informationen zu Ereignissen finden Sie unter [Ereignisse](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_events.html).

## Formeln für häufig verwendete Metriken {#section_E26A01C234484857BF8C74443222AE41}

In der folgenden Tabelle finden Sie Anweisungen zur Berechnung verschiedener häufig verwendeter Metriken.

<table id="table_814EA73C01EE4B2CA3CEB2839E19ADF9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Metrik </th> 
   <th colname="col2" class="entry"> Berechnung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Seitenansichten </td> 
   <td colname="col2"> <p> Page views can be calculated by counting when there is either a value in <code> post_pagename </code> or <code> post_page_url </code>. </p> 
    <p>Sie können ähnliche Logik nutzen, um die benutzerdefinierten Links zu zählen: </p> 
    <ul id="ul_8DFBEE3ED30C465D8E55B1F3880D5263"> 
     <li id="li_009F2B7E3F9443889AE95B3358169444"> <code> post_page_event = 100 </code> , um benutzerspezifische Links zu zählen. </li> 
     <li id="li_866DA2F5C2404347863CD1417F822FE8"> <code> post_page_event = 101 </code> , um Downloadlinks zu zählen. </li> 
     <li id="li_4BC6E62CE8B1474DB22448FA32C9EE01"> <code> post_page_event = 102 </code> , um Ausstiegslinks zu zählen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche </td> 
   <td colname="col2"> 
    <ol id="ol_FE1831195A474650B07D7820DCD38728"> 
     <li id="li_274590E937A142D19B204768B1F10325">Exclude all rows where <code> exclude_hit &gt; 0 </code>. </li> 
     <li id="li_038B8FF66EA44E138C8A8932DA7B39E5">Exclude all rows with <code> hit_source = 5,7,8,9 </code>. Bei 5, 8, und 9 handelt es sich um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. 7 steht für Transaktions-ID-Datenquellen-Uploads, die nicht beim Zählen der Besuche und Besucher enthalten sein sollten. Siehe <a href="/help/export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md"  > Trefferquellensuche </a>. </li> 
     <li id="li_7FCD9BDF4D8547719420B34BA48BFA2D">Kombinieren Sie <code> post_visid_high </code>, <code> post_visid_low </code>, <code> visit_num </code>und <code> visit_start_time_gmt </code>*. Erfassen Sie die Anzahl der eindeutigen Kombinationen. </li> 
    </ol> <p>* In seltenen Fällen können Internetstörungen, Systemstörungen oder die Verwendung benutzerdefinierter Besucher-IDs zu doppelten <code> visit_num </code>-Werten für dieselbe Besucher-ID bei unterschiedlichen <a href="https://marketing.adobe.com/resources/help/en_US/reference/metrics_visit.html"  >Besuchen</a> führen. To avoid resulting issues, also include <code> visit_start_time_gmt </code> when counting visits. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besucher </td> 
   <td colname="col2"> 
    <ol id="ol_E2BC9235A3164EF5936EFC5D9E9327D0"> 
     <li id="li_2C145CA54EBF4B358FC7DC78D8DA577D">Exclude all rows where <code> exclude_hit &gt; 0 </code>. </li> 
     <li id="li_9EF364652A214A4D9B66552BC6BBE527">Exclude all rows with <code> hit_source = 5,7,8,9 </code>. Bei 5, 8, und 9 handelt es sich um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. 7 steht für Transaktions-ID-Datenquellen-Uploads, die nicht beim Zählen der Besuche und Besucher enthalten sein sollten. Siehe <a href="/help/export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md"  > Trefferquellensuche </a> </li> 
     <li id="li_4AB5129315644A29987E8FCB9C9F9C39">Kombinieren Sie <code> post_visid_high </code> mit <code> post_visid_low </code>. Erfassen Sie die Anzahl der eindeutigen Kombinationen. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignisinstanzen </td> 
   <td colname="col2"> <p>When an event is set on a hit, <code> post_event_list </code> contains the event. The <code> post_event_list </code> is de-duplicated and is recommended to determine event instances. </p> <p>Beispiel: </p> 
    <code>
      post_event_list = 1,200 
    </code> <p>Indicates an instance of <code> purchase </code> and <code> event1 </code>. </p> 
    <ol id="ol_84B529A668A54686957D1EB36D944467"> 
     <li id="li_F953D7668C704C1AB7970123E369472A">Exclude all rows where <code> exclude_hit &gt; 0 </code>. </li> 
     <li id="li_65B0B504DB654479844EAE490D9283EB">Exclude all rows with <code> hit_source = 5,8,9 </code>. Es handelt sich dabei um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. Siehe <a href="/help/export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md"  > Trefferquellensuche </a>. </li> 
     <li id="li_FB1C31048EC7415088F41E8CDC01AEBD">Count the number of times the event lookup value appears in <code> post_event_list </code>. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar-Instanzen </td> 
   <td colname="col2"> <p>Wenn für einen Treffer eine eVar festgelegt ist, enthält <code> event_list </code> eine Instanz dieser eVar. </p> <p>Beispiel: </p> 
    <code>
      post_event_list&amp;nbsp;=&amp;nbsp;100,101,106 
    </code> <p>Indicates an instance of <code> eVar1 </code>, <code> eVar2 </code>, and <code> eVar7 </code>. Das bedeutet, dass der Wert für diese drei eVars im Treffer festgelegt war. </p> <p>Um Instanzen für eVars zu berechnen, verwenden Sie dieselbe Logik, die oben im Abschnitt <i>Ereignisinstanzen</i> erläutert ist. Allerdings müssen Sie die Häufigkeit für die eVar-Suche in <code> post_event_list </code> erfassen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchszeit </td> 
   <td colname="col2"> <p>Um die Besuchszeit zu berechnen, müssen Sie Treffer nach Besuchen gruppieren und sie dann entsprechend der Trefferzahl innerhalb des Besuchs ordnen. </p> 
    <ol id="ol_946E7CD6005A42EB9A4B79268BF84066"> 
     <li id="li_D109FAF4686D4935B7A6DCA5D383612F">Exclude all rows where <code> exclude_hit &gt; 0 </code>. </li> 
     <li id="li_D88F3691DB6746EBA84AA52841E56803">Group hits for a visit by concatenating <code> visid_high </code>, <code> visid_low </code>, and <code> visit_num </code>. </li> 
     <li id="li_08792F3BDFEA4DA29E0983C4BE65D73B">Order hits for each visit by <code> visit_page_num </code>. </li> 
     <li id="li_4B956734DBB84603B86DDA6A2B0B41A0">Using <a href="/help/export/analytics-data-feed/c-df-contents/datafeeds-page-event.md"  > page_event </a>, filter the types of hits you want. </li> 
     <li id="li_2C5AC0477CFC409B8F169079354C8226">Suchen Sie nach Treffern, bei denen der Wert festgelegt ist, für den Sie die Besuchsdauer verfolgen möchten. Beispiel: 
      <code>
        hit&nbsp;1:&nbsp;post_prop1=red hit&nbsp;2:&nbsp;post_prop1=blue 
      </code> </li> 
     <li id="li_20106B322F7B45CE8D2FBD9B0CB3D60D">Subtract the <code> post_cust_hit_time </code> for hit 1 from the <code> post_cust_hit_time </code> for hit 2 to determine the seconds between these two hits. The result is the time spent for <code> post_prop1=red </code>. Falls das Ergebnis eine negative Zahl ist, deutet dies darauf hin, dass der Treffer unzulässig ist und die Berechnung verworfen werden sollte. </li> 
    </ol> <p>Diese Logik kann ausgeweitet werden, um die Besuchsdauer für andere Werte zu berechnen. When calculating time spent, Analytics calculates time spent based on the time the value was set in a <code> track </code> ( <code> page_event=0 </code>) or <code> trackLink </code> ( <code> page_event=10|11|12 </code>) call, to the time of the next page view ( <code> track </code> call). </p> <p>Bei der Berichterstellung zur Besuchsdauer für einen spezifischen Zeitraum werden durch Marketing Reports &amp; Analytics sowie Ad Hoc Analysis Treffer nach Ende des Berichtszeitraums ausgewertet, um die Besuchsdauer für Werte innerhalb des Berichtszeitraums zu ermitteln, es sei denn, Beginn- und Enddatum des Zeitraums liegen auf einer Monatsgrenze. Aufgrund der Komplexität dieser Berechnungen kann es sich als schwierig erweisen, der Besuchsdauer exakt zu entsprechen. Data Warehouse wertet keine Treffer nach Ende des Berichtszeitraums aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Umsatz, Aufträge, Einheiten </td> 
   <td colname="col2"> <p>Es wird entsprechend der Einstellungen für die Report Suite eine Währungskonversion auf <code> post_product_list </code> angewendet, daher wird die Verwendung dieser Spalte empfohlen. </p> 
    <ol id="ol_03D62086EDDE42AD82049830D85FDC69"> 
     <li id="li_2A5B8205EA30492986C35DC382B91F16">Exclude all rows where <code> exclude_hit &gt; 0 </code>. </li> 
     <li id="li_6417C228AC414B01A30F85BE4842ED3C">Exclude all rows with <code> hit_source = 5,8,9 </code>. Bei 5 bis 9 handelt es sich um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. Siehe <a href="/help/export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md"  > Trefferquellensuche </a>. </li> 
     <li id="li_C48F91C74F5E4286B5F0B285E33AF733">Ignore purchase data for rows where <code> duplicate_purchase = 1 </code>. Diese Kennzeichnung weist darauf hin, dass der Kauf doppelt erfasst wurde (das bedeutet, dass bereits ein Treffer mit derselben <code> purchaseID </code> erfasst wurde). </li> 
     <li id="li_FA1639FEF516419BA1BFDC37B063B346"> <p><code> post_product_list </code> verwendet dieselbe Syntax wie <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/c_products.html"  >s.products</a>, Sie können diese Zeichenfolge daher zur Berechnung der Metriken analysieren. Beispiel: </p> 
      <code>
        ;Cross Trainers;1;69.95,;Athletic Socks;10;29.99 
      </code> <p>Durch die Analyse dieser Zeichenfolge können Sie ermitteln, dass 1 Paar Laufschuhe für 69,95 USD erworben wurde und dass der Gesamtumsatz in diesem Kauf 99,94 USD betrug. </p> </li> 
    </ol> <p>Hinweis: In Analytics können Währungsereignisse, die Produktumsätze enthalten, durch die Ereigniszeichenfolge weitergegeben werden, d. h., sie müssen möglicherweise Umsätze berücksichtigen, die nicht in der Produktzeichenfolge enthalten sind. Siehe <i>Numerische/Währungsereignisse</i> in <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/c_events.html"  >s.events </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
