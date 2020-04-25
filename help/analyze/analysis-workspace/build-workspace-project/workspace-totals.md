---
description: Berechnung der Gesamtsummen in Workspace.
title: Workspace-Summen
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Workspace-Summen

In Freiformtabellen wird auf jeder Unterteilungsebene eine Zeile insgesamt angezeigt, die zwei Summen enthalten kann:

* **[!UICONTROL Grand Total]** (graue &quot;Out-of&quot;-Zahl) - dieser Gesamtwert stellt alle erfassten Treffer dar, manchmal auch als &quot;Report Suite-Gesamtsumme&quot;bezeichnet. Wenn ein Segment entweder auf Bedienfeldebene oder in der Freiformtabelle angewendet wird, passt sich diese Summe an, um alle Treffer wiederzugeben, die den Segmentkriterien entsprechen.
* **[!UICONTROL Table Total]** (schwarze Zahl) - dieser Gesamtwert entspricht in der Regel dem Wert oder einer Untergruppe des Werts [!UICONTROL Grand Total]. It reflects any table filters applied within the freeform table, including the [!UICONTROL Include None] option.

![](assets/total-row.png)

## Gesamteinstellung anzeigen

Unter **[!UICONTROL Column Settings]** finden Sie Optionen zu **[!UICONTROL Show Totals]** und **[!UICONTROL Show Grand Total]**. Wenn diese Einstellungen deaktiviert sind, werden die Summen aus der Tabelle entfernt. Dies kann in Fällen gewünscht werden, in denen Summen beispielsweise in bestimmten [Szenarien mit berechneten Metriken](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/calcmetrics-reference/cm-totals.html) keinen Sinn ergeben.

![](assets/column-settings-total.png)

## Gesamteinstellungen für statische Zeile

[Die Gesamtwerte für statische Zeilen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.html) verhalten sich unterschiedlich und werden unter **[!UICONTROL Row Settings]**.

* **[!UICONTROL Show sum of current rows as the total]** - Zeigt eine clientseitige Summe der Tabellenzeilen an. Das bedeutet, dass die Gesamtsumme die Duplikat-Metriken wie Besuche oder Besucher **nicht** löscht.
* **[!UICONTROL Show Grand Total]** - dies zeigt eine serverseitige Summe an, d. h. die Gesamtsumme löscht Duplikat-Metriken wie Besuche oder Besucher.

![](assets/static-rows.png)

## Häufig gestellte Fragen

| Fragen | Antwort |
|---|---|
| Auf welcher Summe basieren die grauen Spaltenprozentsätze? | Dies hängt von der **[!UICONTROL Percentages]** Auswahl unter **[!UICONTROL Row Settings]**:<ul><li>Prozentsatz nach Spalte berechnen - Dies ist die Standardeinstellung. Prozentsätze basieren auf der Tabellensumme.</li><li>Prozentsatz nach Zeile berechnen - Prozentsätze werden auf Basis der Gesamtsumme berechnet.</li></ul> |
| Wie wirkt sich die **[!UICONTROL Include Unspecified (None)]** Einstellung auf die Gesamtsumme aus? | If the **[!UICONTROL Include Unspecified (None)]** setting is unchecked, the None/Unspecified row will be removed from the table, the Table Total, and will carry through to any calculated metrics that use [&#39;Total&#39; metric types](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/calcmetric-workflow/m-metric-type-alloc.html) |
| Wenn benutzerdefinierte Tabellenfilter auf eine Freiformtabelle angewendet werden, werden alle berechneten Metriken und die bedingte Formatierung für den Filter berücksichtigt? | Derzeit nicht. **[!UICONTROL Include Unspecified (None)]** berücksichtigt werden, aber benutzerdefinierte Filter für Tabellen haben keine Auswirkungen auf Folgendes:<ul><li>Maximaler/minimaler Spaltenbereich, der bei der bedingten Formatierung verwendet wird, wird über alle Daten hinweg angezeigt.</li><li>Berechnete Metriken, die **[!UICONTROL Grand Total]** Metriktypen nutzen.</li><li>Berechnete Metriken mit Funktionen, die über Zeilen in einer Freiformtabelle berechnen - d. h. Spaltensumme, Spaltenmax., Spaltenanzahl, Anzahl, Mittelwert, Median, Perzentil, Quartil, Zeilenzahl, Standardabweichung, Varianz, Kumulativer Wert, Kumulativer Durchschnitt, Regressionsvarianten, T-Score, T-Test, Z-Score, Z-Test.</li></ul> |
| In Calculated Metrics, what does the **[!UICONTROL Grand Total]** metric type reflect? | **[!UICONTROL Grand Total]** verweist weiterhin auf die Tabelle **[!UICONTROL Grand Total]** und spiegelt keine Filter wider, die auf eine Tabelle oder die Tabelle angewendet wurden **[!UICONTROL Table Total]**. |
| Welcher Gesamtwert wird angezeigt, wenn Daten entweder kopiert und aus einer Freiformtabelle eingefügt oder über CSV heruntergeladen werden? | Die gesamte Zeile spiegelt die **[!UICONTROL Table Total]** einzige wider und berücksichtigt die Spalteneinstellung **[!UICONTROL Show Totals]** . |

