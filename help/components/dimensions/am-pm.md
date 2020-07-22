---
title: Vormittag/Nachmittag
description: Bestimmt, ob der Treffer während der AM- oder PM-Stunden erfolgte.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---


# Vormittag/Nachmittag

Die Dimension &quot;AM/PM&quot;bietet einen Einblick, ob der Treffer während der AM- oder PM-Stunden stattgefunden hat. The time of the hit is based on the [report suite&#39;s time zone](/help/admin/admin/general-acct-settings-admin.md).

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert standardmäßig. Es hat keine Einstellungen zu ändern. Die einzige Abhängigkeit besteht in der Zeitzone der Report Suite, die bestimmt, welche Stunden AM und welche PM sind.

## Dimensionselemente

Diese Dimension enthält immer genau zwei Dimensionselemente: `"AM"` und `"PM"`. Das Dimensionselement `"AM"` `"PM"` gilt für alle Treffer von 12.00 Uhr bis 11.59 Uhr, während das Dimensionselement für alle Treffer von 12.00 Uhr bis 23.59 Uhr gilt.
