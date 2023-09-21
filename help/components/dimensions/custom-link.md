---
title: Benutzerspezifischer Link
description: Der Name des benutzerspezifischen Links.
feature: Dimensions
exl-id: c153f710-f03f-4be6-8e18-5ebf2ed80f01
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 90%

---

# Benutzerspezifischer Link

Der benutzerspezifische Link [Dimension](overview.md) gibt die Namen der auf Ihrer Site implementierten benutzerspezifischen Links an. Diese Dimension ist nützlich, wenn Sie wissen möchten, auf welche Links Besucher am häufigsten klicken.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen für Treffer, die auch die Abfragezeichenfolge `pe` mit dem Wert `lnk_o` aufweisen. Wenn die Abfragezeichenfolge `pe` im Treffer einen anderen Wert hat, werden in dieser Dimension keine Daten erfasst.

Wenn Sie mit AppMeasurement Daten an diese Dimension senden möchten, senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md)-Bildanforderung mit einem Link-Typ-Argument `"o"`. Geben Sie im Linkname-Argument den gewünschten Wert an.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren.
