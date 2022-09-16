---
title: Vormittag/Nachmittag
description: Bestimmt, ob der Treffer am Vormittag oder am Nachmittag stattgefunden hat.
feature: Dimensions
exl-id: 93fcdb9f-2ba3-402c-a389-b02ed8c990d2
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 100%

---

# Vormittag/Nachmittag

Die Dimension „Vormittag/Nachmittag“ bietet einen Einblick, ob der Treffer am Vormittag oder am Nachmittag stattgefunden hat. Die Uhrzeit des Treffers basierend auf der [Zeitzone der Report Suite](/help/admin/admin/general-acct-settings-admin.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ist vorkonfiguriert. Sie hat keine zu ändernden Einstellungen. Sie hängt nur von der Zeitzone der Report Suite ab, die bestimmt, welche Stunden vormittags und welche nachmittags sind.

## Dimensionselemente

Diese Dimension enthält immer genau zwei Dimensionselemente: `"AM"` und `"PM"`. Das Dimensionselement `"AM"` gilt für alle Treffer von 00:00 Uhr bis 11:59 Uhr, während das Dimensionselement `"PM"` für alle Treffer von 12:00 Uhr bis 23:59 Uhr gilt.
