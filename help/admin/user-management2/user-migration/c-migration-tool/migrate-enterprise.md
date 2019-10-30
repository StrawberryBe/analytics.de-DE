---
description: So migrieren Sie Analytics-Benutzerkonten als Enterprise IDs oder Federated IDs in die Admin Console.
seo-description: So migrieren Sie Analytics-Benutzerkonten als Enterprise IDs oder Federated IDs in die Admin Console.
seo-title: Migrieren von Analytics-Benutzerkonten für Enterprise und Federated IDs
title: Migrieren von Analytics-Benutzerkonten für Enterprise und Federated IDs
uuid: f90bf78a-5603-4bef-b714-13215301187c
translation-type: tm+mt
source-git-commit: ae18932eda59c059e2aa635cc30f233b88840031

---


# Migrieren von Analytics-Benutzerkonten für Enterprise und Federated IDs{#migrate-analytics-user-accounts-for-enterprise-and-federated-ids}

So migrieren Sie Analytics-Benutzerkonten als Enterprise IDs oder Federated IDs in die Admin Console.

## Voraussetzungen {#prereqs}

Voraussetzungen für das User Management mit der Admin Console.

Bei neuen Domänen und Verzeichnissen folgen Sie den Schritten bis:

* Verzeichnis einrichten
* Domänen einrichten
* Domänen mit Verzeichnissen verknüpfen

Vgl. als Hilfe [Einrichten eines Identitätssystems](https://helpx.adobe.com/enterprise/using/set-up-identity.html).

Wenn ein Verzeichnis bereits in einer anderen Organisation von einer anderen Geschäftseinheit oder einem anderen Team erstellt wurde, führen Sie die Schritte unter [Vertrauenswürdiges Verzeichnis](https://helpx.adobe.com/enterprise/using/set-up-identity.html#Directorytrusting) durch, um das Verzeichnis in der Organisation zu erstellen, für die Sie Analytics verwenden.

## Migrieren von-Benutzerkonten für Enterprise IDs und Federated IDs {#task-0cfb3e4400fd4ab58e4d9704528b05fa}

Diese Vorgehensweise ermöglicht Ihnen Folgendes:

* Download a user login list from **[!UICONTROL Analytics]** &gt; **[!UICONTROL Analytics Users &amp; Assets]**.

* Download a current users list from the **[!UICONTROL Admin Console]** &gt; **[!UICONTROL Users]**.

* Vergleichen Sie die Listen und suchen Sie nach Duplikaten, um das Überschreiben von Kontodaten in der Admin Console zu vermeiden.
* Upload a finished [!DNL .csv] (from **[!UICONTROL Admin Console]** &gt; **[!UICONTROL Users]**) with Enterprise ID or Federated ID users to the Admin Console.

Wenn Sie bestehende Adobe ID-Benutzerkonten auf eine Enterprise ID oder Federated ID migrieren möchten, wenden Sie sich an die Adobe-Kundenunterstützung und fordern Sie einen [Massenwechsel von Benutzeridentitäten](https://helpx.adobe.com/enterprise/using/bulk-operations.html) an.

**Benutzerkonten migrieren**

1. Laden Sie die Datei mit Analytics-Benutzeranmeldungen ([!DNL User Logins List.tab]) aus dem Analytics User Management herunter, und zwar mit einer der folgenden Methoden (je nachdem, ob Sie bereits Benutzer migriert haben). 
   1. *Navigieren Sie vor der Migration zu***Admin&gt;****Benutzerverwaltung (Legacy)&gt; Benutzer****bearbeitenund klicken Sie dann auf Bericht****herunterladen** .

      ![](assets/download-report.png)

      Der Link „Bericht herunterladen“ wird nur für Kunden angezeigt, die nicht-migrierte Benutzer haben.

   1. *Wenn Sie bereits Benutzer migriert haben,* navigieren Sie zu **[!UICONTROL Analytics]** &gt; **[!UICONTROL Analytics-Benutzer und -Elemente]**.

      ![Schritt-Info](assets/admin-analytics-users-assets.png)

   1. On the [!DNL Users] page, select users, then click **[!UICONTROL Export to CSV]**.

      ![Schritt-Info](assets/export-csv-migrate.png)

   1. Open the downloaded [!DNL User List.csv] file in Excel.

      Seien Sie bereit, die Werte *`Email`*, *`First Name`* und *`Last Name`* in eine [!DNL sample.csv] Datei zu kopieren (siehe nächsten Schritt).

      > [!IMPORTANT] Die Werte in der CSV-Datei müssen durch Kommas getrennt sein.

      > [!TIP] In diesem Schritt empfiehlt Adobe, Ihre Benutzerliste zu optimieren, um sicherzustellen, dass nur die Benutzer mit einer gültigen E-Mail-ID in die Migration der Enterprise ID oder Federated ID einbezogen werden.

1. Laden Sie in der Admin Console eine Liste der Benutzer der Admin Console herunter:

   1. Navigate to [Admin Console](http://adminconsole.adobe.html/#) &gt; **[!UICONTROL Users]**, then click [Export users list to CSV](https://helpx.adobe.com/enterprise/using/users.html).

      ![](assets/export-csv.png)

   1. Compare the two files: the existing Admin Console users in the exported [!DNL .csv] file ( [!DNL sample.csv], in this example) with the users in the Analytics [!DNL User Logins List.csv] file.

      > [!IMPORTANT] Wenn Sie Duplikate finden, löschen Sie sie aus der Analytics- [!DNL User Logins List.csv] Datei. Dieser Schritt verhindert das Überschreiben vorhandener Experience Cloud-Benutzerberechtigungen in der Admin Console und erstellt Ihnen eine Liste der zu migrierenden Konten.

1. Laden Sie die CSV-Vorlage von der Admin Console herunter:
   1. On the Users tab, click **[!UICONTROL Add users by CSV]**, then **[!UICONTROL Download CSV Template]**.

      ![Schritt-Info](assets/add-users-csv.png)

   1. Choose **[!UICONTROL Standard Template]**.

      In diesem Schritt wird eine Vorlagendatei mit dem Namen [!DNL sample.csv] heruntergeladen.

      ![](assets/download-csv-template.png)

1. Kopieren Sie die *`Email`*-, *`First Name`*- und *`Last Name`* -Spaltenwerte aus [!DNL User Logins List.tab] den entsprechenden Spalten in der [!DNL sample.csv] Vorlage.

   **Beispiel für eine Vorlagendatei**

   ![](assets/sample.png)

1. Ergänzen Sie in der Vorlage [!DNL sample.csv] die folgenden Pflichtfelder:

<table id="table_1B5EEFDB5BD8436EB760BE5FFAB1CF02"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feld </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>E-Mail </p> </td> 
   <td colname="col2"> <p>Kopiert aus <span class="filepath">User Logins List.tab</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vorname </p> </td> 
   <td colname="col2"> <p>Kopiert aus <span class="filepath">User Logins List.tab</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nachname </p> </td> 
   <td colname="col2"> <p>Kopiert aus <span class="filepath">User Logins List.tab</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Identitätstyp </p> </td> 
   <td colname="col2"> <p><span class="term"> Federated ID</span> oder <span class="term"> Enterprise ID</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Domäne </p> </td> 
   <td colname="col2"> <p>Achten Sie darauf, dass die Spalten Die Spalte " <span class="term"> Domäne</span> "und " <span class="term"> E-Mail</span> "entsprechen den Domänen, die in den <a href="/help/admin/user-management2/user-migration/c-migration-tool/migrate-enterprise.md#prereqs" format="dita" scope="local"> Voraussetzungen</a>festgelegt wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ländercode </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

For more information about the fields in the [!DNL .csv] file, see [CSV file format](https://helpx.adobe.com/enterprise/using/users.html).

> [!NOTE] Andere Spalten, z. B. *`Product Configurations`* und *`Admin Roles`* können leer sein.

1. On the Users tab in the Admin Console, upload the template file by clicking **[!UICONTROL Add users by CSV]** (as shown in Step 3.).
1. Führen Sie in Analytics das Migrationswerkzeug aus (wie unter Analytics- [Benutzerkonten](/help/admin/user-management2/user-migration/c-migration-tool/t-migrate-users.md)migrieren beschrieben).
1. Click **[!UICONTROL Migrate]** &gt; **[!UICONTROL Migrate as Enterprise IDs]**.

   ![Schritt-Info](assets/migrate-as-enterprise.png)

   When you click **[!UICONTROL Migrate]**, user are linked to the Enterprise ID/Federated ID account in Admin Console. The permissions of the legacy user account in Analytics will match the permissions granted to the Enterprise/Federated ID login in **[!UICONTROL Admin Console]** &gt; **[!UICONTROL Analytics]** &gt; **[!UICONTROL Product Profiles]**. Die Benutzer-ID wird im Bereich Migration abgeschlossen angezeigt. Sie können die bisherigen [!DNL my.omniture.com]-Zugriffsdaten nun deaktivieren.

   After migrating users, the status under the Migration Status column changes from *`Not Initiated`* to *`Migrated`*.

   Auch Adobe ID-Benutzer, die im Migrationstool erscheinen, können in diesem Prozess migriert werden. Sie müssen sich weiterhin mit ihrer Adobe ID anmelden, bis ein Identitätswechsel durchgeführt ist. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Hilfe beim Identitätswechsel benötigen.
