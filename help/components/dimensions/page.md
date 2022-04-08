---
title: Seite
description: Der Name der Seite.
feature: Dimensions
exl-id: 579963c8-8460-425f-b716-3b30d7a259af
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '212'
ht-degree: 100%

---

# Seite

Die Dimension „Seite“ listet die Seitennamen auf Ihrer Site auf. Sie ist eine der am häufigsten verwendeten Dimensionen in Adobe Analytics, da sie Aufschluss darüber gibt, welche Seiten Ihrer Website die beste Leistung erbringen.

Diese Dimension hängt mit den Dimensionen [Website-Bereich](site-section.md) und [Server](server.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`pageName`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in [Aufrufen von Seitenansichten (`t()`)](/help/implement/vars/functions/t-method.md) ab. [Linktracking-Aufrufe (`tl()`)](/help/implement/vars/functions/tl-method.md) entfernen diese Dimension immer, auch wenn die Abfragezeichenfolge `pageName` vorhanden ist.

AppMeasurement erfasst diese Daten mit der [`pageName`](/help/implement/vars/page-vars/pagename.md)-Variable. Wenn die `pageName`-Variable nicht definiert ist, wird auf die Verwendung der [`pageURL`](/help/implement/vars/page-vars/pageurl.md)-Variable zurückgegriffen.

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Seiten auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Einige Organisationen verwenden `document.title` direkt, während andere benutzerdefinierte Breadcrumbs formulieren. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.

>[!NOTE]
>
>In Reports &amp; Analytics verwenden Konversionsmetriken die lineare Attribution für diese Dimension. Der Umsatz wird beispielsweise auf alle Seiten aufgeteilt, die bei einem Besuch vor einem `purchase`-Ereignis aufgerufen wurden. Analysis Workspace verwendet standardmäßig die letzte Attribution mit der Option, ein beliebiges Attributionsmodell zu verwenden.
