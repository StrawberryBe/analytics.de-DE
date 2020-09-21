---
title: Downloadlink
description: Der Name des Downloadlinks.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '180'
ht-degree: 100%

---


# Downloadlink

Die Dimension „Downloadlink“ enthält die Namen der auf Ihrer Site implementierten Downloadlinks. Diese Dimension ist nützlich, wenn Sie mehr über das Verhalten von Besuchern bei Downloadlinks erfahren möchten, z. B. um:

* die Dateien zu bestimmen, die am häufigsten von Ihrer Site heruntergeladen werden.
* zu erkennen, ob bestimmte Dateien zu bestimmten Zeiten häufiger heruntergeladen werden.
* zu überprüfen, ob Besucher verschiedene Dateitypen herunterladen können, falls diese angeboten werden.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen für Treffer, die auch die Abfragezeichenfolge `pe` mit dem Wert `lnk_d` aufweisen. Wenn die Abfragezeichenfolge `pe` im Treffer einen anderen Wert hat, werden in dieser Dimension keine Daten erfasst.

Wenn Sie Daten mit AppMeasurement an diese Dimension senden möchten:

* Füllen Sie die [`linkName`](/help/implement/vars/config-vars/linkname.md)-Variable mit dem gewünschten Wert.
* Stellen Sie die [`linkType`](/help/implement/vars/config-vars/linktype.md)-Variable auf `"d"` ein.
* Senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md)-Bildanforderung.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren.
