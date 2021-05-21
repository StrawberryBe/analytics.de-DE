---
title: Wochentag/Wochenende
description: Bestimmt, ob der Treffer an einem Wochentag oder an einem Wochenende stattgefunden hat.
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '105'
ht-degree: 100%

---

# Wochentag/Wochenende

Die Dimension „Wochentag/Wochenende“ bietet einen Einblick, ob der Treffer an einem Wochentag (Montag–Freitag) oder an einem Wochenende (Samstag–Sonntag) stattgefunden hat. Die Uhrzeit des Treffers basierend auf der [Zeitzone der Report Suite](/help/admin/admin/general-acct-settings-admin.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Diese Dimension enthält immer genau zwei Dimensionselemente: `"Weekday"` und `"Weekend"`. Das Dimensionselement `"Weekday"` gilt für alle Treffer von Montag bis Freitag, während das Dimensionselement `"Weekend"` für alle Treffer am Samstag und Sonntag gilt.
