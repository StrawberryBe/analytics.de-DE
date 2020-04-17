---
title: Analyse der von Ereignissen betroffenen Daten
description: Verstehen Sie, wie die von einem Ereignis betroffenen Daten zur Datenqualität insgesamt beitragen.
translation-type: tm+mt
source-git-commit: dfc2e036711ee2229160f52ab16fb4299f7722e5

---


# Analyse der von Ereignissen betroffenen Daten

Manchmal kann ein Ereignis die Datenqualität in Ihrem Unternehmen beeinträchtigen. Zu den Beispielen gehören:

* Ein Bot sendet Auslieferungsdaten, z. B. Millionen Dollar Umsatz
* Ihr Unternehmen hat eine Aktualisierung Ihrer Website veröffentlicht, die negative Auswirkungen auf Ihre Analytics-Implementierung hat
* Andere Aspekte, die sich auf die Datenqualität oder -vollständigkeit auswirken

Wenn auf Ihrer Site Probleme mit der Datenqualität, Implementierungsprobleme oder andere Datenlücken aufgetreten sind, sollten Sie diese möglicherweise vom Berichte ausschließen, um zu verhindern, dass Entscheidungen zu partiellen Daten getroffen werden. Verwenden Sie diese Abschnitte, um die Auswirkungen des Ereignisses auf Ihre Daten zu messen und festzulegen, wie Sie fortfahren möchten.

## Daten mithilfe der Segmentierung analysieren und ausschließen

Adobe Analytics-Angebot bieten eine einfache und stabile Möglichkeit, Daten mithilfe der Segmentierung zu fokussieren oder auszuschließen. Sie können Datumsbereichsdimensionen in Segmenten verwenden, um diese Daten zu filtern oder sich auf diese Daten zu konzentrieren. Siehe [Ausschließen bestimmter Daten in Analyse](/help/components/c-segmentation/use-cases/exclude-date-range.md) im Komponenten-Benutzerhandbuch.

## Vergleichen eines Ereignisses mit vorherigen Datumsbereichen

Wenn Sie mehr über die Auswirkungen eines Ereignisses auf Ihre Daten im Zeitverlauf erfahren möchten, können Sie den Datumsvergleich in Analyse Workspace verwenden. Mit dieser Funktion können Sie Daten von Tag zu Tag, Woche oder Monat miteinander vergleichen, um einen Vergleich mit vorherigen Bereichen anzustellen. Mit diesem Vergleich können Sie dann bestimmen, wie stark ein Ereignis Trends beeinflusst. Siehe [Datumsvergleiche, die von einem Ereignis beeinflusst wurden, mit vorherigen Bereichen](/help/analyze/analysis-workspace/components/calendar-date-ranges/compare-event.md) im Analysieren-Benutzerhandbuch.

## Trenddaten mit berechneten Metriken korrigieren

Nachdem Sie Segmente erstellt und den Datumsvergleich verwendet haben, können Sie beide Konzepte kombinieren, um Trenddaten mithilfe von berechneten Metriken zu korrigieren. Schließen Sie die Segmente in eine berechnete Metrik ein und multiplizieren Sie dann die betroffenen Tage mit dem beim Datumsvergleich gefundenen Offset. Siehe [Ableiten von Daten, die von Ereignissen](/help/components/c-calcmetrics/cm-events.md) betroffen sind, im Komponentenbenutzerhandbuch.

## Kalendereinstellungen in Reports &amp; Analysen verwenden

Wenn Sie Reports &amp; Analysen verwenden, können Sie mithilfe eines [Kalenderberichts](/help/components/t-calendar-event.md) die betroffenen Ereignis in einem beliebigen Trendbericht hervorheben. Diese Methode gilt nicht für Analyse Workspace.

1. Navigieren Sie zu **[!UICONTROL Components]** > **[!UICONTROL Calendar events]**.
2. Geben Sie den gewünschten Titel, den Datumsbereich und den Notiztext ein.
3. Klicken Sie auf **[!UICONTROL Save]**.

![Kalender-Ereignis](assets/exclude_calendar_event.jpg)
