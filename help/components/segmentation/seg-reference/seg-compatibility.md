---
description: Nicht alle im Segmentaufbau erstellten Segmente sind mit Data Warehouse kompatibel. Diese Tabelle listet die unterstützten Funktionen auf.
title: Data Warehouse-Segmentkompatibilität
topic: Segments
uuid: 370258c5-8614-4434-871c-41753ed77f5c
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 100%

---


# Data Warehouse-Segmentkompatibilität

Nicht alle im Segment Builder erstellten Segmente sind mit [!DNL Data Warehouse] kompatibel. Diese Tabelle listet die unterstützten Funktionen auf.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis </th> 
   <th> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td > <b>Container ausschließen</b> </td> 
   <td> Auf allen Ebenen unterstützt </td> 
   <td> Nur in speziellen Fällen auf der obersten Ebene unterstützt </td> 
  </tr> 
  <tr> 
   <td> <b>Sequenzielle Segmente</b> </td> 
   <td> Unterstützt </td> 
   <td> Nicht unterstützt </td> 
  </tr> 
  <tr> 
   <td> <b>UND und ODER können uneingeschränkt kombiniert werden</b> </td> 
   <td> Unterstützt </td> 
   <td> Einige Einschränkungen. Siehe *Hinweis* unter der Tabelle. </td> 
  </tr> 
  <tr> 
   <td> <b>Verschachtelte Behälter</b> </td> 
   <td> Unterstützt </td> 
   <td> Einige Einschränkungen (der Umfang muss verringert werden, d. h., dass Besucher z. B. Treffer enthalten können, aber nicht umgekehrt) </td> 
  </tr> 
  <tr> 
   <td> <b>Dimensionen</b> </td> 
   <td>Ziehen Sie eine Dimension in das Feld <span class="uicontrol">Definitionen</span> des Segmentaufbaus, um die Produktkompatibilität zu ermitteln. Folgende Dimensionen werden beispielsweise nur in Analysis Workspace, Reports &amp; Analytics und Ad Hoc Analysis unterstützt: 
    <ul> 
     <li>Entryserver </li> 
     <li>Entrykategorie </li> 
     <li>Entrydatum </li> 
     <li>Rangansicht aller Suchseiten </li> 
    </ul> </td> 
   <td> Ziehen Sie eine Dimension in das Feld <span class="uicontrol">Definitionen</span> des Segmentaufbaus, um die Produktkompatibilität zu ermitteln. Folgende Dimensionen werden beispielsweise nur in Data Warehouse unterstützt: 
    <ul> 
     <li>IP-Adresse </li> 
     <li>Seiten-URL </li> 
     <li>Visitor ID </li> 
     <li>Experience Cloud-Besucher-ID </li> 
    </ul> <p>Die folgenden Dimensionen <b>können nicht </b>in Data Warehouse-Segmenten verwendet werden: </p> 
    <ul> 
     <li>Rangansicht aller Suchseiten </li> 
     <li>Vormittag/Nachmittag </li> 
     <li>Tag des Monats </li> 
     <li>Wochentag </li> 
     <li>Tag des Jahres </li> 
     <li>Ursprünglicher Geschäftsbereich </li> 
     <li>Entry (Alle Dimensionen, die mit „Entry“ beginnen, abgesehen von Entrypage) </li> 
     <li>Exit (Alle Dimensionen, die mit „Exit“ beginnen, abgesehen von Exitlink und Exitpage) </li> 
     <li>Hierarchie (Alle Dimensionen, die mit „Hierarchie“ beginnen) </li> 
     <li>Treffertiefe </li> 
     <li>Treffertyp </li> 
     <li>Stunde Tag </li> 
     <li>Monat des Jahres </li> 
     <li>Seiten nicht gefunden </li> 
     <li>Paid Search </li> 
     <li>Quartal des Jahres </li> 
     <li>Rückkehrhäufigkeit </li> 
     <li>Einzelseitenbesuche </li> 
     <li>Zeit vor Ereignis </li> 
     <li>Besuchszeit pro Seite – zusammengefasst </li> 
     <li>Zeit pro Besuch – zusammengefasst </li> 
     <li>Nachverfolgen des Abmeldegrunds </li> 
     <li>US-Staaten </li> 
     <li>Wochentag/Wochenende </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <b>Segmentstapelung</b> </td> 
   <td> Unterstützt </td> 
   <td> Unterstützt </td> 
  </tr>
  <tr>
    <td><b>Operatoren „entspricht beliebigen von“ und „entspricht keinem von“</b></td>
    <td>Unterstützt</td>
    <td>Nicht unterstützt</td>
  </tr>
 </tbody> 
</table>

*Hinweis: Data Warehouse unterstützt nicht alle Fälle der Verwendung eines`exclusion`- oder eines`without`-Containers bei der Verwendung von`AND/OR`. Bei Verwendung einer solchen Kombination werden in Data Warehouse nur Segmente unterstützt, die als `A AND NOT B` neu geschrieben werden können (oder **dieses Merkmal einbeziehen** und **dieses Merkmal ausschließen**).*
