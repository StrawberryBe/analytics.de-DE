---
description: Ermöglicht das Steuern des Zugriffs auf Berichterstellungsdaten. Zu den Optionen gehören sichere Kennwörter, Kennwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen.
solution: Analytics
title: Sicherheits-Manager
topic: Admin tools
uuid: b3fbdba0-e2bf-4d67-92e3-ef05711141d4
translation-type: tm+mt
source-git-commit: 490a856effac7ec3ff2430dff0ffdcee587bf933

---


# Sicherheits-Manager

Mit dem Sicherheitsmanager können Sie den Zugriff auf Berichtsdaten steuern. Zu den Optionen gehören sichere Kennwörter, Kennwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen.

## Einstellungen

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
   <td colname="col2"> <p>(Diese Funktion kann nicht zusammen mit der Experience Cloud-Anmeldung verwendet werden. Beachten Sie, dass diese Funktion ab Oktober 2020 nicht mehr verfügbar ist. [Mehr...](/help/admin/company/login-restrictions-eol.md) Schränkt den Berichtzugriff auf bestimmte IP-Adressen oder IP-Adressbereiche ein. </p> <p>Sie können der Liste „IP-Adressenfilter“ bis zu 100 Einträge hinzufügen. Bei jedem Eintrag kann es sich um eine bestimmte Adresse oder einen Adressbereich handeln. </p> <p>  Die Funktion <span class="wintitle">IP-Anmeldebeschränkungen erzwingen</span> wird nur erzwungen, wenn sich in der Liste „IP-Adressenfilter“ mindestens ein Eintrag befindet. </p> <p> <span class="uicontrol"> Akzeptierte IP-Adresse</span>: Um einen IP-Adressbereich anzugeben, schließen Sie den Bereich in Klammern ein (z. B. <code>
       192.168.10.[20-240]
     </code>). You can also use wildcards (*) to specify any number from 0 to 255 (for example, 
     <code>
       192.168.[10-14].*
     </code>) </p> <p>Fehlgeschlagene Anmeldeversuche werden protokolliert und können im <a href="/help/admin/admin/logs.md#section_6FBAF92D9EA244809C45A78A2F0A7232">Nutzungs- und Zugriffsprotokoll</a> angezeigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> E-Mail-Domänenbeschränkungen erzwingen</span> </td> 
   <td colname="col2"> <p>Filtert die E-Mail-Adressen und Domänen, an die Analytics Lesezeichen, herunterladbare Berichte und Warnhinweise sendet. </p> <p>Die E-Mail-Filterliste kann bis zu 100 Einträge lang sein. Jeder einzelne Eintrag steht für eine E-Mail-Adresse oder eine gesamte E-Mail-Domäne. </p> <p>Wenn ein terminierter Bericht als Zieladresse eine nicht genehmigte E-Mail-Adresse aufweist, versendet Analytics eine E-Mail-Benachrichtigung zu diesem Problem sowie einen Link zur Aufhebung der Berichtsplanung. </p> <p>  Die Funktion <span class="wintitle">Erzwingen der E-Mail-Domänenbeschränkungen</span> wird nur erzwungen, wenn sich in der Liste <span class="wintitle">Akzeptierter E-Mail-Domänenfilter</span> mindestens ein Eintrag befindet. </p> <p> <span class="uicontrol"> Akzeptierte E-Mail-Adresse und -Domänen</span>: Um einen IP-Adressbereich anzugeben, schließen Sie den Bereich in Klammern ein (z. B. <code>
       192.168.10.[20-240]
     </code>). You can also use wildcards (*) to specify any number from 0 to 255 (for example, 
     <code>
       192.168.[10-14].*
     </code>) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Benachrichtigung über Passwortwiederherstellung</span> </td> 
   <td colname="col2"> <p>Benachrichtigt die jeweiligen Administratoren, wenn ein Benutzer versucht, sein Kontopasswort zurückzusetzen. </p> <p> <span class="uicontrol"> Verfügbare Admins:</span> Es wird eine Liste sämtlicher Administratoren angezeigt. Halten Sie bei Bedarf beim Klicken die STRG- bzw. Umschalttaste gedrückt, um mehrere Administratoren gleichzeitig auszuwählen. </p> <p> <span class="uicontrol">E-Mail-Mitglieder</span>: Hiermit wird die aktuell definierte E-Mail-Gruppe angezeigt. </p> </td> 
  </tr> 
 </tbody> 
</table>

| Element | Beschreibung |
|--- |--- |
| Sichere Passwörter erforderlich | Erzwingt die Erstellung sicherer Passwörter, die folgende Regeln beachten: <ul><li>Muss mindestens acht Zeichen lang sein.</li><li>Muss zwischen dem ersten und dem letzten Zeichen mindestens ein Symbol-/Zahlenzeichen aufweisen.</li><li>Muss mindestens ein Alpha-Zeichen enthalten.</li><li>Darf nicht im Wörterbuch stehen oder Begriffe aus dem (englischen) Wörterbuch enthalten.</li><li>Darf nicht drei (3) aufeinanderfolgende Zeichen aus dem Anmeldenamen des Benutzers enthalten.</li><li>Muss sich von den vorhergehenden 10 Passwörtern unterscheiden.</li></ul>**Hinweis**: Diese Funktion wird bei neuen Kennwörtern in Zukunft erzwungen. Vorhandene Passwörter werden nicht überprüft, und die Benutzer werden auch nicht aufgefordert, ihre bisherigen Passwörter zu ändern. Daher sollten Sie in Erwägung ziehen, die Option Passwortablauf zu aktivieren und die Benutzer dazu zu zwingen, neue Passwörter nach den strengeren Passwortregeln festzulegen. |
| Passwortablauf | Erzwingt die regelmäßige Änderung des Kontopassworts durch den Benutzer. Sie können das Intervall festlegen, in dem die Kennwörter ablaufen, und den sofortigen Ablauf von Kennwörtern erzwingen. |
| IP-Anmeldebeschränkungen erzwingen | (Diese Funktion kann nicht zusammen mit der Experience Cloud-Anmeldung verwendet werden. Beachten Sie, dass diese Funktion ab Oktober 2020 nicht mehr verfügbar ist. [Mehr...](/help/admin/company/login-restrictions-eol.md))<br> Schränkt den Berichtzugriff auf bestimmte IP-Adressen oder IP-Adressbereiche ein. Sie können der Liste „IP-Adressenfilter“ bis zu 100 Einträge hinzufügen. Bei jedem Eintrag kann es sich um eine bestimmte Adresse oder einen Adressbereich handeln. Die Funktion IP-Anmeldebeschränkungen erzwingen wird nur erzwungen, wenn sich in der Liste „IP-Adressenfilter“ mindestens ein Eintrag befindet. Accepted IP Address: To specify an IP address range, enclose the range in brackets (for example, `192.168.10.[20-240]`). You can also use wildcards to specify any number from 0 to 255 (for example, `192.168.[10-14].*8) Failed logins are logged and viewable from the [Usage and Access Log](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/logs.html#section_6FBAF92D9EA244809C45A78A2F0A7232). |
| Erzwingen von E-Mail-Domänebeschränkungen | Filtert die E-Mail-Adressen und Domänen, an die Analytics Lesezeichen, herunterladbare Berichte und Warnhinweise sendet. Die E-Mail-Filterliste kann bis zu 100 Einträge lang sein. Jeder einzelne Eintrag steht für eine E-Mail-Adresse oder eine gesamte E-Mail-Domäne. Wenn ein terminierter Bericht als Zieladresse eine nicht genehmigte E-Mail-Adresse aufweist, versendet Analytics eine E-Mail-Benachrichtigung zu diesem Problem sowie einen Link zur Aufhebung der Berichtsplanung. **[!UICONTROL Die Funktion Erzwingen der E-Mail-Domänenbeschränkungen]** wird nur erzwungen, wenn sich in der Liste Akzeptierter E-Mail-Domänenfilter mindestens ein Eintrag befindet. **[!UICONTROL Akzeptierte E-Mail-Adresse und -Domänen]**: Um einen IP-Adressbereich anzugeben, fügen Sie den Bereich in eckigen Klammern ein (z. B. 192.168.10.[20-240]). You can also use wildcards to specify any number from 0 to 255 (for example, 192.168.[10-14].*) |
| Benachrichtigung über Passwortwiederherstellung | Benachrichtigt die jeweiligen Administratoren, wenn ein Benutzer versucht, sein Kontopasswort zurückzusetzen. **[!UICONTROL Verfügbare Admins:]** Es wird eine Liste sämtlicher Administratoren angezeigt. Halten Sie bei Bedarf beim Klicken die STRG- bzw. Umschalttaste gedrückt, um mehrere Administratoren gleichzeitig auszuwählen. **[!UICONTROL E-Mail-Mitglieder]**: Hiermit wird die aktuell definierte E-Mail-Gruppe angezeigt. |
