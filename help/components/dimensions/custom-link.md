---
title: Benutzerspezifischer Link
description: Der Name des benutzerspezifischen Links.
translation-type: tm+mt
source-git-commit: 423e9b753a3b7b1e0a8e8b9748f9694d718abd18
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 80%

---


# Benutzerspezifischer Link

Die Dimension „Benutzerspezifischer Link“ enthält die Namen der auf Ihrer Site implementierten benutzerspezifischen Links. Diese Dimension ist nützlich, wenn Sie wissen möchten, auf welche Links Besucher am häufigsten klicken.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen für Treffer, die auch die Abfragezeichenfolge `pe` mit dem Wert `lnk_o` aufweisen. Wenn die Abfragezeichenfolge `pe` im Treffer einen anderen Wert hat, werden in dieser Dimension keine Daten erfasst.

Wenn Sie Daten mit AppMeasurement an diese Dimension senden möchten, senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md)-Bildanforderung mit einem Linktyp-Argument `"o"`. Füllen Sie das Linknamenargument mit dem gewünschten Wert.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren.
