---
description: In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung ermöglichen.
title: Hinzufügen einer Data Warehouse-Benutzergruppe
feature: Data Warehouse
uuid: d89294db-caa3-4044-b70d-65b512b0dc1c
exl-id: 8737ab60-2ad1-4795-808b-d0200078a333
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 96%

---

# Hinzufügen einer Data Warehouse-Benutzergruppe

In diesen Schritten wird beschrieben, wie Administratoren einer Benutzergruppe den Zugriff auf die Data Warehouse-Berichterstellung ermöglichen.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Benutzerverwaltung]**.
1. Klicken Sie auf **[!UICONTROL „Gruppen bearbeiten“]**.
1. Klicken Sie auf **[!UICONTROL „Neue Benutzergruppe hinzufügen“]**.
1. Geben Sie im Abschnitt **[!UICONTROL Benutzergruppe definieren]** einen Gruppennamen in das entsprechende Feld ein. Geben Sie die folgenden Gruppeninformationen ein:

   Beispiel: `Data Warehouse Access`.
1. Geben Sie eine Beschreibung in das Feld **[!UICONTROL Gruppenbeschreibung]** ein.
1. Wählen Sie im Abschnitt **[!UICONTROL Report Suite-Zugriff]** die Report Suites aus, auf die Gruppenmitglieder zugreifen sollen.
1. Aktivieren Sie unter [!UICONTROL Tools] die Option **[!UICONTROL Alle Tools]**.

   Alternativ können Sie auch auf **[!UICONTROL Benutzerspezifisch]** klicken und die Option **[!UICONTROL Benutzerspezifischer Data Warehouse-Bericht]** aktivieren.

1. Fügen Sie unter [!UICONTROL Benutzeranmeldungen zuweisen] die gewünschten Benutzeranmeldungen hinzu.
1. Klicken Sie auf **[!UICONTROL Gruppe speichern]**.

   Wenn sich die Benutzer, die dieser Gruppe hinzugefügt wurden, das nächste Mal anmelden, sehen sie die Data Warehouse-Option als zusätzlichen Eintrag im Menü [!UICONTROL Reports &amp; Analytics].

   >[!NOTE]
   >
   >Wenn Berechtigungen in Konflikt zueinander stehen (z. B. wenn ein Benutzer zwei Gruppen zugewiesen ist und einer dieser Gruppen der Zugriff auf eine Funktion untersagt, der anderen jedoch gestattet ist), beschränkt das System die Berechtigungen. Benutzer in Gruppen, die den Data Warehouse-Zugriff nicht erlauben, müssen unter Umständen aus diesen Gruppen entfernt werden.

>[!MORELIKETHIS]
>
>* [Gruppen](/help/admin/user-management2/c-user-groups/groups.md)

