---
title: Analyse der von Ereignissen betroffenen Daten
description: Verstehen Sie, wie die von einem Ereignis betroffenen Daten zur Datenqualität insgesamt beitragen.
translation-type: tm+mt
source-git-commit: d400bd219cbd8710f2a2fbdaaa9210f3bc70c40b

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

## Daten mithilfe berechneter Metriken ableiten

Nachdem Sie Segmente erstellt und den Datumsvergleich verwendet haben, können Sie beide Konzepte kombinieren, um Trenddaten mithilfe von berechneten Metriken zu korrigieren. Schließen Sie die Segmente in eine berechnete Metrik ein und multiplizieren Sie dann die betroffenen Tage mit dem beim Datumsvergleich gefundenen Offset. Siehe [Ableiten von Daten, die von Ereignissen](/help/components/c-calcmetrics/cm-events.md) betroffen sind, im Komponentenbenutzerhandbuch.

## Auswirkungen auf Benutzer in Ihrer Organisation kommunizieren

Sobald Sie mit der geplanten Handhabung eines Ereignisses vertraut sind, können Sie mit den Benutzern in Ihrem Unternehmen [kommunizieren](event/event-communicate.md). Adobe Angebote bietet verschiedene Orte in Analytics, an denen Sie Text platzieren können, um den Benutzern mitzuteilen, was passiert ist und welche Komponenten sie verwenden können.
