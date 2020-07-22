---
title: Wochentag/Wochenende
description: Bestimmt, ob der Treffer während eines Wochentags oder Wochenendes stattgefunden hat.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---


# Wochentag/Wochenende

Die Dimension &quot;Wochentag/Wochenende&quot;bietet einen Einblick, ob der Treffer während eines Wochentags (Montag - Freitag) oder Wochenendes (Samstag - Sonntag) stattgefunden hat. The time of the hit is based on the [report suite&#39;s time zone](/help/admin/admin/general-acct-settings-admin.md).

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen Implementierungen standardmäßig. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Diese Dimension enthält immer genau zwei Dimensionselemente: `"Weekday"` und `"Weekend"`. Das Dimensionselement `"Weekday"` `"Weekend"` gilt für alle Treffer von Montag bis Freitag, während das Dimensionselement für alle Treffer von Samstag und Sonntag gilt.
