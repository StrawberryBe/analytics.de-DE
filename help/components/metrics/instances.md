---
title: Instanzen
description: Die Anzahl der Treffer, für die eine Variable festgelegt (und nicht beibehalten) wurde.
feature: Metrics
exl-id: 9d1a66b5-46f9-4834-87a1-5f63e386e61d
source-git-commit: 21029930b5cae6acb6bc6a59836ddc1ca33cb27e
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 65%

---

# Instanzen

Die Metrik „Instanzen“ zeigt an, wie oft eine Dimension explizit in einer Bildanforderung definiert wurde. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), behalten ihre Dimensionselemente über den Treffer hinaus bei, für den sie festgelegt wurden. Diese Metrik ist nützlich, wenn Sie sehen möchten, wie oft ein Dimensionselement ohne die Treffer festgelegt wurde, bei denen dieser Wert beibehalten wurde.

## Berechnung dieser Metrik

Schließen Sie von allen Treffern in einer Report Suite nur Treffer ein, die explizit ein Dimensionselement in der Bildanforderung festlegen. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), bleiben über den Treffer hinaus bestehen, für den sie festgelegt wurden. Metriken, wie [Seitenansichten](page-views.md) und [Vorfälle](occurrences.md), zählen sowohl Anfangswerte als auch beibehaltene Werte. Diese Metrik zählt keine persistenten Werte.

Beispiel: Ein Besucher gelangt auf Ihre Site und verwendet die interne Suche. Sie verfolgen die interne Suche in eVar1. Nachdem sie die interne Suche einmal verwendet haben, besuchen sie fünf weitere Seiten, bevor sie gehen.

Wenn Sie einen Bericht in Workspace anzeigen, würden Sie eine eVar1-Instanz und sechs Vorkommen sehen. Die eine Instanz, die auf der Suchergebnisseite ausgelöst wurde, während die Instanzen den Anfangswert sowie die beibehaltenen Werte gezählt haben.
