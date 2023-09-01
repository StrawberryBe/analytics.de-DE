---
description: Erfahren Sie, wie Sie im Offline-Modus Platzhalterdaten zurückgeben können.
title: Aktivieren des Offline-Modus
uuid: 4eb1f754-b6da-4896-a64f-b737563925b8
feature: Report Builder
role: User, Admin
exl-id: f18859e3-19e4-48af-963f-0bb4d1b46380
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 42%

---

# Offline-Modus zum Erstellen und Bearbeiten von Anforderungen

Im Offline-Modus werden Platzhalterdaten zurückgegeben, um das Erstellen und Bearbeiten von Anfragen zu beschleunigen.

Wenn Sie eine neue Anforderung erstellen oder bearbeiten, werden Berichts-API-Aufrufe durchgeführt, um die Antwort abzurufen. Manchmal verlangsamen diese Aufrufe den Prozess der Anforderungserstellung, da Sie warten müssen, bis die Daten zurückgegeben werden, bevor Sie zum nächsten Schritt übergehen. Im Offline-Modus werden nur Platzhalterdaten zurückgegeben und die API wird nicht ausgeführt.

So aktivieren Sie den Offline-Modus

1. Klicken Sie im Report Builder-Menü auf **[!UICONTROL Optionen]**.

   ![Screenshot des Bildschirms Optionen mit ausgewähltem Offline-Code.](assets/offline_mode.png)

1. Aktivieren Sie neben **[!UICONTROL Aktivieren Sie den Offline-Modus, um Anforderungen zu erstellen und zu bearbeiten]** das Kontrollkästchen.
1. Geben Sie im Feld **[!UICONTROL Metrikdaten anzeigen als]** die Platzhalterdaten ein, die bei Ihrer Anforderung zurückgegeben werden sollen. Geben Sie zum Beispiel „1“ ein.
1. Klicken Sie auf **[!UICONTROL OK]**.
1. Erstellen und führen Sie Ihre Anforderung im Offline-Modus mit dem Anforderungs-Assistenten aus. Der folgende Screenshot zeigt ein Beispiel einer Anfrage mit &quot;1&quot;als Platzhalterdaten.

   ![Screenshot mit dem Beispiel des Offline-Modus unter Verwendung von 1 als Platzhalter.](assets/offline_mode_example.png)

   >[!IMPORTANT]
   >
   >Stellen Sie sicher, dass Sie den Offline-Modus deaktiviert haben, bevor Sie Ihre Anfragen mit echten Daten ausführen.
