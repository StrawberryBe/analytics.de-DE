---
title: Ausstiegsdimensionen
description: Führt Ausstiegsdimensionen und deren Verwendung auf.
keywords: exit page, exit site section, exit server, exit custom insight
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 57%

---


# Ausstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Ausstiege als Dimension funktionieren. Informationen dazu, wie Ausstiege als Metrik funktionieren, finden Sie unter der Metrik[Ausstiege](../metrics/exits.md).*

Ausstiegsdimensionen zeichnen das letzte Dimensionselement auf und wenden es rückwirkend auf alle Treffer im Besuch an. Ausstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/admin/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

## Füllen von Ausstiegsdimensionen mit Daten

Eine gegebene Ausstiegsdimension basiert auf der zugehörigen Traffic-Variablen. Wenn die Nicht-Ausstiegsvariable über Daten verfügt, enthält die zugehörige Ausstiegsdimension auch Daten. Für Ausstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionen

Da Ausstiegsvariablen in der Regel auf benutzerdefinierten Zeichenfolgen in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionselemente sind. Werte in einer gegebenen Ausstiegsdimension stimmen mit Dimensionselementen in der zugehörigen Nicht-Ausstiegsdimension überein. Beispielsweise enthalten Dimensionselemente in der Dimension &quot;Ausstiegsseite&quot;ähnliche Dimensionselemente in der Dimension &quot;Seite&quot;.
