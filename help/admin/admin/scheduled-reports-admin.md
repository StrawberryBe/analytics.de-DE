---
description: Damit können Administratoren terminierte Berichte für die ganze Organisation anzeigen und verwalten.
title: Warteschlange für terminierte Berichte
topic: Reports
uuid: 3fcf92d3-a472-465f-ad7a-c48cd9a8238b
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Warteschlange für terminierte Berichte

Damit können Administratoren terminierte Berichte für die ganze Organisation anzeigen und verwalten.

**[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Scheduled Reports]**

Zu den Admin-spezifischen Fähigkeiten des Managers für terminierte Berichte gehören:

* Die Option zum [Anzeigen aller terminierten Berichte](/help/admin/admin/scheduled-reports-admin.md#section_3F167CAAEEC24140B476CF95B7402690) in Ihrer Organisation.
* [Erweiterte Filterfunktionen](/help/admin/admin/scheduled-reports-admin.md#section_206A52A85DE84947AAB3AD082FBF6275) in Ihrer Organisation.
* Die neue Registerkarte [Berichtwarteschlange](/help/admin/admin/scheduled-reports-admin.md#section_03C866115D354BB182E90BF4D52F1E0B) , auf der alle Berichte Liste werden, die zur Ausführung auf Berichte-Servern in die Warteschlange gestellt werden.
* Anzeige der [Zeitplan-ID](/help/admin/admin/scheduled-reports-admin.md#section_568B70F4228C4229977CB85D2DCD53A1) in der Benutzeroberfläche der Berichtwarteschlange.

## Alle terminierten Berichte anzeigen {#section_3F167CAAEEC24140B476CF95B7402690}

Auf der **[!UICONTROL Report List]** Registerkarte können Sie zusätzlich zu den von Ihnen persönlich geplanten Aktivitäten auch **[!UICONTROL Show All Scheduled Reports]** in Ihrem Unternehmen arbeiten.

>[!NOTE] Die **[!UICONTROL Report Name]** Spalte zeigt den Namen des geplanten Berichts an. In der **[!UICONTROL File Name]** Spalte werden alle von Ihnen unter Erweiterte Versand-Optionen festgelegten benutzerdefinierten Dateinamen angezeigt. Wenn Sie daher mehrere Berichte desselben Berichtstyps planen und für jeden Bericht benutzerspezifische Namen angeben, zeigt der Manager für terminierte Berichte mehrere Einträge mit demselben Berichtsnamen, jedoch unterschiedlichen Dateinamen an. Der Grund dafür ist, dass der terminierte Back-End-Bericht identisch ist. Daher würde die Spalte Berichtsname dieselben Berichtsnamen für alle außer benutzerdefinierten Dateinamen haben (wie festgelegt).

![](assets/show_all_scheduled_reports.png)

## Erweiterte Filterfunktionen {#section_206A52A85DE84947AAB3AD082FBF6275}

For example, if you wanted to filter on all reports that are scheduled hourly, you would specify **[!UICONTROL Frequency equals Hourly]** in the **[!UICONTROL Advanced]** filter and click **[!UICONTROL Apply]**:

![](assets/advanced_filtering_schedl_reports.png)

## Berichtwarteschlange {#section_03C866115D354BB182E90BF4D52F1E0B}

Mit dieser Warteschlange können Sie terminierte Berichte verwalten und möglicherweise löschen, die die Warteschlange &quot;verstopfen&quot;. (Normalerweise wird für Berichte ein Timeout nach 4 Stunden durchgeführt.)

![](assets/scheduled_reports_2.png)

Die Berichtwarteschlange bietet Ihnen außerdem die Möglichkeit, einen terminierten Bericht einmal zu überspringen. Just click the blue icon in the **[!UICONTROL Manage]** column.

## Zeitplan-ID {#section_568B70F4228C4229977CB85D2DCD53A1}

Having the **[!UICONTROL Schedule ID]** exposed in the Report Queue interface helps when you need to contact Adobe Client Care for resolution of a scheduled reports issue.

![](assets/schedule_id.png)
