---
title: 'Instanzen '
description: Die Anzahl der Treffer, die eine Variable festgelegt (und nicht beibehalten) wurde.
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 1%

---


# Instanzen 

Die Metrik &quot;Instanzen&quot;zeigt an, wie oft eine Dimension explizit in einer Bildanforderung definiert wurde. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), behalten ihre Dimensionswerte über den Treffer hinaus bei, für den sie festgelegt wurden. Diese Metrik ist nützlich, wenn Sie sehen möchten, wie oft ein Dimensionswert ohne Treffer festgelegt wurde, bei denen dieser Wert beibehalten wurde.

## Berechnung dieser Metrik

Schließen Sie von allen Treffern in einer Report Suite nur Treffer ein, die explizit einen Dimensionswert in der Bildanforderung festlegen. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), bleiben über den Treffer hinaus erhalten, für den sie festgelegt wurden. Metriken wie [Seitenwerte](page-views.md) und [Vorfälle](occurrences.md) zählen sowohl Anfangswerte als auch beibehaltene Ansichten. Diese Metrik zählt keine beständigen Werte.