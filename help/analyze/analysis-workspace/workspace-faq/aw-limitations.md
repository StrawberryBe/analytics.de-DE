---
description: Liste der bekannten Einschränkungen in Adobe Analysis Workspace und der zugehörigen Komponenten
title: Bekannte Einschränkungen in Analysis Workspace
translation-type: tm+mt
source-git-commit: 025ac334f9191b6455eea0530a2a21c01199000a

---


# Bekannte Einschränkungen in Analysis Workspace

Im Folgenden finden Sie eine Liste der bekannten Einschränkungen in Analysis Workspace und der zugehörigen Komponenten:

## Tabellen

* Datumsvergleichsspalten können nicht hinzugefügt werden, wenn Datumsbereiche oder Metriken als Tabellenzeilen verwendet werden.
* „Metrik aus Auswahl erstellen“ ist deaktiviert, wenn Segmente als Zeilen einer Tabelle verwendet werden. Darüber hinaus sollte die Option „Metrik aus Auswahl erstellen“ nicht auf datumsorientierte Spalten angewendet werden.
* Bedingte Formatierung für Aufschlüsselungszeilen kann keine benutzerdefinierten Bereiche verwenden.
* Tabellengesamtzeilen können nicht als Trend-Ansicht dargestellt werden, wenn die Einstellung für die Berechnung der Summen durch Addition der Zeilenwerte angewendet wird (üblicherweise bei statischen Zeilenelementen).
* [!UICONTROL Contribution Analysis] kann [!UICONTROL daily] nur mit der _Granularität ausgeführt werden_. It cannot be run against [!UICONTROL hourly], [!UICONTROL weekly], etc., data.

## Visualisierungen

* Visualizations that leverage segmentation, such as [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort], and [!UICONTROL Histogram], cannot accept calculated metrics as inputs.
* [!UICONTROL Flow]: Einstiegs-/Ausstiegsdimensionen, z. B. kann [!UICONTROL Entry page]nicht in Fluss verwendet werden.
* [!UICONTROL Cohort]: Nicht-ganze Zahlen können nicht als Kohortenkriterien verwendet werden.

## Bedienfelder

* Segment Comparison: The [!UICONTROL Everyone Else] segment does not get created if a segment template is used in the initial drop zone.

## Komponenten > Segmente

* Certain metrics and dimensions are not segmentable, such as [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], etc.
* Certain components and operators are unavailable if a segment is created from Workspace (as opposed to being created from [!UICONTROL Components > Segments]). Beispiel: IP-Adresse.

## Komponenten > Berechnete Metriken

* Berechnete Metriken können in bestimmten Visualisierungen nicht verwendet werden. Siehe „Visualisierungen“ oben.
* Berechnete Metriken können nicht im Bereich [!UICONTROL Attribution] verwendet werden, da berechnete Metriken selbst separate Attributionsmodelle enthalten können.
* Certain components and operators are unavailable if a calculated metric is created from Workspace (as opposed to being created from [!UICONTROL Components > Segments]). Beispiel: [!UICONTROL IP Address].

## Komponenten > Datumsbereiche

* Benutzerdefinierte Datumsbereiche werden nicht unterstützt [!UICONTROL This day last year], [!UICONTROL This day last month]usw.

## Komponenten > Virtual Report Suites

* Wenn die Berichtszeitverarbeitung aktiviert ist, werden bestimmte Komponenten nicht unterstützt. Eine vollständige Liste finden Sie unter [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md).

## Komponenten > Berichtseinstellungen

* Some of the settings on the [!UICONTROL Report Settings] page do not apply. Analyse Workspace verwendet nur die [!UICONTROL Language/Currency/Encoding] unten stehenden Einstellungen: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding]und [!UICONTROL CSV Separator Character].

## Attribution IQ

* A subset of metrics is not supported in [!UICONTROL Attribution IQ]. Eine vollständige Liste finden Sie in den [häufig gestellten Fragen zu Attribution IQ](/help/analyze/analysis-workspace/c-panels/attribution/attribution-faq.md).
