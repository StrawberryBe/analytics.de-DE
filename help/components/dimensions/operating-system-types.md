---
title: Betriebssystemtypen
description: Das Betriebssystem unabhängig von der Version.
feature: Dimensions
exl-id: 0afd5261-98e8-4247-865a-1b8844c53ff4
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '113'
ht-degree: 100%

---

# Betriebssystemtypen

Die Dimension „Betriebssystemtypen“ zeigt das übergeordnete Betriebssystem an, das der Besucher unabhängig von bestimmten Versionen verwendet hat. Diese Dimension ist nützlich, um nicht nur zu verstehen, welches Betriebssystem und welche Version am häufigsten verwendet werden, sondern auch, welche typischen Besucher der Betriebssystemplattform verwenden.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen zählen die verwendeten Betriebssysteme. Beispiele sind `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"` und `"Apple iOS"`.
