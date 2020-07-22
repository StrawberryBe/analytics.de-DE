---
title: Ausstiegslink
description: Der Name des Ausstiegslinks.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Ausstiegslink

Die Dimension &quot;Ausstiegslink&quot;enthält die Namen der Ausstiegslinks, die auf Ihrer Site implementiert sind. Diese Dimension ist nützlich, wenn Sie wissen möchten, welche Links am beliebtesten sind und auf Domänen außerhalb Ihrer Site verweisen.

## Diese Dimension mit Daten füllen

Diese Dimension erfasst Daten aus der [`pev2` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen für Treffer, die auch die `pe` Abfrage-Zeichenfolge mit dem Wert &quot; `lnk_e`. Wenn die `pe` Abfrage-Zeichenfolge im Treffer einen anderen Wert hat, werden keine Daten von dieser Dimension erfasst.

Wenn Sie Daten mit AppMeasurement an diese Dimension senden möchten:

* Füllen Sie die [`linkName`](/help/implement/vars/config-vars/linkname.md) Variable mit dem gewünschten Wert.
* Set the [`linkType`](/help/implement/vars/config-vars/linktype.md) variable to `"e"`.
* Senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md) Bildanforderung.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente sind. Adobe empfiehlt, Links je nach Bedarf des Berichte in aussagekräftige Kategorien zu gruppieren.
