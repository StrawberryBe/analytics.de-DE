---
description: 'null '
seo-description: 'null '
seo-title: Einschränkungen des Arbeitsbereichs, bekannte Einschränkungen im Analysis Workspace
title: Bekannte Einschränkungen im Analysis Workspace
translation-type: tm+mt
source-git-commit: 9d6b35c7c6de6fcb49fea3b662ff8bc9044b5e29

---


# Bekannte Einschränkungen im Analysis Workspace

Im Folgenden finden Sie eine Liste bekannter Einschränkungen im Analysis Workspace und den zugehörigen Komponenten:

## Tabellen

* Datumsvergleichsspalten können nicht hinzugefügt werden, wenn Datumsbereiche oder Metriken als Zeilen einer Tabelle verwendet werden.
* Die Metrik aus der Auswahl wird deaktiviert, wenn Segmente als Zeilen einer Tabelle verwendet werden. Außerdem sollte die Metrik erstellen aus Auswahl nicht auf datumsbasierte Spalten angewendet werden.
* Bedingte Formatierungen für Unterteilungszeilen können keine benutzerdefinierten Bereiche verwenden.
* Die Tabellengesamtzeilen können bei der Berechnung der Gesamtzahlen durch Addieren der Zeilenwerte (gewöhnlich mit statischen Zeilenelementen) nicht trendansicht durchlaufen werden.
* [!UICONTROL Die Beitragsanalyse] kann nur mit der [!UICONTROL Granularität "Täglich] _«ausgeführt_ werden. It cannot be run against [!UICONTROL hourly], [!UICONTROL weekly], etc., data.

## Visualisierungen

* Visualizations that leverage segmentation, such as [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort], and [!UICONTROL Histogram], cannot accept calculated metrics as inputs.
* [!UICONTROL Fluss]: Einstiegs-/Ausstiegsdimensionen, z. [!UICONTROL B. Entrypage], können nicht im Fluss verwendet werden.
* [!UICONTROL Kohorte: Nicht ganzzahlen können nicht als Kohortenkriterien verwendet werden.]

## Bedienfelder

* Segment Comparison: The [!UICONTROL Everyone Else] segment does not get created if a segment template is used in the initial drop zone.

## Komponenten &gt; Segmente

* Certain metrics and dimensions are not segmentable, such as [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], etc.
* Certain components and operators are unavailable if a segment is created from Workspace (as opposed to being created from [!UICONTROL Components &gt; Segments]). Zum Beispiel IP-Adresse.

## Komponenten &gt; Berechnete Metriken

* Berechnete Metriken können in bestimmten Visualisierungen nicht verwendet werden. Siehe weiter oben.
* Calculated metrics cannot be used in the [!UICONTROL Attribution] panel, since calculated metrics themselves can include separate attribution models.
* Certain components and operators are unavailable if a calculated metric is created from Workspace (as opposed to being created from [!UICONTROL Components &gt; Segments]). For example, [!UICONTROL IP Address].

## Komponenten &gt; Datumsbereiche

* Custom date ranges do not support [!UICONTROL This day last year], [!UICONTROL This day last month], etc.

## Komponenten &gt; Virtual Report Suites

* Wenn die Zeitverarbeitung für Berichte aktiviert ist, werden bestimmte Komponenten nicht unterstützt. For a full list, see [Report Time Processing](/help/components/vrs/vrs-report-time-processing.md).

## Komponenten &gt; Berichtseinstellungen

* Some of the settings on the [!UICONTROL Report Settings] page do not apply. Analysis Workspace uses only the [!UICONTROL Language/Currency/Encoding] settings at the bottom: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding], and [!UICONTROL CSV Separator Character].

## Attribution IQ

* A subset of metrics is not supported in [!UICONTROL Attribution IQ]. For a full list, see the [Attribution IQ FAQ](/help/analyze/analysis-workspace/attribution-iq/attribution-faq.md).