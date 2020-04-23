---
description: Das müssen Sie über die Migration der Analytics-Benutzer-ID zur Admin Console in Adobe Experience Cloud wissen.
title: Analytics-Benutzermigration zur Admin Console
uuid: 7d020713-693b-4945-aa52-3669a631aacb
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# Analytics-Benutzermigration zur Admin Console {#analytics-user-migration-to-the-admin-console}

Das müssen Sie über die Migration der Analytics-Benutzer-ID zur Admin Console in Adobe Experience Cloud wissen.

Allgemeine Hilfe zu Themen in der Admin-Konsole (die nicht mit der Analytics-Migration in Zusammenhang stehen) finden Sie im [Admin-Konsole Benutzerhandbuch](https://helpx.adobe.com/de/enterprise/administering/user-guide.html).

Nach der Migration können Sie [Benutzer und Produkte der Experience Cloud](https://docs.adobe.com/content/help/de-DE/core-services/interface/manage-users-and-products/admin-getting-started.html) in der Admin Console verwalten.

## Was ist die Migration der Analytics-Benutzer-ID? {#section-adbe49aba10c4e62afa836a97894107c}

Mit der Migration der Analytics-Benutzer-ID können Administratoren Benutzerkonten in Analytics User Management einfach in die Adobe Admin Console migrieren. Nachdem Ihre Benutzer migriert wurden, haben sie Zugriff auf die in der Experience Cloud verfügbaren Lösungen und Hauptdienste. Die Migration wird in Phasen an Kunden durchgeführt.

Die Vorteile der Verwendung der Admin-Konsole sind unter anderem:

<table id="table_E4465796E224474680D750CAC5434ED3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vorteil </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Single Sign-On </p> </td> 
   <td colname="col2"> <p>Analytics-Benutzer können sich mit ihrer Adobe ID oder Enterprise ID bei der Experience Cloud und allen Lösungen anmelden. Diese Anmeldung ermöglicht den Zugriff auf integrierte Lösungen und Hauptdienste in der Experience Cloud. </p> <p>Nach der Migration werden Benutzer, die versuchen, sich über die bisherigen Anmeldedaten anzumelden (<span class="filepath">my.omniture.com</span> und <span class="filepath">sc.omniture.com</span>), an <span class="filepath">experiencecloud.adobe.com</span> weitergeleitet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzeridentität und -berechtigungen verwalten </p> </td> 
   <td colname="col2"> <p>Analytics-Administratoren können Benutzer und Berechtigungen ausschließlich in der <a href="http://adminconsole.adobe.com/enterprise/">Admin Console</a> (http://adminconsole.adobe.com/enterprise/) verwalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Produkte und Hauptdienste verwalten </p> </td> 
   <td colname="col2"> 
    <ul id="ul_01043FEF271E4B27BF34980D629D1932"> 
     <li id="li_DC31AE8BAAB843F39A7CC9EB047265D5">Neue Benutzer einladen </li> 
     <li id="li_73724DD7D79E41F8A1D58C74E37674BA">Erstellen von Profilen </li> 
     <li id="li_7E75FC68E0F84873A9A211D2707B6DE7">Gewähren Sie Benutzern Zugriff auf bestimmte Produkte und Dienste </li> 
     <li id="li_9C8A340A7C9A45A98EC0BD4AF9E100FF">Zugriff auf <a href="https://docs.adobe.com/content/help/de-DE/core-services/interface/experience-cloud.html">lösungsübergreifende Core Services</a> von Adobe Experience Cloud </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Informationen vor der Migration von Benutzer-IDs (FAQ) {#section-b0fc7f0bbd4b488e95b0c8e77ff077a9}

Antworten auf Fragen, die Sie vielleicht vor der Migration haben.

<table id="table_36FD7EF1DAB44D359F4FC186D93147E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage/Aufgabe </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ich bin Analytics-Administrator und habe eine E-Mail vor der Migration erhalten. Was mache ich zuerst? </p> </td> 
   <td colname="col2"> <p>Stellen Sie sicher, dass Sie über eine Adobe ID und Zugriff auf die <a href="https://adminconsole.adobe.com/enterprise/">Experience Cloud Admin Console</a> verfügen. </p> <p>Wenden Sie sich andernfalls an die <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html">Adobe-Kundenunterstützung</a>. (Sie sollten sich zunächst an Ihren System- oder Produktadministrator wenden, um eine Einladung zur entsprechenden Organisation zu erhalten.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AEM-Integrationen mit Analytics </p> </td> 
   <td colname="col2"> <p> AEM-Benutzer mit einer Integration in Analytics müssen ihre Konfiguration ändern, um anstelle des Kennworts den gemeinsamen Analytics-geheimen Schlüssel zu verwenden. </p> <p> Dies sollten Sie tun, bevor die Migration aktiviert ist. Nach der Deaktivierung der Migration ist das ursprünglich konfigurierte Kennwort nicht mehr gültig. </p> <p><b>So rufen Sie das Shared-Secret in Analytics ab</b> </p> <p> Der gemeinsam genutzte geheime Schlüssel kann von Analytics (<span class="uicontrol">Analytics</span> &gt; <span class="uicontrol">Benutzerverwaltung</span>) bezogen werden und ist für jeden Benutzer unterschiedlich. </p> <p><b>Aktualisieren Ihrer AEM-Konfiguration mit dem gemeinsam genutzten geheimen Schlüssel</b> </p> <p>Sehen Sie <a href="https://helpx.adobe.com/de/experience-manager/6-3/sites/administering/using/adobeanalytics-connect.html">Verbinden mit Adobe Analytics und Erstellen von Frameworks</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Builder aktualisieren </p> </td> 
   <td colname="col2"> <p> <p>Wichtig: Aktualisieren Sie Ihre Installation von <a href="https://marketing.adobe.com/resources/help/de_DE/arb/t_install_arb.html">Report Builder</a> auf die neueste Version. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wann beginnt die Migration? </p> </td> 
   <td colname="col2"> <p>Adobe benachrichtigt Analytics-Administratoren per E-Mail über den Beginn der Migration. </p> <p>Die Migration zur Admin-Konsole erfolgt in Schüben. Am Tag der Migration benachrichtigt Adobe Analytics-Administratoren und gewährt ihnen Zugriff auf das Migrationswerkzeug. Nachdem eine Firma bei der Anmeldung die für jede Migrationswelle festgelegten Kriterien erfüllt hat, wird Adobe: </p> 
    <ul id="ul_D7DDC62A08AB4407B122985EDEA6ABD1"> 
     <li id="li_BA0AD50DCDC14C90ADD513DEF6F78180">Legen Sie die Beginns- und Enddaten für die Migration der Firma fest. </li> 
     <li id="li_C048A5C64FAA46C4BB41EF24F1CEDF62">Senden Sie ungefähr 30 Tage vor der Migration eine E-Mail-Benachrichtigung an die aktuellen Analytics-Administratoren der Firma. </li> 
     <li id="li_476265B24CE2404B995201170C75D674">Zeigt eine Produktbenachrichtigung an, in der Administratoren über das Datum des Beginns der Migration informiert werden. </li> 
    </ul> <p> Am Tag der Migration werden Ihre bisherigen Berechtigungsgruppen automatisch in die Admin-Konsole kopiert. Sie können dann in den Analytics Admin Tools keine Benutzer mehr einladen und keine neuen Gruppen mehr erstellen. </p> <p>Nach der Migration: </p> 
    <ul id="ul_4639963EB08F407F8C18ACE2B3D30223"> 
     <li id="li_7F24A3FC900146C3B2E988D399C859EA">Administratoren verwenden die Admin-Konsole, um ihre Analytics-Benutzer und -Berechtigungen zu verwalten. (Sie verwenden die Benutzeroberfläche der Benutzerverwaltung nicht mehr unter Analytics &gt; Admin &gt; Benutzerverwaltung.) </li> 
     <li id="li_5B5234D4F94A4B96A8920F6A5831A64C">Benutzer greifen mit ihrer Adobe oder Enterprise ID über Experience Cloud auf Analytics zu, statt über <span class="filepath">my.omniture.com</span>. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was geschieht am Beginn der Migration? </p> </td> 
   <td colname="col2"> <p>Um 10.00 Uhr UTC am Beginn der Migration: </p> 
    <ul id="ul_25D1DBDF5C804D048E741F31550FF5F3"> 
     <li id="li_418476105FE341229CE146E730AAB33D">Ihre in Analytics vorhandenen Berechtigungsgruppen werden automatisch in der Admin-Konsole als Produkt-Profil repliziert, einschließlich Beschreibungen und granularen Berechtigungen für Report Suites, Metriken, Dimensionen, Analytics und Report Suite Tools. </li> 
     <li id="li_412F88C454B0455A8F3BC8016226855C">Wenn einer Ihrer aktuellen Analytics-Benutzer in der Admin-Konsole erstellt wurde (d. h. über eine verknüpfte Adobe/Enterprise-ID verfügt), wird er den entsprechenden Produkt-Profilen in der Admin-Konsole hinzugefügt. </li> 
     <li id="li_8A05137EC05C4FD5910E73FE58300DCB">Der Abschnitt zum User Management auf der Admin-Registerkarte wird <span class="term"> schreibgeschützt</span>. Sie werden nicht mehr in der Lage sein, neue Benutzer oder Berechtigungsgruppen hier zu erstellen, und müssen diese Funktionen über die Admin Console nutzen. Weitere Informationen dazu finden Sie unter <a href="/help/admin/user-management2/user-migration/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56">Nicht unterstützte Analytics-Funktionen in der Admin Console</a>. </li> 
     <li id="li_2742DE69E9B547198A58E1F33E908361">Als Administrator erhalten Sie Zugriff auf das <a href="https://marketing.adobe.com/resources/help/de_DE/experience-cloud/admin-console/analytics-migration/t_migrate-users.html">Benutzer-ID-Migrationswerkzeug</a>. Zusätzlich wird eine Produktbenachrichtigung angezeigt, die das Enddatum der Migration (in der Regel 60 Tage in der Zukunft) sowie Links zu Hilfeinhalten und FAQs enthält. </li> 
     <li id="li_095D42E3A3544FC59A60A8C8F94C971B">Sie erhalten Zugriff auf die Registerkarte "Berechtigungen"in der Admin-Konsole, mit der Sie Produkt-Profil mit allen detaillierten Optionen erstellen können, mit denen Sie in Analytics vertraut sind. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wie migriere ich Benutzer-IDs? </p> </td> 
   <td colname="col2"> <p> Klicken Sie auf der Admin-Seite unter „User Management“ auf <a href="/help/admin/user-management2/user-migration/t-migrate-users.md#task-f3355f3b14a340feae58cfa04c0ba1c9">Benutzer-IDs migrieren</a>. Verwenden Sie das Tool, um Benutzer zu Produkt-Profilen in der Admin-Konsole hinzuzufügen (repliziert aus Berechtigungsgruppen in Analytics). Sie können Benutzer-IDs in Ihrem eigenen Tempo migrieren. </p> <p>Administratorrechte sind erforderlich. Nach Abschluss der Migration kann sie nicht mehr rückgängig gemacht werden. </p> <p>Am Enddatum der Migration wird der Zugriff auf <span class="filepath">my.omniture.com</span> für Benutzer innerhalb ihres angemeldeten Unternehmens deaktiviert. Benutzer (auch die, die noch migriert werden müssen) werden zur Anmeldung über die Experience Cloud-URL weitergeleitet (<span class="filepath">experiencecloud.adobe.com</span>). </p> <p>Hinweis: Adobe empfiehlt, vor der Migration die Gelegenheit für eine Prüfung Ihrer Benutzer und Gruppen zu nutzen. Löschen Sie alte und nicht verwendete Konten sowie solche, die keinen Zugriff mehr auf das Produkt haben sollten (z. B. Mitarbeiter, die nicht mehr im Unternehmen arbeiten). </p> <p>Verwandtes Thema: <a href="/help/admin/user-management2/user-migration/migrate-enterprise.md">Migrieren von Analytics-Benutzerkonten für Enterprise und Federated IDs</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hat die Migration Auswirkungen auf meine Analytics-Implementierung oder auf die Art der Datenerfassung? </p> </td> 
   <td colname="col2"> <p>Nein. </p> <p>Das Migrationswerkzeug dient der Erleichterung der Übertragung von IDs und Berechtigungen aus Analytics User Management in die <a href="https://adminconsole.adobe.com/enterprise/">Experience Cloud Admin Console</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wie lange dauert der Migrationsprozess? </p> </td> 
   <td colname="col2"> <p>Alle aktuellen Analytics-Administratoren erhalten vier Wochen vor der Migration eine Benachrichtigung per E-Mail. (Das tatsächliche Datum des Beginns wird auf der Benutzeroberfläche von Analytics angezeigt.) </p> <p>Wenn die Migration beginnt, haben Administratoren 60 Tage Zeit, um den Prozess abzuschließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich meine Migration beschleunigen? </p> </td> 
   <td colname="col2"> <p>Ja. Adobe empfiehlt jedoch, die Zeit zu verwenden, bevor die Migration beginnt: </p> 
    <ul id="ul_52C7EC44A5534975BFD7A6F37A829C25"> 
     <li id="li_8CFFF72877E8456DAC3241143AD648AD">Überprüfen Sie, ob Sie Analytics-Produktadministrator in der Admin-Konsole sind. </li> 
     <li id="li_25DAA8D1EEDA45A0B5B59472BD8896C4">Teilen Sie Ihrer Benutzerbasis mit, dass sich deren Anmeldeerfahrung ändert, wenn die Migration beginnt. </li> 
     <li id="li_5B50F942F6A8483FAFA500AFF428702C">Prüfen Sie Ihre aktuellen Benutzer und Berechtigungen und führen Sie Bereinigungen durch. </li> 
    </ul> <p>Wenden Sie sich zur Beschleunigung der Migration an Ihren Customer Success Manager bei der <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html">Adobe-Kundenunterstützung</a> und beantragen Sie ein früheres Startdatum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ich bin Analytics-Administrator ohne Zugriff auf die Admin-Konsole. Wer kann mir beim Zugriff auf die Admin-Konsole helfen? </p> </td> 
   <td colname="col2"> <p>Alle System- oder Produktadministratoren, die Zugriff auf die Admin Console Ihrer Organisation haben, können Ihnen Zugriff gewähren. Wenn Sie sich nicht sicher sind, wer in Ihrer Organisation über Administratorberechtigungen in der Konsole verfügt, wenden Sie sich an die <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html">Adobe-Kundenunterstützung</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich das Startdatum der Migration verschieben? </p> </td> 
   <td colname="col2"> <p>Ja. Wenden Sie sich an die <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html">Adobe-Kundenunterstützung</a>. </p> 
    <draft-comment> 
     <p>Im Folgenden finden Sie eine Beschreibung der Änderungen an Ihrer Analytics-Benutzer- und -Berechtigungsverwaltung am Startdatum. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wo erstelle ich vor dem Beginn der Migration neue Benutzer und Berechtigungsgruppen, nachdem meine Firma zur Admin-Konsole migriert wird? </p> </td> 
   <td colname="col2"> <p>Vor dem Migrationsdatum können Sie Beginn in der Admin-Konsole oder in Analytics &gt; Benutzerverwaltung erstellen. </p> <p>Nach Beginn der Migration können Sie Benutzer und Berechtigungsgruppen nur noch in der Admin-Konsole erstellen. </p> 
    <draft-comment> 
     <p>Weitere Informationen dazu, was am Startdatum der Migration geschieht, finden Sie im Abschnitt „Migration“ weiter unten. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wann kann ich Single Sign-On mit Federated IDs implementieren? </p> </td> 
   <td colname="col2"> <p> In Kürze steht in der Admin-Konsole ein Tool zur Verfügung, mit dem Sie ID-Typen von Adobe IDs in Federated IDs ändern können. Während der Migration können Sie Benutzer nicht als Federated IDs migrieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Informationen während der Migration (FAQ) {#section-d394524aa6d046d79025bbd7499792bc}

Wichtige Informationen zum Migrationsprozess und zu dessen Auswirkungen auf die aktuelle Benutzerverwaltung.

<table id="table_0E37BB1DEA6143F0B5F4E861FCFA7189"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Wie werden Berechtigungsgruppen in der Admin-Konsole repliziert? Was ist mit meinen Benutzern? </p> </td> 
   <td colname="col2"> <p>Eine migrierte Analytics-Gruppe ist ein so genanntes <i>Produkt-Profil</i> in der Admin-Konsole. Berechtigungseinstellungen für die ursprüngliche Gruppe werden bei der Migration beibehalten. Die der Gruppe zugewiesenen Benutzer werden jedoch nicht migriert. Wenn ein Benutzer, der zu dieser Gruppe gehört, mithilfe des Migrationswerkzeugs migriert wird, wird dieser Benutzer diesem Profil zugewiesen. </p> <p>Eine Berechtigungsgruppe der West Coast Operations, die ihre Mitglieder zum ReportBuilder und zum Analyse Workspace berechtigt (mit bestimmten Report Suites, Metriken, Dimensionen), wird zum Profil der West Coast Operations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich die Migrationsbemühungen an einen anderen Administrator delegieren? </p> </td> 
   <td colname="col2"> <p>Sobald Ihre Migration beginnt, kann jeder Administrator, der über Experience Cloud auf Ihre Analytics-Instanz zugreift, mit dem Migrationswerkzeug die Migration von Benutzern starten (oder fortsetzen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich die Mitgliedschaft in einer Berechtigungsgruppe für nicht migrierte Benutzer aktualisieren? </p> </td> 
   <td colname="col2"> <p>Ja. Sie können die Gruppenmitgliedschaft von nicht migrierten Benutzern im Bereich "Analytics-Benutzerverwaltung"ändern. </p> 
    <draft-comment> 
     <p>In Erwartung einer Klarstellung von Ashok darüber, wo das geschieht. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich Benutzer und Berechtigungsgruppen in Analytics nach Beginn der Migration erstellen und diese dann mit dem Migrationswerkzeug in die Admin-Konsole verschieben? </p> </td> 
   <td colname="col2"> <p> Nein. Nach Beginn der Migration müssen alle neuen Benutzer und Berechtigungsgruppen (in der Admin-Konsole als "Product Profils"bezeichnet) in der Admin-Konsole erstellt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Würden Benutzern, die ich mit dem Migrationstool migriere, dieselben Berechtigungen wie in Analytics zugewiesen? </p> </td> 
   <td colname="col2"> <p>Ja. Mit dem Tool migrierte Benutzer erhalten die Berechtigungen, die sie derzeit in Analytics haben. Darüber hinaus behalten sie Zugriff auf ihre Analytics-Assets (z. B. Segmente, Projekte, berechnete Metriken usw.), wenn sie über die Experience Cloud auf Analytics zugreifen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Haben Benutzer, die ich in die Admin Console migriere, weiterhin Zugriff auf Analytics über <span class="filepath">my.omniture.com</span>? </p> </td> 
   <td colname="col2"> <p>Ja. Migrierte Benutzer können bis zum Enddatum der Migration mit ihrem bisherigen Benutzernamen und Passwort über <span class="filepath">my.omniture.com</span> auf Analytics zugreifen, außer Sie deaktivieren den Zugriff mit den bisherigen Anmeldedaten über das Migrationswerkzeug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zwei oder mehr meiner Benutzer haben dieselbe E-Mail-ID in ihrem Analytics-Datensatz. Was passiert, wenn ich sie migriere? </p> </td> 
   <td colname="col2"> <p>Da für Benutzerkonten in der Admin-Konsole eindeutige E-Mail-IDs erforderlich sind, wird bei der Migration von mehr als einem dieser Duplikat der Fehler "-E-Mail-ID"angezeigt. Sie können die E-Mail-IDs nicht migrierter Benutzer im Abschnitt Benutzerverwaltung (Legacy) aktualisieren, bevor Sie die Migration erneut durchführen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Was mache ich nach der Migration meiner Benutzer? </p> </td> 
   <td colname="col2"> <p>Deaktivieren Sie den Zugriff mit den bisherigen Anmeldedaten für <span class="filepath">my.omniture.com</span>. Sie können die alte Anmeldung nur dann deaktivieren, wenn sie migriert wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich den Migrationsprozess verfolgen? </p> </td> 
   <td colname="col2"> <p>Das Migrationstool enthält ein Dashboard, in dem angezeigt wird, wie viele Ihrer Benutzer erfolgreich migriert wurden und wie viele von ihnen ihre Legacy-Anmeldung deaktiviert haben. </p> <p> Idealerweise haben Sie Ihre Firma für die Anmeldung erfolgreich in die Admin-Konsole migriert, wenn 100 % Ihrer Benutzer die Migration abgeschlossen haben und die alten Anmeldedaten deaktiviert wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ich muss während der Migration Benutzer- und Berechtigungsverwaltung durchführen. Welches Tool kann ich verwenden, um diese Aufgabe durchzuführen? </p> </td> 
   <td colname="col2"> <p>Nach Beginn der Migration verwenden Sie die Admin-Konsole, um neue Profil und Produkte zu erstellen und zu verwalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was erfahren meine Benutzer, wenn ich sie mit dem Tool migriere? </p> </td> 
   <td colname="col2"> <p>Sie erhalten eine Begrüßungs-E-Mail an die E-Mail-ID in ihrem Analytics-Benutzerdatensatz, in der sie über ihre neue Art des Zugriffs auf Analytics über die Experience Cloud benachrichtigt werden. Wenn sie keine Adobe-ID haben, werden sie aufgefordert, eine zu erstellen, nach der sie mit ihrer Adobe-ID auf die Lösung zugreifen können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich APIs verwenden, um meine Benutzer zu migrieren, anstatt das Migrationstool zu verwenden? </p> </td> 
   <td colname="col2"> <p>Nein. Sie müssen das Migrationswerkzeug verwenden, um sicherzustellen, dass alle Ihre vorhandenen Benutzer in die Admin-Konsole migriert werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Welche Analytics-Funktionen zur Benutzerverwaltung stehen in der Admin-Konsole nicht zur Verfügung? </p> </td> 
   <td colname="col2"> 
    <ul id="ul_3F3747D4C1D3420699F7D28EC0CA1AA0"> 
     <li id="li_BD943B3245FF47E7A0DDA6107EA1EF89">Asset-Übertragung </li> 
     <li id="li_2DF7004D67ED4C6CB40461EEFB038A5A">Ablauf des Benutzers </li> 
     <li id="li_980E3F5B98F344A492B0EBAD7F1DA60C">Benutzerprotokolle </li> 
    </ul> <p>Diese stehen Ihnen in der Analytics-Benutzerverwaltung weiterhin zur Verfügung. </p> <p>Weitere Informationen dazu finden Sie unter <a href="/help/admin/user-management2/user-migration/c-migration-tool.md">Nicht unterstützte Analytics-Funktionen in der Admin Console</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>In der Admin-Konsole wurden verschiedene Konfigurationen erstellt und den Analytics-Berechtigungsgruppen zugeordnet. Was passiert mit diesen Konfigurationen, wenn die Migration beginnt? </p> </td> 
   <td colname="col2"> <p>Analytics-Berechtigungsgruppen werden in der Admin-Konsole ebenso wie alle anderen Profil neu erstellt. Dies bedeutet, dass Sie zwei Profil in der Konsole sehen, die im Wesentlichen über Duplikat-Berechtigungen verfügen. Sie können Duplikat-Profil aus der Admin-Konsole löschen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was ist mein nächster Schritt nach der Benutzermigration? </p> </td> 
   <td colname="col2"> <p>Wenn Sie einen Benutzer oder einen Benutzersatz migriert haben, besteht der nächste Schritt in der Deaktivierung der bisherigen Anmeldedaten über <span class="filepath">my.omniture.com</span>. Dazu wählen Sie diese Benutzer im Migrationswerkzeug aus und klicken Sie auf die Kontextoption "Legacy-Anmeldung deaktivieren", die oben im Bildschirm angezeigt wird. Beachten Sie, dass diese Option nur angezeigt wird, wenn Sie einen Benutzer oder eine Gruppe von Benutzern auswählen, die alle erfolgreich in die Admin-Konsole migriert wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was geschieht am Ende der Migration? </p> </td> 
   <td colname="col2"> <p>Nach dem Migrationsenddatum (60 Tage nach dem Beginn der Migration) werden alle Benutzer Ihrer Anmelde-Firma mithilfe ihrer Adobe-IDs über die Experience Cloud-Anmeldeseite weitergeleitet, um sich anzumelden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ich konnte nicht alle meine Benutzer bis zum Ende der Migration migrieren. Würden nicht migrierte Benutzer ihren Zugriff auf Analytics verlieren? </p> </td> 
   <td colname="col2"> <p>Benutzer, die nicht bis zum Enddatum migriert wurden, werden auf die Experience Cloud-Anmeldeseite weitergeleitet (experiencecloud.adobe.com) und können nicht auf Analytics zugreifen. Allerdings haben Sie weiterhin Zugriff auf das Migrationswerkzeug. So können Sie die entsprechenden Benutzer finden und ihren Zugriff wiederherstellen. </p> </td> 
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
   <td colname="col1"> <p>Löschen von Benutzern aus der Admin-Konsole </p> </td> 
   <td colname="col2"> <p> In Analytics wird ein gelöschter Benutzer als <span class="term"> abgelaufen</span>, aber das Konto existiert weiterhin. Durch das Speichern des Kontos werden die übertragenen Elemente, wie Segmente, berechnete Metriken, terminierte Berichte, Projekte usw., aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kontoabläufe </p> </td> 
   <td colname="col2"> <p> Sie können in den Admin Tools manuell ein Ablaufdatum für das Konto in Analytics festlegen. Sobald das Ablaufdatum erreicht ist, kann der Benutzer nicht mehr auf Analytics zugreifen, sondern auf sein aktuelles Experience Cloud-Benutzerkonto (z. B. Adobe ID, Enterprise ID, Federated ID usw.) läuft nicht ab. Sie können sich immer noch bei Experience Cloud anmelden. Sie können dann einfach nicht in Analytics klicken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nicht unterstützte Analytics-Funktionen in der Admin Console {#section-928ffba27a0446e0af575b720434ef56}

>[!IMPORTANT]
>
>Lernen Sie über die folgenden Probleme, die während der Migration bei Ihnen auftreten können.

<table id="table_88E2FA03D5F241B79AB54D12F64B51DA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage/Problem </th> 
   <th colname="col2" class="entry"> Antworten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Anmelden als </p> </td> 
   <td colname="col2"> <p> Administratoren, die in die Admin-Konsole migrieren, können nicht mehr die Funktion "Anmelden als"verwenden, um auf Benutzerkonten von Nichtadministratoren zuzugreifen, die in die Admin-Konsole migriert wurden. Diese Funktion wird in Analytics nicht mehr unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ablauf des Benutzers und Asset-Übertragung </p> </td> 
   <td colname="col2"> <p> Die Admin-Konsole unterstützt weder den Ablauf noch die Asset-Übertragung von Benutzern. Administratoren verwenden für beide Funktionen den Abschnitt "Analytics-Benutzer und -Assets"unter "Admin Tools in Analytics". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Letzter Zugriff (letzte Anmeldung) </p> </td> 
   <td colname="col2"> <p> Details zum Datum und zur Uhrzeit der letzten Anmeldung eines Benutzers finden Sie im Link "Analytics-Benutzer und -Elemente"und nicht in der Admin-Konsole. Das letzte Anmeldedatum in Analytics bezieht sich auf den Zeitpunkt, zu dem Benutzer tatsächlich über die Experience Cloud auf Analytics zugegriffen haben, und nicht auf das Datum/die Zeit, zu dem/der sie sich bei der Experience Cloud angemeldet haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>User Management-APIs – <a href="https://helpx.adobe.com/de/enterprise/help/identity.html">von Adobe unterstützte Identitätstypen</a> </p> </td> 
   <td colname="col2"> <p> Administratoren, die zur Admin-Konsole migrieren, sollten die in der Adobe-E/A-Datei angebotenen Benutzerverwaltungs-APIs<a href="https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html"></a> für den programmatischen Zugriff auf Benutzerkonten in der Admin-Konsole konfigurieren. </p> <p>Die Analytics-Berechtigungs-APIs werden deaktiviert, wenn Sie für die Migration aktiviert sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Web-Service-Zugriffsberechtigungen </p> </td> 
   <td colname="col2"> <p> Die Anmeldeinformationen für den Webdienst der Benutzer (und ihr gemeinsamer geheimer Schlüssel) stehen in der Admin-Konsole nicht zur Verfügung und können über einen Klick auf den jeweiligen Benutzer im Abschnitt "Analytics-Benutzer und -Assets"aufgerufen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Single Sign-on </p> </td> 
   <td colname="col2"> <p> Analytics-Konfigurationen für die einmalige Anmeldung werden nach Abschluss der Migration entfernt. Sie werden während der Migration aktiv bleiben. Kunden, die Analytics Single Sign-on verwenden, sollten ein Upgrade auf <a href="https://helpx.adobe.com/de/enterprise/help/identity.html">Adobe Federated ID</a> durchführen. </p> <p>Analytics empfiehlt, dass Sie Ihre Benutzer zunächst als Adobe-IDs migrieren, um die Experience Cloud-Konten einfach zu erstellen, und diese dann in Federated Single-Sign-Benutzer konvertieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Herunterladen von Berechtigungsgruppen </p> </td> 
   <td colname="col2"> <p> Das Herunterladen von Berechtigungsgruppeninformationen wird weder in den Analytics Admin Tools noch in der Adobe Admin Console unterstützt. Kunden sollten die Adobe.io-APIs zur Benutzerverwaltung verwenden, um Informationen zu Berechtigungsgruppen stapelweise abzurufen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Erstellungsdatum des Kontos </p> </td> 
   <td colname="col2"> <p>Informationen zum Erstellungsdatum von Konten werden weder in den Analytics Admin Tools noch in der Adobe Admin Console unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Massen-E-Mail </p> </td> 
   <td colname="col2"> <p>Massen-E-Mails an Benutzer werden weder in der Analytics Admin-Konsole noch in der Adobe Admin Console unterstützt. Kunden können die E-Mail-Adressen ihrer Benutzer stapelweise aus der Adobe Admin Console exportieren und eine E-Mail mit einem beliebigen E-Mail-Client senden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Benachrichtigung der Benutzer über die Migration {#section-f3b25f672a3a4d03b0559656fd99d20a}

Möglicherweise möchten Sie Ihren aktuellen Benutzern diesen Migrationsplan proaktiv mitteilen. Hier eine Vorlage, die Sie anpassen können, um alle Ihre aktuellen Analytics-Benutzer zu senden:

Um eine E-Mail an alle Benutzer zu senden, navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]** > [E-Mail-Benutzer](https://marketing.adobe.com/resources/help/de_DE/reference/t_email_users.html).

**Betreff:** In Kürze: Eine neue Anmeldeart für Adobe Analytics und Adobe Experience Cloud.

**Textkörper:** Für Adobe Analytics-Kunden

In unserem Unternehmen werden alle Adobe Analytics-Konten von [!DNL https://my.omniture.com/login/] auf Adobe Experience Cloud ([experiencecloud.adobe.com](http://experiencecloud.adobe.com/)) migriert. Mit dieser Migration wird Ihr Adobe Analytics-Konto aktualisiert, um Zugriff auf Analytics über die Adobe Experience Cloud zu ermöglichen. Während sich die Methode zum Zugriff auf Analytics ändert, bleiben alle vorhandenen Berechtigungen für Ihre Report Suites und Tools erhalten.

**Nächste Schritte:** Wir beginnen mit der Migration von Benutzern am **DATUM EINFÜGEN**. Achten Sie auf eine Begrüßungsnachricht mit Ihrer neuen Anmeldung, die an die E-Mail-ID gerichtet ist, die unter Ihrem Analytics-Konto aufgeführt ist. Wenn Sie keine mit Ihrer E-Mail-Adresse verknüpfte [Adobe-ID](https://helpx.adobe.com/de/x-productkb/global/adobe-id-account-change.html) eingerichtet haben, werden Sie aufgefordert, ein Konto einzurichten.

**Hilfreiche Ressourcen:**

[Anmelden und Profileinstellungen verwalten](https://marketing.adobe.com/resources/help/de_DE/mcloud/getting-started-experience-cloud.html).

[Informationen zu Clouds, Hauptdiensten und Lösungen](https://marketing.adobe.com/resources/help/en_US/mcloud/solutions_capability_names.html) in der Experience Cloud

Wenden Sie sich bei Fragen oder Bedenken an Ihren Analytics-Administrator.

Best,

Analytics-Admin
