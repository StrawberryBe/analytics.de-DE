---
title: Treffertyp
description: Bestimmt, ob es sich bei dem Treffer um einen Vordergrund- oder Hintergrundtreffer handelt.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '163'
ht-degree: 100%

---


# Treffertyp

Die Dimension „Treffertyp“ bestimmt, ob sich eine mobile App im Vordergrund oder Hintergrund befand, wenn der Treffer an die Datenerfassungs-Server der Adobe gesendet wurde. Diese Dimension ist nur für Report Suites relevant, die Daten für mobile Apps enthalten. Über AppMeasurement erfasste Browser-Daten melden den Treffer immer als „Vordergrund“.

## Füllen dieser Dimension mit Daten

Diese Dimension funktioniert bei allen Mobile SDK-Implementierungen ab Version 4.13.6 standardmäßig. Wenn Sie das Mobile SDK nicht verwenden, werden alle Treffer unter dem Dimensionselement „Vordergrund“ aufgelistet. Wenn „Ältere Berichterstellung und Attribution deaktivieren, um Hintergrundtreffer zu erhalten“ ausgewählt wird, werden Hintergrundtreffer nur in [Virtual Report Suites](../vrs/vrs-mobile-visit-processing.md) angezeigt.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Foreground"` und `"Background"`. Jeder Treffer, der nicht im Hintergrund einer mobilen App gesendet wurde, gehört zum Dimensionselement `"Foreground"`. Jeder Treffer, der gesendet wird, wenn die mobile App im Hintergrund war, gehört zum Dimensionselement `"Background"`.
