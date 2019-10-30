---
description: Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.
seo-description: Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.
seo-title: '[!DNL Activity Map]-Berichte in Analytics'
solution: Analytics
title: '[!DNL Activity Map]-Berichte in Analytics'
topic: Activity Map
uuid: 057c6ab2-aa06-4779-ac16-f9b367d9ea43
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# [!DNL Activity Map] Berichterstellung in Analytics

Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.

## Set permissions {#section_BDCD9914B31A4066A50D23DDDF1ABB37}

Before users can report on [!DNL Activity Map] dimensions, you as the Admin need to

* [Fügen Sie Benutzer zur Zugriffsgruppe](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)[!DNL Activity Map] hinzu.
* Report Suites hinzufügen, die auf diese Gruppe zugreifen können sollen. Navigate to **[!UICONTROL Admin]** &gt; **[!UICONTROL User Management]** &gt; **[!UICONTROL Groups]** &gt; **[!UICONTROL [!DNL Activity Map]Access]** &gt; **[!UICONTROL Edit]**.
* Den Anwenderzugriff auf Abmessungen anpassen. Weitere Informationen dazu finden Sie im unten stehenden Abschnitt.

## Analytics- [!DNL Activity Map] Dimensionen {#section_9395A7A5585F4ABE9F7C6CD0124B02A5}

Sie können den [Anwenderzugriff auf Abmessungen](https://marketing.adobe.com/resources/help/en_US/reference/groups-dimensions.html) auf einer detaillierteren Ebene anpassen. Here are the [!DNL Activity Map] dimensions available in Analytics:

| Dimension | Beschreibung |
|---|---|
| [!DNL Activity Map] Seite | Führt die Seiten auf, auf denen auf einen Link geklickt wurde. |
| [!DNL Activity Map] Region | Listet alle erfassten Linkregionen auf der gesamten Website auf. Beachten Sie, dass die Metrik über alle Seiten hinweg erfasst wird, wenn eine Region auf mehreren Seiten angezeigt wird. |
| [!DNL Activity Map] Links | Listet alle erfassten Links auf der gesamten Website auf. |
| [!DNL Activity Map] Links und Region | Listet alle erfassten Links zusammen mit ihrer Region über die gesamte Website hinweg auf. |
| [!DNL Activity Map] XY | Nicht verwendet |

* Diese Abmessungen sollten in Analysis Workspace, Reports &amp; Analytics und Report Builder verfügbar sein, sofern Ihre Analytics-Implementierung [enabled for [!DNL Activity Map]](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md).
* In Reports &amp; Analytics, navigate to **[!UICONTROL View All Reports]** &gt; **[!UICONTROL [!DNL Activity Map]]**.

* To look at a link and region for a specific page, all you need to do is create a breakdown from the desired [!DNL Activity Map] page into the [!DNL Activity Map] Links &amp; Region.

