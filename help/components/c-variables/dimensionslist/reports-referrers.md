---
description: Zeigt an, wo Ihre Besucher herkommen, bevor sie zu Ihrer Site gelangten, welche Methoden Ihre Besucher zum Suchen Ihrer Website verwenden und wie viele Besuche Ihrer Site von diesen verweisenden Stellen stammen.
seo-description: Zeigt an, wo Ihre Besucher herkommen, bevor sie zu Ihrer Site gelangten, welche Methoden Ihre Besucher zum Suchen Ihrer Website verwenden und wie viele Besuche Ihrer Site von diesen verweisenden Stellen stammen.
seo-title: Referrer
solution: Analytics
title: Verweisende Stellen
topic: 'Berichte    '
uuid: e 63 b 47 b 4-49 f 3-43 af -8409-3272 bec 0484 e
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Verweisende Stellen

Zeigt an, wo Ihre Besucher herkommen, bevor sie zu Ihrer Site gelangten, welche Methoden Ihre Besucher zum Suchen Ihrer Website verwenden und wie viele Besuche Ihrer Site von diesen verweisenden Stellen stammen.

Wenn beispielsweise ein Besucher auf Site A auf einen Link klickt und zu Ihrer Seite gelangt, ist Site A der Referrer, falls diese nicht als Teil Ihrer Domäne definiert ist. Während der Implementierung kann Ihr Implementierungsberater Ihnen helfen, die Domänen und URLs zu definieren, die Teil Ihrer Website sind. (Diese Änderung kann nach der Implementierung vorgenommen werden.)

Domänen oder URLs, die nicht Bestandteil der definierten Domänen und URLs sind, gelten als Verweisende Stellen. Beispiel: Webseite A und Webseite B werden zum internen URL-Filter hinzugefügt, aber Webseite C nicht. In diesem Fall gilt Webseite C als Referrer.

## Zuordnung, Ablauf und spezielle Werte {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Marketing Reports &amp; Analytics (SiteCatalyst) </th> 
   <th colname="col3" class="entry"> Ad-hoc-Analysen </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Metrikzuordnung </td> 
   <td colname="col2"> Zuletzt verwendet </td> 
   <td colname="col3"> Zuletzt verwendet </td> 
   <td colname="col4"> Zuletzt verwendet </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Werte laufen ab nach </td> 
   <td colname="col2"> Besuch </td> 
   <td colname="col3"> Besuch </td> 
   <td colname="col4"> Besuch </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Wertgrenzen </td> 
   <td colname="col2"> Keine Grenzen (ändert sich möglicherweise in einer zukünftigen Version) </td> 
   <td colname="col3"> Keine Grenzen (ändert sich möglicherweise in einer zukünftigen Version) </td> 
   <td colname="col4"> Keine </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Spezielle Werte </td> 
   <td colname="col2"> <p>„Keine“: Summen für die gesamte Site, die während des Besuchs über keine verweisenden Stellen verfügten. </p> </td> 
   <td colname="col3"> <p>„Keine“: Summen für die gesamte Site, die während des Besuchs über keine verweisenden Stellen verfügten. </p> </td> 
   <td colname="col4"> <p> Leer – entspricht „Keine“: Summen für die gesamte Site, die während des Besuchs über keine verweisenden Stellen verfügten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Hinweise {#section_B83A3571D64E4E7792712FAF740D7955}

* Die verweisende Stelle, der Typ der verweisenden Stelle und die verweisende Domäne werden beim ersten Treffer jedes Besuchs festgelegt, oder während eines Besuchs, wenn es sich um eine externe verweisende Stelle handelt (z. B. wenn ein Besucher Ihre Site verlässt, eine Suchmaschine verwendet und zur Site zurückkehrt, bevor der erste Besuch abläuft). Diese Werte werden gleichzeitig festgelegt und bleiben für die Dauer des Besuchs persistent.
* Interne URLs werden gefiltert. Nur verweisende Stellen, die nicht mit den internen URL-Filtern übereinstimmen, werden in diesen Bericht aufgenommen.
* Die entsprechende Metrik heißt in Ad Hoc Analysis Referrer-Instanz.
* Eingegebene/mit Lesezeichen versehene Werte werden nicht in den Referrer-Bericht aufgenommen. Das bedeutet, dass die Besuche der gesamten Site nicht mit den Besuchen in diesem Bericht übereinstimmen.

## Berichte – Verlauf {#section_6C0FCEA9DAF04D97BA056E153B7E4628}

<table id="table_9DFA79EC6A5A48648F2FB5418E1752DB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum </th> 
   <th colname="col2" class="entry"> Ändern </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 16.01.2014 </td> 
   <td colname="col2"> Data Warehouse wurde aktualisiert, um der Logik von Marketing Reports &amp; Analytics zu entsprechen. Vor diesem Datum waren Suchkeywords nicht für die Dauer des Besuchs persistent. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 19.06.2012 </td> 
   <td colname="col2"> <p> Bis Juli 2012 umfasste „Keine“ den gesamten mobilen Traffic, Eingaben/Lesezeichen und Besuche ohne JavaScript. Seit Juli 2012 umfasst „Keine“ nur Treffer ohne JavaScript auf der ersten Besuchsseite. </p> </td> 
  </tr> 
 </tbody> 
</table>

