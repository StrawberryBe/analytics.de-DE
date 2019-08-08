---
description: Beschreibt die evars und Ereignisse, die für die einzelnen Report Suites reserviert werden sollen.
seo-description: Beschreibt die evars und Ereignisse, die für die einzelnen Report Suites reserviert werden sollen.
seo-title: Adobe Analytics-Variablen für Lyris konfigurieren
solution: Analytics
title: Adobe Analytics-Variablen für Lyris konfigurieren
uuid: 12 e 150 c 4-052 a -481 c -8 c 27-ef 45 ee 801977
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Adobe Analytics-Variablen für Lyris konfigurieren{#configure-adobe-analytics-variables-for-lyris}

Beschreibt die evars und Ereignisse, die für die einzelnen Report Suites reserviert werden sollen.

Für diese Integration sind mindestens 2 evars für jede Report Suite-Implementierung erforderlich. Zusätzlich zu diesen evars sind einige Ereignisse möglicherweise reserviert, je nachdem, welche Lyris-Daten Sie in Analytics sehen möchten. Diese evars und Ereignisse werden in der folgenden Tabelle beschrieben:

<table id="table_43E32344E9E54FED8491F28047249329"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablentyp </th> 
   <th colname="col2" class="entry"> Variablenname </th> 
   <th colname="col3" class="entry"> Verwendung der Variablen </th> 
   <th colname="col4" class="entry"> Einstellungen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> So erfassen Sie die Identifizierung der einzelnen E-Mail-Kampagnen </td> 
   <td colname="col4"> <p>Status: Aktiviert </p> <p>Zuordnung: Zuletzt verwendet </p> <p>Läuft ab nach: " Geschäftsentscheidung « </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Email Recipient ID </td> 
   <td colname="col3"> So erfassen Sie die anonyme Identifikation für Ihren Kunden, der auf die E-Mail-Kampagne geklickt hat </td> 
   <td colname="col4"> <p>Status: Aktiviert </p> <p>Zuordnung: Zuletzt verwendet </p> <p>Läuft ab nach: " Geschäftsentscheidung « </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - Gesendete E-Mails </td> 
   <td colname="col3"> Zum Speichern von. von E-Emails, die von Lyris gesendet werden </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - Geöffnete E-Mails </td> 
   <td colname="col3"> Zum Speichern von. von E-Emails, die geöffnet wurden </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - Eindeutige E-Mails geöffnet </td> 
   <td colname="col3"> Zum Speichern von. Eindeutiger E-Emails, die geöffnet wurden </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - E-Mail-Clickthroughs </td> 
   <td colname="col3"> Zum Speichern von. Zeiten, an denen auf eine E-Email geklickt wurde </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - E-Mail-Absprünge </td> 
   <td colname="col3"> Um das Nein zu speichern. von E-Emails, die abspringen </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - E-Mail abonnieren </td> 
   <td colname="col3"> Um das Nein zu speichern. E-Email-Abonnements, die deaktiviert wurden </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
 </tbody> 
</table>

