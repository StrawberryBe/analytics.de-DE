---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anforderung erstellen.
title: Allgemeine Einstellungen für Data Warehouse-Anfragen
feature: Data Warehouse
exl-id: f564d5a9-78a2-431e-987a-78c4b0b9d31e
source-git-commit: baac0c0384b714cf2ca536149ca10eec3a7065ad
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 24%

---

# Allgemeine Einstellungen für Data Warehouse-Anfragen

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Im Folgenden wird beschrieben, wie Sie allgemeine Einstellungen für die Anfrage konfigurieren.

Informationen zum Erstellen einer Anforderung sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

So konfigurieren Sie allgemeine Einstellungen für eine Data Warehouse-Anforderung:

1. Erstellen einer Data Warehouse-Anforderung in Adobe Analytics durch Auswahl von **[!UICONTROL Instrumente]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**].

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite Neue Data Warehouse-Anforderung die [!UICONTROL **Allgemeine Einstellungen**] Registerkarte.

   ![Berichtsziel-Tab](assets/dw-general-settings.png)

1. Füllen Sie die folgenden Felder aus:

   | Option | Funktion |
   |---------|----------|
   | Anfragename | Dieser Name wird auf der Hauptseite der Data Warehouse angezeigt, wenn Anforderungen verwaltet werden. |
   | Datumsbereiche | Wählen Sie den Datumsbereich aus, der in den Bericht aufgenommen werden soll. <p>Sie können benutzerdefinierte Datumswerte oder einen vordefinierten Datumsbereich auswählen. Vorgabenbereiche beziehen sich auf das Datum des Berichtversands.</p><p>Die folgenden voreingestellten Optionen sind verfügbar:</p><ul><li>Am aktuellen Tag</li><li>Am Vortag</li><li>Letzte 7 Tage</li><li>Letzte 30 Tage</li><li>Diese Woche</li><li>Letzte Woche</li><li>Letzte 2 Wochen</li><li>Letzte 3 Wochen</li><li>Letzte 4 Wochen</li><li>Diesen Monat</li><li>Letzter Monat</li><li>Letzte Stunde</li></ul> |
   | Granularität | <!--what does this setting do? It's not the schedule/frequency... --> Die Zeitgranularität. Gültige Werte sind „Keine“, „Stunde“, „Tag“, „Woche“, „Monat“, „Quartal“ und „Jahr“.<p>Die Berichtgranularität verlängert die Verarbeitungszeit. Wenn Sie die monatliche Granularität über ein ganzes Jahr in einem Bericht darstellen, so wird der Bericht erheblich schneller verarbeitet, wenn Sie je eine Berichtanforderung für jeden Monat senden.</p> |
   | Für Benutzende in Ihrer Organisation verfügbar machen | Alle Data Warehouse-Anforderungen sind nur für Sie und alle Systemadministratoren sichtbar. Aktivieren Sie diese Option, wenn Sie die Anforderung für alle Mitarbeiter in Ihrer Organisation sichtbar machen möchten. <p>Die Aktivierung dieser Option ist nützlich, wenn Sie möchten, dass andere Benutzer in Ihrer Organisation beim Erstellen oder Aktualisieren der Anforderung helfen.</p> |

   {style="table-layout:auto"}

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der [!UICONTROL **Bericht erstellen**] Registerkarte. Weitere Informationen finden Sie unter [Erstellen eines Berichts für eine Data Warehouse-Anforderung](/help/export/data-warehouse/create-request/dw-request-build-report.md).
