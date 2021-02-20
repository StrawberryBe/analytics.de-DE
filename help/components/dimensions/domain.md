---
title: Domäne
description: Die Organisation oder der ISP, die bzw. den der Besucher für den Internetzugang verwendet.
translation-type: tm+mt
source-git-commit: c2d371cee2821360ab87240b1a81695798af4f9f
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 41%

---


# Domäne

Die Dimension &quot;Domäne&quot;erfasst Zugriffspunkte, die Besucher für den Internetzugang verwenden.

## Füllen dieser Dimension mit Daten

Adobe arbeitet mit [Digital Element](https://info.digitalelement.com/de/) zusammen, um die Zugriffspunktdomäne zu bestimmen. Zur Bestimmung der Zugriffspunktdomäne werden verschiedene Methoden, einschließlich umgekehrter DNS-Suche, verwendet. Es ist keine Konfiguration erforderlich und es gibt keine Variablen zum Ausfüllen. Sie ist bei allen AppMeasurement-Implementierungen vorkonfiguriert.

## Dimensionselemente

Beispiele für Dimensionselemente sind `comcast.net`, `rr.com`, `sbcglobal.net` und `amazonaws.com`. Beachten Sie, dass es sich bei diesen Domänen um Zugriffspunkte handelt und nicht unbedingt um die Domäne, die einen ISP oder ein Unternehmen darstellt.

Die Dimension von `None` bedeutet, dass der Inhaber des Zugriffspunkts IP-Adresse keine Domäne angegeben hat.
