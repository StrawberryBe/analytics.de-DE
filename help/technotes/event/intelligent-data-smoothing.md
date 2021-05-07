---
title: Intelligente Datenausgleichung
description: Erfahren Sie, wie Intelligente Datenausgleichung historische Trends analysiert, um den Wert einer Metrik innerhalb eines betroffenen Zeitraums vorherzusagen.
feature: AI-Tools
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: aa9f0a8f5b7b1780d0b0be729775c573e12caa35
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%

---

# Intelligente Datenausgleichung

In seltenen Fällen können einige Faktoren die Datenqualität beeinflussen. Bot-Traffic, Implementierungsänderungen oder Service-Unterbrechungen können die Integrität der erfassten Daten beeinträchtigen. Sie verkomplizieren auch die Analyse, wie sich das Ereignis auf die Datenvollständigkeit ausgewirkt haben könnte.

Intelligente Datenausgleichung ist ein Prototyp in [Analytics Labs](/help/analyze/tech-previews/overview.md), der diese Ansicht durch Analyse historischer Trends abschließen kann, um den Wert einer Metrik innerhalb des betreffenden Zeitraums vorherzusagen. Der Prototyp wendet erweiterte Algorithmen des maschinellen Lernens an, um die erwarteten Werte für die Metriken im Analysezeitraum darzustellen.

## Intelligente Datenglättung ausführen

1. Navigieren Sie zu Adobe Analytics Labs:
   ![Labs](assets/labs.png)
1. Starten Sie den Prototyp &quot;Intelligente Datenglättung&quot;.
   ![Prototyp starten](assets/intelligent-ds.png)
1. hinzufügen die Metrik, die in die Freiform-Tabelle analysiert werden muss. Der Prototyp funktioniert nur mit täglicher Granularität. Achten Sie daher darauf, dass die Dimension in der Tabelle &quot;Tag&quot;lautet.
   ![Metrik hinzufügen](assets/add-metric.png)
1. Wählen Sie einen Datumsbereich, der größer als das Ereignis ist, stellen Sie jedoch sicher, dass das Ereignis darin enthalten ist.
   ![Datumsbereich](assets/date-range.png)
1. Klicken Sie auf das Zahnradsymbol für die Metrik in der Freiform-Tabelle.
   ![Zahnradsymbol](assets/gear-icon.png)
1. Wählen Sie unter [!UICONTROL Dateneinstellungen] die Option [!UICONTROL Datenglättung].
   ![Datenglättung](assets/column-setting.png)
1. Wählen Sie den Datums-/Datumsbereich für das Ereignis aus und klicken Sie auf [!UICONTROL Apply].
Stellen Sie sicher, dass der Datenbereich für die Datenglättung eine Untergruppe des für den Bereich ausgewählten Datumsbereichs ist. Die Metrik in der Tabelle und im Diagramm werden durch die prognostizierten Werte ersetzt.
   ![Prognostizierte Werte](assets/predictive-values.png)