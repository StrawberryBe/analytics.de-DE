---
title: Cookie-Unterstützung
description: Stellt fest, ob der Browser Cookies unterstützt.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Cookie-Unterstützung

Die Dimension &quot;Cookie-Unterstützung&quot;wird angezeigt, wenn der Browser Cookies für einen bestimmten Treffer unterstützt. Es ist nützlich, den Anteil der Besucher zu ermitteln, die Browser verwenden, die Cookies unterstützen, und diejenigen, die sie absichtlich deaktivieren.

## Diese Dimension mit Daten füllen

Diese Dimension erfasst Daten aus der [`k` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen. AppMeasurement versucht, ein Cookie mit dem Namen `s_cc`zu setzen und erkennt dann, ob das Cookie vorhanden ist. Das Ergebnis ist der Parameterwert für die Zeichenfolge der Abfrage `Y` (wenn der Browser Cookies unterstützt und aktiviert hat) oder `N` (wenn die Cookies im Browser deaktiviert sind). Wenn Sie AppMeasurement verwenden (z. B. beim Starten der Adobe Experience Platform), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie bei jedem Treffer den Parameter für die `k` Abfrage-Zeichenfolge mit dem Wert `Y` oder `N`dem Wert angeben.

## Dimensionselemente

Dimensionselemente umfassen `Enabled`, `Disabled`und `Unknown`.

* **`Enabled`**: Der Browser unterstützt Cookies und aktiviert sie.
* **`Disabled`**: Cookies werden vom Browser nicht unterstützt oder vom Besucher deaktiviert.
* **`Unknown`**: AppMeasurement konnte die Cookie-Unterstützung nicht ermitteln. Die `k` Abfrage-Zeichenfolge war in der Bildanforderung nicht vorhanden.
