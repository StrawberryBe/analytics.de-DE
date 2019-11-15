---
description: 'null'
title: Bekannte Einschränkungen im Analysis Workspace
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Bekannte Einschränkungen im Analysis Workspace

Im Folgenden finden Sie eine Liste der bekannten Einschränkungen im Analysis Workspace und den zugehörigen Komponenten:

## Tabellen

* Datumsvergleichsspalten können nicht hinzugefügt werden, wenn Datumsbereiche oder Metriken als Tabellenzeilen verwendet werden.
* Metrik aus Auswahl erstellen ist deaktiviert, wenn Segmente als Zeilen einer Tabelle verwendet werden. Darüber hinaus sollte die Option Metrik aus Auswahl erstellen nicht auf datumsorientierte Spalten angewendet werden.
* Bedingte Formatierung für Aufschlüsselungszeilen kann keine benutzerdefinierten Bereiche verwenden.
* Tabellengesamtzeilen können nicht als Trendansicht dargestellt werden, wenn die Einstellung für die Berechnung der Summen durch Addition der Zeilenwerte angewendet wird (üblicherweise bei statischen Zeilenelementen).
* [!UICONTROL Die Beitragsanalyse] kann [!UICONTROL nur mit der Granularität ]pro Tag _ausgeführt werden_. Es kann nicht mit [!UICONTROL stündlichen], [!UICONTROL wöchentlichen]usw. ausgeführt werden.

## Visualisierungen

* Visualisierungen, die die Segmentierung nutzen, wie [!UICONTROL Trichteranalyse], [!UICONTROL Fluss], [!UICONTROL Kohorte]und [!UICONTROL Histogramm], können keine berechneten Metriken als Eingaben akzeptieren.
* [!UICONTROL Fluss]: Einstiegs-/Ausstiegsdimensionen, z. B. [!UICONTROL Einstiegsseite], können nicht in Fluss verwendet werden.
* [!UICONTROL Kohorte]: Nicht-ganze Zahlen können nicht als Kohortenkriterien verwendet werden.

## Bedienfelder

* Segmentvergleich: Das Segment " [!UICONTROL Alle anderen] "wird nicht erstellt, wenn eine Segmentvorlage in der ersten Dropzone verwendet wird.

## Komponenten &gt; Segmente

* Bestimmte Metriken und Dimensionen können nicht segmentiert werden, wie [!UICONTROL Vorfälle], [!UICONTROL Unique Visitors]usw.
* Bestimmte Komponenten und Operatoren sind nicht verfügbar, wenn ein Segment aus Workspace erstellt wird (im Gegensatz zu [!UICONTROL Komponenten &gt; Segmente]). Beispiel: IP-Adresse.

## Komponenten &gt; Berechnete Metriken

* Berechnete Metriken können in bestimmten Visualisierungen nicht verwendet werden. Siehe "Visualisierungen" oben.
* Berechnete Metriken können nicht im Bereich [!UICONTROL Zuordnung] verwendet werden, da berechnete Metriken selbst separate Zuordnungsmodelle enthalten können.
* Bestimmte Komponenten und Operatoren sind nicht verfügbar, wenn eine berechnete Metrik aus Workspace erstellt wird (im Gegensatz zu [!UICONTROL Komponenten &gt; Segmente]). Beispiel: [!UICONTROL IP-Adresse].

## Komponenten &gt; Datumsbereiche

* Benutzerdefinierte Datumsbereiche werden nicht unterstützt [!UICONTROL Dieser Tag im letzten Jahr], [!UICONTROL Dieser Tag im letzten Monat]usw.

## Komponenten &gt; Virtual Report Suites

* Wenn die Berichtszeitverarbeitung aktiviert ist, werden bestimmte Komponenten nicht unterstützt. Eine vollständige Liste finden Sie unter [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md).

## Komponenten &gt; Berichtseinstellungen

* Einige der Einstellungen auf der Seite [!UICONTROL Berichtseinstellungen] gelten nicht. Der Arbeitsbereich für Analysen verwendet am unteren Rand nur die [!UICONTROL Einstellungen für Sprache/Währung/Kodierung] : Trennzeichen[!UICONTROL für ]Tausende, [!UICONTROL terminierte Berichtskodierung]und [!UICONTROL CSV-Trennzeichen].

## Attribution IQ

* Eine Untergruppe von Metriken wird in [!UICONTROL Zuordnung IQ]nicht unterstützt. Eine vollständige Liste finden Sie in den häufig gestellten Fragen zu [Attribution IQ](/help/analyze/analysis-workspace/attribution-iq/attribution-faq.md).
