---
title: Farbtiefe
description: Die Farbtiefe des Geräts.
translation-type: tm+mt
source-git-commit: a8dc233e962a49674a30ff3c9f0b5d0d45b09f24
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Farbtiefe

Die Dimension &quot;Farbtiefe&quot;zeigt an, wie viele Farben das Gerät unterstützt. Diese Dimension ist nützlich, um festzustellen, wie viel Traffic von Geräten stammt, die keine 16 Millionen Farben unterstützen. Historisch gesehen war dieser Bericht wertvoll, als das aufstrebende mobile Web neu war; Die meisten Geräte im aktuellen Alter unterstützen jedoch 16 Millionen Farben (0-255 für Rot, Grün und Blau). <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## Diese Dimension mit Daten füllen

Diese Dimension referenziert eine Suchtabelle und übersetzt den Bitwert in ein lesbareres Format. Es erfasst Daten aus der [`c` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen. AppMeasurement verwendet die `screen.colorDepth` Variable, um die Abfrage der Bildanforderung zu füllen. Wenn Sie AppMeasurement verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter für die `c` Abfrage-Zeichenfolge bei jedem Treffer mit einem gültigen Bitwert einschließen.

## Dimensionswerte

Dimensionswerte beinhalten die Anzahl der vom Gerät unterstützten Farben. Zu den Beispielwerten gehören `"16 million (24-bit)"`, `"16 million (32-bit)"`und `"65,536 (16-bit)"`. Wenn AppMeasurement nicht in der Lage ist, die Farbtiefe zu bestimmen, wird dies als `"None"`.

> [!TIP] Der Unterschied zwischen 24-Bit- und 32-Bit-Unterstützung besteht darin, dass 32-Bit einen Alpha-Kanal (RGBA) unterstützen, während 24-Bit dies nicht (RGB) tun. Weitere Informationen zu diesem Konzept finden Sie unter [Farbtiefe](https://en.wikipedia.org/wiki/Color_depth) auf Wikipedia.
