---
title: Farbtiefe
description: Die Farbtiefe des Geräts.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 94%

---


# Farbtiefe

Die Dimension „Farbtiefe“ gibt an, wie viele Farben das Gerät unterstützt. Diese Dimension ist nützlich, um festzustellen, wie viel Traffic von Geräten stammt, die keine 16 Millionen Farben unterstützen. Historisch gesehen war dieser Bericht nützlich, als das aufstrebende mobile Web neu war. Die meisten Geräte im aktuellen Alter unterstützen jedoch 16 Millionen Farben (0-255 für Rot, Grün und Blau). <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine Suchtabelle und übersetzt den Bitwert in ein lesbareres Format. Sie erfasst Daten aus der [`c`-Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen. AppMeasurement verwendet die `screen.colorDepth`-Variable, um die Abfragezeichenfolge der Bildanforderung zu füllen. Wenn Sie AppMeasurement verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `c` bei jedem Treffer mit einem gültigen Bit-Wert einbeziehen.

## Dimensionen

Dimensionen beinhalten die Anzahl der vom Gerät unterstützten Farben. Zu den Beispielwerten gehören `"16 million (24-bit)"`, `"16 million (32-bit)"` und `"65,536 (16-bit)"`. Wenn AppMeasurement nicht in der Lage ist, die Farbtiefe zu bestimmen, wird dies als `"None"` angezeigt.

>[!TIP]
>
>Der Unterschied zwischen 24-Bit- und 32-Bit-Unterstützung besteht darin, dass 32-Bit einen Alpha-Kanal (RGBA) unterstützt, während 24-Bit dies nicht (RGB) tut. Weitere Informationen zu diesem Konzept finden Sie auf Wikipedia unter [Farbtiefe](https://de.wikipedia.org/wiki/Farbtiefe_(Computergrafik)).
