---
description: Es gibt Besuchermetriken in Adobe Analytics und Adobe Audience Manager, die ähnliche Definitionen haben, die sich aber aus verschiedenen Gründen nicht zu 100 % entsprechen.
title: Unterschiede in der Besucherzahl
uuid: c3bbb887-bd02-4c1c-9a2b-64811c0ef56a
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 100%

---


# Unterschiede in der Besucherzahl

Es gibt Besuchermetriken in Adobe Analytics und Adobe Audience Manager, die ähnliche Definitionen haben, die sich aber aus verschiedenen Gründen nicht zu 100 % entsprechen.

Die Besuchermetriken sind:

<table id="table_F9FE107A89934C3B854C55D7D76AC6E8"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> Metrik </th> 
   <th colname="col3" class="entry"> Definition </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p><a href="https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/features/segments/segment-builder-data.html"  > AAM: Segmentpopulation insgesamt</a> </p> </td> 
   <td colname="col3"> <p>Anzahl der Geräte (Experience Cloud IDs), die während des Lookback-Zeitraums Teil Ihres Segments waren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><a href="https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/segments/segment-builder-data.html"  > AAM: Segmentpopulation in Echtzeit</a> </p> </td> 
   <td colname="col3"> <p>Anzahl der Geräte (Experience Cloud IDs), die während des Lookback-Zeitraums Teil Ihres Segments waren und Ihre Eigenschaften erreicht haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics: Unique Visitors </p> </td> 
   <td colname="col3"> <p>Zeigt die Anzahl der Unique Visitors an, die Ihre Eigenschaften während des Berichtfensters erreicht haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics: Besucher mit Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>Zeigt die Anzahl der Unique Visitors mit Experience Cloud ID an, die Ihre Eigenschaften während des Berichtfensters erreicht haben. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die AAM-Segmentpopulation in Echtzeit und die in der Audience Analytics-Berichterstellung verwendeten Analytics-Besucher mit Experience Cloud ID entsprechen sich am ehesten. In der nächsten Zeit gibt es dabei jedoch aufgrund verschiedener Faktoren leichte Diskrepanzen. Die Faktoren, die dazu beitragen, sind:

<table id="table_A391B37CC077456F8BB83BAA3C640EF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Faktor </th> 
   <th colname="col2" class="entry"> AAM: Segmentpopulation in Echtzeit </th> 
   <th colname="col3" class="entry"> Analytics: Besucher mit Experience Cloud ID </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Zeitzone </p> </td> 
   <td colname="col2"> <p>UTC (koordinierte Weltzeit) </p> </td> 
   <td colname="col3"> <p>Für jede Report Suite einzeln festgelegt </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerdefinierte Filter </p> </td> 
   <td colname="col2"> <p>Nein </p> </td> 
   <td colname="col3"> <p>Ja, z. B. IP-Filter, Bot-Filter </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Begrenzung von 150 Segmenten </p> </td> 
   <td colname="col2"> <p>Nein </p> </td> 
   <td colname="col3"> <p>Ja – Zählungen in Analytics können von der Integrationsbegrenzung von 150 Segmenten zu bis zu 5 % betroffen sein. „Zielgruppenlimit erreicht“ wird in der Dimension „Zielgruppenname“ angezeigt, wenn es zu einer Kürzung kam. </p> </td> 
  </tr> 
 </tbody> 
</table>

Siehe [Segmente in Analytics und Audience Manager – Grundlagen](/help/integrate/c-audience-analytics/aam-analytics-segments.md) für zusätzliche Erklärungen zu den Nuancen zwischen Daten und der Segmentierung zwischen Analytics und Audience Manager.
