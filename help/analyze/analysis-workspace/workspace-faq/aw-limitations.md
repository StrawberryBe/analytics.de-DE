---
description: Liste der bekannten Einschränkungen in Adobe Analysis Workspace und der zugehörigen Komponenten
title: Bekannte Einschränkungen in Analysis Workspace
translation-type: tm+mt
source-git-commit: 00f36d8583ec9224337404cfd7fa020502d89c2d
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 100%

---


# Bekannte Einschränkungen in Analysis Workspace

Im Folgenden finden Sie eine Liste der bekannten Einschränkungen in Analysis Workspace und der zugehörigen Komponenten:

## Tabellen

* Datumsvergleichsspalten können nicht hinzugefügt werden, wenn Datumsbereiche oder Metriken als Tabellenzeilen verwendet werden.
* „Metrik aus Auswahl erstellen“ ist deaktiviert, wenn Segmente als Zeilen einer Tabelle verwendet werden. Darüber hinaus sollte die Option „Metrik aus Auswahl erstellen“ nicht auf datumsorientierte Spalten angewendet werden.
* Bedingte Formatierung für Aufschlüsselungszeilen kann keine benutzerdefinierten Bereiche verwenden.
* Tabellengesamtzeilen können nicht als Trend-Ansicht dargestellt werden, wenn die Einstellung für die Berechnung der Summen durch Addition der Zeilenwerte angewendet wird (üblicherweise bei statischen Zeilenelementen).
* Die [!UICONTROL Beitragsanalyse] kann [!UICONTROL nur] mit der Granularität _Täglich_ ausgeführt werden. Sie kann nicht mit Daten des Typs [!UICONTROL Stündlich], [!UICONTROL Wöchentlich] usw. ausgeführt werden.

## Visualisierungen

* Visualisierungen, die die Segmentierung nutzen, wie [!UICONTROL Fallout], [!UICONTROL Fluss], [!UICONTROL Kohorte] und [!UICONTROL Histogramm], können keine berechneten Metriken als Eingaben akzeptieren.
* [!UICONTROL Fluss]: Einstiegs-/Ausstiegsdimensionen, z. B. [!UICONTROL Entrypage], können nicht im Fluss verwendet werden.
* [!UICONTROL Kohorte]: Nur Ganzzahlen können als Kohortenkriterien verwendet werden.

## Bedienfelder

* Segmentvergleich: Das Segment [!UICONTROL Alle anderen] wird nicht erstellt, wenn eine Segmentvorlage in der ersten Dropzone verwendet wird.

## Komponenten > Segmente

* Bestimmte Metriken und Dimensionen können nicht segmentiert werden, wie [!UICONTROL Vorfälle], [!UICONTROL Unique Visitors] usw.
* Ad-hoc-Segmente, die in der [Bedienfeld-Dropzone](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de-DE) erstellt wurden, werden nicht in der linken Leiste von Workspace oder im Segment-Komponenten-Manager angezeigt, es sei denn, sie werden veröffentlicht. Dies erreichen Sie durch das Bearbeiten des Segments und Auswählen von **[!UICONTROL Dieses Segment veröffentlichen]**.

## Komponenten > Berechnete Metriken

* Berechnete Metriken können in bestimmten Visualisierungen nicht verwendet werden. Siehe „Visualisierungen“ oben.
* Berechnete Metriken können nicht im Bereich [!UICONTROL Attribution] verwendet werden, da berechnete Metriken selbst separate Attributionsmodelle enthalten können.
* Bestimmte Komponenten und Operatoren sind nicht verfügbar, wenn eine berechnete Metrik aus Workspace erstellt wird (im Gegensatz zu [!UICONTROL Komponenten > Segmente]). Beispiel: [!UICONTROL IP-Adresse].

## Komponenten > Datumsbereiche

* Benutzerdefinierte Datumsbereiche werden nicht unterstützt [!UICONTROL Dieser Tag im letzten Jahr], [!UICONTROL Dieser Tag im letzten Monat] usw.

## Komponenten > Virtual Report Suites

* Wenn die Berichtszeitverarbeitung aktiviert ist, werden bestimmte Komponenten nicht unterstützt. Eine vollständige Liste finden Sie unter [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md).

## Komponenten > Berichtseinstellungen

* Einige der Einstellungen auf der Seite [!UICONTROL Berichtseinstellungen] gelten nicht. Analysis Workspace verwendet nur die [!UICONTROL Einstellungen für Sprache/Währung/Kodierung] am unteren Rand: [!UICONTROL Tausendertrennzeichen], [!UICONTROL Kodierung des terminierten Berichts] und [!UICONTROL CSV-Trennzeichen].

## Attribution IQ

* Eine Untergruppe von Metriken wird in [!UICONTROL Attribution IQ] nicht unterstützt. Eine vollständige Liste finden Sie in den [häufig gestellten Fragen zu Attribution IQ](../attribution/faq.md).
