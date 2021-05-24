---
title: Attributionsbedienfeld
description: Verwendung und Interpretation des Attributionsbedienfelds in Analysis Workspace.
feature: Attribution
role: Business Practitioner, Administrator
exl-id: 96ce3cb9-7753-4ec0-b551-e70a1508e3b7
source-git-commit: c38e20a7f9a295609181cc9435489ac86cda0852
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 72%

---

# Attributionsbedienfeld

Das [!UICONTROL Attributionsbedienfeld] bietet eine einfache Möglichkeit, eine Analyse zu erstellen, mit der verschiedene Attributionsmodelle verglichen werden. Dabei handelt es sich um eine Funktion in [Attribution IQ](../attribution/overview.md), die Ihnen einen eigenen Arbeitsbereich bietet, um Attributionsmodelle zu verwenden und zu vergleichen.

## Erstellen eines Attributionsbedienfeldes

1. Klicken Sie links auf das Bedienfeldsymbol.
1. Ziehen Sie das [!UICONTROL Attributionsbedienfeld] in Ihr Analysis Workspace-Projekt.

   ![Neues Attributionsbedienfeld](assets/Attribution_Panel_1.png)

1. Fügen Sie eine Metrik hinzu, die Sie zuordnen möchten, und fügen Sie eine beliebige Dimension hinzu, gegen die Sie zuordnen möchten. Beispiele sind Marketing-Kanäle oder benutzerdefinierte Dimensionen wie interne Promotions.

   ![Dimension und Metrik auswählen](assets/attribution_panel2.png)

1. Wählen Sie die [Attributionsmodelle und das Lookback-Fenster](../attribution/models.md) aus, die Sie vergleichen möchten.

1. Das Attributionsbedienfeld gibt einen umfangreichen Satz an Daten und Visualisierungen zurück, die die Attribution für die ausgewählte Dimension und Metrik vergleichen.

   ![Visualisierungen der Attribution](assets/attr_panel_vizs.png)

## Visualisierungen der Attribution

* **Gesamtmetrik**: Die Gesamtanzahl der im Berichtszeitfenster aufgetretenen Konversionen. Hierbei handelt es sich um die Konversionen, die über die von Ihnen ausgewählte Dimension hinweg mit Attributen versehen werden.
* **Balkendiagramm für den Vergleich der Metrik-Attribution**: Vergleicht visuell die zugeordneten Konversionen über die einzelnen Dimensionselemente der von Ihren ausgewählten Dimension hinweg. Jede Balkenfarbe stellt ein bestimmtes Attributionsmodell dar.
* **Attributionsvergleichstabelle**: Zeigt dieselben Daten wie das Balkendiagramm in Tabellenform an. Durch die Auswahl verschiedener Spalten oder Zeilen in dieser Tabelle werden das Balkendiagramm sowie mehrere andere Visualisierungen im Bedienfeld gefiltert. Diese Tabelle ähnelt anderen Freiformtabellen in Workspace. Sie können damit Komponenten wie Metriken, Segmente oder Aufschlüsselungen hinzufügen.
* **Überlagerungsdiagramm**: Ein Venn-Diagramm, das die drei wichtigsten Dimensionselemente zeigt und wie oft sie gemeinsam an einer Konversion beteiligt sind. Beispielsweise gibt die Größe der Blasenüberlagerung an, wie oft Konversionen auftraten, wenn ein Besucher beiden Dimensionselementen ausgesetzt war. Durch die Auswahl anderer Zeilen in der angrenzenden Freiformtabelle wird die Visualisierung entsprechend Ihrer Auswahl aktualisiert.
* **Leistungsdetails**: Hiermit können Sie bis zu drei Attributionsmodelle visuell mit einem Streudiagramm vergleichen.
* **Trendleistung**: Standardmäßig zeigt den Konversionsleistungstrend nach Attributionsmodell für die erste Dimension an, die in der angrenzenden Freiformtabelle aufgeführt ist. Sie können verschiedene Dimensionszeilen in der Freiformtabelle auswählen, um den Trend für die ausgewählten Dimensionen anzuzeigen (z. B. Gesamtumsatz für jedes Attributionsmodell für Social-Media-Kampagnen und gebührenpflichtige Suche). Alternativ können Sie Zellen in den Spalten für beliebige Metrik- und Attributionstypkombinationen in der Freiformtabelle auswählen, um die Trendleistung nach Dimensionswert für die angegebenen Attributionsmodelle anzuzeigen (z. B. Gesamtumsatz nach Marketing-Kanal mit Letztkontakt- und Erstkontakt-Attribution).
* **Fluss**: Hiermit können Sie anzeigen, mit welchen Kanälen am häufigsten interagiert wird und wie sich die Reihenfolge in der Journey eines Besuchers darstellt.
