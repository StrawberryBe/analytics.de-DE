---
description: Metriken, die sich ausschließlich auf die horizontale/vertikale Distanz der Daten im Browser-Fenster beziehen. Genauer gesagt, auf den Browser
title: Browserbreite/-höhe
topic: Metrics
uuid: 1c0d3ea9-e001-4152-9bfc-8fe6406bc755
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Browserbreite/-höhe

Metriken, die sich ausschließlich auf die horizontale/vertikale Distanz der Daten im Browser-Fenster beziehen. Genauer gesagt, auf den Browser

Adobe Analytics verwendet die Browserhöhe und -breite lediglich vom ersten Treffer eines Besuchs an. Die übrigen Treffer erhalten nicht die Zuordnung für den gleichen Besuch.
Die Abmessungen von Browserbreite/-höhe sind ähnlich, aber nicht identisch mit der [Bildschirmgröße bei Mobilgeräten](/help/components/c-variables/dimensionslist/reports-mobile.md#topic_D306EA4558194488AC47A45B9C570150).

Wenn beispielsweise die Browserbreite oder -höhe auf die Auflösung von Mobilgeräten herunterskaliert werden, sollten folgende Unterscheidungen beachtet werden:

* Die Mobilgeräteauflösungen entsprechen den physischen Werten des Geräts. Beispielsweise erscheint das Galaxy S8 unter „Mobilgeräteauflösungen“ als 2.960 x 1.440. Die Mobilgeräteauflösung erhalten wir von einem Drittanbieter, nachdem das Gerät erkannt wurde.
* Im Gegensatz dazu sehen Sie bei den Werten zu Browserbreite und -höhe die (logischen) CSS-Werte von 740 x 360. Die Browserwerte hängen von JavaScript/CSS-Daten ab.
* Eine kurze Diskussion dazu finden Sie [in diesem Thread](https://stackoverflow.com/questions/8785643/what-exactly-is-device-pixel-ratio).

