---
title: Woche
description: Die Woche, in der die Metrik aufgetreten ist.
feature: Dimensions
exl-id: 944ec843-998c-473f-b8e6-16cf126745b4
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 92%

---

# Woche

Die &quot;Woche&quot; [Dimension](overview.md) gibt die Woche an, in der eine bestimmte Metrik aufgetreten ist. Das erste Dimensionselement ist die erste Woche im Datumsbereich und das letzte Dimensionselement die letzte Woche im Datumsbereich. Diese Dimension ist für Trend-Berichte von entscheidender Bedeutung, da sie es Ihnen ermöglicht, Metriken im Zeitverlauf anzuzeigen.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Dimensionselemente in Analysis Workspace umfassen das Datum (Monat, Tag und Jahr) des ersten Wochentages.

In Data Warehouse enthalten Dimensionselemente nummerierte Wochen, die auf dem Datumsbereich der Anfrage basieren. Die erste volle Woche ist beispielsweise `"Week 1"`. Wenn eine Anfrage einen Teil einer Woche enthält, werden die Daten in das Dimensionselement `"Week 0"` gruppiert.
