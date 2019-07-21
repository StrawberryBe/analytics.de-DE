---
description: Ermöglicht das Steuern des Zugriffs auf Berichterstellungsdaten. Zu den Optionen gehören sichere Kennwörter, Kennwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen.
seo-description: Ermöglicht das Steuern des Zugriffs auf Berichterstellungsdaten. Zu den Optionen gehören sichere Kennwörter, Kennwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen.
seo-title: Sicherheitsmanager
solution: Analytics
title: Sicherheits-Manager
topic: Admin Tools
uuid: b 3 fbdba 0-e 2 bf -4 d 67-92 e 3-ef 57711141 d 4
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Sicherheits-Manager

Ermöglicht das Steuern des Zugriffs auf Berichterstellungsdaten. Zu den Optionen gehören sichere Kennwörter, Kennwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Unternehmenseinstellungen]** &gt; **[!UICONTROL Sicherheit]**

<table id="table_F1AD9DE5094A4FC2B9DA8D01198F944B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Sichere Passwörter erforderlich </span> </td> 
   <td colname="col2">Erzwingt die Erstellung sicherer Passwörter, die folgende Regeln beachten: 
    <ul id="ul_100CC57EB4374DAA87B2074BA8B46F26"> 
     <li id="li_4D9102C361044FADBC14402A8398F2F3">Muss mindestens acht Zeichen lang sein. </li> 
     <li id="li_AFE9568C14894E93BFDFDC84DCD2838D">Muss mindestens ein Symbol oder eine Zahl zwischen dem ersten und dem letzten Zeichen enthalten. </li> 
     <li id="li_ECA05BEF7BFD4430B09D4A953B41D2A6">Muss mindestens einen Buchstaben enthalten. </li> 
     <li id="li_6928045588E94E28851BB15991C8D51E">Darf nicht im Wörterbuch stehen oder Begriffe aus dem (englischen) Wörterbuch enthalten. </li> 
     <li id="li_C3DD4608CA6F43E4B1E4FCFC6D116371">Darf nicht drei (3) aufeinanderfolgende Zeichen aus dem Anmeldenamen des Benutzers enthalten. </li> 
     <li id="li_687838CA01B94EE29EF4C09F485C5537">Muss sich von den vorhergehenden 10 Passwörtern unterscheiden. </li> 
    </ul> <p>Hinweis: Diese Funktion wird bei neuen Kennwörtern für die Zukunft erzwungen. Vorhandene Passwörter werden nicht überprüft, und die Benutzer werden auch nicht aufgefordert, ihre bisherigen Passwörter zu ändern. Daher sollten Sie in Erwägung ziehen, die Option Passwortablauf zu aktivieren und die Benutzer dazu zu zwingen, neue Passwörter nach den strengeren Passwortregeln festzulegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Passwortablauf</span> </td> 
   <td colname="col2"> Erzwingt die regelmäßige Änderung des Kontopassworts durch den Benutzer. Sie können das Intervall festlegen, in dem die Kennwörter ablaufen, und den sofortigen Ablauf von Kennwörtern erzwingen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> IP-Anmeldebeschränkungen erzwingen</span> </td> 
   <td colname="col2"> <p>Schränkt den Berichtzugriff auf bestimmte IP-Adressen oder IP-Adressenbereiche ein. </p> <p>Sie können der Liste „IP-Adressenfilter“ bis zu 100 Einträge hinzufügen. Bei jedem Eintrag kann es sich um eine bestimmte Adresse oder einen Adressbereich handeln. </p> <p>Die Funktion <span class="wintitle">IP-Anmeldebeschränkungen erzwingen</span> wird nur erzwungen, wenn sich in der Liste „IP-Adressenfilter“ mindestens ein Eintrag befindet.</p> <p><span class="uicontrol"> Akzeptierte IP-Adresse</span>: Um einen IP-Adressbereich anzugeben, fügen Sie den Bereich in eckigen Klammern an (z. B.
       <code>
        192.168.10.[20-240]
       </code>). You can also use wildcards (*) to specify any number from 0 to 255 (for example, 
       <code>
        192.168.[10-14].*
       </code>) </p> <p>Fehlgeschlagene Anmeldeversuche werden protokolliert und können im <a href="../../admin/admin/logs.md#section_6FBAF92D9EA244809C45A78A2F0A7232" format="dita" scope="local">Nutzungs- und Zugriffsprotokoll</a> angezeigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> E-Mail-Domänenbeschränkungen erzwingen</span> </td> 
   <td colname="col2"> <p>Filtert die E-Mail-Adressen und Domänen, an die Analytics Lesezeichen, herunterladbare Berichte und Warnhinweise sendet. </p> <p>Die E-Mail-Filterliste kann bis zu 100 Einträge lang sein. Jeder einzelne Eintrag steht für eine E-Mail-Adresse oder eine gesamte E-Mail-Domäne. </p> <p>Wenn ein terminierter Bericht als Zieladresse eine nicht genehmigte E-Mail-Adresse aufweist, versendet Analytics eine E-Mail-Benachrichtigung zu diesem Problem sowie einen Link zur Aufhebung der Berichtsplanung. </p> <p>  Die Funktion <span class="wintitle">Erzwingen der E-Mail-Domänenbeschränkungen</span> wird nur erzwungen, wenn sich in der Liste <span class="wintitle">Akzeptierter E-Mail-Domänenfilter</span> mindestens ein Eintrag befindet. </p> <p> <span class="uicontrol"> Akzeptierte E-Mail-Adresse und Domänen</span>: Um einen IP-Adressbereich anzugeben, fügen Sie den Bereich in eckigen Klammern an (z. B.
       <code>
        192.168.10.[20-240]
       </code>). You can also use wildcards (*) to specify any number from 0 to 255 (for example, 
       <code>
        192.168.[10-14].*
       </code>) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Benachrichtigung über Passwortwiederherstellung</span> </td> 
   <td colname="col2"> <p>Benachrichtigt die jeweiligen Administratoren, wenn ein Benutzer versucht, sein Kontopasswort zurückzusetzen. </p> <p> <span class="uicontrol"> Verfügbare Admins:</span> Es wird eine Liste sämtlicher Administratoren angezeigt. Halten Sie bei Bedarf beim Klicken die STRG- bzw. Umschalttaste gedrückt, um mehrere Administratoren gleichzeitig auszuwählen. </p> <p> <span class="uicontrol">E-Mail-Mitglieder</span>: Hiermit wird die aktuell definierte E-Mail-Gruppe angezeigt.  </p> </td> 
  </tr> 
 </tbody> 
</table>

