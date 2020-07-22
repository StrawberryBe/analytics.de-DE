---
title: Seiten nicht gefunden
description: URLs, die einen Fehler auf Ihrer Site zurückgegeben haben.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 2%

---


# Seiten nicht gefunden

*Auf dieser Hilfeseite wird beschrieben, wie &quot;Seiten nicht gefunden&quot;als Dimension funktioniert. Weitere Informationen finden Sie in der Metrik &quot;[Seiten nicht gefunden](../metrics/pages-not-found.md)&quot;.*

Die Dimension &quot;Seiten nicht gefunden&quot;zeigt URLs an, die einen Fehler enthalten. Diese Dimension ist nützlich, wenn Sie die Anzahl der Fehler verringern möchten, die Besucher auf Ihrer Site erhalten.

* Sie können diese Dimension in einer [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) verwenden, um zu sehen, durch welche Seiten Besucher den Fehler erreichen. Anschließend können Sie mit Entwicklungsteams in Ihrem Unternehmen zusammenarbeiten, um den Link auf jeder Seite zu reparieren.
* Sie können diese Dimension mit der Dimension [&quot;Werber&quot;verwenden, um zu sehen, wo Besucher über externe Links zu Ihrer Site gelangen](referrer.md) . Sie können dann entweder Umleitungen zum gewünschten Ort implementieren oder mit dem Drittanbieter zusammenarbeiten, um den Link zu reparieren.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus den Zeichenfolgen [`pageType` und der `g` Abfrage](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. Wenn die `pageType` Abfrage gleich `errorPage`ist, wird die `g` Abfrage (Seiten-URL) aufgezeichnet. AppMeasurement erfasst diese Daten mit der [`pageType`](/help/implement/vars/page-vars/pagetype.md) Variablen. Wenn die `pageType` Variable nicht definiert oder auf einen anderen Wert als `errorPage`festgelegt ist, werden keine Daten für diese Dimension erfasst.

## Dimensionselemente

Dimensionselemente umfassen die URLs der Seiten auf Ihrer Site, auf denen ein Fehler aufgetreten ist.
