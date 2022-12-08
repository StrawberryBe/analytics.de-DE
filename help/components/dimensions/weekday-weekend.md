---
title: Wochentag/Wochenende
description: Bestimmt, ob der Treffer an einem Wochentag oder an einem Wochenende stattgefunden hat.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 100%

---

# Wochentag/Wochenende

Die Dimension „Wochentag/Wochenende“ bietet einen Einblick, ob der Treffer an einem Wochentag (Montag–Freitag) oder an einem Wochenende (Samstag–Sonntag) stattgefunden hat. Die Uhrzeit des Treffers basierend auf der [Zeitzone der Report Suite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Diese Dimension enthält immer genau zwei Dimensionselemente: `"Weekday"` und `"Weekend"`. Das Dimensionselement `"Weekday"` gilt für alle Treffer von Montag bis Freitag, während das Dimensionselement `"Weekend"` für alle Treffer am Samstag und Sonntag gilt.
