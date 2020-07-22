---
title: Trackingcode
description: Der Name des Rückverfolgungscodes oder der Kampagne.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# Trackingcode

Die Dimension &quot;Rückverfolgungscode&quot;Liste die Namen der Rückverfolgungscodes auf Ihrer Site. Diese Dimension wird in der Regel mithilfe von Abfrage-Zeichenfolgenparametern erfasst. Sie können Links mit verschiedenen Abfragen-Zeichenfolgenparametern an verschiedenen Stellen im Internet platzieren. Diese Dimension berichtet, welche Links den Traffic zu Ihrer Site am erfolgreichsten geleitet haben.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`v0` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`campaign`](/help/implement/vars/page-vars/campaign.md) Variablen.

## Dimensionselemente

Dimensionselemente enthalten die Namen der Rückverfolgungscodes auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten.
