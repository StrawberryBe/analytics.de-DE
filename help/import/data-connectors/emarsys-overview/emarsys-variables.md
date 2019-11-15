---
description: Die Data Connectors-Integration für emarsys verwendet Analytics-Variablen zur Verfolgung verschiedener emarsys-Metriken.
title: Analytics-Variablen
uuid: 4d5e087c-f495-4aab-9ad1-9b901d34a254
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Analytics-Variablen{#analytics-variables}

Die Data Connectors-Integration für emarsys verwendet Analytics-Variablen zur Verfolgung verschiedener emarsys-Metriken.

Nachdem Sie die Ereignisse und eVars identifiziert haben, die mit der eVars-Integration verwendet werden sollen, aktivieren Sie sie in der [Admin-Konsole](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/c-admin-tools.html).

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
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Absprünge insgesamt </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Das Ereignis "Absprünge insgesamt"zeigt die Anzahl der E-Mail-Nachrichten an, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Angeklickt </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Geöffnet </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Das Ereignis "Geöffnet"zeigt die Anzahl der Besucher an, die die E-Mail geöffnet haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Gesendet </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Mit dem Sends-Ereignis können Sie die Anzahl der gesendeten E-Mail-Nachrichten anzeigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Nicht abonniert </td> 
   <td colname="col3"> <p>Automatisch aus Emarsys importiert </p> </td> 
   <td colname="col4"> <p>Mit dem Abmeldung-Ereignis können Sie sehen, wie viele Besucher die E-Mail geöffnet, aber dann auf den Link Abmelden geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrem Unternehmen abzumelden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Recipient ID </td> 
   <td colname="col3"> <p>Wird über die automatisierte Erfassungsmethode oder ein JavaScript-Plug-In aus Abfrageparametern in E-Mail-Links erfasst. </p> </td> 
   <td colname="col4"> Recipient ID </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar oder s.campaign </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> <p>Wird über die automatisierte Erfassungsmethode oder ein JavaScript-Plug-In aus Abfrageparametern in E-Mail-Links erfasst. </p> </td> 
   <td colname="col4"> Dieser Wert wird häufig in der Kampagnenvariablen gespeichert. </td> 
  </tr> 
 </tbody> 
</table>

