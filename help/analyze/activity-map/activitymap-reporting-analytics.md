---
description: Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.
seo-description: Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.
seo-title: Activity Map-Berichterstellung in Analytics
solution: Analytics
title: Activity Map-Berichterstellung in Analytics
topic: Activity Map
uuid: 057 c 6 ab 2-aa 06-4779-ac 16-f 9 b 367 d 9 ea 43
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Activity Map-Berichterstellung in Analytics

Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.

## Set permissions {#section_BDCD9914B31A4066A50D23DDDF1ABB37}

Bevor Anwender Berichte zu Activity Map-Abmessungen erstellen können, müssen Sie als der Administrator

* [Der Activity Map Access Group Anwender hinzufügen](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md).
* Report Suites hinzufügen, die auf diese Gruppe zugreifen können sollen. Navigate to **[!UICONTROL Admin]** &gt; **[!UICONTROL User Management]** &gt; **[!UICONTROL Groups]** &gt; **[!UICONTROL Activity Map Access]** &gt; **[!UICONTROL Edit]**.
* Den Anwenderzugriff auf Abmessungen anpassen. Weitere Informationen dazu finden Sie im unten stehenden Abschnitt.

## Analytics Activity Map dimensions {#section_9395A7A5585F4ABE9F7C6CD0124B02A5}

Sie können den [Anwenderzugriff auf Abmessungen](https://marketing.adobe.com/resources/help/en_US/reference/groups-dimensions.html) auf einer detaillierteren Ebene anpassen. In Analytics verfügbare Activity Map-Abmessungen:

| Dimension | Beschreibung |
|---|---|
| Activity Map-Seite | Führt die Seiten auf, auf denen auf einen Link geklickt wurde. |
| Activity Map-Region | Listet alle erfassten Linkregionen auf der gesamten Website auf. Beachten Sie, dass die Metrik über alle Seiten hinweg erfasst wird, wenn eine Region auf mehreren Seiten angezeigt wird. |
| Activity Map-Links | Listet alle erfassten Links auf der gesamten Website auf. |
| Activity Map-Links und -Region | Listet alle erfassten Links zusammen mit ihrer Region über die gesamte Website hinweg auf. |
| Activity Map XY | Nicht verwendet |

* Diese Abmessungen sollten in Analysis Workspace, Reports &amp; Analytics und Report Builder verfügbar sein, sofern Ihre Analytics-Implementierung [für Activity Map aktiviert ist](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md).
* In Reports &amp; Analytics, navigate to **[!UICONTROL View All Reports]** &gt; **[!UICONTROL Activity Map]**.

* Um einen Link und eine Region für eine bestimmte Seite anzusehen, müssen Sie nur eine Aufschlüsselung der gewünschten Activity Map-Seite erstellen, der die Activity Map-Links und -Region enthält.

