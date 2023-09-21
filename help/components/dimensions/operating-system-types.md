---
title: Betriebssystemtypen
description: Das Betriebssystem unabhängig von der Version.
feature: Dimensions
exl-id: 0afd5261-98e8-4247-865a-1b8844c53ff4
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 85%

---

# Betriebssystemtypen

Die Betriebssystemtypen [Dimension](overview.md) zeigt das übergreifende Betriebssystem an, das der Besucher verwendet hat, unabhängig von bestimmten Versionen. Diese Dimension ist nützlich, um nicht nur zu verstehen, welches Betriebssystem und welche Version am häufigsten verwendet werden, sondern auch, welche typischen Besucher der Betriebssystemplattform verwenden.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen zählen die verwendeten Betriebssysteme. Beispiele sind `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"` und `"Apple iOS"`.
