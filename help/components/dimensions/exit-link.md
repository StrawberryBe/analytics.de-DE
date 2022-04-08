---
title: Exitlink
description: Der Name des Exitlinks.
feature: Dimensions
exl-id: 090d5fee-4b35-4be7-866c-5ef1d1c4c0a6
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '156'
ht-degree: 100%

---

# Exitlink

Die Dimension „Exitlink“ enthält die Namen der auf Ihrer Site implementierten Exitlinks. Diese Dimension ist nützlich, wenn Sie wissen möchten, welche Links am beliebtesten sind und auf Domänen außerhalb Ihrer Site verweisen.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen für Treffer, die auch die Abfragezeichenfolge `pe` mit dem Wert `lnk_e` aufweisen. Wenn die Abfragezeichenfolge `pe` im Treffer einen anderen Wert hat, werden in dieser Dimension keine Daten erfasst.

Wenn Sie mit AppMeasurement Daten an diese Dimension senden möchten, senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md)-Bildanforderung mit einem Link-Typ-Argument `"e"`. Geben Sie im Linkname-Argument den gewünschten Wert an.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren.
