---
description: Das müssen Sie über die Migration der Analytics-Benutzer-ID zur Admin Console in der Adobe Experience Cloud wissen.
seo-description: Das müssen Sie über die Migration der Analytics-Benutzer-ID zur Admin Console in der Adobe Experience Cloud wissen.
seo-title: Analytics-Benutzermigration zur Admin Console
title: Analytics-Benutzermigration zur Admin Console
uuid: 7d020713-693b-4945-aa52-3669a631aacb
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Analytics-Benutzermigration zur Admin Console{#analytics-user-migration-to-the-admin-console}

Das müssen Sie über die Migration der Analytics-Benutzer-ID zur Admin Console in der Adobe Experience Cloud wissen.

<!--
<p>FAQ <a href="https://wiki.corp.adobe.com/display/DMTM/Migration+FAQ" format="https" scope="external"> Source</a> </p>
-->

<!--
<p>Help publish link: <a href="https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/</a> </p>
<p>https://wiki.corp.adobe.com/display/analyticssolution/Migration+of+Analytics+Access+and+User+Management+to+the+Marketing+Cloud </p>
-->

Auf dieser Seite finden Sie folgende Informationen:

* [Was ist die Benutzer-ID-Migration?](../c-migration-tool/c-migration-tool.md#section-adbe49aba10c4e62afa836a97894107c)
* [Informationen vor der Migration von Benutzer-IDs (FAQ)](../c-migration-tool/c-migration-tool.md#section-b0fc7f0bbd4b488e95b0c8e77ff077a9)
* [Informationen während der Migration (FAQ)](../c-migration-tool/c-migration-tool.md#section-d394524aa6d046d79025bbd7499792bc)
* [Informationen nach der Migration (FAQ)](../c-migration-tool/c-migration-tool.md#section-9681baa01b8c41cdb9659b73b70b50ff)
* [Nicht unterstützte Analytics-Funktionen in der Admin Console](../c-migration-tool/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56)
* [Benachrichtigung der Benutzer über die Migration](../c-migration-tool/c-migration-tool.md#section-f3b25f672a3a4d03b0559656fd99d20a)

Generelle Hilfestellung zu Admin Console-Themen (nicht in Bezug auf die Analytics-Migration) finden Sie im [Admin Console-Benutzerhandbuch](https://helpx.adobe.com/enterprise/administering/user-guide.html).

Nach der Migration können Sie[Benutzer und Produkte der Experience Cloud](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/) in der Admin Console verwalten.

## Was ist die Migration der Analytics-Benutzer-ID? {#section-adbe49aba10c4e62afa836a97894107c}

Die Migration der Analytics-Benutzer-ID ermöglicht es Administratoren, Benutzerkonten einfach vom Analytics User Management zur Adobe Admin Console zu migrieren. Nachdem Sie Ihre Benutzer migriert haben, erhalten diese Zugang zu den Lösungen und Services, die in der Experience Cloud verfügbar sind. Die Migration erfolgt für Kunden stufenweise.

Vorteile der Verwendung der Admin Console sind unter anderem:

<table id="table_E4465796E224474680D750CAC5434ED3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vorteil </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Single Sign-on </p> </td> 
   <td colname="col2"> <p>Analytics-Benutzer können sich bei der Experience Cloud und allen Lösungen mit der Adobe ID oder Enterprise ID anmelden. Durch diese Anmeldung erhalten sie Zugriff auf integrierte Lösungen und Hauptdienste in der Experience Cloud. </p> <p>After the migration, users who attempt to sign in via legacy logins (<span class="filepath"> my.omniture.com</span> and <span class="filepath"> sc.omniture.com</span>) are redirected to <span class="filepath"> experiencecloud.adobe.com</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzeridentität und -berechtigungen verwalten </p> </td> 
   <td colname="col2"> <p>Analytics-Administratoren können Benutzer und Berechtigungen ausschließlich in der <a href="http://adminconsole.adobe.com/enterprise/" format="http" scope="external">Admin Console</a> (http://adminconsole.adobe.com/enterprise/) verwalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Produkte und zentrale Dienste verwalten </p> </td> 
   <td colname="col2"> 
    <ul id="ul_01043FEF271E4B27BF34980D629D1932"> 
     <li id="li_DC31AE8BAAB843F39A7CC9EB047265D5">Neue Benutzer einladen </li> 
     <li id="li_73724DD7D79E41F8A1D58C74E37674BA">Produktprofile anlegen </li> 
     <li id="li_7E75FC68E0F84873A9A211D2707B6DE7">Benutzerberechtigungen für bestimmte Produkte und Dienstleistungen erteilen </li> 
     <li id="li_9C8A340A7C9A45A98EC0BD4AF9E100FF">Sichern Sie sich Zugriff auf die <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/solutions_capability_names.html" format="html" scope="external">lösungsübergreifenden Hauptdienste</a> der Adobe Experience Cloud </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Informationen vor der Migration von Benutzer-IDs (FAQ) {#section-b0fc7f0bbd4b488e95b0c8e77ff077a9}

Antworten auf Fragen, die Sie vielleicht vor der Migration haben

<table id="table_36FD7EF1DAB44D359F4FC186D93147E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage/Aufgabe </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ich bin ein Analytics-Administrator und habe vor der Migration eine E-Mail erhalten. Was muss ich als Erstes tun? </p> </td> 
   <td colname="col2"> <p>Stellen Sie sicher, dass Sie über eine Adobe ID und Zugriff auf die <a href="https://adminconsole.adobe.com/enterprise/" format="https" scope="external">Experience Cloud Admin Console</a> verfügen. </p> <p>Wenden Sie sich andernfalls an die <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html" format="html" scope="external">Adobe-Kundenunterstützung</a>. (Sie sollten sich zunächst an Ihren System- oder Produktadministrator wenden, um eine Einladung zum entsprechenden Unternehmen zu erhalten.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Integrationen von AEM mit Analytics </p> </td> 
   <td colname="col2"> <p> AEM-Benutzer mit einer Integration in Analytics müssen ihre Konfiguration ändern, um den gemeinsam genutzten geheimen Schlüssel von Analytics anstelle des Passworts zu verwenden. </p> <p> Dies sollten Sie tun, bevor die Migration aktiviert wird. Sobald die Migration deaktiviert ist, ist das ursprünglich konfigurierte Passwort nicht mehr gültig. </p> <p><b>So erhalten Sie den gemeinsam genutzten geheimen Schlüssel von Analytics</b> </p> <p> Der gemeinsam genutzte geheime Schlüssel kann von Analytics (<span class="uicontrol">Analytics</span> &gt; <span class="uicontrol">User Management</span>) bezogen werden und ist für jeden Benutzer unterschiedlich. </p> <p><b>So aktualisieren Sie Ihre AEM-Konfiguration mit dem gemeinsam genutzten geheimen Schlüssel</b> </p> <p>Vgl.<a href="https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/adobeanalytics-connect.html" format="html" scope="external">Verbinden mit Adobe Analytics und Creating Frameworks</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Builder aktualisieren </p> </td> 
   <td colname="col2"> <p> <p>Wichtig: Aktualisieren Sie Ihre Installation von <a href="https://marketing.adobe.com/resources/help/en_US/arb/t_install_arb.html" format="html" scope="external">Report Builder</a> auf die neueste Version. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wann beginnt die Migration? </p> </td> 
   <td colname="col2"> <p>Analytics-Administratoren erhalten von Adobe eine E-Mail mit Angaben dazu, wann die Migration beginnt. </p> <p>Migrationen zur Admin Console werden in Schüben durchgeführt. Am Tag der Migration werden Analytics-Administratoren von Adobe benachrichtigt und erhalten Zugriff auf das Migrationswerkzeug. Wenn ein angemeldetes Unternehmen die Kriterien des jeweiligen Migrationsschubs erfüllt, führt Adobe Folgendes durch: </p> 
    <ul id="ul_D7DDC62A08AB4407B122985EDEA6ABD1"> 
     <li id="li_BA0AD50DCDC14C90ADD513DEF6F78180">Festlegen von Start- und Enddatum für die Migration </li> 
     <li id="li_C048A5C64FAA46C4BB41EF24F1CEDF62">ca. 30 Tage vor der Migration Senden einer E-Mail-Benachrichtigung an die aktuellen Analytics-Administratoren des Unternehmens </li> 
     <li id="li_476265B24CE2404B995201170C75D674">Anzeige einer Benachrichtigung für Administratoren im Produkt selbst zum Startdatum der Migration </li> 
    </ul> <p> Am Tag der Migration werden Ihre vorherigen Berechtigungsgruppen automatisch in die Admin Console kopiert. Sie können dann in den Analytics Admin Tools keine Benutzer mehr einladen oder neue Gruppen erstellen. </p> <p>Nach der Migration: </p> 
    <ul id="ul_4639963EB08F407F8C18ACE2B3D30223"> 
     <li id="li_7F24A3FC900146C3B2E988D399C859EA">Administratoren verwenden die Admin Console zur Verwaltung der Analytics-Benutzer und -Berechtigungen. (Sie verwenden nicht mehr die Benutzeroberfläche zur Verwaltung unter Analytics &gt; Admin &gt; User Management.) </li> 
     <li id="li_5B5234D4F94A4B96A8920F6A5831A64C">Benutzer greifen mit ihrer Adobe oder Enterprise ID über die Experience Cloud auf Analytics zu, statt über <span class="filepath">my.omniture.com</span>. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was geschieht am Startdatum der Migration? </p> </td> 
   <td colname="col2"> <p>Um 10:00 Uhr UTC am Startdatum der Migration: </p> 
    <ul id="ul_25D1DBDF5C804D048E741F31550FF5F3"> 
     <li id="li_418476105FE341229CE146E730AAB33D">Ihre in Analytics vorhandenen Berechtigungsgruppen werden automatisch in der Admin Console als Produktprofile repliziert, inklusive ihrer Beschreibungen und granularen Berechtigungen in verschiedenen Report Suites, Metriken, Analytics und Report Suite-Werkzeugen. </li> 
     <li id="li_412F88C454B0455A8F3BC8016226855C">Wurde ein aktueller Analytics-Besucher in der Admin Console erstellt (also mit verknüpfter Adobe/Enterprise ID), wird dieser dem entsprechenden Produktprofil in der Admin Console hinzugefügt. </li> 
     <li id="li_8A05137EC05C4FD5910E73FE58300DCB">Der Abschnitt zum User Management auf der Admin-Registerkarte wird <span class="term"> schreibgeschützt</span>. Sie werden nicht mehr in der Lage sein, neue Benutzer oder Berechtigungsgruppen hier zu erstellen, und müssen diese Funktionen über die Admin Console nutzen. Weitere Informationen dazu finden Sie unter <a href="../c-migration-tool/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56" format="dita" scope="local">Nicht unterstützte Analytics-Funktionen in der Admin Console</a>. </li> 
     <li id="li_2742DE69E9B547198A58E1F33E908361">Als Administrator erhalten Sie Zugriff auf das [Benutzer-ID-Migrationswerkzeug] (https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/t_migrate-users.html). Außerdem erscheint im Produkt selbst eine Benachrichtigung, die das Enddatum der Migration (in der Regel 60 Tage später) sowie Links zu Hilfeinhalten und FAQs enthält. </li> 
     <li id="li_095D42E3A3544FC59A60A8C8F94C971B">Sie erhalten Zugriff auf eine „Berechtigungen“-Registerkarte in der Admin Console, über die Sie Produktprofile mit allen granularen Optionen erstellen können, die Sie aus Analytics kennen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wie funktioniert die Migration von Benutzer-IDs? </p> </td> 
   <td colname="col2"> <p> Click <a href="../c-migration-tool/t-migrate-users.md#task-f3355f3b14a340feae58cfa04c0ba1c9" format="dita" scope="local"> Migrate User IDs</a> on the Admin page, under User Management. Verwenden Sie das Tool, um Benutzer zu Produktprofilen in der Admin Console hinzuzufügen (repliziert aus Berechtigungsgruppen in Analytics). Sie können Benutzer-IDs ganz nach Ihren Wünschen migrieren. </p> <p>Dazu sind Administrationsberechtigungen erforderlich. Nach Abschluss der Migration kann diese nicht rückgängig gemacht werden. </p> <p>Am Enddatum der Migration wird der Zugriff auf <span class="filepath">my.omniture.com</span> für Benutzer innerhalb ihres angemeldeten Unternehmens deaktiviert. Users (including those that are yet to be migrated) will be redirected to login via the new Experience Cloud URL (<span class="filepath"> experiencecloud.adobe.com</span>) </p> <p>Hinweis: Adobe empfiehlt, vor der Migration die Gelegenheit für eine Prüfung Ihrer Benutzer und Gruppen zu nutzen. Löschen Sie alte und nicht verwendete Konten sowie solche, die keinen Zugriff mehr auf das Produkt haben sollten (z. B. Mitarbeiter, die nicht mehr im Unternehmen arbeiten). </p> <p>Related topic: <a href="../c-migration-tool/migrate-enterprise.md#topic-6fd22bc6fbc14fd69ce6a8518a5b9c00" format="dita" scope="local"> Migrate Analytics user accounts for Enterprise and Federated IDs</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wirkt sich die Migration auf meine Analytics-Implementierung oder darauf aus, wie Daten erfasst werden? </p> </td> 
   <td colname="col2"> <p>Nein. </p> <p>Das Migrationswerkzeug dient der Erleichterung Ihrer Übertragung von IDs und Berechtigungen aus dem Analytics User Management in die <a href="https://adminconsole.adobe.com/enterprise/" format="https" scope="external">Experience Cloud Admin Console</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wie viel Zeit nimmt die Migration in Anspruch? </p> </td> 
   <td colname="col2"> <p>Alle aktuellen Analytics-Administratoren erhalten vier Wochen vor der Migration eine entsprechende Benachrichtigungs-E-Mail. (Das tatsächliche Startdatum wird in der Analytics-Oberfläche angezeigt.) </p> <p>Bei Migrationsstart haben Administratoren 60 Tage Zeit, um den Prozess abzuschließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich die Migration beschleunigen? </p> </td> 
   <td colname="col2"> <p>Ja. Allerdings empfiehlt Adobe, die Zeit vor dem Migrationsstart für Folgendes zu nutzen: </p> 
    <ul id="ul_52C7EC44A5534975BFD7A6F37A829C25"> 
     <li id="li_8CFFF72877E8456DAC3241143AD648AD">Stellen Sie sicher, dass Sie ein Analytics-Produktadministrator in der Admin Console sind </li> 
     <li id="li_25DAA8D1EEDA45A0B5B59472BD8896C4">Benachrichtigen Sie Ihre Benutzer, dass sich der Anmeldeprozess beim Migrationsstart ändert. </li> 
     <li id="li_5B50F942F6A8483FAFA500AFF428702C">Prüfen Sie Ihre aktuellen Benutzer und Berechtigungen und führen Sie verschiedene Bereinigungsaktivitäten durch. </li> 
    </ul> <p>Wenden Sie sich zur Beschleunigung der Migration an Ihren Customer Success Manager bei der <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html" format="html" scope="external">Adobe-Kundenunterstützung</a> und beantragen Sie ein früheres Startdatum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ich bin ein Analytics-Administrator ohne Zugriff auf die Admin Console. Wie erhalte ich Zugriff darauf? </p> </td> 
   <td colname="col2"> <p>Alle System- oder Produktadministratoren, die Zugriff auf die Admin Console Ihres Unternehmens haben, können Ihnen Zugriff gewähren. Wenn Sie sich nicht sicher sind, wer in Ihrem Unternehmen über Administratorberechtigungen in der Konsole verfügt, wenden Sie sich an die <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html" format="html" scope="external">Adobe-Kundenunterstützung</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich das Startdatum der Migration verschieben? </p> </td> 
   <td colname="col2"> <p>Ja. Wenden Sie sich an die <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html" format="html" scope="external">Adobe-Kundenunterstützung</a>. </p> 
    <draft-comment> 
     <p>Eine Beschreibung der Änderungen am aktuellen Analytics-Benutzer- und -Berechtigungsverwaltungsdatum finden Sie unten. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mein Unternehmen migriert nun zur Admin Console. Wo erstelle ich jetzt Benutzer und Berechtigungsgruppen vor dem Start der Migration? </p> </td> 
   <td colname="col2"> <p>Vor dem Startdatum der Migration können Sie Benutzer in der Admin Console oder unter Analytics &gt; User Management erstellen. </p> <p>Nach Beginn der Migration können Sie Benutzer und Berechtigungsgruppen nur noch in der Admin Console erstellen. </p> 
    <draft-comment> 
     <p>Weitere Informationen dazu, was am Startdatum der Migration geschieht, finden Sie im Abschnitt Migration weiter unten. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wann kann ich Single Sign-on mit Federated IDs implementieren? </p> </td> 
   <td colname="col2"> <p> In Kürze wird in der Admin Console ein Werkzeug zur Verfügung stehen, mit dem Sie ID-Typen von Adobe IDs in Federated IDs ändern können. Während der Migration können Sie keine Benutzer als Federated IDs migrieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Informationen während der Migration (FAQ) {#section-d394524aa6d046d79025bbd7499792bc}

Wichtige Informationen zum Migrationsprozess und dazu, welche Auswirkungen dieser auf das aktuelle User Management hat.

<table id="table_0E37BB1DEA6143F0B5F4E861FCFA7189"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Wie werden Berechtigungsgruppen in der Admin Console repliziert? Was geschieht mit meinen Benutzern? </p> </td> 
   <td colname="col2"> <p>Eine migrierte Analytics-Gruppe wird in der Admin Console <i>Produktprofil</i> genannt. Die Berechtigungseinstellungen der ursprünglichen Gruppe werden bei der Migration beibehalten. Allerdings werden die Benutzer, die der Gruppe zugewiesen sind, nicht migriert. Wenn ein Benutzer, der zu dieser Gruppe gehört, mit dem Migrationstool migriert wird, wird dieser Benutzer diesem Produktprofil zugeordnet. </p> <p>Beispielsweise wird eine West Coast Operations-Berechtigungsgruppe, deren Mitglieder über Berechtigungen für Report Builder und Analysis Workspace (mit bestimmten Report Suites, Metriken und Dimensionen) verfügen, zu einem West Coast Operations-Produktprofil. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich die Migration an einen anderen Administrator delegieren? </p> </td> 
   <td colname="col2"> <p>Sobald die Migration beginnt, können alle Administratoren, die über die Experience Cloud auf Ihre Analytics-Instanz zugreifen, das Migrationswerkzeug verwenden, um die Migration von Benutzern zu starten (oder fortzusetzen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich die Zugehörigkeit zu einer Berechtigungsgruppe für nicht migrierte Benutzer aktualisieren? </p> </td> 
   <td colname="col2"> <p>Ja. Sie können die Zugehörigkeit zu einer Gruppe für nicht migrierte Benutzer über das Analytics User Management ändern. </p> 
    <draft-comment> 
     <p>In Erwartung einer Klarstellung von Ashok, wo das geschieht. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich nach Beginn der Migration Benutzer und Berechtigungsgruppen in Analytics erstellen und sie dann mit dem Migrationswerkzeug in die Admin Console migrieren? </p> </td> 
   <td colname="col2"> <p> Nein. Nach dem Beginn der Migration müssen alle Benutzer und Berechtigungsgruppen („Produktprofile“ in der Admin Console) in der Admin Console erstellt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Erhalten Benutzer, die ich mithilfe des Migrationswerkzeugs migriere, dieselben Berechtigungen wie in Analytics? </p> </td> 
   <td colname="col2"> <p>Ja. Benutzer, die mithilfe des Werkzeugs migriert werden, erhalten die Berechtigungen, über die sie derzeit in Analytics verfügen. Außerdem haben sie auch weiterhin Zugriff auf ihre Analytics-Assets (wie Segmente, Projekte, berechnete Metriken usw.), wenn sie über die Experience Cloud auf Analytics zugreifen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Haben Benutzer, die ich in die Admin Console migriere, weiterhin Zugriff auf Analytics über <span class="filepath">my.omniture.com</span>? </p> </td> 
   <td colname="col2"> <p>Ja. Migrierte Benutzer können bis zum Enddatum der Migration mit ihrem bisherigen Benutzernamen und Passwort über <span class="filepath">my.omniture.com</span> auf Analytics zugreifen, außer Sie deaktivieren den Zugriff mit den bisherigen Anmeldedaten über das Migrationswerkzeug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Für mindestens zwei meiner Benutzer ist in ihren Analytics-Aufzeichnungen dieselbe E-Mail-ID hinterlegt. Was geschieht, wenn ich sie migriere? </p> </td> 
   <td colname="col2"> <p>Da für Benutzerkonten in der Admin Console einzigartige E-Mail-IDs erforderlich sind, wird der Fehler „Doppelte E-Mail-ID“ ausgegeben, wenn Sie mehr als einen dieser Benutzer migrieren. Sie können die E-Mail-IDs nicht migrierter Benutzer vor einem erneuten Migrationsversuch im (bisherigen) User Management aktualisieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Was mache ich nach der Migration meiner Benutzer? </p> </td> 
   <td colname="col2"> <p>Deaktivieren Sie den Zugriff mit den bisherigen Anmeldedaten für <span class="filepath">my.omniture.com</span>. Sie können die bisherigen Anmeldedaten nicht deaktivieren, wenn Benutzer nicht migriert wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich den Migrationsprozess nachverfolgen? </p> </td> 
   <td colname="col2"> <p>Im Migrationswerkzeug ist ein Dashboard enthalten, in dem angezeigt wird, wie viele Ihrer Benutzer erfolgreich migriert wurden und für wie viele die bisherigen Anmeldedaten deaktiviert wurden. </p> <p> Idealerweise haben Sie Ihr angemeldetes Unternehmen erfolgreich in die Admin Console migriert, wenn die Migration für 100 % Ihrer Benutzer abgeschlossen wurde und ihre bisherigen Anmeldedaten deaktiviert wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ich muss während der Migration Benutzer und Berechtigungen verwalten. Welches Werkzeug kann ich dafür verwenden? </p> </td> 
   <td colname="col2"> <p>Nach dem Beginn der Migration verwenden Sie die Admin Console zur Erstellung und Verwaltung neuer Benutzer und Produktprofile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was geschieht für meine Benutzer, wenn ich die Migration mithilfe des Werkzeugs durchführe? </p> </td> 
   <td colname="col2"> <p>Ihnen wird eine Willkommensnachricht an die E-Mail-ID gesendet, die in ihren Analytics-Benutzeraufzeichnungen hinterlegt ist. Darin werden sie über die neue Zugriffsmethode für Analytics über die Experience Cloud informiert. Wenn sie noch nicht über eine Adobe ID verfügen, werden sie dazu aufgefordert, eine zu erstellen. Danach können sie mit ihrer Adobe ID auf die Lösung zugreifen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich statt des Migrationswerkzeugs APIs für die Migration meiner Benutzer verwenden? </p> </td> 
   <td colname="col2"> <p>Nein. Sie müssen das Migrationswerkzeug verwenden, um sicherzustellen, dass alle Ihre vorhandenen Benutzer in die Admin Console migriert werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Welche Analytics-Funktionen zum User Management sind in der Admin Console nicht verfügbar? </p> </td> 
   <td colname="col2"> 
    <ul id="ul_3F3747D4C1D3420699F7D28EC0CA1AA0"> 
     <li id="li_BD943B3245FF47E7A0DDA6107EA1EF89">Asset-Übertragung </li> 
     <li id="li_2DF7004D67ED4C6CB40461EEFB038A5A">Benutzergültigkeit </li> 
     <li id="li_980E3F5B98F344A492B0EBAD7F1DA60C">Benutzerprotokolle </li> 
    </ul> <p>Diese stehen Ihnen im Analytics User Management weiterhin zur Verfügung. </p> <p>Weitere Informationen dazu finden Sie unter <a href="../c-migration-tool/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56" format="dita" scope="local">Nicht unterstützte Analytics-Funktionen in der Admin Console</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wir haben verschiedene Konfigurationen in der Admin Console erstellt und sie Analytics-Berechtigungsgruppen zugeordnet. Was geschieht bei Migrationsbeginn mit diesen Konfigurationen? </p> </td> 
   <td colname="col2"> <p>Analytics-Berechtigungsgruppen werden in der Admin Console als Produktprofile wiederhergestellt, ebenso wie alle anderen Gruppen. Daher werden Ihnen in der Konsole zwei Produktprofile angezeigt, die grundlegend doppelte Berechtigungen aufweisen. Sie können doppelte Produktprofile über die Admin Console löschen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was ist der nächste Schritt nach der Migration von Benutzern? </p> </td> 
   <td colname="col2"> <p>Wenn Sie einen Benutzer oder einen Benutzersatz migriert haben, besteht der nächste Schritt in der Deaktivierung der bisherigen Anmeldedaten über <span class="filepath">my.omniture.com</span>. Wählen Sie dazu die entsprechenden Benutzer im Migrationswerkzeug aus und klicken Sie auf die Kontextoption „Bisherige Anmeldedaten deaktivieren“, die oben im Fenster erscheint. Diese Option wird nur angezeigt, wenn Sie einen Benutzer oder einen Benutzersatz auswählen, der erfolgreich in die Admin Console migriert wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was geschieht am Enddatum der Migration? </p> </td> 
   <td colname="col2"> <p>Nach dem Enddatum (60 Tage nach dem Startdatum) der Migration werden alle Benutzer in Ihrem angemeldeten Unternehmen zur Anmeldung mit ihren Adobe IDs über die Experience Cloud-Anmeldeseite weitergeleitet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ich konnte nicht alle meine Benutzer bis zum Enddatum der Migration migrieren. Verlieren nicht migrierte Benutzer ihren Zugriff auf Analytics? </p> </td> 
   <td colname="col2"> <p>Benutzer, die nicht bis zum Enddatum migriert wurden, werden zur Experience Cloud-Anmeldeseite (experience.adobe.com) umgeleitet und können nicht auf Analytics zugreifen. Allerdings haben Sie weiterhin Zugriff auf das Migrationswerkzeug. So können Sie die entsprechenden Benutzer finden und ihren Zugriff wiederherstellen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Informationen nach der Migration (FAQ) {#section-9681baa01b8c41cdb9659b73b70b50ff}

<table id="table_F48CC9DFE3424AC9AD76A16882701C8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage/Problem </th> 
   <th colname="col2" class="entry"> Antworten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Löschen von Benutzern aus der Admin Console </p> </td> 
   <td colname="col2"> <p> In Analytics wird ein gelöschter Benutzer als <span class="term"> expired</span>, but the account continues to exist. Die Kontoerhaltung ermöglicht die Übertragung von Assets wie Segmenten, berechneten Kennzahlen, terminierten Berichten, Projekten usw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kontogültigkeit </p> </td> 
   <td colname="col2"> <p> Sie können in Analytics in den Admin Tools manuell ein Ablaufdatum für ein Konto festlegen. Sobald das Ablaufdatum erreicht ist, kann der Benutzer nicht mehr auf Analytics zugreifen, aber sein aktuelles Experience Cloud-Benutzerkonto (z. B. Adobe ID, Enterprise ID, Federated ID usw.) behält Gültigkeit. Er kann sich immer noch in die Experience Cloud einloggen, kann aber in Analytics keine Klicks mehr ausführen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nicht unterstützte Analytics-Funktionen in der Admin Console {#section-928ffba27a0446e0af575b720434ef56}

>[!IMPORTANT]
>
>Überprüfen Sie die folgenden Probleme, die während der Migration für Sie zutreffen können.

<table id="table_88E2FA03D5F241B79AB54D12F64B51DA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage/Problem </th> 
   <th colname="col2" class="entry"> Antworten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Anmeldung als </p> </td> 
   <td colname="col2"> <p> Admins, die zur Admin Console migrieren, können die Funktion „Anmeldung als“ nicht mehr für den Zugriff auf Nicht-Admin-Benutzerkonten verwenden, die in die Admin Console migriert wurden. Diese Funktion ist in Analytics nicht vorhanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzergültigkeit und Asset-Übertragung </p> </td> 
   <td colname="col2"> <p> In der Admin Console werden Benutzergültigkeit und Asset-Übertragung nicht unterstützt. Admins verwenden für beide Funktionen den Abschnitt „Analytics-Benutzer und Assets“ in den Admin Tools in Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Letzter Zugriff (Letzte Anmeldung) </p> </td> 
   <td colname="col2"> <p> Details zum letzten Anmeldedatum und zur letzten Anmeldezeit eines Benutzers sind unter dem Link „Analytics-Benutzer und Assets“ und nicht in der Admin Console verfügbar. Das Datum der letzten Anmeldung in Analytics ist spezifisch für den Zeitpunkt, zu dem Benutzer tatsächlich von Experience Cloud aus auf Analytics zugegriffen haben, und gibt nicht das Datum/die Uhrzeit der Anmeldung bei der Experience Cloud an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>User Management-APIs – <a href="https://helpx.adobe.com/enterprise/help/identity.html" format="html" scope="external">von Adobe unterstützte Identitätstypen</a> </p> </td> 
   <td colname="col2"> <p> Admins, die zur Admin Console migrieren, sollten von Adobe I/O angebotene <a href="https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html" format="html" scope="external">User Management-APIs</a> konfigurieren, um programmgesteuerten Zugriff auf Benutzerkonten in der Admin Console zu erhalten. </p> <p>Die Analytics-Berechtigungs-APIs werden deaktiviert, wenn die Migration für Sie aktiviert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Web-Service-Zugriffsberechtigungen </p> </td> 
   <td colname="col2"> <p> Die Web-Service-Zugriffsberechtigungen für Benutzer (und ihr gemeinsam genutzter geheimer Schlüssel) sind nicht in der Admin Console verfügbar. Auf sie kann durch Klick auf die spezifischen Benutzer im Abschnitt „Analytics-Benutzer und Assets“ zugegriffen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Single Sign-on </p> </td> 
   <td colname="col2"> <p> Analytics Single Sign-on-Konfigurationen werden entfernt, wenn Sie die Migration abgeschlossen haben. Sie bleiben während der Migration aktiv. Kunden, die Analytics Single Sign-on verwenden, sollten ein Upgrade auf <a href="https://helpx.adobe.com/enterprise/help/identity.html" format="html" scope="external">Adobe Federated ID</a> durchführen. </p> <p>Analytics empfiehlt, dass Sie Ihre Benutzer zunächst als Adobe IDs migrieren, um Experience Cloud-Konten einfach zu erstellen, und diese Konten dann in Federated Single Sign-on-Benutzer konvertieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Herunterladen von Berechtigungsgruppen </p> </td> 
   <td colname="col2"> <p> Das Herunterladen von Informationen zu Berechtigungsgruppen wird nicht mehr in den Analytics Admin Tools und der Adobe Admin Console unterstützt. Kunden können die adobe.io-User Management-APIs verwenden, um Informationen zu Berechtigungsgruppen in großen Mengen zu erhalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Erstellungsdatum des Kontos </p> </td> 
   <td colname="col2"> <p>Informationen zum Erstellungsdatum des Kontos werden in den Analytics Admin Tools und der Adobe Admin Console nicht mehr unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Massen-E-Mail </p> </td> 
   <td colname="col2"> <p>Massen-E-Mails an Benutzer werden weiterhin weder in der Analytics Admin Console noch in der Adobe Admin Console unterstützt. Kunden können Benutzer-E-Mail-Adressen in großen Mengen aus der Adobe Admin Console exportieren und E-Mails anhand eines beliebigen E-Mail-Clients senden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Benachrichtigung der Benutzer über die Migration {#section-f3b25f672a3a4d03b0559656fd99d20a}

Sie sollten Ihre aktuellen Benutzer über diesen Migrationsplan proaktiv benachrichtigen. Es folgt eine Vorlage, die Sie anpassen und an all Ihre aktuellen Analytics-Benutzer senden können:

To email all users, navigate to **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL User Management]** &gt; [Email Users](https://marketing.adobe.com/resources/help/en_US/reference/t_email_users.html).

**Betreff:** In Kürze: Eine neue Anmeldeart für Adobe Analytics und die Adobe Experience Cloud

** Haupttext:** Hallo Adobe Analytics-Benutzer!

Our company will begin migrating all Adobe Analytics accounts away from [!DNL https://my.omniture.com/login/] to Adobe Experience Cloud ([experiencecloud.adobe.com](http://experiencecloud.adobe.com/)). Mit dieser Migration erhält Ihr Adobe Analytics-Konto ein Upgrade, um den Zugriff auf Analytics über die Adobe Experience Cloud zu ermöglichen. Zwar ändert sich die Zugriffsmethode auf Analytics, doch alle Ihre vorhandenen Berechtigungen für Ihre Report Suites und Werkzeuge bleiben bestehen.

** Nächste Schritte:** Wir beginnen mit der Migration von Benutzern, beginnend mit <INSERT DATE>. Sie erhalten eine Willkommensnachricht mit Ihren neuen Anmeldedaten an die E-Mail-ID, die in Ihrem Analytics-Konto hinterlegt ist. Wenn Sie keine [Adobe ID](https://helpx.adobe.com/x-productkb/global/adobe-id-account-change.html) mit Ihrer E-Mail-Adresse verknüpft haben, werden Sie dazu aufgefordert, ein solches Konto einzurichten.

**Hilfreiche Ressourcen:**

[Anmelden und Profileinstellungen verwalten](https://marketing.adobe.com/resources/help/en_US/mcloud/getting-started-experience-cloud.html).

[Informationen zu Hauptdiensten und Lösungen](https://marketing.adobe.com/resources/help/en_US/mcloud/solutions_capability_names.html) in der Experience Cloud

Wenden Sie sich bei Fragen oder Bedenken an Ihre Analytics-Administratoren.

Mit freundlichen Grüßen

Analytics-Admin
