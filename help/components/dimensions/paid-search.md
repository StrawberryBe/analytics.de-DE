---
title: Paid Search
description: Unterscheidet Metriken von gebührenpflichtiger und kostenloser Suche.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '148'
ht-degree: 100%

---


# Paid Search

Mit der Dimension „Paid Search“ können Sie eine beliebige Metrik betrachten und zwischen gebührenpflichtiger und kostenloser Suche vergleichen. Alle anderen Treffer außerhalb der Suchmaschinen werden weggelassen. Diese Dimension ist hilfreich, um zu verstehen, wie sich Ihre gebührenpflichtigen Suchbemühungen mit der kostenlosen Suche vergleichen.

## Füllen dieser Dimension mit Daten

Die einzige Voraussetzung für die ordnungsgemäße Funktion dieser Dimension ist, dass die [gebührenpflichtige Sucherkennung](/help/admin/admin/paid-search-detection/paid-search-detection.md) in den Einstellungen der Report Suite korrekt konfiguriert ist. Wenn die gebührenpflichtige Sucherkennung korrekt konfiguriert ist und eine Report Suite Daten enthält, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehören zwei statische Werte: `"Natural"` und `"Paid"`. Wenn ein Besuch die Kriterien für eine Suchmaschine erfüllt und auch mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum Dimensionselement `"Paid"`. Wenn ein Besuch die Kriterien für eine Suchmaschine erfüllt und *nicht* mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum Dimensionselement `"Natural"`.
