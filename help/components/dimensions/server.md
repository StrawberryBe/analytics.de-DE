---
title: Server
description: Der Name des Servers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---


# Server

Die Dimension &quot;Server&quot;Liste normalerweise den Hostnamen der Site. Bei Report Suites, die mehrere Domänen oder Subdomänen kombinieren, ist diese Dimension nützlich, um zu sehen, welche Domänen oder Subdomänen die beste Leistung erbringen.

Diese Dimension bezieht sich auf die Dimensionen [Seiten](page.md) und [Site-Abschnitt](site-section.md) . Die Seite ist am granularsten, der Server ist am wenigsten granular und der Site-Abschnitt befindet sich zwischen den beiden.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`server` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`server`](/help/implement/vars/page-vars/server.md) Variablen.

## Dimensionselemente

Dimensionselemente enthalten Server auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Einige Organisationen verwenden `window.location.hostname`die Methode, während andere benutzerdefinierte Werte formulieren. Vergewissern Sie sich, welche Methode Sie auch verwenden, dass sie konsistent ist und dass Sie sie in einem [Lösungsdesign-Dokument](/help/implement/prepare/solution-design.md)aufzeichnen.
