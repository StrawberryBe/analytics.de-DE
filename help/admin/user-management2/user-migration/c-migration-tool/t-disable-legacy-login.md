---
description: Erfahren Sie, wie Sie vormalige Logins für Analytics-Benutzer deaktivieren können.
seo-description: Erfahren Sie, wie Sie vormalige Logins für Analytics-Benutzer deaktivieren können.
seo-title: Bisherige Anmeldedaten deaktivieren
title: Bisherige Anmeldedaten deaktivieren
uuid: 085874b2-10bf-4a56-a337-f3104428d71e
translation-type: tm+mt
source-git-commit: 56d27762320a752dff6ab4d9d763bbbf6e0deff5

---


# Bisherige Anmeldedaten deaktivieren{#disable-legacy-logins}

Erfahren Sie, wie Sie vormalige Logins für Analytics-Benutzer deaktivieren können.

Nachdem Ihre Benutzer von dem bisherigen Analytics User Management-System zur Adobe Admin Console migriert wurden, können Sie deren bisherige Anmeldedaten deaktivieren. Das Deaktivieren von bisherigen Logins leitet Benutzer zum Experience Cloud-Login um, wenn sie versuchen, das bisherige Login zu verwenden.

1. Open the Migration tool in **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL User ID Migration]**.
1. In the [!DNL User Information] section, locate the domain containing the users you want to work with, then click **[!UICONTROL Select Users]**.
1. Wählen Sie die Benutzer mit bisherigen Anmeldedaten aus, die Sie deaktivieren möchten.

   ![](assets/user-info.png)

   Die Benutzer, die berechtigt sind, haben in der Spalte Migrationsstatus den Status *`Migrated`* . Sie können die bisherigen Anmeldedaten von Benutzern erst deaktivieren, wenn sie migriert wurden.
1. Click **[!UICONTROL Disable Legacy Login]**, then click **[!UICONTROL Done]**.

   Bisherige Anmeldedaten deaktivieren gibt an, welcher Ihrer Benutzer seinen alten [!DNL my.omniture.com]-Benutzernamen und sein Passwort weiterhin verwenden kann.

   Sie können bisherige Logins für einen Benutzer, der noch nicht migriert wurde, nicht deaktivieren. Nach der Deaktivierung muss sich der Benutzer mit seiner Experience Cloud ID anmelden und auf Analytics zugreifen.

