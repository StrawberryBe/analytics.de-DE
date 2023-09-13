---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anforderung erstellen.
title: Berichtsziel für eine Data Warehouse-Anforderung konfigurieren
feature: Data Warehouse
source-git-commit: 3b116cb8d0d3f3eb86b512d712f37b29876f2b22
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 15%

---

# Planungsoptionen für Data Warehouse-Anfragen konfigurieren

>[!AVAILABILITY]
>
>Einige der in diesem Artikel beschriebenen Data Warehouse-Funktionen (und andere Data Warehouse-Artikel in diesem Abschnitt) sind nur in der Phase der eingeschränkten Testphase der Veröffentlichung verfügbar und sind möglicherweise noch nicht in Ihrer Umgebung verfügbar.
>
>Informationen darüber, welche Funktionen noch nicht für alle Kunden verfügbar sind, sowie Informationen über die Veröffentlichungszeitleiste dieser Funktionen finden Sie in der [Versionshinweise](/help/release-notes/latest.md).
>
>Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Im Folgenden wird beschrieben, wie Sie Planungsoptionen für die Anfrage konfigurieren.

Informationen zum Erstellen einer Anforderung sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

So konfigurieren Sie Planungsoptionen für eine Data Warehouse-Anforderung:

1. Erstellen einer Anforderung in Adobe Analytics durch Auswahl von **[!UICONTROL Instrumente]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**].

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite Neue Data Warehouse-Anforderung die [!UICONTROL **Planungsoptionen**] Registerkarte.

   ![Berichtsziel-Tab](assets/dw-scheduling-options.png) <!-- update screenshot -->

1. Füllen Sie die folgenden Felder aus:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Bericht jetzt senden**] | Sendet den Bericht als einmaligen Bericht. Wenn diese Option aktiviert ist, werden alle Planungsoptionen ausgeblendet. |
   | [!UICONTROL **Für später einplanen**] | Bietet Optionen zur Planung der Berichtbereitstellung. Alle Optionen werden nachfolgend beschrieben. |
   | [!UICONTROL **Berichtshäufigkeit**] | Die Häufigkeit der Bereitstellung von Berichten. <p>Die folgenden Optionen sind verfügbar:</p><ul><li>Stündlich</li><p>[!UICONTROL **Stündlich**] ist nur verfügbar, wenn die [!UICONTROL **Datumsbereiche**] -Option auf [!UICONTROL **Allgemeine Einstellungen**] Registerkarte auf [!UICONTROL **Letzte Stunde**].</p><li>Täglich</li><li>Wöchentlich</li><li>Monatlich</li><li>Jährlich</li></ul><p>Je nach der ausgewählten Häufigkeit werden weitere Optionen angezeigt.</p> |
   | [!UICONTROL **Startet am**] | Das Datum, an dem der neue Zeitplan beginnen soll. |
   | [!UICONTROL **Tageszeit**] | Die Tageszeit, zu der der Bericht gesendet werden soll. |
   | [!UICONTROL **Versandoptionen beenden**] | Wählen Sie aus, wann die geplanten Sendungen beendet werden sollen. Sie können festlegen, dass niemals ein Ende, ein Ende nach einer bestimmten Anzahl von Vorkommnissen oder ein Ende an einem bestimmten Datum erfolgen soll. |

   {style="table-layout:auto"}

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der [!UICONTROL **Benachrichtigungs-E-Mail**] Registerkarte. Weitere Informationen finden Sie unter [Benachrichtigungs-E-Mail für eine Data Warehouse-Anfrage konfigurieren](/help/export/data-warehouse/create-request/dw-request-email.md).

