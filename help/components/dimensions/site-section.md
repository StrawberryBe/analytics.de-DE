---
title: Website-Bereich
description: Der Name des Website-Bereichs.
feature: Dimensions
exl-id: 349bace0-4596-4b4c-bf29-6cd8866c246b
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 90%

---

# Website-Bereich

Der &quot;Website-Bereich&quot; [Dimension](overview.md) listet die Namen der Sitebereiche auf Ihrer Site auf. Bei großen Sites ist es hilfreich, Seiten in Bereiche zu gruppieren. Diese Dimension ist nützlich, um die am meisten angezeigten oder leistungsstärksten Website-Bereiche anzuzeigen.

Diese Dimension hängt mit den Dimensionen [Seite](page.md) und [Server](server.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`ch` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`channel`](/help/implement/vars/page-vars/channel.md)-Variable.

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Website-Bereiche auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
