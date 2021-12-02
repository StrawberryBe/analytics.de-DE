---
description: Verwalten Sie Analytics-Benutzer, -Gruppen und -Produkte in der Admin Console.
subtopic: Users and groups
title: Verwalten von Benutzern und Produkten
feature: Admin Tools
uuid: 891a8cb3-b77d-46f6-ab23-cbed49f215b5
exl-id: c0fbbb3a-0011-49d2-89a2-70fce11e0fb2
source-git-commit: 6fe67311c73fc766e8051e57a047224b8fb17747
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 65%

---

# Verwalten von Benutzern und Produkten

Verwalten Sie Analytics-Benutzer, -Gruppen und -Produkte in der Admin Console.

>[!IMPORTANT]
>
>Die Benutzer- und Produktverwaltung wurde in die [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html). Sie werden von Adobe erfahren, wann Sie Benutzer migrieren müssen.

## Hilfematerialien für Admin Console-Administratoren {#section_C13BBB89E4F248F193358BB3A59DD502}

<table id="table_9263797773A749628E12BB3C1EBE620B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Aufgabe oder Ressource </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Migrieren von Analytics-Benutzer-IDs in die Adobe Admin Console </p> </td> 
   <td colname="col2"> <p> Adobe unterstützt Analytics-Administratoren bei der Migration von Benutzer-IDs in die Admin Console. Dieser Ansatz erfolgt in Wellen. Wenn Sie mit dem Migrieren Ihrer Benutzer an der Reihe sind, benachrichtigt Adobe die Analytics-Administratoren per E-Mail mit entsprechenden Anweisungen. Zu diesem Zeitpunkt ist ein <a href="https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html">Migrationstool</a> in Analytics User Management verfügbar, um diese Aufgabe zu vereinfachen. </p> <p>Wichtig: Am Tag der Benutzermigration werden Ihre vorherigen Berechtigungsgruppen automatisch in die Admin Console kopiert. Sie können dann in den Analytics Admin Tools keine Benutzer mehr einladen und keine neuen Gruppen mehr erstellen. Lesen Sie die häufig gestellten Fragen und Hilfe unter <a href="https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html"> Analytics-Benutzermigration zur Adobe Admin Console</a> Informationen zur Vorbereitung auf die Migration und zu den betroffenen Verwaltungsfunktionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Admin Console starten </p> </td> 
   <td colname="col2"> <p>Nachdem die Benutzerkonten migriert wurden, können Sie Benutzer und Produkte über alle Lösungen hinweg in der Admin Console verwalten. </p> <p>Gehen Sie zu: <a href="https://adminconsole.adobe.com/enterprise/#">https://adminconsole.adobe.com/enterprise/</a>. </p> <p>Hilfe finden Sie unter <a href="https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de"> Verwalten von Experience Cloud-Benutzern und -produkten</a> für Aktualisierungen der Experience Cloud-Benutzer- und -Produktverwaltung in der Adobe Admin Console. </p> </td> 
  </tr> 
 </tbody> 
</table>

<!---
## User Management Descriptions {#section_7C19842A3D4249109A9399D4DF18DE75}

The following table describes elements on the [!UICONTROL Users] tab in [!UICONTROL User Management].

<table id="table_6F81D1095EB945D8995FF971B65BA52A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins available</span> </td> 
   <td colname="col2"> The maximum number of user accounts you can create for this company. If necessary, you can contact your Account Representative or Customer Care to increase this number at no charge. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins in use</span> </td> 
   <td colname="col2"> The number of user accounts currently in use for this company. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins Remaining</span> </td> 
   <td colname="col2"> The difference between the user account maximum and the number of existing user accounts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Add New User</span> </td> 
   <td colname="col2"> <p>Lets you add a user account to the company. This link is available only if the Number of User Logins Remaining is greater than 0. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Download Report</span> </td> 
   <td colname="col2">Exports the contents of the <span class="wintitle"> Users</span> table to a tab-delimited file. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Login</span> </td> 
   <td colname="col2"> <p>The user name. You can click the user name to edit the user account properties. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> First Name</span> </td> 
   <td colname="col2"> The user's first (given) name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Last Name</span> </td> 
   <td colname="col2"> The user's surname (family name). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Title</span> </td> 
   <td colname="col2"> The user's job title. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Admin</span> </td> 
   <td colname="col2"> Specifies if the user account has administrative privileges. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Last Login</span> </td> 
   <td colname="col2"> Displays a timestamp of the last login for this user account. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Create Time</span> </td> 
   <td colname="col2"> Shows the date and time when the login account was created. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Expires</span> </td> 
   <td colname="col2"> Displays the account expiration account, if applicable. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Manage</span> </td> 
   <td colname="col2"> Provides links for user account management. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Edit</span> </td> 
   <td colname="col2"> <p>Edit user account settings. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Delete</span> </td> 
   <td colname="col2"> Delete the user account. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Transfer</span> </td> 
   <td colname="col2">Assign the privileges (permissions and resource access) of one user account to another. <p>See <a href="/help/admin/user-management2/c-user-management/t-transfer-user-accout-privileges.md"> Transfer user account privileges</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Login as this user</span> </td> 
   <td colname="col2"> <p>Allows admins to impersonate and log in as a non-admin account. Admin accounts cannot be impersonated. </p> </td> 
  </tr> 
 </tbody> 
</table>
-->