---
description: In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung erteilen.
title: Hinzufügen einer Data Warehouse-Benutzergruppe
topic: Data warehouse
uuid: d89294db-caa3-4044-b70d-65b512b0dc1c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Hinzufügen einer Data Warehouse-Benutzergruppe

In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung erteilen.

1. Klicken Sie auf **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Benutzerverwaltung]**.
1. Click **[!UICONTROL Edit Groups]**.
1. Click **[!UICONTROL Add New User Group]**.
1. In the **[!UICONTROL Define User Group]** section, type a name in the Group Name field. Geben Sie die folgenden Gruppeninformationen ein:

   Beispiel, `Data Warehouse Access`.
1. Type a description in the **[!UICONTROL Group Description]** field.
1. Wählen Sie im Abschnitt **Report Suite-Zugriff** die Report Suites aus, auf die Gruppenmitglieder zugreifen sollen.
1. Aktivieren Sie unter [!UICONTROL Tools]**die Option[!UICONTROL Alle Tools]**.

   Alternatively, click **[!UICONTROL Customize]**, then enable **[!UICONTROL Custom Data Warehouse Report]**.

1. Fügen Sie unter [!UICONTROL Benutzeranmeldungen zuweisen] die gewünschten Benutzeranmeldungen hinzu.
1. Klicken Sie auf **[!UICONTROL Gruppe speichern]**.

   Wenn sich die Benutzer, die dieser Gruppe hinzugefügt wurden, das nächste Mal anmelden, sehen sie die Data Warehouse-Option als zusätzlichen Eintrag im Menü [!UICONTROL Reports &amp; Analytics].

   >[!NOTE]
   >
   >Bei Berechtigungen, die in Konflikt zueinander stehen (z. B. wenn ein Benutzer zwei Gruppen zugewiesen ist, von denen eine den Zugriff auf eine Funktion verweigert und die andere den gleichen Zugriff gewährt), beschränkt das System die Berechtigungen. Benutzer in Gruppen, die den Data Warehouse-Zugriff nicht erlauben, müssen unter Umständen aus diesen Gruppen entfernt werden.

>[!MORELIKETHIS]
>
>* [Gruppen](/help/admin/user-management2/c-user-groups/groups.md)

