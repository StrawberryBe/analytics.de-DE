---
description: Berechnung der Gesamtsummen des Arbeitsbereichs.
title: Arbeitsflächensummen
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

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
| Wenn benutzerdefinierte Tabellenfilter auf eine Freiform-Tabelle angewendet werden, werden alle berechneten Metriken und die bedingte Formatierung für den Filter berücksichtigt? | Nicht aktuell. **[!UICONTROL "Nicht angegeben einschließen"(Keine)]** wird berücksichtigt, benutzerdefinierte Tabellenfilter haben jedoch keine Auswirkungen auf Folgendes:<ul><li>Der maximale/minimale Spaltenbereich, der bei der bedingten Formatierung verwendet wird, wird über alle Daten hinweg angezeigt.</li><li>Berechnete Metriken, die Metriktypen **[!UICONTROL insgesamt]** nutzen.</li><li>Berechnete Metriken mit Funktionen, die über Zeilen in einer Freiformtabelle berechnen - d.h. Spaltensumme, Spaltenmax, Spaltenanzahl, Anzahl, Mittelwert, Median, Perzentil, Quartil, Zeilenzahl, Standardabweichung, Varianz, Kumulativer, Kumulativer Durchschnitt, Regressionsvarianten, T-Score, T-Test, Z-Score, Z-Test.</li></ul> |
| Was spiegelt der Metriktyp **[!UICONTROL Gesamtsumme]** in berechneten Metriken wider? | **[!UICONTROL Die Gesamtsumme]** bezieht sich weiterhin auf die **[!UICONTROL Gesamtsumme]** und spiegelt keine Filter wider, die auf eine Tabelle oder die **[!UICONTROL Tabellensumme]** angewendet wurden. |
| Welcher Gesamtwert wird angezeigt, wenn Daten entweder kopiert und aus einer Freiform-Tabelle eingefügt oder über CSV heruntergeladen werden? | Die Zeile insgesamt spiegelt nur die **[!UICONTROL Tabellensumme]** wider und berücksichtigt die Einstellung " **[!UICONTROL Gesamt]** anzeigen". |

