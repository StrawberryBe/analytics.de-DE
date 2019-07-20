---
description: Liste der in Analytics verwendeten benutzerdefinierten Variablen
keywords: Analytics-Implementierung
seo-description: Liste der in Analytics verwendeten benutzerdefinierten Variablen
seo-title: Benutzerdefinierte Variablen
solution: Analytics
title: Benutzerdefinierte Variablen
topic: Entwickler und Implementierung
uuid: 54 adf 622-7 f 5-49 c 0-b 7 e 6-702 bb 2 f 17 b 1 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Benutzerdefinierte Variablen

Liste der in Analytics verwendeten benutzerdefinierten Variablen

<table id="table_E8C7871F63F648A59644638FB56BD0E1"> 
 <thead> 
  <tr> 
   <th class="entry"> Variable </th> 
   <th class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Traffic-Variablen </td> 
   <td> Überprüfen Sie den Wert von prop1–75. Die folgenden Punkte sind zu überprüfen: 
    <ul id="ul_0EE2D50BA90F4F21BD63268A5082F980"> 
     <li id="li_A6E4D66E8A03400491A26A08E4945908">Ist die Groß-/Kleinschreibung korrekt? „WertA“ ist ein anderer Datensatz als „wertA“. Sie können alles klein schreiben, da einige wenige Browser sämtliche Variablen in Kleinbuchstaben umwandeln. </li> 
     <li id="li_65CBFB908E7B4ED5AF9518FE5B58D4E2">Sind die Werte kürzer als 100 Zeichen? Wenn nicht, kann es vorkommen, dass längere Teile abgeschnitten werden. </li> 
     <li id="li_CC506D114AFE44699D89AB84BBCCEBFC"> Gehören alle Werte in einer Eigenschaft zu einer Variablen, oder sind Werte anscheinend fehl am Platz? </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> Konversionsvariablen </td> 
   <td> <span class="wintitle"> Econversion</span>-Variablen beinhalten eVar 1–75. Die folgenden Punkte sind zu überprüfen: 
    <ul id="ul_CA10C5B9F24B4C49A64CA84A9DCE8E63"> 
     <li id="li_8CCD92F3AD5E49EBA91C9B008DA47016">Ist die Groß-/Kleinschreibung korrekt? „WertA“ ist ein anderer Datensatz als „wertA“. Sie können alles klein schreiben, da einige wenige Browser sämtliche Variablen in Kleinbuchstaben umwandeln. </li> 
     <li id="li_5B6FDEDB2C32409AA59D6BB0DF2346CB">Sind die Werte kürzer als 255 Zeichen? Wenn nicht, kann es vorkommen, dass längere Teile abgeschnitten werden. </li> 
     <li id="li_C31AFBAC99D84E96A1244E795CE7765D">Gehören alle Werte in einer Eigenschaft zu einer eVar, oder sind Werte anscheinend fehl am Platz? </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> Benutzerspezifische Ereignisse </td> 
   <td> Zu Ereignissen gehören sowohl die Standardwerte (<span class="wintitle">prodView</span>, <span class="wintitle">scOpen</span>, <span class="wintitle">scAdd</span>, <span class="wintitle">scCheckout</span> und <span class="wintitle">purchase</span>) als auch benutzerspezifische Ereignisse von „event1“ bis „event100“. Alle Ereignisse werden in der Ereignisvariablen gesendet. Wenn auf einer Seite mehrere Ereignisse vorhanden sind, müssen diese mit Kommas (nicht mit Leerzeichen!) getrennt werden. 
    <ul id="ul_2213CC9DE892433FAF6FC1F5A2B841B4"> 
     <li id="li_15E31A9FF1654DFA93C158F422B9EAE3">Bei allen standardmäßigen Konversion-Ereignissen muss 'products' auch mit den entsprechenden Produkten aufgefüllt werden. Bei allen Ereignissen außer 'purchase' sind die Elemente 'qty' ind 'price' optional. </li> 
     <li id="li_03ED9AAC45DA47A58AB482E2CEBF5108">Das Ereignis <span class="wintitle">purchase</span> muss in einer Sitzung nur ein einziges Mal festgelegt werden, nachdem der Einkauf durchgeführt und bestätigt wurde. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

