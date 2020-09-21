---
title: Cookie-Unterstützung
description: Stellt fest, ob der Browser Cookies unterstützt.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '187'
ht-degree: 100%

---


# Cookie-Unterstützung

Die Dimension „Cookie-Unterstützung“ wird angezeigt, wenn der Browser Cookies für einen bestimmten Treffer unterstützt. Es ist nützlich, den Anteil der Besucher zu ermitteln, die Browser verwenden, die Cookies unterstützen, und diejenigen, die sie absichtlich deaktivieren.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`k`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen. AppMeasurement versucht, ein Cookie mit dem Namen `s_cc` zu setzen und erkennt dann, ob das Cookie vorhanden ist. Das Ergebnis ist der Zeichenfolgenparameterwert `Y` (wenn der Browser Cookies unterstützt und diese aktiviert hat) oder `N` (wenn die Cookies im Browser deaktiviert sind). Wenn Sie AppMeasurement verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `k` bei jedem Treffer mit dem Wert `Y` oder `N` einbeziehen.

## Dimensionselemente

Zu den Dimensionselementen gehören `Enabled`, `Disabled` und `Unknown`.

* **`Enabled`**: Der Browser unterstützt Cookies und hat diese aktiviert.
* **`Disabled`**: Cookies werden vom Browser nicht unterstützt oder sie wurden vom Besucher deaktiviert.
* **`Unknown`**: AppMeasurement konnte die Cookie-Unterstützung nicht ermitteln. Die Abfragezeichenfolge `k` war in der Bildanforderung nicht vorhanden.
