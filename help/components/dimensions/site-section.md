---
title: Site-Abschnitt
description: Der Name des Site-Abschnitts.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Site-Abschnitt

Die Dimension &quot;Site-Abschnitt&quot;Liste die Namen der Site-Abschnitte auf Ihrer Site. Bei großen Sites ist es hilfreich, Seiten in Abschnitte zu gruppieren. Diese Dimension ist nützlich, um die am meisten angezeigten oder leistungsstärksten Sitebereiche anzuzeigen.

Diese Dimension bezieht sich auf die [Seiten](page.md) - und [Server](server.md) -Dimensionen. Die Seite ist am granularsten, der Server ist am wenigsten granular und der Site-Abschnitt befindet sich zwischen den beiden.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`ch` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`channel`](/help/implement/vars/page-vars/channel.md) Variablen.

## Dimensionswerte

Dimensionswerte umfassen die Namen der Sitebereiche auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionswerte Sie verwenden möchten. Vergewissern Sie sich, welche Methode Sie auch verwenden, dass sie konsistent ist und dass Sie sie in einem [Lösungsdesign-Dokument](/help/implement/prepare/solution-design.md)aufzeichnen.
