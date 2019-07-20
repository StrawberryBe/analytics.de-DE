---
description: In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Datenfeeds berechnet werden.
keywords: Datenfeed; job; Metriken; pre column; Post-Spalte; Bots; Datumsfilterung; event string; common; Formeln
seo-description: In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Datenfeeds berechnet werden.
seo-title: Berechnete Metriken
solution: Analytics
title: Berechnete Metriken
topic: Reports and Analytics
uuid: a 45 ea 5 bb -7 c 83-468 f-b 94 a -63 add 78931 d 7
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Berechnete Metriken

In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Datenfeeds berechnet werden.

<!--Meike, I commented out this heading because it contains no content, and I'm troubleshooting a dita error-Bob
## Pre vs. Post column {#section_19967AF2FD9D44D6A8EC30F77E71F2ED}
-->

## Bots {#section_06753B95800F47668AAF52E7227F27C8}

Bots werden aufgrund der für Ihre Report Suite definierten [Botregeln](https://marketing.adobe.com/resources/help/en_US/reference/?f=bot_rules) aus den Datenfeeds ausgeschlossen.

## Datumsfilterung {#section_3BFF4F7EED1F4FA69EBF12BF98B347E8}

Schließen Sie Zeilen aus dem gewünschten Datumsbereich ein, indem Sie nach dem Feld `date_time` filtern. The `date_time` field is human readable (for example, `YYYY-MM-DD HH:MM:SS`) and is adjusted to the time zone of the report suite. For example, `date_time starts with "2013-12"` includes hits from December 2013.

## Ereigniszeichenfolge {#section_87B686512EFD4A6CA072165CB28A130A}

The event string in `event_list` and `post_event_list` contains a comma-delimited list of events, which may have a value and/or a unique ID. Es wird empfohlen, die gesamte Verarbeitung für `post_event_list` vorzunehmen, da diese bereits dedupliziert ist und Logik zur Entfernung doppelter Ereignisse mit derselben ID angewendet wird (siehe [Ereignis-Serialisierung](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=c_event_serialization)).

Weitere Informationen zur Ereignis-ID mithilfe der Namenszuordnung finden Sie in der Ereignisabfrage, die mit dem Datenfeed geliefert wird.

Weitere Informationen zu Ereignissen finden Sie unter [Ereignisse](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_events).

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
   <td colname="col2"> <p> Seitenansichten können durch Zählen vorhandener Werte für <code>post_pagename</code> oder <code>post_page_url</code> berechnet werden . </p> 
    <p>Sie können ähnliche Logik nutzen, um die benutzerdefinierten Links zu zählen: </p> 
    <ul id="ul_8DFBEE3ED30C465D8E55B1F3880D5263"> 
     <li id="li_009F2B7E3F9443889AE95B3358169444"> <code> post_page_event = 100</code> zum Zählen benutzerdefinierter Links. </li> 
     <li id="li_866DA2F5C2404347863CD1417F822FE8"> <code> post_page_event = 101</code> zum Zählen von Downloadlinks. </li> 
     <li id="li_4BC6E62CE8B1474DB22448FA32C9EE01"> <code> post_page_event = 102</code> zum Zählen von Exitlinks. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchen </td> 
   <td colname="col2"> 
    <ol id="ol_FE1831195A474650B07D7820DCD38728"> 
     <li id="li_274590E937A142D19B204768B1F10325">Schließen Sie alle Zeilen mit <code>exclude_hit &gt; 0</code> aus . </li> 
     <li id="li_038B8FF66EA44E138C8A8932DA7B39E5">Schließen Sie alle Zeilen mit <code>hit_source = 5,7,8,9</code> aus . Bei 5, 8, und 9 handelt es sich um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. 7 steht für Transaktions-ID-Datenquellen-Uploads, die nicht beim Zählen der Besuche und Besucher enthalten sein sollten. Siehe <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42" format="dita" scope="local"> Trefferquellensuche </a>. </li> 
     <li id="li_7FCD9BDF4D8547719420B34BA48BFA2D">Fassen Sie <code>post_visid_high</code>, <code>post_visid_low</code>, <code>visit_num</code> und <code>visit_start_time_gmt</code>* zusammen. Erfassen Sie die Anzahl der eindeutigen Kombinationen. </li> 
    </ol> <p>* In seltenen Fällen können Internetstörungen, Systemstörungen oder die Verwendung benutzerdefinierter Besucher-IDs zu doppelten <code>visit_num</code>-Werten für dieselbe Besucher-ID bei unterschiedlichen <a href="https://marketing.adobe.com/resources/help/en_US/reference/?f=metrics_visit" format="http" scope="external">Besuchen</a> führen. Um Folgeprobleme zu vermeiden, schließen Sie beim Zählen der Besuchszahlen auch <code>visit_start_time_gmt</code> ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchern </td> 
   <td colname="col2"> 
    <ol id="ol_E2BC9235A3164EF5936EFC5D9E9327D0"> 
     <li id="li_2C145CA54EBF4B358FC7DC78D8DA577D">Schließen Sie alle Zeilen mit <code>exclude_hit &gt; 0</code> aus . </li> 
     <li id="li_9EF364652A214A4D9B66552BC6BBE527">Schließen Sie alle Zeilen mit <code>hit_source = 5,7,8,9</code> aus . Bei 5, 8, und 9 handelt es sich um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. 7 steht für Transaktions-ID-Datenquellen-Uploads, die nicht beim Zählen der Besuche und Besucher enthalten sein sollten. Siehe <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42" format="dita" scope="local"> Trefferquellensuche </a> </li> 
     <li id="li_4AB5129315644A29987E8FCB9C9F9C39">Fassen Sie <code>post_visid_high</code> mit <code>post_visid_low</code> zusammen . Erfassen Sie die Anzahl der eindeutigen Kombinationen. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignisinstanzen </td> 
   <td colname="col2"> <p>Wenn für einen Treffer ein Ereignis festgelegt ist, enthält <code>post_event_list</code> das Ereignis. <code>post_event_list</code> wird dedupliziert und für die Ermittlung der Ereignisinstanzen empfohlen. </p> <p>Beispiel: </p> 
    <code>post_ event_ list = 1.200 </code>
  <p>Gibt eine Instanz von <code>purchase</code> und <code>event1</code> an . </p> 
    <ol id="ol_84B529A668A54686957D1EB36D944467"> 
     <li id="li_F953D7668C704C1AB7970123E369472A">Schließen Sie alle Zeilen mit <code>exclude_hit &gt; 0</code> aus . </li> 
     <li id="li_65B0B504DB654479844EAE490D9283EB">Schließen Sie alle Zeilen mit <code>hit_source = 5,8,9</code> aus . Es handelt sich dabei um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. Siehe <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42" format="dita" scope="local"> Trefferquellensuche </a>. </li> 
     <li id="li_FB1C31048EC7415088F41E8CDC01AEBD">Zählen Sie die Häufigkeit, mit der der Ereignissuchwert in <code>post_event_list</code> auftritt . </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar-Instanzen </td> 
   <td colname="col2"> <p>Wenn für einen Treffer eine eVar festgelegt ist, enthält <code>event_list</code> eine Instanz dieser eVar. </p> <p>Beispiel: </p> 
    <code>post_ event_ list &amp; amp; nbsp; = &amp; amp; nbsp; 100,101,106 </code>
  <p>Gibt eine Instanz von <code>eVar1</code>, <code>eVar2</code> und <code>eVar7</code> an . Das bedeutet, dass der Wert für diese drei eVars im Treffer festgelegt war. </p> <p>Um Instanzen für eVars zu berechnen, verwenden Sie dieselbe Logik, die oben im Abschnitt <i>Ereignisinstanzen</i> erläutert ist. Allerdings müssen Sie die Häufigkeit für die eVar-Suche in <code>post_event_list</code> erfassen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchszeit </td> 
   <td colname="col2"> <p>Um die Besuchszeit zu berechnen, müssen Sie Treffer nach Besuchen gruppieren und sie dann entsprechend der Trefferzahl innerhalb des Besuchs ordnen. </p> 
    <ol id="ol_946E7CD6005A42EB9A4B79268BF84066"> 
     <li id="li_D109FAF4686D4935B7A6DCA5D383612F">Schließen Sie alle Zeilen mit <code>exclude_hit &gt; 0</code> aus . </li> 
     <li id="li_D88F3691DB6746EBA84AA52841E56803">Gruppieren Sie die Treffer für einen Besuch durch Verknüpfen von <code>visid_high</code>, <code>visid_low</code> und <code>visit_num </code>. </li> 
     <li id="li_08792F3BDFEA4DA29E0983C4BE65D73B">Ordnen Sie die Treffer für jeden Besuch nach <code>visit_page_num </code>. </li> 
     <li id="li_4B956734DBB84603B86DDA6A2B0B41A0">Using <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-page-event.md#concept_A3AC076C3728445EB4CC572A6EDA5263" format="dita" scope="local"> page_event </a>, filter the types of hits you want. </li> 
     <li id="li_2C5AC0477CFC409B8F169079354C8226">Suchen Sie nach Treffern, bei denen der Wert festgelegt ist, für den Sie die Besuchsdauer verfolgen möchten. For example: 
      <code>
        hit 1: post_prop1=red hit 2: post_prop1=blue 
      </code> </li> 
     <li id="li_20106B322F7B45CE8D2FBD9B0CB3D60D">Ziehen Sie <code>post_cust_hit_time</code> für Treffer 1 von <code>post_cust_hit_time</code> für Treffer 2 ab, um die Sekundenzahl zwischen den beiden Treffern zu ermitteln. Das Ergebnis entspricht der Besuchsdauer für <code>post_prop1=red </code>. Falls das Ergebnis eine negative Zahl ist, deutet dies darauf hin, dass der Treffer unzulässig ist und die Berechnung verworfen werden sollte. </li> 
    </ol> <p>Diese Logik kann ausgeweitet werden, um die Besuchsdauer für andere Werte zu berechnen. Bei der Ermittlung der Besuchsdauer berechnet Analytics sie ausgehend von der Zeit, zu der der Wert in einer Anfrage vom Typ <code>track</code> (<code>page_event=0</code>) oder <code>trackLink</code> (<code>page_event=10|11|12</code>) eingestellt wurde, bis zum Zeitpunkt der nächsten Seitenansicht (<code>track</code>-Anfrage). </p> <p>Bei der Berichterstellung zur Besuchsdauer für einen spezifischen Zeitraum werden durch Marketing Reports &amp; Analytics sowie Ad Hoc Analysis Treffer nach Ende des Berichtszeitraums ausgewertet, um die Besuchsdauer für Werte innerhalb des Berichtszeitraums zu ermitteln, es sei denn, Beginn- und Enddatum des Zeitraums liegen auf einer Monatsgrenze. Aufgrund der Komplexität dieser Berechnungen kann es sich als schwierig erweisen, der Besuchsdauer exakt zu entsprechen. Data Warehouse wertet keine Treffer nach Ende des Berichtszeitraums aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Umsatz, Aufträge, Einheiten </td> 
   <td colname="col2"> <p>Es wird entsprechend der Einstellungen für die Report Suite eine Währungskonversion auf <code>post_product_list</code> angewendet, daher wird die Verwendung dieser Spalte empfohlen. </p> 
    <ol id="ol_03D62086EDDE42AD82049830D85FDC69"> 
     <li id="li_2A5B8205EA30492986C35DC382B91F16">Schließen Sie alle Zeilen mit <code>exclude_hit &gt; 0</code> aus . </li> 
     <li id="li_6417C228AC414B01A30F85BE4842ED3C">Schließen Sie alle Zeilen mit <code>hit_source = 5,8,9</code> aus . Bei 5 bis 9 handelt es sich um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. Siehe <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42" format="dita" scope="local"> Trefferquellensuche </a>. </li> 
     <li id="li_C48F91C74F5E4286B5F0B285E33AF733">Ignorieren Sie Kaufdaten bei Zeilen, für die <code>duplicate_purchase = 1</code> gilt . Diese Kennzeichnung weist darauf hin, dass der Kauf doppelt erfasst wurde (das bedeutet, dass bereits ein Treffer mit derselben <code>purchaseID</code> erfasst wurde). </li> 
     <li id="li_FA1639FEF516419BA1BFDC37B063B346"> <p><code>post_product_list</code> verwendet dieselbe Syntax wie <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=c_products" format="http" scope="external">s.products</a>, Sie können diese Zeichenfolge daher zur Berechnung der Metriken analysieren. Beispiel: </p> 
      <code>; Cross-Tracker; 1; 69.95; Sportsocken; 10; 29.99 </code>
  <p>Durch die Analyse dieser Zeichenfolge können Sie ermitteln, dass 1 Paar Laufschuhe für 69,95 USD erworben wurde und dass der Gesamtumsatz in diesem Kauf 99,94 USD betrug. </p> </li> 
    </ol> <p>Hinweis: In Analytics können Währungsereignisse, die Produktumsätze enthalten, durch die Ereigniszeichenfolge weitergegeben werden, d. h., sie müssen möglicherweise Umsätze berücksichtigen, die nicht in der Produktzeichenfolge enthalten sind. Siehe <i>Numerische/Währungsereignisse</i> in <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=c_events" format="http" scope="external">s.events </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
