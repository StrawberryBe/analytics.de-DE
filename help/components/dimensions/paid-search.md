---
title: Paid Search
description: Unterscheidet Metriken von gebührenpflichtiger und kostenloser Suche.
feature: Dimensions
exl-id: b12665a3-e92f-4fc1-acd3-ea17a316e5e5
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 87%

---

# Paid Search

Die &quot;gebührenpflichtige Suche&quot; [Dimension](overview.md) ermöglicht Ihnen, eine beliebige Metrik anzuzeigen und sie zwischen Paid Search und kostenloser Suche zu vergleichen. Alle anderen Treffer außerhalb der Suchmaschinen werden weggelassen. Diese Dimension ist hilfreich, um zu verstehen, wie sich Ihre gebührenpflichtigen Suchbemühungen mit der kostenlosen Suche vergleichen.

## Füllen dieser Dimension mit Daten

Die einzige Voraussetzung für die ordnungsgemäße Funktion dieser Dimension ist, dass die [gebührenpflichtige Sucherkennung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md) in den Einstellungen der Report Suite korrekt konfiguriert ist. Wenn die gebührenpflichtige Sucherkennung korrekt konfiguriert ist und eine Report Suite Daten enthält, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehören zwei statische Werte: `"Natural"` und `"Paid"`. Wenn ein Besuch die Kriterien für eine Suchmaschine erfüllt und auch mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum Dimensionselement `"Paid"`. Wenn ein Besuch die Kriterien für eine Suchmaschine erfüllt und *nicht* mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum Dimensionselement `"Natural"`.
