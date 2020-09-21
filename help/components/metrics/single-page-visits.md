---
title: Einzelseitenbesuche
description: Die Häufigkeit, mit der sich das Dimensionselement „Seite“ bei einem Besuch nicht geändert hat.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '166'
ht-degree: 100%

---


# Einzelseitenbesuche

*Auf dieser Hilfeseite wird beschrieben, wie „Einzelseitenbesuche“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Einzelseitenbesuche](../dimensions/single-page-visits.md).*

Die Metrik „Einzelseitenbesuche“ gibt die Anzahl der Besuche an, bei denen das Dimensionselement [Seite](../dimensions/page.md) nur einen einzigen eindeutigen Wert für den gesamten Besuch enthielt. Diese Metrik ist hilfreich im Zusammenhang mit Dimensionen, in denen Sie kurze Besuche sehen möchten, aber keine so strengen Regeln wie [Absprünge](bounces.md) haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Besuche, bei denen das Dimensionselement „Seite“ nur einen einzigen eindeutigen Wert für den gesamten Besuch enthielt. Wenn ein Besucher die Seite neu lädt oder Linktracking-Aufrufe auslöst, zählt dies immer noch als Einzelseitenbesuch. Sobald die Dimension „Seite“ in einen zweiten eindeutigen Wert geändert wird, gilt der Besuch nicht mehr als ein Einzelseitenbesuch.

Einen Vergleich der Metriken finden Sie unter [Einzelzugriff](single-access.md).
