---
title: Einstiegsdimensionen
description: Listen geben Dimensionen und ihre Verwendung ein.
keywords: entry page, entry site section, entry server, entry custom insight
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Einstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Einträge als Dimension funktionieren. Informationen zur Funktionsweise von Einträgen als Metrik finden Sie in der Metrik &quot;[Einstiege](../metrics/entries.md)&quot;.*

Einstiegsdimensionen sind besuchsbasiert. Sie zeichnen den ersten Dimensionswert auf und behalten ihn für die gesamte Dauer des Besuchs bei. Einstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/admin/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

## Einstiegsdimensionen mit Daten füllen

Eine bestimmte Einstiegsdimension basiert auf der zugehörigen Traffic-Variablen. Wenn die Nicht-Einstiegsvariable über Daten verfügt, enthält die zugehörige Einstiegsdimension auch Daten. Für Einstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionswerte

Da Einstiegsvariablen in der Regel auf benutzerdefinierten Zeichenfolgen in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionswerte verwendet werden. Werte in einer bestimmten Einstiegsdimension stimmen mit Dimensionswerten in der zugehörigen Nicht-Einstiegsdimension überein. Beispielsweise enthalten Dimensionswerte in der Dimension &quot;Entrypage&quot;ähnliche Dimensionswerte in der Dimension &quot;Seite&quot;.

## Original der Entrypage

Die Dimension &quot;Original der Entrypage&quot;unterscheidet sich von anderen Einstiegsdimensionen. Anstatt die Einstiegsseite für einen bestimmten Besuch beizubehalten, wird die erste Einstiegsseite für die gesamte Dauer des Cookies dieses Besuchers beibehalten. Wenn Sie z. B. `https://example.com/page4` zum ersten Mal die Site besuchen und dann ein Jahr später auf der Site landen, wird die Dimension &quot;Original der Entrypage&quot; `https://example.com/store``https://example.com/page4` als Dimensionswert Liste.
