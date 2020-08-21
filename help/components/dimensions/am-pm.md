---
title: Vormittag/Nachmittag
description: Bestimmt, ob der Treffer am Vormittag oder am Nachmittag stattgefunden hat.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 70%

---


# Vormittag/Nachmittag

Die Dimension „Vormittag/Nachmittag“ bietet einen Einblick, ob der Treffer am Vormittag oder am Nachmittag stattgefunden hat. Die Uhrzeit des Treffers basierend auf der [Zeitzone der Report Suite](/help/admin/admin/general-acct-settings-admin.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ist vorkonfiguriert. Sie hat keine zu ändernden Einstellungen. Sie hängt nur von der Zeitzone der Report Suite ab, die bestimmt, welche Stunden vormittags und welche nachmittags sind.

## Dimensionen

This dimension always contains exactly two dimension items: `"AM"` and `"PM"`. The dimension item `"AM"` applies to all hits from 12:00 AM to 11:59 AM, while the dimension item `"PM"` applies to all hits from 12:00 PM to 11:59 PM.
