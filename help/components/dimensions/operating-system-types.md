---
title: Betriebssystemtypen
description: Das Betriebssystem unabhängig von der Version.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 100%

---


# Betriebssystemtypen

Die Dimension „Betriebssystemtypen“ zeigt das übergeordnete Betriebssystem an, das der Besucher unabhängig von bestimmten Versionen verwendet hat. Diese Dimension ist nützlich, um nicht nur zu verstehen, welches Betriebssystem und welche Version am häufigsten verwendet werden, sondern auch, welche typischen Besucher der Betriebssystemplattform verwenden.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen zählen die verwendeten Betriebssysteme. Beispiele sind `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"` und `"Apple iOS"`.
