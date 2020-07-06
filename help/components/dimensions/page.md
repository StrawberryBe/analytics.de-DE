---
title: Seite
description: Der Name der Seite.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---


# Seite

Die Dimension &quot;Seite&quot;Liste die Seitennamen auf Ihrer Site. Es gehört zu den gebräuchlichsten Dimensionen, die in Adobe Analytics verwendet werden, da es einen Einblick gibt, welche Seiten auf Ihrer Site am besten funktionieren.

Diese Dimension bezieht sich auf die Dimensionen [Site-Abschnitt](site-section.md) und [Server](server.md) . Die Seite ist am granularsten, der Server ist am wenigsten granular und der Site-Abschnitt befindet sich zwischen den beiden.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`pageName` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der `pageName` Variablen. Wenn die `pageName` Variable nicht definiert ist, wird die URL der Seite verwendet.

## Dimensionswerte

Dimensionswerte umfassen die Namen der Seiten auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionswerte Sie verwenden möchten. Einige Organisationen verwenden direkt `document.title`und andere formulieren einen benutzerspezifischen Breadcrumb. Vergewissern Sie sich, welche Methode Sie auch verwenden, dass sie konsistent ist und dass Sie sie in einem [Lösungsdesign-Dokument](/help/implement/prepare/solution-design.md)aufzeichnen.

>[!NOTE]
>
>In Reports &amp; Analytics verwenden Konversionsmetriken für diese Dimension die lineare Zuordnung. For example, revenue is split between all pages viewed in a visit before a `purchase` event. Analysis Workspace verwendet standardmäßig die letzte Zuordnung mit der Option, ein beliebiges Zuordnungsmodell zu verwenden.
