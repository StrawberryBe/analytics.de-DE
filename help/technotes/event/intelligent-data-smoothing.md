---
title: Intelligente Datenausgleichung
description: Erfahren Sie, wie intelligente Datenausgleichung historische Trends analysiert, um den Wert einer Metrik innerhalb eines betroffenen Zeitraums vorherzusagen.
feature: KI-Tools
role: User, Admin
source-git-commit: a9d892ab8caaeb797fbbd9b5aa136c5dab76f8bd
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 5%

---

# Intelligente Datenausgleichung

In seltenen Fällen können einige Faktoren die Datenqualität beeinflussen. Bot-Traffic, Implementierungsänderungen oder Dienstunterbrechungen können sich auf die Integrität der erfassten Daten auswirken. Sie verkomplizieren auch die Analyse, wie sich das Ereignis auf die Vollständigkeit der Daten ausgewirkt haben kann.

Intelligente Datenausgleichung ist ein Prototyp in [Analytics Labs](/help/analyze/labs.md), der dazu beitragen kann, diese Ansicht abzuschließen, indem historische Trends analysiert werden, um den Wert einer Metrik im betroffenen Zeitraum vorherzusagen. Der Prototyp wendet erweiterte maschinelle Lernalgorithmen an, um die erwarteten Werte für Metriken im Analysezeitraum darzustellen.

## Intelligente Datenausgleichung ausführen

1. Navigieren Sie zu Adobe Analytics Labs:
   ![Labs](assets/labs.png)
1. Starten Sie den Prototyp Intelligente Datenausgleichung .
   ![Launch-Prototyp](assets/intelligent-ds.png)
1. Fügen Sie die zu analysierende Metrik zur Freiformtabelle hinzu. Der Prototyp arbeitet nur mit einer täglichen Granularität. Stellen Sie daher sicher, dass die Dimension in der Tabelle &quot;Tag&quot;ist.
   ![Metrik hinzufügen](assets/add-metric.png)
1. Wählen Sie einen Datumsbereich aus, der größer als das Fenster des Ereignisses ist, stellen Sie jedoch sicher, dass er das Ereignis enthält.
   ![Datumsbereich](assets/date-range.png)
1. Klicken Sie auf das Zahnradsymbol für die Metrik in der Freiformtabelle.
   ![Zahnradsymbol](assets/gear-icon.png)
1. Wählen Sie unter [!UICONTROL Dateneinstellungen] die Option [!UICONTROL Datenausgleichung] aus.
   ![Datenausgleichung](assets/column-setting.png)
1. Wählen Sie das Datum/den Datumsbereich aus, das/der dem Ereignis entspricht, und klicken Sie auf [!UICONTROL Anwenden].
Stellen Sie sicher, dass der Datenbereich für die Datenausgleichung eine Teilmenge des für den Bereich ausgewählten Datumsbereichs ist. Die Metrik in der Tabelle und im Diagramm werden durch die prognostizierten Werte ersetzt.
   ![Vorhergesagte Werte](assets/predictive-values.png)
