---
description: Die Frequenz, mit der ein bestimmter Wert erfasst wird, plus die Anzahl der Seitenansichten, für die dieser Wert weiter besteht. Das heißt, Vorfälle sind die Summe der Seitenansichten und der Seitenereignisse. Vorkommen sind in Analysis Workspace und Ad Hoc Analysis zu finden.
seo-description: Die Frequenz, mit der ein bestimmter Wert erfasst wird, plus die Anzahl der Seitenansichten, für die dieser Wert weiter besteht. Das heißt, Vorfälle sind die Summe der Seitenansichten und der Seitenereignisse. Vorkommen sind in Analysis Workspace und Ad Hoc Analysis zu finden.
seo-title: Vorfälle
solution: Analytics
title: Vorfälle
topic: Metriken
uuid: ff 999 fba-fcb 7-4 b 16-9446-001 facd 0 f 15 d
translation-type: tm+mt
source-git-commit: ecc762f73f9a303cebf48668b807fef9a2f055c5

---


# Vorfälle

Die Frequenz, mit der ein bestimmter Wert erfasst wird, plus die Anzahl der Seitenansichten, für die dieser Wert weiter besteht. Das heißt, Vorfälle sind die Summe der Seitenansichten und der Seitenereignisse. Vorkommen sind in Analysis Workspace und Ad Hoc Analysis zu finden.

## Vergleichen von Instanzen und Vorfällen {#section_4B0741AC1A78456E98AE0D4D28D70D29}

Zwei Metriken sind aufgeführt, die sich zu ähneln scheinen:

**[Instanzen](../../../components/c-variables/c-metrics/metrics-instance.md#concept_E3D0FEC81E1F4987B39CC467F19FFCFF)**: Gibt an, wie oft ein Wert für eine Variable festgelegt wurde.

**Vorfälle**: Gibt an, wie oft ein Wert insgesamt festgelegt oder beibehalten wurde.

| Situation | Beschreibung |
|---|---|
| Vorfälle größer als Instanzen | Dies muss für Konversionsvariablen erwartet werden, weil Vorfälle auch beinhalten, wie oft die Variable festgelegt wurde (Instanzen). |
| Instanzen größer als Vorfälle | Dies ist für Berichte nicht möglich, weil alle Instanzen auch als Vorfälle erfasst werden. |
| Instanzen gleich Vorfälle | Dies ist für Traffic-Variablen der Normalfall, weil sie naturgemäß nach der Bildanforderung nicht mehr weiter bestehen. |

>[!MORE_LIKE_THIS]
>
>* [Instanzen](/help/components/c-variables/c-metrics/metrics-instance.md)

