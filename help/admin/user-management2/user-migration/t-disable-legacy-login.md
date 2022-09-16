---
description: Erfahren Sie, wie Sie vormalige Logins für Analytics-Benutzer deaktivieren können.
title: Deaktivieren von veralteten Anmeldedaten
feature: Admin Tools
exl-id: 3e619700-722d-429b-94dc-7aa162e114c0
source-git-commit: 0143496648e59e95c360388735def726e63ee71b
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---

# Deaktivieren von veralteten Anmeldedaten{#disable-legacy-logins}

Erfahren Sie, wie Sie vormalige Logins für Analytics-Benutzer deaktivieren können.

Nachdem Ihre Benutzer von dem bisherigen Analytics User Management-System zur Adobe Admin Console migriert wurden, können Sie deren bisherige Anmeldedaten deaktivieren. Das Deaktivieren von bisherigen Logins leitet Benutzer zum Experience Cloud-Login um, wenn sie versuchen, das bisherige Login zu verwenden.

1. Öffnen Sie das Migrationstool in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Benutzer-ID-Migration]**.
1. Suchen Sie im Abschnitt „[!DNL User Information]“ nach der Domain mit den Benutzern, mit denen Sie arbeiten möchten, und klicken Sie dann auf **[!UICONTROL Benutzer auswählen]**.
1. Wählen Sie die Benutzer mit bisherigen Anmeldedaten aus, die Sie deaktivieren möchten.

   ![](assets/user-info.png)

   Die Benutzer, die berechtigt sind, haben in der Spalte „Migrationsstatus“ den Status *`Migrated`*. Sie können die bisherigen Anmeldedaten von Benutzern erst deaktivieren, wenn sie migriert wurden.
1. Klicken Sie auf **[!UICONTROL Bisherige Anmeldedaten deaktivieren]** und dann auf **[!UICONTROL Fertig]**.

   „Bisherige Anmeldedaten deaktivieren“ gibt an, welcher Ihrer Benutzer seinen alten [!DNL my.omniture.com]-Benutzernamen und sein Passwort weiterhin verwenden kann.

   Sie können bisherige Logins für einen Benutzer, der noch nicht migriert wurde, nicht deaktivieren. Nach der Deaktivierung muss sich der Benutzer mit seiner Experience Cloud ID anmelden und auf Analytics zugreifen.
