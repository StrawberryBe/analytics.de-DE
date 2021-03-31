---
description: Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.
title: Activity Map – Berichterstattung in Analytics
uuid: 057c6ab2-aa06-4779-ac16-f9b367d9ea43
feature: Activity Map
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 98%

---


# Activity Map – Berichterstattung in Analytics

Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.

## Berechtigungen festlegen {#section_BDCD9914B31A4066A50D23DDDF1ABB37}

Bevor Anwender Berichte zu Activity Map-Abmessungen erstellen können, müssen Sie als der Administrator

* [Der Activity Map Access Group Anwender hinzufügen](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md).
* Report Suites hinzufügen, die auf diese Gruppe zugreifen können sollen. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Benutzerverwaltung]** > **[!UICONTROL Gruppen]** > **[!UICONTROL Activity Map-Zugriff]** > **[!UICONTROL Bearbeiten]**.
* Den Anwenderzugriff auf Abmessungen anpassen. Weitere Informationen dazu finden Sie im unten stehenden Abschnitt.

## Analytics Activity Map-Abmessungen {#section_9395A7A5585F4ABE9F7C6CD0124B02A5}

Sie können den [Anwenderzugriff auf Abmessungen](https://docs.adobe.com/content/help/de-DE/analytics/admin/user-product-management/customize-report-access/groups-dimensions.html) auf einer detaillierteren Ebene anpassen. In Analytics verfügbare Activity Map-Abmessungen:

| Dimension | Beschreibung |
|---|---|
| Activity Map-Seite | Führt die Seiten auf, auf denen auf einen Link geklickt wurde. |
| Activity Map-Region | Listet alle erfassten Linkregionen auf der gesamten Website auf. Beachten Sie, dass die Metrik über alle Seiten hinweg erfasst wird, wenn eine Region auf mehreren Seiten angezeigt wird. |
| Activity Map-Links | Listet alle erfassten Links auf der gesamten Website auf. |
| Activity Map-Links und -Region | Listet alle erfassten Links zusammen mit ihrer Region über die gesamte Website hinweg auf. |
| Activity Map XY | Nicht verwendet |

* Diese Abmessungen sollten in Analysis Workspace, Reports &amp; Analytics und Report Builder verfügbar sein, sofern Ihre Analytics-Implementierung  [für Activity Map aktiviert ist](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md).
* Navigieren Sie in Reports &amp; Analytics zu **[!UICONTROL Alle Berichte anzeigen]** > **[!UICONTROL Activity Map]**.

* Um einen Link und eine Region für eine bestimmte Seite anzusehen, müssen Sie nur eine Aufschlüsselung auf der gewünschten Activity Map-Seite nach „Activity Map-Links und -Region“ erstellen.

