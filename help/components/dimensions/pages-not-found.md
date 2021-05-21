---
title: Seiten nicht gefunden
description: URLs, die einen Fehler auf Ihrer Site zurückgegeben haben.
exl-id: 28c22565-7fcf-49f1-8876-0db88f12a182
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '214'
ht-degree: 100%

---

# Seiten nicht gefunden

*Auf dieser Hilfeseite wird beschrieben, wie „Seiten nicht gefunden“ als Dimension funktioniert. Weitere Informationen finden Sie unter der Metrik [Seiten nicht gefunden](../metrics/pages-not-found.md).*

Die Dimension „Seiten nicht gefunden“ gibt URLs an, die einen Fehler enthalten. Diese Dimension ist nützlich, wenn Sie die Anzahl der Fehler verringern möchten, die Besucher auf Ihrer Site erhalten.

* Sie können diese Dimension in einer [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) verwenden, um zu sehen, durch welche Seiten Besucher klicken, um den Fehler zu erreichen. Anschließend können Sie mit Entwicklungs-Teams in Ihrem Unternehmen zusammenarbeiten, um den Link auf jeder Seite zu reparieren.
* Sie können diese Dimension mit der Dimension [Referrer](referrer.md) verwenden, um zu sehen, wo Besucher über externe Links zu Ihrer Site gelangen. Sie können dann entweder Umleitungen zum gewünschten Ort implementieren oder mit dem Drittanbieter zusammenarbeiten, um den Link zu reparieren.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus den  [`pageType`- und `g`-Abfragezeichenfolgen](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. Wenn die Abfragezeichenfolge `pageType` gleich `errorPage` ist, wird die Abfragezeichenfolge `g` (Seiten-URL) aufgezeichnet. AppMeasurement erfasst diese Daten mit der [`pageType`](/help/implement/vars/page-vars/pagetype.md)-Variable. Wenn die Variable `pageType` nicht definiert oder auf einen anderen Wert als `errorPage` festgelegt ist, werden keine Daten für diese Dimension erfasst.

## Dimensionselemente

Zu den Dimensionselementen gehören die URLs der Seiten auf Ihrer Site, auf denen ein Fehler aufgetreten ist.
