---
description: 'null '
keywords: Gruppen; Berechtigungen
seo-description: 'null '
seo-title: Änderungen der Berechtigungen für Benutzer und Gruppe
solution: Analytics
subtopic: Benutzer und Gruppen
title: Änderungen der Berechtigungen für Benutzer und Gruppe
topic: Admin Tools
uuid: 94 f 2727 b -17 e 4-4003-a 222-35 c 821 d 6959 e
translation-type: tm+mt
source-git-commit: 0837416ae67936fbf81af2b7051a7ed9f522f5b5

---


# Änderungen der Berechtigungen für Benutzer und Gruppe

>[!IMPORTANT]
>
>User and product management is moving to the [Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html). Sie werden von Adobe erfahren, wann Sie Benutzer migrieren müssen. After all customers have migrated, help content for **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin Tools]** &gt; **[!UICONTROL User Management]** will be retired.

## Was hat sich geändert? {#section_2C205DE94155441B9E9D3E4C46CCF2EE}

**[!UICONTROL Admin]** &gt; **[!UICONTROL Benutzerverwaltung]** &gt; **[!UICONTROL Gruppen]**

>[!NOTE]
>
>Aufgrund der zahlreichen verfügbaren Berechtigungskombinationen können wir keine Dokumentation zur Beschreibung aller API-Methoden bereitstellen, die in jeder Kombination aus Berechtigungen verwendet werden können. Im Allgemeinen gilt Folgendes: Benutzer ohne Administratorstatus, die Web-Services-Zugriff erhalten, haben nur Lesezugriff auf API-Methoden. Sie verfügen im Hinblick auf Methoden nicht über Schreibzugriff.

Weil API und Oberfläche dasselbe Berechtigungssystem verwenden, wird es sich bei allen Berechtigungen, die ein bestimmter Benutzer ohne Administratorstatus von einem Administrator in der Oberfläche (Adobe Admin Console) erhalten hat, um dieselben Berechtigungen handeln, die der Benutzer in der API hat.

<table id="table_D1DB0DE37752450BBCCA44DB760BB505"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Verbesserung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p id="reportaccess">Änderung am <span class="uicontrol">Berichtszugriff</span> (Anpassen von Gruppen) </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Neue Gruppe hinzufügen</span> &gt; <span class="uicontrol">Zugriff auf Bericht</span> </p> <p>Der Abschnitt <span class="wintitle">Zugriff auf Bericht</span> auf der Seite <span class="wintitle">Gruppen &gt; Neue Benutzergruppe hinzufügen</span> wurde auf vier Kategorien aufgeteilt, die es Ihnen erlauben, Berechtigungen detailliert anzupassen. </p> <p><img  src="assets/report-access.png" id="image_CB83E5C7DB4343619421A1FAA61478D0"> </img> </p> <p>Elemente, ehemals verfügbar in </p> 
    <ul id="ul_16D5EF18D57D4608AEEDEC40D90D8828"> 
     <li id="li_F29E84C6228A464C8807F09205AEAAC6"> <p> <a href="../../../admin/user-management2/c-customize-report-access/groups-analytics-tools.md#concept_C4383A6C0F5E4130875FDD3756F2E2FC" format="dita" scope="local"> Analytics-Werkzeuge</a>: Gewähren Sie Benutzern Zugriff auf allgemeine Elemente (Rechnungsstellung, Protokolle usw.), Unternehmensverwaltung, Werkzeuge, Web-Services, den Report Builder und die Data Connectors-Integration. </p> <p> <b>Hinweis:</b> Die Unternehmenseinstellungen aus der Kategorie „Anpassung der Admin Console“ sind nun in den Analytics-Tools zu finden. </p> </li> 
     <li id="li_A6EB788162A2455E94CE54B9279A854D"> <p> <a href="../../../admin/user-management2/c-customize-report-access/groups-report-suite-tools.md#concept_C94E9864349B428AB9CCE0CA4B0A40FF" format="dita" scope="local"> Report Suite-Tools</a>: Gewähren Sie Benutzern Zugriff auf Web-Services, Report Suite-Verwaltung, Tools und Berichte sowie Dashboard-Elemente. </p> </li> 
     <li id="li_EDB0255E009B4F1CAFAF53966B41363C"> <p> <a href="../../../admin/user-management2/c-customize-report-access/groups-metrics.md#concept_05D54436430E4320A48C7C685D337FBE" format="dita" scope="local"> Metriken</a>: Gewähren Sie Zugriff auf Traffic, Konversion, benutzerdefinierte Ereignisse, Lösungsereignisse, Content-Unterstützung und mehr. </p> </li> 
     <li id="li_8DAE87D1DEF54803A9C6FE31C01F0FB0"> <p> <a href="../../../admin/user-management2/c-customize-report-access/groups-dimensions.md#concept_68B36161345341369B6D01DC7DD42A22" format="dita" scope="local"> Dimensionen</a>: Legen Sie Benutzerrechte granular fest, einschließlich eVars, Traffic-Berichten, Lösungsberichten und Pfadsetzungsberichten. </p> </li> 
    </ul> <p>Sie können beispielsweise eine Gruppe mit Zugriff auf mehrere Analytics-Tools (<span class="wintitle">Analysis Workspace</span>, <span class="wintitle">Reports &amp; Analytics</span> und <span class="wintitle">Report Builder</span>) erstellen, die Zugriff auf bestimmte Metriken und Dimensionen (einschließlich eVars) erhält und beispielswiese Segmente oder berechnete Metriken erstellen kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Änderungen an vordefinierten Gruppen </p> </td> 
   <td colname="col2"> <p> <b>Administratorzugriff:</b> Vordefinierte Gruppen sind für Administratoren nicht länger notwendig. Administratoren haben jetzt Zugriff auf alle Elemente (Tools, Dimensionen und Metriken) sowie auf Web Service, Report Builder, Activity Map und Ad Hoc Analysis. </p> <p>Sinn und Zweck von Gruppen ist es künftig, den Zugriff von Nichtadministratoren zu ermöglichen oder einzuschränken. </p> <p> <b>Benutzerspezifische Gruppen:</b> Vordefinierte Gruppen wurden durch benutzerspezifische Gruppen ersetzt. Bestehende vordefinierte Gruppen werden in benutzerspezifische Gruppen migriert und mit dem gleichen Gruppennamen gekennzeichnet. Von Ihnen erstellte benutzerspezifische Gruppen und deren Einstellungen bleiben dabei erhalten. Sie werden jedoch möglicherweise bemerken, dass die Einstellungen sich an einem anderen Ort befinden. Die Unternehmenseinstellungen beispielsweise (früher in der Anpassung der Admin Console) befinden sich nun in der <a href="../../../admin/user-management2/c-customize-report-access/groups-analytics-tools.md#concept_C4383A6C0F5E4130875FDD3756F2E2FC" format="dita" scope="local"> Anpassung der Analytics-Tools</a>. </p> <p> Users belonging to <span class="term"> All Report Access</span> have been migrated to a custom group with access to: </p> 
    <ul id="ul_696A9243F5FD4AF187352C2F4B1CFDC2"> 
     <li id="li_683A0A3BB7214CFFBC61D5A4CD237F48">Alle Dimensionen </li> 
     <li id="li_D8FDBF6A32224731AB706315DEA0A03E">Alle Metriken </li> 
     <li id="li_65ABE5C95D43444D88E63EE95C9AED05">Alle Report Suites </li> 
     <li id="li_7ED1505590144B38B3B9851BAA6BBB49">Berechtigung für Kanalbericht </li> 
     <li id="li_F718FE1FCF9A4B05AB933CA3F105F3EC">Berechtigung für Anomalieerkennungsbericht </li> 
     <li id="li_527BD52007E846FE8B5F71AB3C12F695">Berechtigung für Echtzeitbericht </li> 
     <li id="li_AFFB58C7FB644AC8A85E2D76BA7D51F5">Berechtigung für Zugriff auf Analysis Workspace </li> 
    </ul> <p>Administratoren können benutzerspezifische Gruppen löschen und eigene Gruppen erstellen, da sämtliche zuvor in vordefinierten Gruppen zur Verfügung stehenden Einstellungen auch für die Anpassung mit Einstellungen für den <span class="wintitle">Zugriff auf Berichte</span> unter <a href="../c-user-groups/groups.md" format="dita" scope="local">Benutzergruppen definieren</a> verfügbar sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berechtigungen auf Dimensionsebene </p> </td> 
   <td colname="col2"> <p>Sie können Berechtigungen so anpassen, dass der Zugriff auf bestimmte Dimensionen (zusätzlich zu den Metriken) eingeschränkt oder ausgeweitet werden kann. </p> 
    <ul id="ul_DA5A54223673474E9151AF979DA50659"> 
     <li id="li_C3E82F7BC07A4F2F83A85D3D511292CC"> <p>Alle aktuellen Dimensionen und Metriken in benutzerdefinierten Gruppen wurden automatisch in die neuen Kategorien migriert. Wenn in einer bestehenden Gruppe Metriken aktiv sind, werden für diese Gruppe sämtliche Dimensionen, für die neue Berechtigungen erteilt werden (eVars und inhaltsbasiert), und Metriken als Standardeinstellungen festgelegt. </p> </li> 
     <li id="li_CC56F9181CC14AB59318628E72F2E8C9"> Classifications Importer (bisher SAINT) berechtigt für: Zugriff auf Classifications wird durch Zugriff auf die <a href="https://marketing.adobe.com/resources/help/en_US/reference/c_classifications.html" format="html" scope="external">Variable</a> bestimmt, auf der Classification basiert. </li> 
    </ul> <p>See <a href="../../../admin/user-management2/c-customize-report-access/groups-dimensions.md#concept_68B36161345341369B6D01DC7DD42A22" format="dita" scope="local"> Customize Dimension Permissions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Admin Console </p> </td> 
   <td colname="col2"> <p>Wird nur neuen Kunden empfohlen sowie Kunden mit Unternehmen, die in <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/core_services.html" format="html" scope="external">Experience Cloud</a> bereitgestellt wurden. Für bestehende <span class="keyword">Analytics</span>-Kunden ist eine Migration in das Identitätsverwaltungssystem von <span class="keyword">Experience Cloud</span> geplant. </p> <p>More information is available in <a href="https://helpx.adobe.com/enterprise/using/manage-permissions-and-roles.html" format="html" scope="external"> Manage product permissions in the Admin Console</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Häufig gestellte Fragen zu Berechtigungsänderungen in Analytics {#section_02809EFC95054B40A089E6C6E4FACA13}

Hier finden Sie wichtige neue Informationen zu neuen und geplanten Aktualisierungen sowie zu den Auswirkungen, die sie auf Ihre Administrationsumgebung haben.

<table id="table_1E93F45C66E841E6882FB602509F30A3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Welche Berechtigungen wurden in der Version vom <b>Juli 2016</b> eingeführt? </td> 
   <td colname="col2"> <p> <b>Zugriff auf alle Report Suites</b> </p> <p>Wird eine Report Suite einer Gruppe hinzugefügt, können Sie die Option <span class="uicontrol">Zugriff auf alle Report Suites</span> auswählen. Mit dieser Einstellung kann die Gruppe auf alle bestehenden und künftig erstellten Report Suites zugreifen. </p> <p>Navigieren Sie zur Aktivierung dieser Funktion zu <span class="uicontrol">Benutzerverwaltung</span> &gt; <span class="uicontrol">Gruppen</span> &gt; <span class="uicontrol">Neue Benutzergruppe hinzufügen</span> und wählen Sie <span class="uicontrol">Zugriff auf alle Report Suites</span> aus. </p> <p><img placement="break"  src="assets/all-report-suites.png" width="300px" id="image_9E814D412E87484C940F1100D6DE2B0F" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sollte ich die Admin-Konsole zur Verwaltung von Benutzern oder zur vorhandenen Analytics User Management verwenden? </p> </td> 
   <td colname="col2"> <p>Änderungen, die in Analytics &gt; Admin &gt; Benutzerverwaltung vorgenommen wurden, werden nicht in der Admin-Konsole angezeigt. Daher sollten nur neue Kunden, die die Admin-Konsole für Benutzer- und Gruppenverwaltung bereits verwenden, dies auch weiterhin tun. Eine Migration für bestehende Analytics-Gruppenverwaltung in die Admin-Konsole ist geplant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Welche Berechtigungen haben sich in der Version <b>Oktober 2016</b> geändert? </p> </td> 
   <td colname="col2"> <p>Es wurden folgende Verbesserungen an der aktuellen Oberfläche der <span class="wintitle">Admin Tools</span> vorgenommen: </p> <p> 
     <ul id="ul_2A31E8DC17A94B7FABDBA9C87C3947EF"> 
      <li id="li_AE2ECCA01CC64D30B109BE74379EE474">Permission changes as described in <a href="../../../admin/user-management2/c-user-management/permissions-changes.md#concept_86581595B86B47D5B8F90282FC3E31EF" format="dita" scope="local"> Administrative Changes - Fall 2016</a>. </li> 
      <li id="li_33CB2B6A2E5F45BE97CC5E0983AF280E">Entfernung erloschener Traffic-Berichte, die nicht mehr im Menü aufgeführt wurden. </li> 
      <li id="li_57234CF27E1D405987DE89312CD62C52">Berechtigungen für Classifications: Der Zugriff auf Klassifizierungen wird durch Zugriff auf die Variable bestimmt, für die die Classification gilt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Muss ich bestimmte Voraussetzungen erfüllen, um Benutzer migrieren zu können? </p> </td> 
   <td colname="col2"> <p>Nein, sämtliche Berechtigungen werden transparent migriert. </p> <p> 
     <ul id="ul_654F85286EC04416B3E0BA725EBE10AD"> 
      <li id="li_8050B8941F794103B82A0ADF0930D216">Alle aktuellen Traffic-Berichte in benutzerspezifischen Gruppen werden automatisch in die neue Dimensionskategorie migriert. </li> 
      <li id="li_B97079DB29A346B98D066F11AB7F94AF">Sollten für eine benutzerspezifische Gruppe bereits Metriken aktiviert worden sein, erhalten ihre Mitglieder automatisch Zugriff auf entsprechende neue Dimensionen (eVars und Lösungsvariablen). </li> 
      <li id="li_F1219EF490DA473BA15F2B215F2995AE"> Eine benutzerspezifische Gruppe mit mindestens einer Metrik erhält automatisch Zugriff auf alle eVars und andere inhaltsbezogene Dimensionen <b>mit Ausnahme</b> der neuen Traffic-Dimensionen (ehemals Traffic-Berichte). </li> 
      <li id="li_F494CE6144A04A6199CFBBA1D7BEA32B">Jede vordefinierte Gruppe wird in eine Berechtigung umgewandelt. Diese neuen Berechtigungen werden einer neuen Kategorie der <span class="uicontrol">Analytics-Tools</span> hinzugefügt. </li> 
      <li id="li_2FCD9254FC3C4FD7871EEF9453E5CE1E">Jeder benutzerspezifischen Gruppe mit Metriken werden Lösungsereignisse als neue Metrik hinzugefügt. </li> 
      <li id="li_34C4560769B64F28A4E83BAE71065DCC">Jeder Benutzer, der Zugriff auf alle Berichte hatte, wird einer entsprechenden neuen, benutzerspezifischen Gruppe hinzugefügt. Die Option „Zugriff auf alle Berichte“ gibt es nicht mehr. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was ändert sich nicht? </p> </td> 
   <td colname="col2"> <p>Besucherattribute verfügen weiterhin nicht über Berechtigungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Schnellverweis zu Berechtigungen {#section_A3FDD8259F524B21A5489833533D1B28}

In der folgenden Tabelle finden Sie Aufgaben und deren Durchführungszeitpunkt (abhängig vom Status des Unternehmens).

>[!NOTE]
>
>A *`migrated user`* and *`Experience Cloud user`* refer to users who have accepted an email invitation to join the Experience Cloud. Wenn die E-Email-Einladung nicht akzeptiert wird, sind Benutzer weiterhin Analytics-Benutzer und können nicht in der Admin-Konsole verwaltet werden. (Die Ausnahme ist, wenn für die Migration [Enterprise oder Federated IDs](https://helpx.adobe.com/enterprise/using/set-up-identity.html) verwendet werden. In diesem Fall wird der Benutzer migriert, wenn der Administrator Benutzer einzeln migriert.)

<table id="table_B68FD00FC5D24823A86BB69558C0327C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Aufgabe </th> 
   <th colname="col2" class="entry"> Nicht migrierendes Anmeldeunternehmen </th> 
   <th colname="col3" class="entry"> Aktuell migrierendes Unternehmen </th> 
   <th colname="col4" class="entry"> Anmeldeunternehmen mit abgeschlossener Migration </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Einen Benutzer erstellen </td> 
   <td colname="col2"> <p>Admin Console (creating a user and adding him or her to an Analytics <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/admin_getting_started.html" format="html" scope="external"> product configuration</a> also creates the user account in Analytics). </p> <p> <a href="../../../admin/user-management2/c-user-management/t-add-user-account.md#task_60F86F36CB86446699EA7C7E5FB03EA7" format="dita" scope="local"> Admin Tools</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://adminconsole.adobe.com/enterprise/" format="http" scope="external"> Admin-Konsole</a> </p> </td> 
   <td colname="col4"> <p> <a href="https://adminconsole.adobe.com/enterprise/" format="http" scope="external"> Admin-Konsole</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Einen Benutzer bearbeiten </td> 
   <td colname="col2"> <p> <a href="../../../admin/user-management2/c-user-management/t-add-user-account.md#task_60F86F36CB86446699EA7C7E5FB03EA7" format="dita" scope="local"> Admin Tools</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://adminconsole.adobe.com/enterprise/" format="http" scope="external"> Admin-Konsole</a> </p> <p> Admin Tools – Das Bearbeiten migrierter Benutzer über die Admin Tools ist auf die Verwaltung von API-Schlüsseln sowie das Löschen oder Übertragen von Assets beschränkt. </p> </td> 
   <td colname="col4"> <p> <a href="https://adminconsole.adobe.com/enterprise/" format="http" scope="external"> Admin-Konsole</a> </p> <p> Admin Tools – Das Bearbeiten ist auf die Verwaltung von API-Schlüsseln und das Löschen oder Übertragen von Assets beschränkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Einen Benutzer löschen </td> 
   <td colname="col2"> <p>Admin-Konsole - für Benutzer von Experience Cloud </p> <p>Admin Tools – für alle Benutzer außer Benutzer von Experience Cloud wird nur der zugeordnete Analytics-Benutzer, nicht das Experience Cloud-Konto gelöscht. </p> </td> 
   <td colname="col3"> <p>Admin-Konsole - für migrierte Benutzer. </p> <p>Admin Tools – für Benutzer, die ausschließlich Analytics nutzen </p> </td> 
   <td colname="col4"> <p>Admin Console </p> <p> Admin Tools - Nach dem Löschen eines Experience Cloud-Benutzers oder Aufheben der Verknüpfung sein Konto in der Admin-Konsole können Sie die Analytics-Anmeldung aus den Admin Tools löschen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bei Analytics anmelden </td> 
   <td colname="col2"> <p> <b>Experience Cloud: </b> <span class="filepath"> marketing.adobe.com</span>. Ausschließlich für Benutzer von Experience Cloud verfügbar. </p> <p> <b>Analytics (veraltet):</b> <span class="filepath">sc.omniture.com</span>. Für Benutzer, die ausschließlich Analytics verwenden, sowie für Benutzer von Experience Cloud mit deren Analytics-Anmeldedaten </p> </td> 
   <td colname="col3"> <p> <span class="filepath">marketing.adobe.com</span> – ausschließlich für Benutzer von Experience Cloud verfügbar </p> <p> <span class="filepath">sc.omniture.com</span> – für Benutzer, die ausschließlich Analytics verwenden, sowie für Benutzer von Experience Cloud mit deren Analytics-Anmeldedaten </p> <p>Während der Migration können Administratoren die Anmeldung über <span class="filepath">omniture.com</span> für bestimmte Benutzer deaktivieren. </p> </td> 
   <td colname="col4"> <p>Admin Console </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eine Gruppe erstellen </td> 
   <td colname="col2"> <p>Admin-Konsole: Wenn eine Gruppe in der Admin-Konsole erstellt wird, wird in den Admin Tools eine zugeordnete Gruppe in Analytics angezeigt. Diese zugeordnete Gruppe kann jedoch nicht von den Admin Tools geändert oder aus den Admin Tools gelöscht werden. </p> <p>Admin Tools. </p> </td> 
   <td colname="col3"> <p>Admin Console (<a href="https://marketing.adobe.com/resources/help/en_US/mcloud/admin_getting_started.html" format="html" scope="external"> create product configuration</a>) </p> </td> 
   <td colname="col4"> <p>Admin Console (<a href="https://marketing.adobe.com/resources/help/en_US/mcloud/admin_getting_started.html" format="html" scope="external"> create product configuration</a>) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Benutzer in einer Gruppe bearbeiten </td> 
   <td colname="col2"> <p>Admin-Konsole - nur für Benutzer von Experience Cloud </p> <p>Admin Tools – sowohl für Benutzer, die ausschließlich Analytics verwenden, als auch für Benutzer von Experience Cloud, die Mitglieder von in den Admin Tools bearbeitbaren Gruppen sind. Wenn ein Experience Cloud-Benutzer jedoch Teil einer Gruppe in der Admin-Konsole ist, kann er in den Admin Tools nicht aus der Gruppe entfernt werden. </p> </td> 
   <td colname="col3"> <p>Admin-Konsole - nur Experience Cloud-Benutzer </p> <p> Admin Tools – Benutzer, die ausschließlich Analytics verwenden, können nach wie vor Gruppen in Analytics hinzugefügt oder daraus entfernt werden. </p> </td> 
   <td colname="col4"> <p>Admin Console </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Berechtigungen einer Gruppe bearbeiten </td> 
   <td colname="col2"> <p>Admin-Konsole - Sie können in der Admin-Konsole erstellte Gruppen bearbeiten. </p> <p>Admin Tools – Sie können die Berechtigungen beliebiger Gruppen bearbeiten. </p> </td> 
   <td colname="col3"> <p>Admin-Konsole </p> </td> 
   <td colname="col4"> <p>Admin-Konsole </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gruppe löschen </td> 
   <td colname="col2"> <p>Admin-Konsole - Sie können nur in der Admin-Konsole erstellte Gruppen löschen. </p> <p>Admin Tools – Sie können ausschließlich mit den Admin Tools erstellte Gruppen löschen. </p> </td> 
   <td colname="col3"> <p>Admin-Konsole </p> </td> 
   <td colname="col4"> <p>Admin-Konsole </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Administratorstatus eines Benutzers ändern </td> 
   <td colname="col2"> <p>Admin-Konsole - nur für Benutzer von Experience Cloud. </p> <p>Admin Tools </p> </td> 
   <td colname="col3"> <p>Admin-Konsole - nur für Benutzer von Experience Cloud. </p> <p>Admin Tools – nur für Benutzer von Analytics. </p> </td> 
   <td colname="col4"> <p>Admin Console </p> </td> 
  </tr> 
 </tbody> 
</table>
