---
title: Anzeigen von Anmerkungen
description: Anzeigen von Anmerkungen in Workspace.
role: User, Admin
feature: Annotations
exl-id: 52b179fd-d9a4-4119-a3c6-f6a36f24f8ea
source-git-commit: 285bb11eb34ad02bf57227341f9a0931860c5c88
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 40%

---

# Anzeigen von Anmerkungen

>[!NOTE]
>
>Die schrittweise Einführung dieser Funktion beginnt am 23. März 2022. Allgemeine Verfügbarkeit: 11. April 2022.

Anmerkungen werden je nachdem, ob sie sich über einen einzelnen Tag oder einen Datumsbereich erstrecken, etwas unterschiedlich angezeigt.

## Anzeigen von Anmerkungen in Liniendiagrammen oder Tabellen

| Datum | Erscheinungsbild |
| --- | --- |
| **Einzeltag** | ![](assets/single-day.png)<p>When you hover over the annotation, you can see its details, you can edit it by selecting the pen icon, or you can delete it:<p> ![](assets/hover.png) |
| **Datumsbereich** | Das Symbol ändert sich, und wenn Sie den Mauszeiger darüber bewegen, wird der Datumsbereich angezeigt.<p>![](assets/multi-day.png)<p>When you select it in the line chart, the annotation metadata appear, and you can edit or delete it:![](assets/multi-hover.png)<p>In einer Tabelle wird an jedem Datum im Datumsbereich ein Symbol angezeigt.<p>![](assets/multi-day-table.png) |
| **Überlappende Anmerkungen** | On days that have more than one annotation tied to them, the icon appears in a grey color.<p>![](assets/grey.png)<p>Wenn Sie den Mauszeiger über das graue Symbol bewegen, werden alle überlappenden Anmerkungen angezeigt:<p>![](assets/overlap.png) |

## Anzeigen von Anmerkungen in einer PDF-Datei

Da Symbole in einer PDF-Datei nicht auf den Mauszeiger reagieren können, enthält diese Datei (nach dem Export) am unteren Rand eines Bedienfelds Anmerkungen zu Erklärungen. Siehe folgendes Beispiel:

![](assets/ann-pdf.png)

## Anzeigen von Anmerkungen mit Daten ohne Trendansicht

Sometimes annotation are shown with non-trended data, but tied to a specific dimension. In diesem Fall werden sie nur in einer Zusammenfassungsanmerkung in der rechten unteren Ecke angezeigt. Siehe folgendes Beispiel:

![](assets/non-date.png)

Das Zusammenfassungsdiagramm wird in allen Visualisierungstypen in der Ecke angezeigt, nicht nur in nicht Trend-Freiformtabellen und Zusammenfassungsnummern. Es wird auch in Visualisierungen wie [!UICONTROL Ringdiagramm], [!UICONTROL Fluss],[!UICONTROL Fallout],[!UICONTROL Kohorte]usw.

![](assets/ann-summary.png)
