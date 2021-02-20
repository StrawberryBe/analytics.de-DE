---
title: Website-Bereich
description: Der Name des Website-Bereichs.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
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
