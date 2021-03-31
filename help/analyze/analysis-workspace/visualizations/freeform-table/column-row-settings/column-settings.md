---
description: Mithilfe der Spalteneinstellungen können Sie die Spaltenformatierung konfigurieren. Einige davon sind bedingt.
title: Spalteneinstellungen
uuid: 151d66da-04f7-4d0f-985c-4fdd92bc1308
feature: Freiformtabellen
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 99%

---


# [!UICONTROL Spalteneinstellungen]

Mithilfe der [!UICONTROL Spalteneinstellungen] können Sie die Spaltenformatierung konfigurieren. Einige davon sind bedingt.

## [!UICONTROL Spalteneinstellungen] bearbeiten {#edit-column-settings}

Um die [!UICONTROL Spalteneinstellungen] aufzurufen, ziehen Sie eine Freiformtabelle in das Projekt und klicken Sie dann auf das Zahnrad-Symbol in der Spaltenüberschrift.

![](assets/column_settings.png)

Sie können Einstellungen **für mehrere Spalten gleichzeitig** bearbeiten. Wählen Sie hierzu einfach mehrere Spalten aus und klicken Sie in einer der Spalten auf das Einstellungs-Symbol. Sämtliche Änderungen, die Sie hier vornehmen, werden auf die markierten Zellen aller Spalten angewendet.

| Element | Beschreibung |
| --- | --- |
| **Summenzellen** |  |
| Summen anzeigen | Dieser Gesamtwert entspricht in der Regel der [!UICONTROL Gesamtsumme] oder einer Untergruppe davon. Er spiegelt alle Tabellenfilter wider, die innerhalb der Freiformtabelle angewendet werden, einschließlich der Option [!UICONTROL Keine einschließen]. |
| Gesamtsumme anzeigen | Dieser Gesamtwert stellt alle erfassten Hits dar, die manchmal als „Report Suite-Gesamtsumme“ bezeichnet werden. Wenn ein Segment entweder auf Bedienfeldebene oder in der Freiformtabelle angewendet wird, passt sich diese Summe an, um alle Hits wiederzugeben, die den Segmentkriterien entsprechen. Gesamtsumme wird für Tabellen oder Aufschlüsselungen mit [statischen Zeilen](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md) nicht unterstützt. |
| **Zellen der Tabelle** |  |
| Nummer | Definition, ob in einer Zelle der numerische Wert der Metrik angezeigt wird oder nicht. Ist die Metrik beispielsweise „Seitenansichten“, ist der numerische Wert die Anzahl an Seitenansichten für dieses Zeilenelement. |
| Prozent | Definition, ob in einer Zelle der Prozentwert der Metrik angezeigt wird oder nicht. Ist die Metrik beispielsweise „Seitenansichten“, ist der Prozentwert die Anzahl an Seitenansichten für dieses Zeilenelement geteilt durch die Gesamtanzahl der Seitenansichten für diese Spalte.  Hinweis: Für eine höhere Genauigkeit können Prozentsätze über 100 % angezeigt werden. Außerdem wird die obere Grenze auf 1.000 % verschoben, damit Spalten auch verbreitert werden können. |
| Anomalien | Definition, ob die Anomalieerkennung für die Werte dieser Spalte ausgeführt wird |
| Kopfzeilentext umbrechen | Hiermit können Sie den Kopfzeilentext in Freiformtabellen umbrechen, damit Kopfzeilen besser lesbar und Tabellen einfacher freizugeben sind. Diese Funktion ist beim .pdf-Rendering und für Metriken mit langen Namen nützlich. Standardmäßig aktiviert. |
| Null nicht als Wert interpretieren | Definition, ob in Zellen mit 0-Wert eine 0 oder nichts angezeigt wird. Diese Option ist praktisch, wenn Sie die Daten für einzelne Tage eines Monats anzeigen und einige Tage noch in der Zukunft liegen.  Statt für in der Zukunft liegende Daten eine 0 anzuzeigen, kann die entsprechende Zelle auch leer angezeigt werden. In Diagrammen wird diese Einstellung ebenfalls berücksichtigt (ist diese Einstellung aktiviert, wird in Diagrammen also keine Linie bzw. kein Balken mit 0-Werten angezeigt). |
| Hintergrund | Definition, ob in einer Zelle alle Zellformatierungen ein-/ausgeblendet werden, einschließlich Balkendiagramm und bedingter Formatierung |
| Balkendiagramm | Zeigt ein horizontales Balkendiagramm mit dem Zellenwert in Relation zum Gesamtwert der Spalte an. |
| Bedingte Formatierung | Weitere Informationen dazu finden Sie im unten stehenden Abschnitt. |
| Vorschau der Tabellenzelle | Vorschau der jeweiligen Zelle mit allen ausgewählten Formatierungsoptionen |

## Bedingte Formatierung {#conditional-formatting}

Die bedingte Formatierung gilt für Obergrenzen, Mittelwerte und Untergrenzen, die Sie definieren. Das Anwenden bedingter Formatierung (Farben etc.) in Freiformtabellen ist bei Aufschlüsselungen auch automatisch aktiviert, wenn keine benutzerdefinierten Beschränkungen ausgewählt sind.

![](assets/conditional-formatting.png)

| Element | Beschreibung |
| --- | --- |
| Bedingte Formatierung | Färbt Zellen je nach Datenwerten wie folgt ein: <ul><li>Grün: hohe Werte</li><li>Gelb: Mittelpunktwerte</li><li>Rot: niedrige Werte</li></ul> <br> Wenn Sie eine Dimension in der Tabelle ersetzen, werden die Grenzwerte für die bedingte Formatierung zurückgesetzt. Wenn Sie eine Metrik ersetzen, werden die Grenzwerte für diese Spalte zurückgesetzt (dabei wird eine Metrik auf der X-Achse und eine Dimension auf der Y-Achse dargestellt). |
| Prozentbegrenzungen verwenden | Ändern Sie das Limit, das auf Prozentsätzen basieren soll anstatt auf absoluten Werten. Diese Einstellung funktioniert mit Metriken, die rein prozentbasiert sind (beispielweise Absprungrate) oder eine Anzahl und einen Prozentsatz aufweisen (beispielsweise Seitenansichten). |
| Automatisch generiert | Obere/mittlere/untere Limits automatisch auf Basis der Daten berechnen. Die Obergrenze entspricht dem höchsten Wert in dieser Spalte. Die Untergrenze entspricht dem niedrigsten Wert und der Mittelpunkt ist der Durchschnittswert der Ober- und der Untergrenze. |
| Anpassen | Obere/mittlere/untere Limits manuell zuweisen. So können Sie flexibel bestimmen, ob der Wert einer Spalte gut, durchschnittlich oder schlecht ist. |

## Nicht standardmäßiges Attributionsmodell verwenden {#attribution}

Analysis Workspace unterstützt die [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) für nahezu jede Metrik.

1. Klicken Sie auf das Zahnradsymbol „Einstellungen“ in einer Freiformtabellenspalte.

   ![Kontrollkästchen „Attribution“](assets/attribution-checkbox.png)

1. Aktivieren Sie unter **[!UICONTROL Dateneinstellungen]** die Option **[!UICONTROL Nicht standardmäßiges Attributionsmodell verwenden]**. Weitere Informationen zu den unterschiedlichen Attributionsmodellen finden Sie unter [Attributionsmodelle](/help/analyze/analysis-workspace/attribution/models.md).

   ![Attributionsmodell auswählen](assets/attribution-select.png)

>[!MORELIKETHIS]
>
>* [Data Sources verwalten](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md)

