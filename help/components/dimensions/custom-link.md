---
title: Benutzerspezifischer Link
description: Der Name des benutzerspezifischen Links.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '148'
ht-degree: 100%

---


# Benutzerspezifischer Link

Die Dimension „Benutzerspezifischer Link“ enthält die Namen der auf Ihrer Site implementierten benutzerspezifischen Links. Diese Dimension ist nützlich, wenn Sie wissen möchten, auf welche Links Besucher am häufigsten klicken.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen für Treffer, die auch die Abfragezeichenfolge `pe` mit dem Wert `lnk_o` aufweisen. Wenn die Abfragezeichenfolge `pe` im Treffer einen anderen Wert hat, werden in dieser Dimension keine Daten erfasst.

Wenn Sie Daten mit AppMeasurement an diese Dimension senden möchten:

* Füllen Sie die [`linkName`](/help/implement/vars/config-vars/linkname.md)-Variable mit dem gewünschten Wert.
* Stellen Sie die [`linkType`](/help/implement/vars/config-vars/linktype.md)-Variable auf `"o"` ein.
* Senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md)-Bildanforderung.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren.
