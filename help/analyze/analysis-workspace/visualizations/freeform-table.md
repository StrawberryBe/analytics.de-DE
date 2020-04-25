---
title: Freiformtabelle
description: Weitere Information zu Freiformtabellen und zum Freiformtabellen-Builder
translation-type: tm+mt
source-git-commit: ce06a5ca2caeb266c729947c76e93c611502e6d9

---


# Freiformtabelle

In Analysis Workspace ist eine Freiformtabelle nicht nur eine Datentabelle, sondern auch eine interaktive Visualisierung. Sie können eine Kombination von [Komponenten](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html) per Drag &amp; Drop in die Zeilen und Spalten ziehen, um eine benutzerdefinierte Tabelle für Ihre Analyse zu erstellen. Da jede Komponente abgelegt wird, wird die Tabelle sofort aktualisiert, damit Sie eine schnelle Analyse durchführen können.

Sie können die Tabelle auf verschiedene Arten anpassen:

* **Zeilen**
   * Jede Dimensionsreihe kann bis zu 400 Zeilen anzeigen, bevor die Paginierung erfolgt. Sie können mehr Zeilen in einen einzigen Bildschirm einpassen, indem Sie die [Anzeigedichte](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html) des Projekts anpassen.
   * Zeilen können nach zusätzlichen Komponenten aufgeschlüsselt werden. Um mehrere Zeilen gleichzeitig zu aufzuschlüsseln, wählen Sie einfach mehrere Zeilen aus und ziehen dann die nächste Komponente auf die ausgewählten Zeilen. Weitere Informationen zu [Aufschlüsselungen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.html).
   * Zeilen können [gefiltert](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/pagination-filtering-sorting.html) werden, um einen reduzierte Anzahl von Elementen anzuzeigen. Weitere Einstellungen finden Sie unter [Zeileneinstellungen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/table-settings.html).

* **Spalten**
   * Komponenten können innerhalb von Spalten gestapelt werden, um segmentierte Metriken, tabellenübergreifende Analysen und mehr zu erstellen.
   * Die Ansicht jeder Spalte kann unter den [Spalteneinstellungen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html) angepasst werden.
   * Über das [Kontextmenü](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/using-the-right-click-menu.html) sind verschiedene Aktionen verfügbar. Das Menü enthält verschiedene Aktionen, je nachdem, ob Sie auf die Tabellenüberschrift, die Zeilen oder die Spalten klicken.

## Freiformtabellen-Builder

Wenn Sie Ihrer Tabelle lieber zuerst mehrere Komponenten hinzufügen und dann die Daten rendern möchten, können Sie Freiformtabellen-Builder aktivieren. Wenn der Tabellen-Builder aktiviert ist, können Sie für komplexe Fragen Tabellen mit vielen Dimensionen, Unterteilungen, Metriken und Segmenten per Drag &amp; Drop erstellen. Data will not update on-the-fly, it will update once you click **[!UICONTROL Build]**.

Der Tabellen-Builder ist eine zeitsparende Option, wenn Sie eine komplexe Frage zu den Daten stellen müssen und eine Vorstellung von der Tabelle haben, die Sie zur Beantwortung Ihrer Frage erstellen möchten. Weitere Vorteile des Tabellen-Builder sind:

* Anordnen der Tabelle im gewünschten Format, ohne auf das Rendern jeder Aktion warten zu müssen.
* Schnelle Ausführung von bis zu vier Stufen von Aufschlüsselungen.
* Definieren der Einstellungen für Zeile und Aufschlüsselung für jede Tabellenzeile und Dimensionsspalte.
* **[!UICONTROL Breakdown by Position]** für jede Tabellenebene (in den herkömmlichen Freiform-Tabellen ist der Standardwert **[!UICONTROL Breakdown by Item]**)
* Manuelles Anordnen statischer Zeilen in der Tabelle manuell. Zum Beispiel, wenn Metrikzeilen in einer bestimmten Reihenfolge angezeigt werden sollen.
* Anzeigen einer Vorschau des Tabellenformats, bevor Sie echte Daten rendern.

Sehen Sie sich [hier](https://youtu.be/GUMWiJAmMGI) den Freiformtabellen-Builder in Aktion an.

## Exportieren von Freiformtabellendaten

Die Daten in einer Freiform-Tabelle können auf verschiedene Weise aus Analysis Workspace kopiert werden:

* Klicken Sie mit der rechten Maustaste auf die Tabellenüberschrift und wählen Sie **[!UICONTROL Copy to Clipboard]**. Dadurch wird die gesamte (sichtbare) Tabelle exportiert.
* Highlight specific cells in the table, right-click and select **[!UICONTROL Copy to Clipboard]**, or use the Ctrl + C hotkey.
* **[!UICONTROL Project > Download CSV]**. Dadurch werden alle sichtbaren Tabellen im Projekt als CSV exportiert.
