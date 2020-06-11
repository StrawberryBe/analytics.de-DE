---
title: Download-Link
description: Der Name des Downloadlinks.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 15%

---


# Download-Link

Die Dimension &quot;Download-Link&quot;enthält die Namen der auf Ihrer Site implementierten Downloadlinks. Diese Dimension ist nützlich, wenn Sie mehr über das Verhalten von Besuchern bei Downloadlinks erfahren möchten, z. B.:

* die Dateien zu bestimmen, die am häufigsten von Ihrer Site heruntergeladen werden.
* zu erkennen, ob bestimmte Dateien zu bestimmten Zeiten häufiger heruntergeladen werden.
* Überprüfen Sie, ob Besucher verschiedene Dateitypen herunterladen können, falls diese angeboten werden.

## Diese Dimension mit Daten füllen

Diese Dimension erfasst Daten aus der [`pev2` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen für Treffer, die auch die `pe` Abfrage-Zeichenfolge mit dem Wert &quot; `lnk_d`. Wenn die `pe` Abfrage-Zeichenfolge im Treffer einen anderen Wert hat, werden keine Daten von dieser Dimension erfasst.

Wenn Sie Daten mit AppMeasurement an diese Dimension senden möchten:

* Füllen Sie die [`linkName`](/help/implement/vars/config-vars/linkname.md) Variable mit dem gewünschten Wert.
* Set the [`linkType`](/help/implement/vars/config-vars/linktype.md) variable to `"d"`.
* Senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md) Bildanforderung.

## Dimensionswerte

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionswerte verwendet werden. Adobe empfiehlt, Links je nach Bedarf des Berichte in aussagekräftige Kategorien zu gruppieren.
