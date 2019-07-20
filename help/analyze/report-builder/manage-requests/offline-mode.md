---
description: Im Offline-Modus werden Platzhalterdaten zurückgegeben, um das Erstellen und Bearbeiten von Anforderungen zu beschleunigen.
seo-description: Im Offline-Modus werden Platzhalterdaten zurückgegeben, um das Erstellen und Bearbeiten von Anforderungen zu beschleunigen.
seo-title: Offline-Modus zum Erstellen und Bearbeiten von Anforderungen
solution: Analytics
title: Offline-Modus zum Erstellen und Bearbeiten von Anforderungen
topic: ReportBuilder
uuid: 4 eb 1 f 754-b 6 da -4896-a 64 f-b 375563925 b 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Offline-Modus zum Erstellen und Bearbeiten von Anforderungen

Im Offline-Modus werden Platzhalterdaten zurückgegeben, um das Erstellen und Bearbeiten von Anforderungen zu beschleunigen.

Wenn Sie eine neue Anforderung erstellen oder bearbeiten, werden Berichts-API-Aufrufe zum Abrufen der Antwort gestartet. Dadurch wird die Anforderungserstellung verlangsamt, weil Sie warten müssen, bis die Daten zurückgegeben werden, bevor Sie zum nächsten Schritt übergehen können. Im Offline-Modus werden nur Platzhalterdaten zurückgegeben; es müssen also keine API-Aufrufe gestartet werden.

So aktivieren Sie den Offline-Modus:

1. Klicken Sie im ReportBuilder-Menü auf **[!UICONTROL Optionen].**

   ![](assets/offline_mode.png)

1. Aktivieren Sie neben **[!UICONTROL Aktivieren Sie den Offline-Modus, um Anforderungen zu erstellen und zu bearbeiten. das Kontrollkästchen]**.
1. Geben Sie im Feld **[!UICONTROL Metrikdaten anzeigen als]die Platzhalterdaten ein, die bei Ihrer Anforderung zurückgegeben werden sollen.** Geben Sie zum Beispiel „1“ ein.
1. Klicken Sie auf **[!UICONTROL OK]**.
1. Nun können Sie mithilfe des Anforderungs-Assistenten Ihre Anforderung erstellen und ausführen (im Offline-Modus).
1. Ihre Anforderung, bei der Sie für die Platzhalterdaten „1“ eingegeben haben, wird etwa wie folgt aussehen:

   ![](assets/offline_mode_example.png)

   >[!IMPORTANT]
   >
   >Stellen Sie sicher, dass Sie den Offline-Modus deaktivieren, bevor Sie Ihre Anforderungen mit echten Daten ausführen. Hierfür gehen Sie einfach zurück zu **[!UICONTROL Optionen]und entfernen Sie den Haken.**

