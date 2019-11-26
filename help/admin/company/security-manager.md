---
description: Ermöglicht das Steuern des Zugriffs auf Berichterstellungsdaten. Zu den Optionen gehören sichere Kennwörter, Kennwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen.
solution: Analytics
title: Sicherheits-Manager
topic: Admin tools
uuid: b3fbdba0-e2bf-4d67-92e3-ef05711141d4
translation-type: tm+mt
source-git-commit: 229ce50a24bd7b86e3859775bb4fbeba1c6a5668

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
   <td colname="col2"> <p>(Diese Funktion kann nicht zusammen mit der Experience Cloud-Anmeldung verwendet werden. Beachten Sie, dass diese Funktion ab Oktober 2020 nicht mehr verfügbar ist.) Schränkt den Berichtzugriff auf bestimmte IP-Adressen oder IP-Adressenbereiche ein. </p> <p>Sie können der Liste „IP-Adressenfilter“ bis zu 100 Einträge hinzufügen. Bei jedem Eintrag kann es sich um eine bestimmte Adresse oder einen Adressbereich handeln. </p> <p>  Die Funktion <span class="wintitle">IP-Anmeldebeschränkungen erzwingen</span> wird nur erzwungen, wenn sich in der Liste „IP-Adressenfilter“ mindestens ein Eintrag befindet. </p> <p> <span class="uicontrol"> Akzeptierte IP-Adresse</span>: Um einen IP-Adressbereich anzugeben, schließen Sie den Bereich in Klammern ein (z. B. <code>
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

## Ende der Lebensdauer für IP-Anmeldebeschränkungen [!UICONTROL erzwingen]

Die Funktion **[!UICONTROL IP-Anmeldebeschränkungen]** erzwingen ist eine Analytics-Funktion, mit der Sie bald ältere IP-Adressen freigeben können, die als sicher gelten, um eine erfolgreiche Anmeldung und den Zugriff auf Ihre Adobe Analytics-Umgebung zu ermöglichen. In vielen Fällen wird diese Funktion verwendet, um eine Unternehmens-IP-Adresse als einzige sichere IP-Adresse einzurichten, von der aus Benutzer sich anmelden können. Um Adobe Analytics verwenden zu können, müssen sich die Benutzer daher entweder in einer Firmenzentrale befinden oder sich über VPN im Netzwerk anmelden.

### Warum erwägen wir es für das Ende des Lebens?

Diese Funktion wird unter bestimmten Umständen durch die Migration der Experience Cloud-Anmeldung und/oder die Experience Cloud-Anmeldung unterbrochen. Es ist bekannt, dass es für Kunden mit **[!UICONTROL Kundenattributen]** oder **[!UICONTROL Zielgruppenbibliothek]** beschädigt wird.

Wenn Sie über mehrere Experience Cloud-Lösungen verfügen, können Sie diese Anforderung umgehen, indem Sie sich mit einer der anderen Lösungen bei der Experience Cloud anmelden, da diese Funktion außerhalb von Analytics selbst nicht vorhanden ist oder nicht unterstützt wird. Benutzer können dies auch über IP-Spoofing umgehen.

Schließlich verfügt Adobe über eine funktionierende und weitaus überlegene Alternativlösung mit Single-Sign-On- und Federated-IDs. Diese Funktion bietet Ihnen mehr Kontrolle und Sicherheit über die Anmeldeerfahrung Ihrer Benutzer.

### Wie wirkt sich das Entfernen dieser Funktion auf Sie aus?

Für alle Kunden, die IP-Anmeldebeschränkungen **[!UICONTROL erzwingen]** , wird diese Funktion im Oktober 2020 entfernt. Zu diesem Zeitpunkt werden noch geltende IP-Anmeldebeschränkungen nicht mehr erzwungen. Wenn Sie die Anmeldung weiterhin nach IP-Adresse beschränken müssen, sollten Sie die empfohlene Lösung für Single-Sign-On und Federated IDs (weitere Informationen und Ressourcen unten) überprüfen und implementieren.

Außerdem wird der Manager für IP-Anmeldebeschränkungen **** erzwingen aus der Benutzeroberfläche von Analytics unter **[!UICONTROLAdmin &gt; Unternehmenseinstellungen &gt; Sicherheitsmanager]** entfernt (siehe unten).

![](assets/sec-manager2.png)

### Welche anderen Optionen haben Sie?

Wie oben erläutert, wird diese Analytics-Funktion beendet. Damit Sie Zeit haben, SSO- und Federated IDs zu implementieren, haben wir das EOL-Datum auf Oktober 2020 verschoben.

Sowohl SSO- als auch Federated IDs sind überlegene Lösungen für die IP-Anmeldebeschränkung, die wir heute haben, und bieten Ihnen mehr Kontrolle, Sicherheit und Funktionen.

Informationen zum Einrichten von SSO/Federated IDs finden Sie in der folgenden Hilfedokumentation. Sie sollten diese gründlich lesen und mit Ihrer IT-Abteilung zusammenarbeiten, um sie implementieren zu können:

* [Single Sign-On und die Experience Cloud](https://spark.adobe.com/page/JeSB8EPEQIvjD/)
* [Admin-Konsole - Dokumentation zur Identitätseinrichtung](https://helpx.adobe.com/enterprise/using/set-up-identity.html)
* [Admin-Konsole - Lernprogramm zur Identitätseinrichtung (Video)](https://helpx.adobe.com/enterprise/how-to/identity-directories-domains.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&ref=helpx.adobe.com)
* [Übungen zur Konfiguration von Federated ID (Video)](https://helpx.adobe.com/enterprise/how-to/identity-configure-ids.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&ref=helpx.adobe.com)
* [Single-Sign-On - häufige Fragen](https://helpx.adobe.com/enterprise/using/sso-faq.html)
* [Von Adobe unterstützte Identitätstypen](https://helpx.adobe.com/enterprise/using/identity.html)

Wenn Sie weiterhin Ihre Unterstützung für IP-Anmeldebeschränkungen äußern und beantragen möchten, dass diese von Experience Cloud bereitgestellt wird, können Sie auf unserer [Forumsseite](https://forums.adobe.com/ideas/11648)für diese Funktion stimmen. Für weitere Fragen oder Informationen zu SSO/Federated IDs und dem EXC wenden Sie sich bitte an Ryan Monger (monger@adobe.com).
