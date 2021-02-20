---
title: Browser
description: Name und Version des verwendeten Browsers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 100%

---


# Browser

Die Dimension „Browser“ zeigt den Namen und die Version des Browsers an, der den Treffer sendet. Diese Dimension ist nützlich, um zu verstehen, welche Browser von Besuchern am häufigsten verwendet werden. Beim Testen neuer Versionen Ihrer Site können Sie diese Tests mit den wichtigsten Browsern in dieser Dimension ausführen, um den Aufwand für die Qualitätssicherung zu optimieren.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören die verwendeten Browsernamen und -versionen. Verschiedene Versionen desselben Browsers sind separate Dimensionselemente.

Einige Dimensionselemente enthalten `"(unknown version)"` anstelle ihrer Versionsnummer. Dieses Dimensionselement verweist auf eine kürzlich veröffentlichte Browserversion, die von der Adobe nicht zu denn Suchtabellen hinzugefügt wurde. Da Browser häufig aktualisiert werden, ist `"(unknown version)"` für einen bestimmten Browser üblich und vorübergehend. Adobe aktualisiert die Suchtabellen in der Regel während der monatlichen Wartungsversionen.
