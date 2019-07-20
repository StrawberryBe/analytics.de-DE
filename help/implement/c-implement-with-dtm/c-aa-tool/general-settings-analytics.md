---
description: Beschreibung der Felder für die allgemeinen Einstellungen im Dynamic Tag Manager zur Bereitstellung von Adobe Analytics.
keywords: Analytics-Implementierung; Implementierungsmethode; dynamisches Tag-Management; dtm; allgemeine Einstellungen; EU-Konformität; Zeichensatz; Währungscode; Tracking-Server; SSL-Tracking-Server
seo-description: Beschreibung der Felder für die allgemeinen Einstellungen im Dynamic Tag Manager zur Bereitstellung von Adobe Analytics.
seo-title: Allgemein
solution: Analytics
title: Allgemein
topic: Entwickler und Implementierung
uuid: 93008719-6 fb 6-4 e 39-9 a 75-c 937 fe 3247 b 9
translation-type: tm+mt
source-git-commit: 49c81e50ff10060ef7a3debe82132d1099e25118

---


# Allgemein

Feldbeschreibungen für die allgemeinen Einstellungen in DTM für die Bereitstellung von Adobe Analytics.

**[!UICONTROL &lt; Eigenschaft &gt;]** &gt; ![](assets/settings_gear.png)**[!UICONTROL Tool bearbeiten]** &gt; **[!UICONTROL Allgemein]**

<table id="table_DD8DA303698041D296DD5DB080AF7971"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>EU-Konformität für <span class="keyword">Adobe Analytics</span> aktivieren  </p> </td> 
   <td colname="col2"> <p> Dadurch wird das Tracking auf der Grundlage des Cookies zum Datenschutz in der EU aktiviert oder deaktiviert. </p> <p>Wenn eine Seite geladen wird, überprüft das System, ob ein Cookie mit dem Namen <span class="filepath">sat_track</span> festgelegt ist (oder das benutzerdefinierte Cookie mit dem Namen, der auf der Seite <span class="wintitle">Eigenschaft bearbeiten</span> angegeben wurde). Die folgenden Informationen sind zu berücksichtigen: </p> 
    <ul id="ul_42A6D728F0BC4FBABB0069EFB66DCB01"> 
     <li id="li_227CB14326344AA3980F20C7EACF2AD2"> <p> Wenn das Cookie nicht vorhanden ist oder wenn das Cookie vorhanden ist und auf einen anderen Wert als <span class="term"> true </span>, wird das Laden des Tools übersprungen, wenn diese Einstellung aktiviert ist. Das bedeutet, dass der Teil der Regel, der sich auf das Tool stützt, keine Anwendung findet. </p> <p>Wenn eine Regel Analysen umfasst, die der EU-Compliance entsprechen und Drittanbietercode umfassen, wird das Cookie auf <span class="term"> false </span>, der Drittanbietercode wird dennoch ausgeführt. Die Analysevariablen werden jedoch nicht festgelegt. </p> </li> 
     <li id="li_1E74E02D7E4646ACA86D862A1D3C6679"> Wenn das Cookie vorhanden ist, jedoch auf <span class="term"> true </span>, wird das Tool normal geladen. </li> 
    </ul> <p>You are responsible for setting the <span class="filepath"> sat_track </span> (or custom named) cookie to <span class="term"> false </span> if a visitor opts out. Dazu können Sie den folgenden benutzerdefinierten Code verwenden: </p> <p> 
     <code>_ satellite. setcookie («sat_ track», &amp; amp; nbsp; false (falsch); </code>
  </p> <p> You must also have a mechanism to set that cookie to <span class="term"> true </span> if you want a visitor to be able to opt in later: </p> <p> 
     <code>_ satellite. setcookie («sat_ track», &amp; amp; nbsp; " true "); </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zeichensatz </p> </td> 
   <td colname="col2"> <p>Zeigt die verfügbaren Zeichenkodierungssätze an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Währungscode </p> </td> 
   <td colname="col2"> <p>Zeigt die unterstützten Währungscodes zur Auswahl an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tracking-Server </p> </td> 
   <td colname="col2"> <p>Die Domäne, in der die Bildanforderung und das Cookie geschrieben werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL-Tracking-Server </p> </td> 
   <td colname="col2"> <p>Die Domäne, in der die Bildanforderung und das Cookie geschrieben werden. Wird bei sicheren Seiten verwendet. Wenn   nichts definiert ist, werden die SSL-Daten an  <span class="term"> trackingServer </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datencenter </p> </td> 
   <td colname="col2"> <p>Das Adobe-Datencenter, das für die Datensammlung verwendet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

