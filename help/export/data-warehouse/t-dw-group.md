---
description: In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung ermöglichen.
title: Hinzufügen einer Data Warehouse-Benutzergruppe
topic: Data warehouse
uuid: d89294db-caa3-4044-b70d-65b512b0dc1c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Hinzufügen einer Data Warehouse-Benutzergruppe

In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung ermöglichen.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]**.
1. Klicken Sie auf **[!UICONTROL Edit Groups]**.
1. Klicken Sie auf **[!UICONTROL Add New User Group]**.
1. In the **[!UICONTROL Define User Group]** section, type a name in the Group Name field. Geben Sie die folgenden Gruppeninformationen ein:

   Beispiel: `Data Warehouse Access`.
1. Geben Sie eine Beschreibung in das **[!UICONTROL Group Description]** Feld ein.
1. In the **[!UICONTROL Report Suite Access]** section, select the report suites that you want group members to be able to access.
1. Aktivieren Sie [!UICONTROL Tools]unter **[!UICONTROL All Tools]**.

   Alternativ können Sie auf klicken **[!UICONTROL Customize]** und dann aktivieren **[!UICONTROL Custom Data Warehouse Report]**.

1. Fügen Sie unter [!UICONTROL Assign User Logins]dem Feld die gewünschten Benutzeranmeldungen hinzu.
1. Klicken Sie auf **[!UICONTROL Save Group]**.

   Wenn sich die Benutzer, die dieser Gruppe hinzugefügt wurden, das nächste Mal anmelden, sehen sie die Data Warehouse-Option als zusätzlichen Eintrag im Menü [!UICONTROL Reports & Analytics].

   >[!NOTE]
   >
   >Wenn Berechtigungen in Konflikt zueinander stehen (z. B. wenn ein Benutzer zwei Gruppen zugewiesen ist und einer dieser Gruppen der Zugriff auf eine Funktion untersagt, der anderen jedoch gestattet ist), beschränkt das System die Berechtigungen. Benutzer in Gruppen, die den Data Warehouse-Zugriff nicht erlauben, müssen unter Umständen aus diesen Gruppen entfernt werden.

>[!MORELIKETHIS]
>
>* [Gruppen](/help/admin/user-management2/c-user-groups/groups.md)

