---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anfrage erstellen.
title: Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage
feature: Data Warehouse
exl-id: e5f8acaa-156f-41fb-a0fc-bc5475f1f3b7
source-git-commit: 4e4b5e1c362778223be01f78b173a698c53f9b32
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 27%

---

# Planungsoptionen für Data Warehouse-Anfragen konfigurieren

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Im Folgenden wird beschrieben, wie Sie Planungsoptionen für die Anfrage konfigurieren.

Informationen zum Erstellen einer Anfrage sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

So konfigurieren Sie Planungsoptionen für eine Data Warehouse-Anforderung:

1. Beginnen Sie, falls noch nicht geschehen, mit der Erstellung einer Anforderung in Adobe Analytics, indem Sie **[!UICONTROL Instrumente]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**].

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite Neue Data Warehouse-Anforderung die [!UICONTROL **Planungsoptionen**] Registerkarte.

   ![Berichtsziel-Tab](assets/dw-scheduling-options.png) <!-- update screenshot -->

1. Füllen Sie die folgenden Felder aus:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Bericht jetzt senden**] | Sendet den Bericht als einmaligen Bericht. Wenn diese Option aktiviert ist, werden alle Planungsoptionen ausgeblendet. |
   | [!UICONTROL **Für später einplanen**] | Bietet Optionen zur Planung der Berichtbereitstellung. Alle Optionen werden nachfolgend beschrieben. |
   | [!UICONTROL **Berichtsfrequenz**] | Die Häufigkeit der Bereitstellung von Berichten. <p>Die folgenden Optionen sind verfügbar:</p><ul><li>Stündlich</li><p>[!UICONTROL **Stündlich**] ist nur verfügbar, wenn die [!UICONTROL **Datumsbereiche**] -Option auf [!UICONTROL **Allgemeine Einstellungen**] Registerkarte auf [!UICONTROL **Letzte Stunde**].</p><li>Täglich</li><li>Wöchentlich</li><li>Monatlich</li><li>Jährlich</li></ul><p>Je nach der ausgewählten Häufigkeit werden weitere Optionen angezeigt.</p> |
   | [!UICONTROL **Starten am**] | Das Datum, an dem der neue Zeitplan beginnen soll. |
   | [!UICONTROL **Tageszeit**] | Die Tageszeit, zu der der Bericht gesendet werden soll. |
   | [!UICONTROL **Optionen für den endgültigen Versand**] | Wählen Sie aus, wann die geplanten Sendungen beendet werden sollen. Sie können festlegen, dass niemals ein Ende, ein Ende nach einer bestimmten Anzahl von Vorkommnissen oder ein Ende an einem bestimmten Datum erfolgen soll. |

   {style="table-layout:auto"}

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der [!UICONTROL **Benachrichtigungs-E-Mail**] Registerkarte. Weitere Informationen finden Sie unter [Benachrichtigungs-E-Mail für eine Data Warehouse-Anfrage konfigurieren](/help/export/data-warehouse/create-request/dw-request-email.md).
