---
description: Verwalten Sie Analytics-Benutzer, -Gruppen und -Produkte in der Adobe Admin Console.
subtopic: Users and groups
title: Verwalten von Benutzern und Produkten
feature: Admin Tools
exl-id: c0fbbb3a-0011-49d2-89a2-70fce11e0fb2
source-git-commit: 24ae07993e8f51b8220f817873fbd8dc1df70cda
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 69%

---

# Benutzer und Produkte verwalten (alt)

Verwalten Sie Analytics-Benutzer, -Gruppen und -Produkte in der Adobe Admin Console.

>[!IMPORTANT]
>
>Die Verwaltung von Benutzern und Produkten wurde in die [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html) verschoben. Informationen zum Verwalten von Benutzerberechtigungen für Adobe Analytics-Benutzer finden Sie unter [Analytics in der Adobe Admin Console](/help/admin/admin-console/home.md).

## Hilfe-Ressourcen für Adobe Admin Console-Administratoren {#section_C13BBB89E4F248F193358BB3A59DD502}

| Aufgabe oder Ressource | Beschreibung |
| --- | --- |
| Migrieren von Benutzer-IDs aus Analytics in die Adobe Admin Console | Adobe unterstützt Analytics-Administratoren bei der Migration von Benutzer-IDs in die Admin Console. Dieser Ansatz erfolgt in Wellen. Wenn Sie mit dem Migrieren Ihrer Benutzer an der Reihe sind, benachrichtigt Adobe die Analytics-Administratoren per E-Mail mit entsprechenden Anweisungen. Zur Vereinfachung dieser Aufgabe ist in [Analytics User Management](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=de) ein Migrationswerkzeug verfügbar.<p>**Wichtig**: Am Tag der Benutzermigration werden Ihre vorherigen Berechtigungsgruppen automatisch in die Adobe Admin Console kopiert. Sie können dann in den Analytics Admin Tools keine Benutzer mehr einladen und keine neuen Gruppen mehr erstellen. Lesen Sie die häufig gestellten Fragen und die Hilfe unter „Analytics-Benutzermigration in die Adobe Admin Console“, um Informationen zur Vorbereitung der Migration und zu betroffenen administrativen Funktionen zu erhalten. |
| Starten der Adobe Admin Console | Nach der Migration Ihrer Benutzerkonten können Sie Benutzer und Produkte lösungsübergreifend in der Adobe Admin Console verwalten. Navigieren Sie zu: `https://adminconsole.adobe.com/enterprise/`. Siehe auch [Verwalten von Experience Cloud-Benutzern und -Produkten](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html?lang=de). |
| Verwalten von Adobe Analytics-Produktprofilen, -Benutzern und -Berechtigungen | Siehe auch [Analytics in der Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=de). |

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