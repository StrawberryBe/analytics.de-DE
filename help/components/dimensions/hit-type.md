---
title: Treffertyp
description: Bestimmt, ob es sich bei dem Treffer um einen Vordergrund- oder Hintergrundschlag handelt.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# Treffertyp

Die Dimension &quot;Treffertyp&quot;bestimmt, ob sich eine mobile App im Vordergrund oder Hintergrund befindet, wenn der Treffer an Adobe-Datenerfassungsserver gesendet wurde. Diese Dimension ist nur für Report Suites relevant, die Daten für mobile Anwendungen enthalten. Über AppMeasurement erfasste Browserdaten melden den Treffer immer als &quot;Vordergrund&quot;.

## Diese Dimension mit Daten füllen

Diese Dimension funktioniert bei allen mobilen SDK-Implementierungen ab Version 4.13.6 standardmäßig. Wenn Sie das mobile SDK nicht verwenden, werden alle Treffer unter dem Dimensionswert &quot;Vordergrund&quot;Liste. If &quot;Disable Legacy Reporting and Attribution for Background Hits&quot; is checked, then background hits will show up only in [Virtual report suites](../vrs/vrs-mobile-visit-processing.md).

## Dimensionswerte

Dimensionswerte enthalten `"Foreground"` und `"Background"`. Jeder Treffer, der nicht im Hintergrund einer mobilen Anwendung gesendet wurde, gehört zum `"Foreground"` Dimensionswert. Jeder Treffer, der gesendet wird, wenn sich die Mobilanwendung im Hintergrund befindet, gehört zum `"Background"` Dimensionswert.
