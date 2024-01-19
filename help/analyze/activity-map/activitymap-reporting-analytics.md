---
description: Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.
title: Activity Map – Berichterstattung in Analytics
feature: Activity Map
role: User, Admin
exl-id: 8d7be302-bdfc-4370-b8f0-ab1af1e439ca
source-git-commit: a979fc8787fa96f8fa8317996ac66341a6f54354
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 79%

---

# Activity Map – Berichterstattung in Analytics

Beschreibt, wie Berechtigungen festgelegt werden und welche Abmessungen in Analytics verfügbar sind.

## Berechtigungen festlegen {#permissions}

Bevor Anwender Berichte zu Activity Map-Abmessungen erstellen können, müssen Sie als der Administrator

* [Benutzer zum Produktprofil Activity Map-Zugriff hinzufügen](/help/analyze/activity-map/activitymap-getting-started/activitymap-enable.md).
* Den Anwenderzugriff auf Abmessungen anpassen. Weitere Informationen dazu finden Sie im unten stehenden Abschnitt.

## Analytics-Activity Map-Dimensionen {#dimensions}

Sie können den [Anwenderzugriff auf Abmessungen](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/customize-report-access/groups-dimensions.html) auf einer detaillierteren Ebene anpassen. In Analytics verfügbare Activity Map-Abmessungen:

| Dimension | Beschreibung |
|---|---|
| Activity Map-Seite | Führt die Seiten auf, auf denen auf einen Link geklickt wurde. |
| Activity Map-Region | Listet alle erfassten Linkregionen auf der gesamten Website auf. Beachten Sie, dass die Metrik über alle Seiten hinweg erfasst wird, wenn eine Region auf mehreren Seiten angezeigt wird. |
| Activity Map-Links | Listet alle erfassten Links auf der gesamten Website auf. |
| Activity Map-Links und -Region | Listet alle erfassten Links zusammen mit ihrer Region über die gesamte Website hinweg auf. |
| Activity Map XY | Nicht verwendet |

* Diese Dimensionen sollten in Analysis Workspace und Report Builder verfügbar sein, sofern Ihre Analytics-Implementierung [aktiviert für Activity Map](/help/analyze/activity-map/activitymap-getting-started/activitymap-enable.md).
* Ziehen Sie in Analysis Workspace die Activity Map-bezogenen Dimensionen in einen Bericht.
* Um einen Link und eine Region für eine bestimmte Seite anzusehen, müssen Sie nur eine Aufschlüsselung auf der gewünschten Activity Map-Seite nach „Activity Map-Links und -Region“ erstellen.
