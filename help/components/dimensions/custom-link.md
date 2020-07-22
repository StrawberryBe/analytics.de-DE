---
title: Benutzerspezifischer Link
description: Der Name des benutzerspezifischen Links.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Benutzerspezifischer Link

Die Dimension &quot;Benutzerspezifischer Link&quot;zeigt die Namen von benutzerspezifischen Links an, die auf Ihrer Site implementiert sind. Diese Dimension ist nützlich, wenn Sie wissen möchten, auf welche Links Besucher am häufigsten klicken.

## Diese Dimension mit Daten füllen

Diese Dimension erfasst Daten aus der [`pev2` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen für Treffer, die auch die `pe` Abfrage-Zeichenfolge mit dem Wert &quot; `lnk_o`. Wenn die `pe` Abfrage-Zeichenfolge im Treffer einen anderen Wert hat, werden keine Daten von dieser Dimension erfasst.

Wenn Sie Daten mit AppMeasurement an diese Dimension senden möchten:

* Füllen Sie die [`linkName`](/help/implement/vars/config-vars/linkname.md) Variable mit dem gewünschten Wert.
* Set the [`linkType`](/help/implement/vars/config-vars/linktype.md) variable to `"o"`.
* Senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md) Bildanforderung.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente sind. Adobe empfiehlt, Links je nach Bedarf des Berichte in aussagekräftige Kategorien zu gruppieren.
