---
description: In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung erteilen.
seo-description: In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung erteilen.
seo-title: Hinzufügen einer Data Warehouse-Benutzergruppe
solution: Analytics
title: Hinzufügen einer Data Warehouse-Benutzergruppe
topic: Data Warehouse
uuid: d 89294 db-caa 3-4044-b 70 d -65 b 512 b 0 dc 1 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Hinzufügen einer Data Warehouse-Benutzergruppe

In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung erteilen.

1. Click **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL User Management]**.
1. Click **[!UICONTROL Edit Groups]**.
1. Click **[!UICONTROL Add New User Group]**.
1. In the **[!UICONTROL Define User Group]** section, type a name in the Group Name field. Geben Sie die folgenden Gruppeninformationen ein:

   Beispiel, `Data Warehouse Access`.
1. Type a description in the **[!UICONTROL Group Description]** field.
1. Wählen Sie im Abschnitt **Report Suite-Zugriff** die Report Suites aus, auf die Gruppenmitglieder zugreifen sollen.
1. Aktivieren Sie unter [!UICONTROL Tools]**die Option[!UICONTROL Alle Tools]**.

   Alternatively, click **[!UICONTROL Customize]**, then enable **[!UICONTROL Custom Data Warehouse Report]**.

1. Fügen Sie unter [!UICONTROL Benutzeranmeldungen zuweisen] die gewünschten Benutzeranmeldungen hinzu.
1. Click **[!UICONTROL Save Group]**.

   Wenn sich die Benutzer, die dieser Gruppe hinzugefügt wurden, das nächste Mal anmelden, sehen sie die Data Warehouse-Option als zusätzlichen Eintrag im Menü [!UICONTROL Reports &amp; Analytics].

   >[!NOTE]
   >
   >Im Falle von Zugriffsberechtigungen (z. B. einem Benutzer, der zwei Gruppen zugewiesen ist, von denen einer den Zugriff auf eine Funktion untersagt und die andere diesen Zugriff gestattet), beschränkt das System die Berechtigungen. Benutzer in Gruppen, die den Data Warehouse-Zugriff nicht erlauben, müssen unter Umständen aus diesen Gruppen entfernt werden.

>[!MORE_LIKE_THIS]
>
>* [Gruppen](/help/admin/user-management2/c-user-groups/groups.md)

