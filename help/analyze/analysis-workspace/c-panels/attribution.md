---
title: Attributionsbedienfeld
description: Verwendung und Interpretation des Zuordnungsbedienfelds in Analysis Workspace.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 13%

---


# Attributionsbedienfeld

Der Attributionsbereich bietet eine einfache Möglichkeit, eine Analyse zu erstellen, mit der verschiedene Attributionsmodelle verglichen werden. Es ist eine Funktion in [Attribution IQ](../attribution/overview.md) , die Ihnen einen eigenen Arbeitsbereich bietet, um Zuordnungsmodelle zu verwenden und zu vergleichen.

## Zuordnungsbedienfeld erstellen

1. Klicken Sie auf das Bedienfeldsymbol auf der linken Seite.
1. Ziehen Sie den Attributionsbereich in Ihr Analysis Workspace-Projekt.

   ![Neues Zuordnungsbedienfeld](assets/Attribution_Panel_1.png)

1. Hinzufügen Sie eine Metrik, die Sie zuordnen möchten, und fügen Sie beliebige Dimensionen hinzu, die Sie zuweisen möchten. Beispiele sind Marketing-Kanal oder benutzerdefinierte Dimensionen wie interne Promotions.

   ![Dimension und Metrik auswählen](assets/attribution_panel2.png)

1. Wählen Sie die [Zuordnungsmodelle und das Lookback-Fenster](../attribution/models.md) aus, die Sie vergleichen möchten.

1. Das Zuordnungsbedienfeld gibt einen umfangreichen Satz an Daten und Visualisierungen zurück, die die Zuordnung für die ausgewählte Dimension und Metrik vergleichen.

   ![Visualisierungen der Zuordnung](assets/attr_panel_vizs.png)

## Visualisierungen der Zuordnung

* **Metrik** insgesamt: Die Gesamtzahl der Konversionen, die im Zeitfenster des Berichte stattgefunden haben. Hierbei handelt es sich um die Konversionen, die über die von Ihnen ausgewählte Dimension hinweg mit Attributen versehen werden.
* **Metrikzuordnungsvergleichsleistendiagramm**: Vergleicht visuell die zugeordneten Konvertierungen über die einzelnen Dimensionselemente Ihrer ausgewählten Dimension hinweg. Jede Balkenfarbe stellt ein eindeutiges Zuordnungsmodell dar.
* **Metrikzuordnung Freeform-Tabelle**: Zeigt dieselben Daten wie das Balkendiagramm an, das als Tabelle dargestellt wird. Durch Auswahl verschiedener Spalten oder Zeilen in dieser Tabelle werden das Balkendiagramm sowie einige andere Visualisierungen im Bedienfeld Filter. Diese Tabelle ähnelt jeder anderen Freiform-Tabelle in Workspace, sodass Sie Komponenten wie Metriken, Segmente oder Aufschlüsselungen hinzufügen können.
* **Dimensionsüberschneidungsdiagramm**: Ein Venn-Diagramm, das die drei wichtigsten Dimensionselemente und deren gemeinsame Teilnahme an einer Konversion anzeigt. Beispielsweise zeigt die Größe der Überschneidung des Punktdiagramms an, wie oft Konversionen stattgefunden haben, wenn ein Besucher beiden Dimensionselementen ausgesetzt war. Durch Auswahl anderer Zeilen in der angrenzenden Freiform-Tabelle wird die Visualisierung entsprechend Ihrer Auswahl aktualisiert.
* **Marketing-Touchpoints pro Fahrt**: Ein Histogramm, das die Anzahl der Touchpoints angibt, die ein Besucher im Lookback-Fenster hatte. Dies ist hilfreich, um nachzuvollziehen, wie wirkungsvoll die Mehrkontaktattribution für Ihren Datensatz ist. Wenn fast alle Besucher nur über einen einzigen Touchpoint verfügen, zeigen unterschiedliche Zuordnungsmodelle wahrscheinlich ähnliche Daten.
* **Leistungsdetails** für Marketing Kanal: Ermöglicht den visuellen Vergleich von bis zu drei Zuordnungsmodellen mithilfe eines Streudiagramms.
* **Marketing-Kanal-Fluss**: Hier können Sie sehen, mit welchen Kanälen am häufigsten und in welcher Reihenfolge während der Reise eines Besuchers interagiert wird.
