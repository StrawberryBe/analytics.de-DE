---
title: Seite
description: Der Name der Seite.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 82%

---


# Seite

Die Dimension „Seite“ listet die Seitennamen auf Ihrer Site auf. Sie ist eine der am häufigsten verwendeten Dimensionen in Adobe Analytics, da sie Aufschluss darüber gibt, welche Seiten Ihrer Website die beste Leistung erbringen.

Diese Dimension hängt mit den Dimensionen [Website-Bereich](site-section.md) und [Server](server.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`pageName` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in [Ansicht-Aufrufen (`t()`)](/help/implement/vars/functions/t-method.md) ab. [Linktracking-Aufrufe (`tl()`)](/help/implement/vars/functions/tl-method.md) entfernen diese Dimension, auch wenn die  `pageName` Abfrage-Zeichenfolge vorhanden ist.

AppMeasurement erfasst diese Daten mit der [`pageName`](/help/implement/vars/page-vars/pagename.md)-Variable. Wenn die Variable `pageName` nicht definiert ist, wird wieder die Variable [`pageURL`](/help/implement/vars/page-vars/pageurl.md) verwendet.

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Seiten auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Einige Organisationen verwenden `document.title` direkt, während andere benutzerdefinierte Breadcrumbs formulieren. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.

>[!NOTE]
>
>In Reports &amp; Analytics verwenden Konversionsmetriken die lineare Attribution für diese Dimension. Der Umsatz wird beispielsweise auf alle Seiten aufgeteilt, die bei einem Besuch vor einem `purchase`-Ereignis aufgerufen wurden. Analysis Workspace verwendet standardmäßig die letzte Attribution mit der Option, ein beliebiges Attributionsmodell zu verwenden.
