---
title: Einstiegsdimensionen
description: Führt Einstiegsdimensionen und deren Verwendung auf.
keywords: entry page, entry site section, entry server, entry custom insight
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 58%

---


# Einstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Einstiege als Dimension funktionieren. Informationen dazu, wie Einstiege als Metrik funktionieren, finden Sie unter der Metrik[Einstiege](../metrics/entries.md).*

Einstiegsdimensionen sind besuchsbasiert. Sie zeichnen das erste Dimensionselement auf und behalten es für die gesamte Dauer des Besuchs bei. Einstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/admin/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

## Füllen von Einstiegsdimensionen mit Daten

Eine gegebene Einstiegsdimension basiert auf der zugehörigen Traffic-Variablen. Wenn die Nicht-Einstiegsvariable über Daten verfügt, enthält die zugehörige Einstiegsdimension auch Daten. Für Einstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionen

Da Einstiegsvariablen in der Regel auf benutzerdefinierten Zeichenfolgen in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionselemente sind. Werte in einer bestimmten Einstiegsdimension stimmen mit Dimensionselementen in der zugehörigen Nicht-Einstiegsdimension überein. Beispielsweise enthalten Dimensionselemente in der Dimension &quot;Entrypage&quot;ähnliche Dimensionselemente in der Dimension &quot;Seite&quot;.

## Ursprüngliche Entrypage

Die Dimension „Ursprüngliche Entrypage“ unterscheidet sich von anderen Einstiegsdimensionen. Anstatt die Entrypage für einen bestimmten Besuch beizubehalten, wird die erste Entrypage für die gesamte Dauer des Cookies dieses Besuchers beibehalten. For example, if you land on `https://example.com/page4` for your first visit to the site, then a year later land on `https://example.com/store`, The &#39;Entry page original&#39; dimension lists `https://example.com/page4` as the dimension item.
