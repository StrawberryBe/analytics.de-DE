---
title: Wochentag/Wochenende
description: Bestimmt, ob der Treffer an einem Wochentag oder an einem Wochenende stattgefunden hat.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 68%

---


# Wochentag/Wochenende

Die Dimension „Wochentag/Wochenende“ bietet einen Einblick, ob der Treffer an einem Wochentag (Montag–Freitag) oder an einem Wochenende (Samstag–Sonntag) stattgefunden hat. Die Uhrzeit des Treffers basierend auf der [Zeitzone der Report Suite](/help/admin/admin/general-acct-settings-admin.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionen

This dimension always contains exactly two dimension items: `"Weekday"` and `"Weekend"`. The dimension item `"Weekday"` applies to all hits Monday through Friday, while the dimension item `"Weekend"` applies to all hits on Saturday and Sunday.
