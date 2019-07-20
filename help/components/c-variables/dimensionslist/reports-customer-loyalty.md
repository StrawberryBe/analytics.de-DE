---
description: Kundenloyalität veranschaulicht die Einkaufsmuster der Kunden.
seo-description: Kundenloyalität veranschaulicht die Einkaufsmuster der Kunden.
seo-title: Kundenloyalität
solution: Analytics
title: Kundenloyalität
topic: 'Berichte    '
uuid: 7 dc 30 b 57-7 b 18-4228-a 6 ab -6 eb 66 b 3 d 9402
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kundenloyalität

Kundenloyalität veranschaulicht die Einkaufsmuster der Kunden.

Dieser Bericht gibt Aufschluss über Einkaufsmuster von Kunden, wobei vier Loyalitätskategorien zugrunde gelegt werden:

* Kein Kunde
* Neuer Kunde
* Rückkehrender Kunde
* Loyaler Kunde

Auch wenn in diesem Bericht nicht einkaufsbasierte Metriken (z. B. zu benutzerspezifischen oder Warenkorb-Ereignissen usw.) angezeigt werden können, basieren die Kategorien immer auf der Anzahl aufgegebener Bestellungen. Beispielsweise könnte ein Besucher ein benutzerspezifisches Ereignis namens „Interne Suchläufe“ zum Bericht hinzufügen. Im Zeileneintrag [!UICONTROL „Rückkehrender Kunde“] würde dann die Zahl der internen Suchläufe angezeigt, die von Kunden, die zuvor zwei Käufe getätigt haben, durchgeführt wurden – nicht aber die Anzahl der Besucher allgemein, die zwei interne Suchläufe durchgeführt haben.

**Verarbeitung der Kundenloyalität**

In den folgenden Tabellen finden Sie Informationen dazu, wie Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis und Data Warehouse derzeit Kundentreue verarbeiten:

<table id="table_E6A5CA96BE5C47F29F09688A4D41BC60"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Nach dem 19. Mai 2016 </p> </th> 
   <th colname="col3" class="entry"> <p>Zwischen dem 21. April und dem 19. Mai 2016 </p> <p>(gilt nicht für Data Warehouse) </p> </th> 
   <th colname="col4" class="entry"> <p>Vor dem 21. April 2016 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Kein Kunde </p> </td> 
   <td colname="col2"> <p>Besucher, die nie gekauft haben </p> </td> 
   <td colname="col3"> <p>Besucher, die bis zur Beendigung eines Besuchs nicht gekauft haben </p> </td> 
   <td colname="col4"> <p>Nicht verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Neuer Kunde </p> </td> 
   <td colname="col2"> <p>Besucher, die einmal gekauft haben </p> </td> 
   <td colname="col3"> <p>Besucher, die bis zur Beendigung eines Besuchs einmal gekauft haben </p> <p>(Wurde gekauft, wurde der Kundenstatus beim nächsten Besuch nach diesem Kauf aktualisiert.) </p> </td> 
   <td colname="col4"> <p>Besucher, die bis zur Beendigung des Besuchs nicht gekauft haben </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rückkehrender Kunde </p> </td> 
   <td colname="col2"> <p>Besucher, die zweimal gekauft haben </p> </td> 
   <td colname="col3"> <p>Besucher, die bis zum Ende des Besuchs, während dessen sie den zweiten Einkauf tätigten, zweimal gekauft haben. </p> <p>(Wurde gekauft, wurde der Kundenstatus beim nächsten Besuch nach diesem Kauf aktualisiert.) </p> </td> 
   <td colname="col4"> <p>Besucher, die bis zum Ende des Besuchs, während dessen sie diesen Einkauf tätigten, einmal gekauft haben. </p> <p>(Wurde gekauft, wurde der Kundenstatus beim nächsten Besuch nach diesem Kauf aktualisiert.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Loyaler Kunde </p> </td> 
   <td colname="col2"> <p>Besucher, die mehr als dreimal gekauft haben </p> </td> 
   <td colname="col3"> <p>Besucher, die bis zum Ende des Besuchs, während dessen sie den letzten Einkauf tätigten, mindestens dreimal gekauft haben. </p> <p>(Wurde gekauft, wurde der Kundenstatus beim nächsten Besuch nach diesem Kauf aktualisiert.) </p> </td> 
   <td colname="col4"> <p>Besucher, die bis zum Ende des Besuchs, während dessen sie den letzten Einkauf tätigten, mindestens zweimal gekauft haben. </p> <p>(Wurde gekauft, wurde der Kundenstatus beim nächsten Besuch nach diesem Kauf aktualisiert.) </p> </td> 
  </tr> 
 </tbody> 
</table>

| Kundenloyalität in Version 14 (aktuell) |
|---|
| Neuer Kunde | 1 Besuch und 1 Kauf |
| Rückkehrender Kunde | Mehr als 1 Besuch und 2 Käufe |
| Loyaler Kunde | Mehr als 1 Besuch und mehr als 3 Käufe |

Der Treuestatus ändert sich unmittelbar nach einem Kaufereignis innerhalb desselben Besuchs. Beispiel: Ein Neukunde (1 Einkauf) tätigt einen Kauf und registriert sich dann innerhalb desselben Besuchs für einen Newsletter. Das Newsletter-Registrierungsereignis wird als Interaktion mit einem rückkehrenden Kunden angesehen, da sich der Status der Kundenloyalität unmittelbar nach dem Einkauf geändert hat.
