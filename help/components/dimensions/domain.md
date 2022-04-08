---
title: Domain
description: Die Organisation oder der ISP, die bzw. den der Besucher für den Internetzugang verwendet.
feature: Dimensions
exl-id: 292dc256-e9e7-47be-8586-774f1c047011
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '124'
ht-degree: 100%

---

# Domain

Die Dimension „Domain“ erfasst Zugriffspunkte, die Besucher für den Internetzugang verwenden.

## Füllen dieser Dimension mit Daten

Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um die Zugriffspunkt-Domain zu bestimmen. Zur Bestimmung der Zugriffspunkt-Domain werden verschiedene Methoden verwendet, einschließlich Reverse DNS Lookup. Es ist keine Konfiguration erforderlich und es gibt keine Variablen zum Ausfüllen. Sie ist bei allen AppMeasurement-Implementierungen vorkonfiguriert.

## Dimensionselemente

Beispiele für Dimensionselemente sind `comcast.net`, `rr.com`, `sbcglobal.net` und `amazonaws.com`. Beachten Sie, dass es sich bei diesen Domains um Zugriffspunkte handelt und nicht unbedingt um die Domain, die einen ISP oder ein Unternehmen repräsentiert.

Dimensionswerte von `None` bedeuten, dass der Inhaber der IP-Adresse des Zugriffspunkts keine Domain angegeben hat.
