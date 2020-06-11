---
title: Ausstiegsdimensionen
description: Listen verlassen Dimensionen und verwenden sie.
keywords: exit page, exit site section, exit server, exit custom insight
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Ausstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Ausstiege als Dimension funktionieren. Informationen dazu, wie Ausstiege als Metrik funktionieren, finden Sie in der Metrik[Ausstiege](../metrics/exits.md).*

Ausstiegsdimensionen zeichnen den letzten Dimensionswert auf und wenden ihn rückwirkend auf alle Treffer im Besuch an. Ausstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/admin/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

## Ausstiegsdimensionen mit Daten füllen

Eine angegebene Ausstiegsdimension basiert auf der zugehörigen Traffic-Variablen. Wenn die Nicht-Ausstiegsvariable über Daten verfügt, enthält die zugehörige Ausstiegsdimension auch Daten. Für Ausstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionswerte

Da Ausstiegsvariablen in der Regel auf benutzerdefinierten Zeichenfolgen in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionswerte verwendet werden. Werte in einer gegebenen Ausstiegsdimension stimmen mit Dimensionswerten in der zugehörigen Nicht-Ausstiegsdimension überein. Beispielsweise enthalten Dimensionswerte in der Dimension &quot;Ausstiegsseite&quot;ähnliche Dimensionswerte in der Dimension &quot;Seite&quot;.
