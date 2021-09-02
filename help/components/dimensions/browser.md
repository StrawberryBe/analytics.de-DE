---
title: Browser
description: Name und Version des verwendeten Browsers.
exl-id: 2bdf2a5a-3482-43fa-b2e1-fbea892918fb
source-git-commit: e6f3beadfba340cea07f5fd2694105ad31de9751
workflow-type: ht
source-wordcount: '178'
ht-degree: 100%

---

# Browser

Die Dimension „Browser“ zeigt den Namen und die Version des Browsers an, der den Treffer sendet. Diese Dimension ist nützlich, um zu verstehen, welche Browser von Besuchern am häufigsten verwendet werden. Beim Testen neuer Versionen Ihrer Site können Sie diese Tests mit den wichtigsten Browsern in dieser Dimension ausführen, um den Aufwand für die Qualitätssicherung zu optimieren.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören die verwendeten Browsernamen und -versionen. Verschiedene Versionen desselben Browsers sind separate Dimensionselemente.

Einige Dimensionselemente enthalten `"(unknown version)"` anstelle ihrer Versionsnummer. Dieses Dimensionselement verweist auf eine kürzlich veröffentlichte Browserversion, die von der Adobe nicht zu denn Suchtabellen hinzugefügt wurde. Da Browser häufig aktualisiert werden, ist `"(unknown version)"` für einen bestimmten Browser üblich und vorübergehend. Adobe aktualisiert die Suchtabellen in der Regel während der monatlichen Wartungsversionen.
