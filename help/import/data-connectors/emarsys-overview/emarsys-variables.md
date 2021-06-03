---
description: Die Data Connectors-Integration für emarsys verwendet Analytics-Variablen zur Verfolgung verschiedener emarsys-Metriken.
title: Analytics-Variablen
uuid: 4d5e087c-f495-4aab-9ad1-9b901d34a254
exl-id: a59216f2-047b-429b-8714-a2bdaa271911
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 97%

---

# Analytics-Variablen {#analytics-variables}

Die Data Connectors-Integration für emarsys verwendet Analytics-Variablen zur Verfolgung verschiedener emarsys-Metriken.

Nachdem Sie das Ereignis und die eVars identifiziert haben, die mit der emarsys-Integration verwendet werden sollen, aktivieren Sie sie in der [Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/c-admin-tools.html).

**Erforderliche Variablen**

<table id="table_5B8F3A1EB55D4BB48F669FB84C857256"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablentyp </th> 
   <th colname="col2" class="entry"> Name </th> 
   <th colname="col3" class="entry"> Erfassungsmethode </th> 
   <th colname="col4" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Rücksendungen insgesamt </td> 
   <td colname="col3"> <p>Automatisch aus emarsys importiert </p> </td> 
   <td colname="col4"> <p>Das Ereignis „Rücksendungen insgesamt“ zeigt die Anzahl der E-Mail-Nachrichten an, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Angeklickt </td> 
   <td colname="col3"> <p>Automatisch aus emarsys importiert </p> </td> 
   <td colname="col4"> <p>Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Geöffnet </td> 
   <td colname="col3"> <p>Automatisch aus emarsys importiert </p> </td> 
   <td colname="col4"> <p>Das Ereignis „Geöffnet“ zeigt die Anzahl der Besucher an, welche die E-Mail geöffnet haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Gesendet </td> 
   <td colname="col3"> <p>Automatisch aus emarsys importiert </p> </td> 
   <td colname="col4"> <p>Das Ereignis „Sendungen“ zeigt die Anzahl der gesendeten E-Mail-Nachrichten an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numerisch) </td> 
   <td colname="col2"> Abo storniert </td> 
   <td colname="col3"> <p>Automatisch aus emarsys importiert </p> </td> 
   <td colname="col4"> <p>Mit dem Ereignis „Abo storniert“ können Sie die Anzahl der Besucher anzeigen, welche die E-Mail geöffnet, aber dann auf den Link „Abonnement kündigen“ geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrer Organisation abzuwählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Empfänger-ID </td> 
   <td colname="col3"> <p>Wird über die automatisierte Erfassungsmethode oder über ein JavaScript-Plug-In aus Abfrageparametern in E-Mail-Links erfasst. </p> </td> 
   <td colname="col4"> Empfänger-ID </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar  oder s.campaign </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> <p>Wird über die automatisierte Erfassungsmethode oder über ein JavaScript-Plug-In aus Abfrageparametern in E-Mail-Links erfasst. </p> </td> 
   <td colname="col4"> Dieser Wert wird häufig in der Kampagnenvariablen gespeichert. </td> 
  </tr> 
 </tbody> 
</table>
