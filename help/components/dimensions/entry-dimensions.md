---
title: Einstiegsdimensionen
description: Führt Einstiegsdimensionen und deren Verwendung auf.
keywords: Entrypage, Einstiegsseiten, Einstiegsserver, Einstiegsseiten, Custom Insight
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 95%

---


# Einstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Einstiege als Dimension funktionieren. Informationen dazu, wie Einstiege als Metrik funktionieren, finden Sie unter der Metrik [Einstiege](../metrics/entries.md).*

Einstiegsdimensionen sind besuchsbasiert. Sie zeichnen das erste Dimensionselement auf und behalten es für die gesamte Dauer des Besuchs bei. Einstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/admin/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

## Füllen von Einstiegsdimensionen mit Daten

Eine gegebene Einstiegsdimension basiert auf der zugehörigen Traffic-Variablen. Wenn die Nicht-Einstiegsvariable über Daten verfügt, enthält die zugehörige Einstiegsdimension auch Daten. Für Einstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionselemente

Da Einstiegsvariablen typischerweise auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Die Werte in einer gegebenen Einstiegsdimension stimmen mit den Dimensionselementen in der zugehörigen Nicht-Einstiegsdimension überein. Beispielsweise ähneln die Dimensionselemente in der Dimension „Entrypage“ den Dimensionselementen in der Dimension „Seite“.

## Ursprüngliche Entrypage

Die Dimension „Ursprüngliche Entrypage“ unterscheidet sich von anderen Einstiegsdimensionen. Anstatt die Entrypage für einen bestimmten Besuch beizubehalten, wird die erste Entrypage für die gesamte Dauer des Cookies dieses Besuchers beibehalten. Wenn Sie z. B. bei Ihrem ersten Besuch der Website zu `https://example.com/page4` gehen und ein Jahr später zu `https://example.com/store`, wird `https://example.com/page4` als Dimensionselement für die Dimension „Ursprüngliche Entrypage“ angegeben.
