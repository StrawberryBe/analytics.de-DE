---
title: Gebührenpflichtige Suche
description: Trennt Metriken von der gebührenpflichtigen und kostenlosen Suche.
translation-type: tm+mt
source-git-commit: d71edc74644907b47bfb6492e7a6c47c06d5984f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Gebührenpflichtige Suche

Mit der Dimension &quot;Gebührenpflichtige Suche&quot;können Sie eine beliebige Metrik betrachten und sie zwischen gebührenpflichtiger und kostenloser Suche vergleichen. Alle anderen Treffer außerhalb der Suchmaschinen werden weggelassen. Diese Dimension ist hilfreich, um zu verstehen, wie Ihre gebührenpflichtigen Suchbemühungen mit der kostenlosen Suche verglichen werden.

## Diese Dimension mit Daten füllen

Die einzige Voraussetzung dafür, dass diese Dimension ordnungsgemäß funktioniert, ist, dass die [gebührenpflichtige Sucherkennung](/help/admin/admin/paid-search-detection/paid-search-detection.md) in den Report Suite-Einstellungen korrekt konfiguriert ist. Wenn die gebührenpflichtige Sucherkennung korrekt konfiguriert ist und eine Report Suite Daten enthält, funktioniert diese Dimension immer.

## Dimensionswerte

Dimensionswerte umfassen zwei statische Werte: `"Natural"` und `"Paid"`. Wenn ein Besuch Kriterien für eine Suchmaschine erfüllt und auch mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum `"Paid"` Dimensionswert. Wenn ein Besuch Kriterien für eine Suchmaschine erfüllt und *nicht* mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum `"Natural"` Dimensionswert.
