---
title: Übersicht über den Segmentvergleich
description: Erfahren Sie, wie Sie das Bedienfeld „Segmentvergleich“, Teil von Segment IQ in Analysis Workspace, verwenden.
keywords: Analysis Workspace;Segment IQ
feature: Panels
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 99%

---


# Übersicht über den Segmentvergleich

Das Bedienfeld „Segmentvergleich“ ist ein Tool von [Segment IQ](../../segment-iq.md), das die statistisch bedeutendsten Unterschiede zwischen einer unbegrenzten Anzahl von Segmenten aufdeckt. Die Funktion iteriert durch eine automatisierte Analyse aller Dimensionen und Metriken, auf die Sie Zugriff haben. Sie entdeckt automatisch die wesentlichen Merkmale der Zielgruppensegmente, die für die KPIs Ihres Unternehmens ausschlaggebend sind, und zeigt Ihnen, wie stark sich die Segmente überschneiden.

## Erstellen eines Bedienfelds „Segmentvergleich“

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
1. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
1. Klicken Sie in der oberen Navigationsleiste auf „Workspace“.
1. Klicken Sie auf die Schaltfläche „Neues Projekt erstellen“.
1. Stellen Sie im modalen Popup sicher, dass „Leeres Projekt“ ausgewählt ist, und klicken Sie dann auf „Erstellen“.
1. Klicken Sie auf die Schaltfläche „Bedienfelder“ auf der linken Seite und ziehen Sie dann das Bedienfeld „Segmentvergleich“ über oder unter den automatisch erstellten Freiformtabellenbereich.

   ![Vergleichsbedienfeld](assets/seg-compare-panel.png)

1. Wählen Sie Segmente aus, die Sie vergleichen möchten, und legen Sie diese auf dem Bedienfeld ab.

   ![Zielgruppen vergleichen](assets/compare-audiences.png)

   Nachdem Sie ein Segment in das Bedienfeld gezogen haben, erstellt Analytics automatisch ein Segment [!UICONTROL Alle anderen], das alle NICHT in das ausgewählte Segment eingeschlossenen enthält. Es handelt sich um ein häufig verwendetes Segment im Vergleichsbedienfeld, Sie können es jedoch entfernen und ein anderes Segment Ihrer Wahl vergleichen.

   ![Alle anderen](assets/everyone-else.png)

1. Nachdem Sie ermittelt haben, welche Segmente Sie vergleichen möchten, klicken Sie auf [!UICONTROL Erstellen].

   Diese Aktion startet einen Backend-Prozess, der nach statistischen Unterschieden zwischen den beiden ausgewählten Segmenten und allen Dimensionen, Metriken und anderen Segmenten sucht. Eine Fortschrittsleiste oben im Bedienfeld gibt die verbleibende Zeit an, bis jede Metrik und Dimension analysiert wird. Die am häufigsten verwendeten Metriken, Dimensionen und Segmente werden bei der Ausführung priorisiert, damit die relevantesten Ergebnisse zuerst zurückgegeben werden.

## Ausschluss von Komponenten bei Vergleichen

Manchmal ist es wünschenswert, Dimensionen, Metriken oder Segmente aus Segmentvergleichen auszuschließen. Beispiel: Sie möchten das Segment „Mobile Nutzer aus den USA“ mit „Mobile Nutzer aus Deutschland“ vergleichen. Die Einbeziehung geografischer Dimensionen wäre nicht sinnvoll, da diese Segmente diese Unterschiede bereits implizieren.

1. Nachdem sich die beiden gewünschten Segmente im Bedienfeld befinden, klicken Sie auf [!UICONTROL Erweiterte Optionen anzeigen].
1. Verschieben Sie die Komponenten, die Sie ausschließen möchten, per Drag-and-Drop in den Bereich [!UICONTROL Ausgeschlossene Komponenten].

   ![Ausgeschlossene Komponenten](assets/excluded-components.png)

Klicken Sie auf [!UICONTROL Als Standard festlegen], um Ihre aktuellen Komponenten bei allen zukünftigen Segmentvergleichen automatisch auszuschließen. Wenn Sie ausgeschlossene Komponenten bearbeiten möchten, klicken Sie auf einen Komponententyp und dann auf das X neben einer Komponente, um sie erneut in Ihre Analyse einzuschließen. Klicken Sie auf „Alle löschen“, um alle Komponenten erneut in Ihren Segmentvergleich einzubeziehen.

![Ausgeschlossene Dimensionen](assets/excluded-dimensions.png)

## Anzeigen eines Segmentvergleichsberichts

Nachdem Adobe die Analyse der beiden gewünschten Segmente abgeschlossen hat, werden die Ergebnisse durch verschiedene Visualisierungen angezeigt:

![Visualisierungen 1](assets/new-viz.png)

![Visualisierungen 2](assets/new-viz2.png)

### Größe und Überschneidung

Veranschaulicht die vergleichenden Größen jedes ausgewählten Segments und wie stark sie sich mithilfe eines Venendiagramms überschneiden. Wenn Sie den Mauszeiger auf die Visualisierung bewegen, sehen Sie, wie viele Besucher in den einzelnen sich überschneidenden oder sich nicht überschneidenden Bereichen enthalten sind. Sie können auch mit der rechten Maustaste auf die Überschneidung klicken, um für weitere Analysen ein ganz neues Segment zu erstellen. Wenn sich die beiden Segmente gegenseitig ausschließen, wird keine Überschneidung zwischen den beiden Kreisen angezeigt (typischerweise bei Segmenten, die einen Hit-Container verwenden).

![Größe und Überschneidung](assets/size-overlap.png)

### Populationszusammenfassungen

Rechts neben der Visualisierung „Größe und Überschneidung“ wird die Gesamtzahl der Unique Visitors in jedem Segment und jeder Überschneidung angezeigt.

![Populationszusammenfassungen](assets/population_summaries.png)

### Top-Metriken

Zeigt die statistisch bedeutendsten Metriken für die beiden Segmente an. Jede Zeile dieser Tabelle steht für eine für einen Unterschied sorgende Metrik. Diese Metriken sind danach geordnet, wie stark ihr Unterschied zwischen den einzelnen Segmenten ist. Ein Differenzwert von 1 bedeutet, dass er statistisch signifikant ist, während ein Differenzwert von 0 bedeutet, dass es keine statistische Bedeutung gibt.

Diese Visualisierung ähnelt den Freiformtabellen in Analysis Workspace. Wenn eine tiefere Analyse einer bestimmten Metrik gewünscht wird, halten Sie den Mauszeiger über ein Zeilenelement und klicken Sie auf „Visualisierung erstellen“. Eine neue Tabelle wird erstellt, um diese spezifische Metrik zu analysieren. Wenn eine Metrik für Ihre Analyse irrelevant ist, halten Sie den Mauszeiger über das Zeilenelement und klicken Sie auf das X, um es zu entfernen.

>[!NOTE]
>
>Metriken, die dieser Tabelle nach Abschluss des Segmentvergleichs hinzugefügt wurden, erhalten keine Differenzbewertung.

![Top-Metriken](assets/top-metrics.png)

### Metrik im Zeitverlauf nach Segment

Rechts neben der Tabelle der Metriken befindet sich eine verknüpfte Visualisierung. Sie können auf ein Zeilenelement in der Tabelle links klicken und diese Visualisierung wird aktualisiert, sodass sie die Metrik im Zeitverlauf anzeigt.

![Zeile „Top-Metriken“](assets/linked-viz.png)

### Top-Dimensionen

Zeigt die statistisch signifikantesten Dimensionselemente für alle Dimensionen an. Alle Zeilen zeigen den Prozentsatz der einzelnen Segmente an, die dieses Dimensionselement enthalten. Diese Tabelle könnte beispielsweise zeigen, dass 100 % der Besucher in Segment A das Dimensionselement „Browsertyp: Google“ hatten, während nur 19,6 % des Segments B dieses Dimensionselement aufwiesen. Ein Differenzwert von 1 bedeutet, dass er statistisch signifikant ist, während ein Differenzwert von 0 bedeutet, dass es keine statistische Bedeutung gibt.

Diese Visualisierung ähnelt den Freiformtabellen in Analysis Workspace. Wenn eine tiefere Analyse eines bestimmten Dimensionselements gewünscht wird, halten Sie den Mauszeiger über ein Zeilenelement und klicken Sie auf „Visualisierung erstellen“. Eine neue Tabelle wird erstellt, um dieses spezifische Dimensionselement zu analysieren. Wenn ein Dimensionselement für Ihre Analyse irrelevant ist, halten Sie den Mauszeiger über den Zeileneintrag und klicken Sie auf das „X“, um es zu entfernen.

>[!NOTE]
>
>Dimensionselemente, die dieser Tabelle nach Abschluss des Segmentvergleichs hinzugefügt werden, erhalten keine Differenzbewertung.

![Top-Dimensionen](assets/top-dimension-item1.png)

### Dimensionselemente nach Segment

Rechts neben der Dimensionstabelle befindet sich eine verknüpfte Balkendiagrammvisualisierung. Es werden alle angezeigten Dimensionselemente in einem Balkendiagramm angezeigt. Durch Klicken auf ein Zeilenelement in der Tabelle links wird die Visualisierung auf der rechten Seite aktualisiert.

![Balkendiagramm für oberste Dimensionen](assets/top-dimension-item.png)

### Top-Segmente

Zeigt, welche anderen Segmente (außer den beiden zum Vergleich ausgewählten Segmenten) statistisch signifikante Überschneidungen aufweisen. Diese Tabelle kann beispielsweise zeigen, dass sich ein drittes Segment, „Wiederholte Besucher“, stark mit „Segment A“ überschneidet, jedoch nicht mit „Segment B“. Ein Differenzwert von 1 bedeutet, dass er statistisch signifikant ist, während ein Differenzwert von 0 bedeutet, dass es keine statistische Bedeutung gibt.

Diese Visualisierung ähnelt den Freiformtabellen in Analysis Workspace. Wenn eine tiefere Analyse eines bestimmten Segments gewünscht wird, halten Sie den Mauszeiger über ein Zeilenelement und klicken Sie auf „Visualisierung erstellen“. Eine neue Tabelle wird erstellt, um dieses spezifische Segment zu analysieren. Wenn ein Segment für Ihre Analyse irrelevant ist, halten Sie den Mauszeiger über das Zeilenelement und klicken Sie auf das X, um es zu entfernen.

>[!NOTE]
>
>Segmente, die dieser Tabelle nach Abschluss des Segmentvergleichs hinzugefügt wurden, erhalten keine Differenzbewertung.

![Top-Segmente](assets/top-segments.png)

### Segmentüberschneidung

Rechts neben der Tabelle der Segmente befindet sich eine verknüpfte Visualisierung. Es zeigt das statistisch bedeutendste Segment, das auf Ihre verglichenen Segmente angewendet wird. Beispiel: „Segment A“ + „Statistisch bedeutendes Segment“ vs. „Segment B“ + „Statistisch bedeutendes Segment“. Wenn Sie auf ein Segmentzeilenelement in der Tabelle links klicken, wird das Venn-Diagramm auf der rechten Seite aktualisiert.

![Venn-Diagramm für Top-Segmente](assets/segment-overlap.png)
