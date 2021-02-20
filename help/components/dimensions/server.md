---
title: Server
description: Der Name des Servers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 100%

---


# Server

Die Dimension „Server“ listet typischerweise den Host-Namen der Site auf. Bei Report Suites, die mehrere Domänen oder Unterdomänen kombinieren, ist diese Dimension nützlich, um zu sehen, welche Domänen oder Unterdomänen die beste Leistung erbringen.

Diese Dimension hängt mit den Dimensionen [Seite](page.md) und [Website-Bereich](site-section.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`server` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`server`](/help/implement/vars/page-vars/server.md)-Variable.

## Dimensionselemente

Die Dimensionselemente umfassen die Server auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Einige Organisationen verwenden `window.location.hostname`, während andere benutzerdefinierte Werte formulieren. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
