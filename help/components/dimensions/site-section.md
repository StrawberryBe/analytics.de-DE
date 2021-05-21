---
title: Website-Bereich
description: Der Name des Website-Bereichs.
exl-id: 349bace0-4596-4b4c-bf29-6cd8866c246b
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '137'
ht-degree: 100%

---

# Website-Bereich

In der Dimension „Website-Bereich“ werden die Namen der Website-Bereiche Ihrer Site aufgelistet. Bei großen Sites ist es hilfreich, Seiten in Bereiche zu gruppieren. Diese Dimension ist nützlich, um die am meisten angezeigten oder leistungsstärksten Website-Bereiche anzuzeigen.

Diese Dimension hängt mit den Dimensionen [Seite](page.md) und [Server](server.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`ch` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`channel`](/help/implement/vars/page-vars/channel.md)-Variable.

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Website-Bereiche auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
