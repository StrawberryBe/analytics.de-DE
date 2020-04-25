---
description: Die Frequenz, mit der ein bestimmter Wert erfasst wird, plus die Anzahl der Seitenansichten, für die dieser Wert weiter besteht. Das heißt, Vorfälle sind die Summe der Seitenansichten und der Seitenereignisse. Vorkommen sind in Analysis Workspace und Ad Hoc Analysis zu finden.
title: Vorfälle
topic: Metrics
uuid: ff999fba-fcb7-4b16-9446-001facd0f15d
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Vorfälle

Die Frequenz, mit der ein bestimmter Wert erfasst wird, plus die Anzahl der Seitenansichten, für die dieser Wert weiter besteht. Das heißt, Vorfälle sind die Summe der Seitenansichten und der Seitenereignisse. Vorkommen sind in Analysis Workspace und Ad Hoc Analysis zu finden.

## Vergleichen von Instanzen und Vorfällen  {#section_4B0741AC1A78456E98AE0D4D28D70D29}

Zwei Metriken sind aufgeführt, die sich zu ähneln scheinen:

**[Instanzen](/help/components/c-variables/c-metrics/metrics-instance.md)**: Gibt an, wie oft ein Wert für eine Variable festgelegt wurde.

**Vorfälle**: Gibt an, wie oft ein Wert insgesamt festgelegt oder beibehalten wurde.

| Situation | Beschreibung |
|---|---|
| Vorfälle größer als Instanzen | Dies muss für Konversionsvariablen erwartet werden, weil Vorfälle auch beinhalten, wie oft die Variable festgelegt wurde (Instanzen). |
| Instanzen größer als Vorfälle | Dies ist für Berichte nicht möglich, weil alle Instanzen auch als Vorfälle erfasst werden. |
| Instanzen gleich Vorfälle | Dies ist für Traffic-Variablen der Normalfall, weil sie naturgemäß nach der Bildanforderung nicht mehr weiter bestehen. |

>[!MORELIKETHIS]
>
>* [Instanzen](/help/components/c-variables/c-metrics/metrics-instance.md)

