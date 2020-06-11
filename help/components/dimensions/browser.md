---
title: Browser
description: Name und Version des verwendeten Browsers.
translation-type: tm+mt
source-git-commit: 4a7b3a00bdbf557c219de530e3e692c2b2db4a84
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Browser

Die Dimension &quot;Browser&quot;zeigt den Namen und die Version des Browsers an, der den Treffer sendet. Diese Dimension ist nützlich, um zu verstehen, welche Browser von Besuchern am häufigsten verwendet werden. Beim Testen neuer Versionen Ihrer Site können Sie diese Tests mit den wichtigsten Browsern in dieser Dimension ausführen, um die Qualitätssicherung zu maximieren.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf eine interne Nachschlagetabelle von Adobe. Der Nachschlagewert basiert auf dem `User-Agent` HTTP-Header in Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig.

## Dimensionswerte

Zu den Dimensionswerten gehören die Browsernamen und verwendeten Versionen. Verschiedene Versionen desselben Browsers sind separate Dimensionswerte.

Einige Dimensionswerte enthalten `"(unknown version)"` anstelle ihrer Versionsnummer. Dieser Dimensionswert verweist auf eine neuere Browserversion, die Adobe nicht zu den Suchtabellen hinzugefügt hat. Da Browser häufig aktualisiert werden, ist der `"(unknown version)"` für einen bestimmten Browser häufig und vorübergehend. In der Regel aktualisiert Adobe die Suchtabellen während der monatlichen Maintenance-Versionen.
