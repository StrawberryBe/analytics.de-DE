---
description: Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Adobe Admin Console.
title: Migrieren von Analytics-Benutzerkonten für Adobe IDs
uuid: 734e9f14-ef8d-44de-8ff3-3ee6dfe0a214
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Migrieren von Analytics-Benutzerkonten für Adobe IDs {#migrate-analytics-user-accounts-for-adobe-ids}

Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Adobe Admin Console.

## Migrieren von Analytics-Benutzerkonten für Adobe IDs {#task-f3355f3b14a340feae58cfa04c0ba1c9}

Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Adobe Admin Console.

>[!NOTE] Versuchen Admins, die nicht über die Experience Cloud angemeldet sind, auf das Benutzer-ID-Migrationstool zuzugreifen, werden sie zur Experience Cloud-Anmeldeseite weitergeleitet.

**Migrieren von Analytics-Benutzern**

1. Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User ID Migration]**.

   ![](assets/migration-progress.png)

   Die Seite &quot;Benutzer-ID-Migration&quot;besteht aus zwei Abschnitten: *Migrationsfortschritt* und *Benutzerinformationen*.

   **Migrationsfortschritt**

   <table id="table_F9F1CFF762C745E198CB075A02BA2DDA"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Phase </th> 
      <th colname="col2" class="entry"> Beschreibung </th> 
   </tr>
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>Abgeschlossene Migrationen </p> </td> 
      <td colname="col2"> <p>Die Benutzer nahmen die Einladung an. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Alte Anmeldung deaktiviert </p> </td> 
      <td colname="col2"> <p>Die alte Anmeldung mit einer Firmen-ID ist deaktiviert. Benutzer können nun mit ihrer Adobe ID oder Enterprise ID auf die Experience Cloud zugreifen. Wenn alle Benutzer diese Phase erreicht haben, haben Sie die Migration abgeschlossen. </p> <p>Bei der Migration ist die bisherige Anmeldung deaktiviert. Benutzer werden zu <span class="filepath">experiencecloud.adobe.com</span> umgeleitet und müssen sich mit der Adobe ID oder Enterprise ID anmelden. </p> </td> 
   </tr> 
   </tbody> 
   </table>

   **Benutzerinformationen**

   In den Benutzerinformationen werden die Benutzer in Ihrer Organisation nach Domänennamen getrennt dargestellt.

   <table id="table_3822E27AF81E4A188562FEB5131548A5"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Element </th> 
      <th colname="col2" class="entry"> Beschreibung </th> 
   </tr>
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>Domäne </p> </td> 
      <td colname="col2"> <p>Domänen sind spezifisch für die E-Mail-IDs der aktuellen Analytics-Benutzerbasis. Eine Domäne kann nur von einem einzigen Unternehmen und nur durch Systemadministratoren in Anspruch genommen werden. Weitere Informationen finden Sie unter <a href="https://helpx.adobe.com/de/enterprise/help/request-access-to-claimed-domain.html">Anfordern des Zugriffs auf eine beanspruchte Domäne</a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Domäne angefordert </p> </td> 
      <td colname="col2"> <p>Wenn Sie Benutzer als Enterprise- oder Federated IDs migrieren möchten, müssen Sie Systemadministrator sein und eine verfügbare Domäne über die Admin Console anfordern, bevor Sie Benutzer migrieren können. <a href="https://helpx.adobe.com/de/enterprise/help/identity.html">Weitere Informationen</a>. </p> <p>Wenn Sie keine Domänen für Enterprise- oder Federated IDs anfordern möchten, überspringen Sie diesen Schritt und migrieren Sie Benutzer als Adobe IDs. Erfahren Sie <a href="https://helpx.adobe.com/de/enterprise/help/identity.html">hier</a> mehr über ID-Typen. </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Locate the domain containing the user IDs you want to migrate, then, under **[!UICONTROL Requiring Migration]**, click **[!UICONTROL Select Users]**.
1. On the [!DNL Users] page, select the users you want to migrate, then click **[!UICONTROL Migrate]**.

   When you click **[!UICONTROL Migrate]**, users receive an invitation (Migration Initiated) and must accept it. Dadurch wird die Benutzer-ID in die Kategorie „Migration abgeschlossen“ verschoben. Sie können dann die bisherigen `[!DNL my.omniture.com].`-Anmeldedaten deaktivieren

   ![](assets/user-info.png)

1. Geben Sie den Typ der ID an, die Sie für die Migration der Benutzer verwenden möchten (Adobe ID oder Enterprise ID)

   Nach der Migration von Benutzern ändert sich der Wert in der Spalte „Migrationsstatus“ von *`Not Initiated`* auf *`Migrated`*.

   Wenn *`Failed`* angezeigt wird, fahren Sie mit dem Maus über das Symbol, um den Grund für das Fehlschlagen der Migration anzuzeigen.
