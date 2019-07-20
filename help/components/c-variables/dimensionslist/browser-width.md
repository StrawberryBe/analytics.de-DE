---
description: Metriken, die sich ausschließlich auf die horizontale/vertikale Distanz der Daten im Browser-Fenster beziehen. Genauer gesagt, auf den Browser
seo-description: Metriken, die sich ausschließlich auf die horizontale/vertikale Distanz der Daten im Browser-Fenster beziehen. Genauer gesagt, auf den Browser
seo-title: Browserbreite/-höhe
solution: Analytics
title: Browserbreite/-höhe
topic: Metriken
uuid: 1 c 0 d 3 ea 9-e 001-4152-9 bfc -8 fe 6406 bc 755
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Browserbreite/-höhe

Metriken, die sich ausschließlich auf die horizontale/vertikale Distanz der Daten im Browser-Fenster beziehen. Genauer gesagt, auf den Browser

Adobe Analytics verwendet die Browserhöhe und -breite lediglich vom ersten Treffer eines Besuchs an. Die übrigen Treffer erhalten nicht die Zuordnung für den gleichen Besuch.
The browser width/height dimensions capture similar but distinct values when compared with [mobile screen size](../../../components/c-variables/dimensionslist/reports-mobile.md#topic_D306EA4558194488AC47A45B9C570150).

Wenn beispielsweise die Browserbreite oder -höhe auf die Auflösung von Mobilgeräten herunterskaliert werden, sollten folgende Unterscheidungen beachtet werden:

* Die Mobilgeräteauflösungen entsprechen den physischen Werten des Geräts. Beispielsweise erscheint das Galaxy S8 unter „Mobilgeräteauflösungen“ als 2.960 x 1.440. Die Mobilgeräteauflösung erhalten wir von einem Drittanbieter, nachdem das Gerät erkannt wurde.
* Im Gegensatz dazu sehen Sie bei den Werten zu Browserbreite und -höhe die (logischen) CSS-Werte von 740 x 360. Die Browserwerte hängen von JavaScript/CSS-Daten ab.
* Eine kurze Diskussion dazu finden Sie [in diesem Thread](https://stackoverflow.com/questions/8785643/what-exactly-is-device-pixel-ratio).

