---
title: Vormittag/Nachmittag
description: Bestimmt, ob der Treffer während der AM- oder PM-Stunden erfolgte.
translation-type: tm+mt
source-git-commit: 05ea2778cd5cd324c660fd0f1d2ac02373829f0f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---


# Vormittag/Nachmittag

Die Dimension &quot;AM/PM&quot;bietet einen Einblick, ob der Treffer während der AM- oder PM-Stunden stattgefunden hat. The time of the hit is based on the [report suite&#39;s time zone](/help/admin/admin/general-acct-settings-admin.md).

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert standardmäßig. Es hat keine Einstellungen zu ändern. Die einzige Abhängigkeit besteht in der Zeitzone der Report Suite, die bestimmt, welche Stunden AM und welche PM sind.

## Dimensionswerte

Diese Dimension enthält immer genau zwei Dimensionswerte: `"AM"` und `"PM"`. Der Dimensionswert `"AM"` `"PM"` gilt für alle Treffer von 12:00 Uhr bis 11:59 Uhr, während der Dimensionswert für alle Treffer von 12:00 Uhr bis 23:59 Uhr gilt.
