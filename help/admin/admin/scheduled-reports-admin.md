---
description: Damit können Administratoren terminierte Berichte für die ganze Organisation anzeigen und verwalten.
seo-description: Damit können Administratoren terminierte Berichte für die ganze Organisation anzeigen und verwalten.
seo-title: Warteschlange für geplante Berichte
solution: Analytics
title: Warteschlange für geplante Berichte
topic: 'Berichte    '
uuid: 3 fcf 92 d 3-a 472-465 f-ad 7 a-c 48 cd 9 a 8238 b
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Warteschlange für geplante Berichte

Damit können Administratoren terminierte Berichte für die ganze Organisation anzeigen und verwalten.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Komponenten]** &gt; **[!UICONTROL Geplante Berichte]**

Zu den Admin-spezifischen Fähigkeiten des Managers für terminierte Berichte gehören:

* Die Option [Alle terminierten Berichte anzeigen](../../admin/admin/scheduled-reports-admin.md#section_3F167CAAEEC24140B476CF95B7402690) für Ihre Organisation.
* [Erweiterte Filterfunktionen](../../admin/admin/scheduled-reports-admin.md#section_206A52A85DE84947AAB3AD082FBF6275) für die gesamte Organisation.
* Die neue Registerkarte [Berichtwarteschlange](../../admin/admin/scheduled-reports-admin.md#section_03C866115D354BB182E90BF4D52F1E0B) mit allen Berichten, die zur Ausführung auf Berichtsservern in die Warteschlange gestellt wurden.
* Anzeige der [Zeitplan-ID](../../admin/admin/scheduled-reports-admin.md#section_568B70F4228C4229977CB85D2DCD53A1) in der Benutzeroberfläche der Berichtwarteschlange.

## Alle terminierten Berichte anzeigen {#section_3F167CAAEEC24140B476CF95B7402690}

In der Registerkarte **[!UICONTROL Berichtsliste]** können Sie neben den von Ihnen terminierten Berichten mit der Option **Alle terminierten Berichte anzeigen]alle terminierten Berichte in Ihrer Organisation anzeigen.[!UICONTROL **

>[!NOTE]
>
>The **[!UICONTROL Report Name]** column displays the name of the report which is being scheduled and the **[!UICONTROL File Name]** column displays any custom file name set by you in Advanced Delivery Options. In Folge zeigt der Manager für terminierte Berichte mehrere Einträge mit dem gleichen Berichtsnamen, aber unterschiedlichen Dateinamen an, wenn Sie mehrere Berichte des gleichen Berichtstyps terminieren und jeweils benutzerdefinierte Namen angeben. Das liegt daran, dass der terminierte Back-End-Bericht identisch ist, so dass die Spalte „Berichtsname“ dieselben Berichtsnamen für alle außer den (festgelegten) benutzerdefinierten Dateinamen enthalten würde.

![](assets/show_all_scheduled_reports.png)

## Erweiterte Filterfunktionen {#section_206A52A85DE84947AAB3AD082FBF6275}

For example, if you wanted to filter on all reports that are scheduled hourly, you would specify **[!UICONTROL Frequency equals Hourly]** in the **[!UICONTROL Advanced]** filter and click **[!UICONTROL Apply]**:

![](assets/advanced_filtering_schedl_reports.png)

## Berichtwarteschlange {#section_03C866115D354BB182E90BF4D52F1E0B}

In dieser Warteschlange können Sie alle terminierten Berichte verwalten und nach Bedarf terminierte Berichte löschen, die die Warteschlange blockieren. (Normalerweise tritt nach vier Stunden ein Timeout bei Berichten auf.)

![](assets/scheduled_reports_2.png)

Die Berichtwarteschlange bietet außerdem die Option „Terminierten Bericht einmal überspringen“. Klicken Sie einfach auf das blaue Symbol in der Spalte **[!UICONTROL Verwalten].**

## Zeitplan-ID {#section_568B70F4228C4229977CB85D2DCD53A1}

Die Anzeige der **[!UICONTROL Zeitplan-ID]in der Benutzeroberfläche der Berichtwarteschlange ist nützlich, wenn Sie den Kundendienst von Adobe kontaktieren müssen, um ein Problem mit terminierten Berichten zu lösen.**

![](assets/schedule_id.png)
