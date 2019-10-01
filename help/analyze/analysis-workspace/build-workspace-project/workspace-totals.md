---
description: Berechnung der Gesamtsummen des Arbeitsbereichs.
seo-description: Erfahren Sie, wie die Gesamtsummen des Arbeitsbereichs berechnet werden.
seo-title: Berechnung der Gesamtsummen des Arbeitsbereichs.
title: Arbeitsflächensummen
translation-type: tm+mt
source-git-commit: b2e76715a2bab0931b1ddf8c612c29eea530ce6c

---


# Arbeitsflächensummen

In Freiform-Tabellen wird auf jeder Unterteilungsebene eine Zeile insgesamt angezeigt und kann zwei Summen anzeigen:

* **[!UICONTROL Gesamtsumme]** (graue "Out-of"-Zahl) - dieser Gesamtwert stellt alle erfassten Treffer dar, manchmal auch als "Report Suite-Gesamtsumme"bezeichnet. Wenn ein Segment entweder auf Bereichsebene oder in der Freiformtabelle angewendet wird, passt sich diese Summe an, um alle Treffer wiederzugeben, die den Segmentkriterien entsprechen.
* **[!UICONTROL Tabellensumme]** (schwarze Zahl) - dieser Gesamtwert entspricht in der Regel der [!UICONTROL Gesamtsumme]oder einer Untergruppe davon. Er spiegelt alle Tabellenfilter wider, die innerhalb der Freiform-Tabelle angewendet werden, einschließlich der Option [!UICONTROL Keine] einschließen.

![](assets/total-row.png)

## Gesamteinstellung anzeigen

Unter " **[!UICONTROL Spalteneinstellungen]**"finden Sie Optionen zum **[!UICONTROL Anzeigen der Gesamtanzahl]** und zum **[!UICONTROL Anzeigen der Gesamtsumme]**. Wenn diese Einstellungen deaktiviert sind, werden die Summen aus der Tabelle entfernt. Dies kann in Fällen gewünscht werden, in denen Summen beispielsweise in bestimmten Szenarien mit [berechneten Metriken keinen Sinn ergeben](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetrics-reference/cm-totals.html).

![](assets/column-settings-total.png)

## Gesamteinstellungen für statische Zeile

[Die Gesamtwerte für statische Zeilen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.html) verhalten sich anders und werden unter **[!UICONTROL Zeileneinstellungen]** gesteuert.

* **[!UICONTROL Die Summe der aktuellen Zeilen als Gesamtsumme]** anzeigen - dies zeigt eine clientseitige Summe der Zeilen in der Tabelle, was bedeutet, dass die Gesamtsumme die Metriken wie Besuche oder Besucher **nicht** dedupliziert.
* **[!UICONTROL Gesamte Summe]** anzeigen: Zeigt eine serverseitige Summe an, d. h. die Gesamtsumme dedupliziert Metriken wie Besuche oder Besucher.

![](assets/static-rows.png)

## Häufig gestellte Fragen

| Fragen | Antwort |
|---|---|
| Auf welcher Summe basieren die grauen Spaltenprozentsätze? | Dies hängt von der **[!UICONTROL Einstellung Prozentwerte]** unter **[!UICONTROL Zeileneinstellungen]** ab:<ul><li>Prozentsätze nach Spalte berechnen - Dies ist die Standardeinstellung. Prozentsätze basieren auf der Tabellensumme.</li><li>Prozentsätze nach Zeile berechnen - Prozentsätze werden auf Basis der Gesamtsumme berechnet.</li></ul> |
| Wie wirkt sich die Einstellung "Nicht angegeben **[!UICONTROL einschließen"(Keine)]** auf die Gesamtwerte aus? | Wenn die Einstellung "Nicht **[!UICONTROL angegeben (Keine)]** einschließen"deaktiviert ist, wird die Zeile "Keine/Nicht angegeben"aus der Tabelle, der Tabellensumme entfernt und wird zu allen berechneten Metriken übernommen, die Metriktypen ["Gesamt"verwenden](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetric-workflow/m-metric-type-alloc.html) |
| Wenn benutzerdefinierte Tabellenfilter auf eine Freiform-Tabelle angewendet werden, werden alle berechneten Metriken und die bedingte Formatierung für den Filter berücksichtigt? | Not currently. **[!UICONTROL Include Unspecified (None) will be accounted for, but custom table filters will not impact the following:]**<ul><li>The column max/min range that conditional formatting uses will look across all data.</li><li>Calculated metrics that leverage Grand Total metric types.****</li><li>Calculated metrics with functions that calculate across rows in a freeform table - i.e. Column Sum, Column max, Column min, Count, Mean, Median, Percentile, Quartile, Row Count, Standard Deviation, Variance, Cumulative, Cumulative Average, Regression variants, T-Score, T-Test, Z-Score, Z-Test.</li></ul> |
| In Calculated Metrics, what does the Grand Total metric type reflect?**** | **[!UICONTROL Grand Total]** continues to refer to the **[!UICONTROL Grand Total]**, and does not reflect filters applied to a table or the **[!UICONTROL Table Total]**. |
| What total is shown when data is either copied and pasted from a freeform table or downloaded via CSV? | The total row will reflect the **[!UICONTROL Table Total]** only and respects the column **[!UICONTROL Show Totals]** setting. |

