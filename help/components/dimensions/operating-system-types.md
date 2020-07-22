---
title: Betriebssystemtypen
description: Das Betriebssystem unabhängig von der Version.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Betriebssystemtypen

Die Dimension &quot;Betriebssystemtypen&quot;zeigt das übergeordnete Betriebssystem des verwendeten Besuchers unabhängig von bestimmten Versionen an. Diese Dimension ist nützlich, um nicht nur zu verstehen, welches Betriebssystem und welche Version am häufigsten verwendet wird, sondern welche typischen Betriebssystemplattformen Besucher verwenden.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf eine interne Nachschlagetabelle von Adobe. Der Nachschlagewert basiert auf dem `User-Agent` HTTP-Header in Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. beim Starten der Adobe Experience Platform), funktioniert diese Dimension standardmäßig.

## Dimensionselemente

Zu den Dimensionselementen gehören die Art der verwendeten Betriebssysteme. Examples include `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"`, and `"Apple iOS"`.
