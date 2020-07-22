---
title: Site-Abschnitt
description: Der Name des Site-Abschnitts.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Site-Abschnitt

Die Dimension &quot;Site-Abschnitt&quot;Liste die Namen der Site-Abschnitte auf Ihrer Site. Bei großen Sites ist es hilfreich, Seiten in Abschnitte zu gruppieren. Diese Dimension ist nützlich, um die am meisten angezeigten oder leistungsstärksten Sitebereiche anzuzeigen.

Diese Dimension bezieht sich auf die [Seiten](page.md) - und [Server](server.md) -Dimensionen. Die Seite ist am granularsten, der Server ist am wenigsten granular und der Site-Abschnitt befindet sich zwischen den beiden.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`ch` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`channel`](/help/implement/vars/page-vars/channel.md) Variablen.

## Dimensionselemente

Dimensionselemente enthalten die Namen der Site-Abschnitte auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Vergewissern Sie sich, welche Methode Sie auch verwenden, dass sie konsistent ist und dass Sie sie in einem [Lösungsdesign-Dokument](/help/implement/prepare/solution-design.md)aufzeichnen.
