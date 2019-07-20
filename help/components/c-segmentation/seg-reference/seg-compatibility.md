---
description: Nicht alle im Segmentaufbau erstellten Segmente sind mit Data Warehouse kompatibel. Diese Tabelle listet die unterstützten Funktionen auf.
seo-description: Nicht alle im Segmentaufbau erstellten Segmente sind mit Data Warehouse kompatibel. Diese Tabelle listet die unterstützten Funktionen auf.
seo-title: Data Warehouse-Segmentkompatibilität
solution: Analytics
title: Data Warehouse-Segmentkompatibilität
topic: Segmente
uuid: 370258 c 5-8614-4434-871 c -41753 ed 77 f 5 c
translation-type: tm+mt
source-git-commit: 26bba9528873c983852754056a5495c4004d25e6

---


# Data Warehouse-Segmentkompatibilität

Not all segments created in the Segment Builder are compatible with [!DNL Data Warehouse]. Diese Tabelle listet die unterstützten Funktionen auf.

<table id="table_BBB1DAFDF85041598FA4AF869172CF7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Analysis Workspace, Reports &amp; Analysen, Ad-hoc-Analysen </th> 
   <th colname="col3" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Ausgeschlossen</b> </td> 
   <td colname="col2"> Auf allen Ebenen unterstützt </td> 
   <td colname="col3"> Nur in speziellen Fällen auf der obersten Ebene unterstützt </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Sequenzielle Segmente</b> </td> 
   <td colname="col2"> Unterstützt </td> 
   <td colname="col3"> Nicht unterstützt </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>UND und ODER können uneingeschränkt kombiniert werden</b> </td> 
   <td colname="col2"> Unterstützt </td> 
   <td colname="col3"> Einige Einschränkungen </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verschachtelte Behälter</b> </td> 
   <td colname="col2"> Unterstützt </td> 
   <td colname="col3"> Einige Einschränkungen (der Umfang muss verringert werden, d. h., dass Besucher z. B. Treffer enthalten können, aber nicht umgekehrt) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Dimensionen</b> </td> 
   <td colname="col2">Ziehen Sie eine Dimension in das Feld <span class="uicontrol">Definitionen</span> des Segmentaufbaus, um die Produktkompatibilität zu ermitteln. Diese Dimensionen werden beispielsweise nur in Analysis Workspace, Reports &amp; Analysen und Ad-hoc-Analysen unterstützt: 
    <ul id="ul_BD708CC3A16743F49F998D1046EC70A3"> 
     <li id="li_240DA619D50B4336ACD9117BF59AF10A">Entryserver </li> 
     <li id="li_222D4D4116674EF8A52945CCB9C78719">Entrykategorie </li> 
     <li id="li_5A43C846E2EA4EFCB892DE9E0607C68C">Entrydatum </li> 
     <li id="li_8E9CABBE04FC4A7A9A5D2BDD34AD3C87">Rangansicht aller Suchseiten </li> 
    </ul> </td> 
   <td colname="col3"> Ziehen Sie eine Dimension in das Feld <span class="uicontrol">Definitionen</span> des Segmentaufbaus, um die Produktkompatibilität zu ermitteln. Folgende Dimensionen werden beispielsweise nur in Data Warehouse unterstützt: 
    <ul id="ul_61A5B314CCCF497DB0385324E3309E22"> 
     <li id="li_1254089BDFAE4E0F8E51CB1511BBBF53">IP-Adresse </li> 
     <li id="li_D8E040F77A8C46A084547F4FE685CB10">Seiten-URL </li> 
     <li id="li_4C79AE900CF6458780C124143DC6FA5B">Besucher-ID </li> 
     <li id="li_4EC10645DE9740609D8DDFD4F668FE67">Experience Cloud-Besucher-ID </li> 
    </ul> <p>The following dimensions <b>cannot </b>be used in Data Warehouse segments: </p> 
    <ul id="ul_FE143F6D1ABF45DAA444E1B5691C7D4F"> 
     <li id="li_E77F3CC45BA04674B857FE5AB19D56F1">Rangansicht aller Suchseiten </li> 
     <li id="li_95E1549C13F14BA0B32686401EE78E31">Vormittag/Nachmittag </li> 
     <li id="li_6F1C8FC2E7674A0CA14B70B65784D896">Tag des Monats </li> 
     <li id="li_79D1A91D741D4CCC937D07906D71F964">Wochentag </li> 
     <li id="li_4008565353084611BD782B98D50C0611">Tag des Jahres </li> 
     <li id="li_F87D78F125874087BFF74FAAE2BA46F5">Ursprünglicher Geschäftsbereich </li> 
     <li id="li_53DA4E64C6714CFF90D164245D01C16A">Entry (Alle Dimensionen, die mit „Entry“ beginnen, abgesehen von Entrypage) </li> 
     <li id="li_7F26B0E54A4A48319F31D8FC499D1CF2">Exit (Alle Dimensionen, die mit „Exit“ beginnen, abgesehen von Exitlink und Exitpage) </li> 
     <li id="li_1877D2D8A95B43F29CAA426BF2FE4996">Hierarchie (Alle Dimensionen, die mit „Hierarchie“ beginnen) </li> 
     <li id="li_DF0BCC63ED274ABEA1C5A28274936310">Treffertiefe </li> 
     <li id="li_98BE56213E1A4FD28D4858D53C46D23E">Treffertyp </li> 
     <li id="li_52ECB31657DF4180BDB9C8D21CC74313">Stunde des Tages </li> 
     <li id="li_93716207F2614822ACB84100B35D27BC">Monat des Jahres </li> 
     <li id="li_FFC8E1F7092C4876A7E9F2365CC234B9">Seiten nicht gefunden </li> 
     <li id="li_7A070C8E0F664F5AB554555B17D0E4E6">Gebührenpflichtige Suche </li> 
     <li id="li_12228C18BF90463C8D8394FB810843D3">Viertel des Jahres </li> 
     <li id="li_1833B6E2011C4757A60CAA2C98B35AFA">Rückkehrhäufigkeit </li> 
     <li id="li_39154CD74A534D9AA09C701FE1E2C521">Einzelseitenbesuche </li> 
     <li id="li_84BDE34DD577488881E8842D2DE72D3C">Zeit vor Ereignis </li> 
     <li id="li_552BE3414CC949B3B24BE99298945874">Besuchszeit pro Seite – Zusammengefasst </li> 
     <li id="li_33D815E04CB3493C82BE33E958C2D7B9">Zeit pro Besuch – Zusammengefasst </li> 
     <li id="li_76F2BB88B8CD456DB50D04F36BB7854B">Nachverfolgung der Gründe für den Ausstieg </li> 
     <li id="li_07345E08D0584CEC99128A0542587019">US-Staaten </li> 
     <li id="li_3D6BD9E927334B9BBC29E602D1103F7A">Wochentag/Wochenende </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Segmentstapelung</b> </td> 
   <td colname="col2"> Unterstützt </td> 
   <td colname="col3"> Nicht unterstützt </td> 
  </tr> 
 </tbody> 
</table>

