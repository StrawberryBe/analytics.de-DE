---
title: Woche
description: Die Woche, in der die Metrik aufgetreten ist.
translation-type: tm+mt
source-git-commit: a94b8e090b9a3c75a57fd396cac8486bba2e5d79
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 61%

---


# Woche

Die Dimension „Woche“ zeigt die Woche an, in der eine bestimmte Metrik aufgetreten ist. Das erste Dimensionselement ist die erste Woche im Datumsbereich und das letzte Dimensionselement die letzte Woche im Datumsbereich. Diese Dimension ist für Trend-Berichte von entscheidender Bedeutung, da sie es Ihnen ermöglicht, Metriken im Zeitverlauf anzuzeigen.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

In Analysis Workspace beinhalten Dimensionselemente das Datum (Monat, Tag und Jahr) des ersten Wochentags.

In der Data Warehouse enthalten Dimensionselemente nummerierte Wochen, die auf dem Datumsbereich der Anforderung basieren. Die erste volle Woche ist zum Beispiel `"Week 1"`die. Wenn eine Anforderung eine Teilwoche enthält, werden die Daten in das Dimensionselement gruppiert `"Week 0"`.
