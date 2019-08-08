---
description: Die Data Connectors-Integration für Emarsys verwendet Analytics-Variablen, um verschiedene Emarsys-Metriken zu verfolgen.
seo-description: Die Data Connectors-Integration für Emarsys verwendet Analytics-Variablen, um verschiedene Emarsys-Metriken zu verfolgen.
seo-title: Die Analytics-Variablen
title: Die Analytics-Variablen
uuid: 4 d 5 e 087 c-f 495-4 aab -9 ad 1-9 b 901 d 34 a 254
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Analytics-Variablen{#analytics-variables}

Die Data Connectors-Integration für Emarsys verwendet Analytics-Variablen, um verschiedene Emarsys-Metriken zu verfolgen.

Nachdem Sie das Ereignis und die evars identifiziert haben, die mit der Emarsys-Integration verwendet werden sollen, aktivieren Sie sie in der [Admin-Konsole](https://microsite.omniture.com/t2/help/en_US/reference/index.html?f=conversion_var_admin).

**Erforderliche Variablen**

<table id="table_5B8F3A1EB55D4BB48F669FB84C857256"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablentyp </th> 
   <th colname="col2" class="entry"> Name </th> 
   <th colname="col3" class="entry"> Methode zum Ausfüllen </th> 
   <th colname="col4" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ereignis (numerisch) </td> 
   <td colname="col2"> Absprünge insgesamt </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Mit dem Ereignis "Absprünge" können Sie die Anzahl der E-Email-Nachrichten anzeigen, die aufgrund eines Problems mit der Auslieferung nicht an Empfänger übermittelt wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis (numerisch) </td> 
   <td colname="col2"> Angeklickt </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Mit dem Ereignis "Angeklickt" können Sie erkennen, wie viele Besucher auf die E-Email geklickt haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis (numerisch) </td> 
   <td colname="col2"> Geöffnet </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Mit dem Ereignis "Geöffnet" können Sie erkennen, wie viele Besucher die E-Email geöffnet haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis (numerisch) </td> 
   <td colname="col2"> Gesendet </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Mit dem Ereignis "Sends" können Sie die Anzahl der gesendeten E-Email-Nachrichten anzeigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis (numerisch) </td> 
   <td colname="col2"> Abonnement </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Mit dem nicht abonnierten Ereignis können Sie die Anzahl der Besucher anzeigen, die die E-Email geöffnet haben, aber auf den Link Abonnieren klicken, um zukünftige E-Email-Nachrichten aus Ihrer Organisation abzuwählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Recipient ID </td> 
   <td colname="col3"> <p>Wird aus Abfrageparametern in E-Email-Links über die automatisierte Erfassungsmethode oder ein javascript-Plug-in erfasst. </p> </td> 
   <td colname="col4"> Recipient ID </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar oder s. campaign </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> <p>Wird aus Abfrageparametern in E-Email-Links über die automatisierte Erfassungsmethode oder ein javascript-Plug-in erfasst. </p> </td> 
   <td colname="col4"> Dieser Wert wird oft in der Kampagnenvariablen gespeichert. </td> 
  </tr> 
 </tbody> 
</table>

