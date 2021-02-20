---
description: Beschreibung der Felder für die allgemeinen Einstellungen im Dynamic Tag Manager zur Bereitstellung von Adobe Analytics.
keywords: Analytics-Implementierung;Implementierungsmethode;Dynamic Tag Management;DTM;Allgemeine Einstellungen;EU-Konformität;Zeichensatz;Währungscode;Tracking-Server;SSL-Tracking-Server
title: Allgemein
topic: Developer and implementation
uuid: 93008719-6fb6-4e39-9a75-c937fe3247b9
translation-type: tm+mt
source-git-commit: 0d699a50a764d9ea76771118c7cc083fb46cefe9
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 100%

---


# Allgemein

Beschreibung der Felder für die allgemeinen Einstellungen im DTM zur Implementierung von Adobe Analytics.

**[!UICONTROL *`Property`*]** > ![](assets/settings_gear.png) **[!UICONTROL Tool bearbeiten]** > **[!UICONTROL Allgemein]**

<table id="table_DD8DA303698041D296DD5DB080AF7971"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>EU-Konformität für <span class="keyword">Adobe Analytics</span> aktivieren </p> </td> 
   <td colname="col2"> <p> Dadurch wird das Tracking auf der Grundlage des Cookies zum Datenschutz in der EU aktiviert oder deaktiviert. </p> <p>Wenn eine Seite geladen wird, überprüft das System, ob ein Cookie mit dem Namen <span class="filepath">sat_track</span> festgelegt ist (oder das benutzerdefinierte Cookie mit dem Namen, der auf der Seite <span class="wintitle">Eigenschaft bearbeiten</span> angegeben wurde). Die folgenden Informationen sind zu berücksichtigen: </p> 
    <ul id="ul_42A6D728F0BC4FBABB0069EFB66DCB01"> 
     <li id="li_227CB14326344AA3980F20C7EACF2AD2"> <p> Wenn das Cookie nicht vorhanden ist oder wenn das Cookie vorhanden ist und auf einen anderen Wert als  <span class="term"> true </span> festgelegt ist, wird das Laden des Tools übersprungen, wenn diese Einstellung aktiviert ist. Das bedeutet, dass der Teil der Regel, der sich auf das Tool stützt, keine Anwendung findet. </p> <p>Wenn eine Regel Analysen umfasst, die der EU-Compliance entsprechen und Drittanbietercode umfassen, wird das Cookie auf  <span class="term"> false </span> festgelegt und der Drittanbietercode weiterhin ausgeführt. Die Analysevariablen werden jedoch nicht festgelegt. </p> </li> 
     <li id="li_1E74E02D7E4646ACA86D862A1D3C6679"> Wenn das Cookie vorhanden ist, jedoch auf  <span class="term"> true </span> festgelegt ist, wird das Tool normal geladen. </li> 
    </ul> <p>Sie sind dafür verantwortlich, das Cookie <span class="filepath">sat_track</span> (oder das Cookie mit benutzerdefiniertem Namen) auf <span class="term">false</span> festzulegen, wenn ein Besucher eine Abwahl trifft. Dazu können Sie den folgenden benutzerdefinierten Code verwenden: </p> <p> 
     <code>
       _satellite.setCookie("sat_track",&amp;nbsp;"false"); 
     </code> </p> <p> Sie müssen außerdem über einen Mechanismus verfügen, mit dem dieses Cookie auf <span class="term">true</span> gesetzt wird, wenn ein Besucher die Möglichkeit haben soll, sich später anzumelden: </p> <p> 
     <code>
       _satellite.setCookie("sat_track",&amp;nbsp;"true"); 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zeichensatz </p> </td> 
   <td colname="col2"> <p>Zeigt die verfügbaren Zeichencodierungssätze an. </p> </td> 
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
   <td colname="col2"> <p>Die Domäne, in der die Bildanforderung und das Cookie geschrieben werden. Wird bei sicheren Seiten verwendet. Wenn  nichts definiert ist, werden die SSL-Daten an  <span class="term">trackingServer</span> übermittelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datencenter </p> </td> 
   <td colname="col2"> <p>Das Adobe-Datencenter, das für die Datensammlung verwendet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

