---
description: Für diese Integration sind 2 evars für jede Report Suite-Implementierung erforderlich.
seo-description: Für diese Integration sind 2 evars für jede Report Suite-Implementierung erforderlich.
seo-title: Analytics-Variablen für Selligent konfigurieren
solution: Analytics
title: Analytics-Variablen für Selligent konfigurieren
uuid: 3 b 7 b 8 b 4 b -7614-4439-bcb 0-dbdec 304844
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Analytics-Variablen für Selligent konfigurieren{#configure-analytics-variables-for-selligent}

Für diese Integration sind 2 evars für jede Report Suite-Implementierung erforderlich.

Zusätzlich zu diesen evars können einige Ereignisse je nach den Daten von Selligent reserviert werden, die Sie in Analytics sehen möchten. Diese evars und Ereignisse werden wie folgt beschrieben:

<table id="table_2FFB865DBD80412F90DA8E224B12FB62"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablentyp </th> 
   <th colname="col2" class="entry"> Variablenname </th> 
   <th colname="col3" class="entry"> Verwendungsart </th> 
   <th colname="col4" class="entry"> Einstellungen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> Zur Erfassung der einzelnen E-Mail-Nachrichtenkampagnen. </td> 
   <td colname="col4"> <p><b>Status</b>: Aktiviert </p> <p><b>Zuordnung</b>: Zuletzt verwendet </p> <p><b>Läuft ab nach</b>: " Geschäftsentscheidung « </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ev </td> 
   <td colname="col2"> Recipient ID </td> 
   <td colname="col3"> Um die anonyme Identifizierung für Ihren Kunden zu erfassen, der auf die E-Mail-Kampagne geklickt hat. </td> 
   <td colname="col4"> <p><b>Status</b>: Aktiviert </p> <p><b>Zuordnung</b>: Zuletzt verwendet </p> <p><b>Läuft ab nach</b>: " Geschäftsentscheidung « </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Gesendet </td> 
   <td colname="col3"> Um die Anzahl der E-Emails zu speichern, die von Selligent gesendet werden. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Bereitgestellt </td> 
   <td colname="col3"> Um die Anzahl der ausgelieferten E-Mails zu speichern. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Ansichten </td> 
   <td colname="col3"> Zum Speichern der Anzahl der eindeutigen E-Mails, die angezeigt wurden. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Klicks </td> 
   <td colname="col3"> Um zu speichern, wie oft auf eine E-Mail geklickt wurde. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Abgebrochen </td> 
   <td colname="col3"> Um die Anzahl der versprungenen E-Mails zu speichern. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
 </tbody> 
</table>

