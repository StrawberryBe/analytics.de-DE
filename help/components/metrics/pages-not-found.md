---
title: Seiten nicht gefunden (Metriken)
description: Die Anzahl der Treffer, die einen Fehler enthalten.
feature: Dimensions
exl-id: 28c22565-7fcf-49f1-8876-0db88f12a182
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Seiten nicht gefunden

*Auf dieser Hilfeseite wird beschrieben, wie „Seiten nicht gefunden“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).*

Die Metrik „Seiten nicht gefunden“ zeigt die Anzahl der Treffer an, bei denen die Seite einen Fehler enthielt. Diese Metrik ist nützlich, wenn Sie sehen möchten, welche Seiten oder URLs Fehlermeldungen enthalten haben (z. B. 404), sodass Sie die Fehlerursache ermitteln und beheben können.

* Berechnung dieser Metrik[](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)
* Diese Metrik zählt alle Treffer, bei denen die [`pageType`](/help/implement/vars/page-vars/pagetype.md)-Variable dem Wert von `"errorPage"` entspricht. Dies ist das Metrik-Äquivalent der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).](referrer.md)

## Populate this dimension with data

This dimension retrieves data from the [`pageType` and `g` query strings](/help/implement/validate/query-parameters.md) in image requests. If the `pageType` query string equals `errorPage`, the `g` query string (page URL) is recorded. AppMeasurement collects this data using the [`pageType`](/help/implement/vars/page-vars/pagetype.md) variable. If the `pageType` variable is not defined or set to anything other than `errorPage`, no data for this dimension is collected.

## Dimension items

Dimension items include the URLs of pages on your site where an error occurred.
