---
description: Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.
seo-description: Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.
seo-title: Übersicht über intelligente Warnhinweise
title: Übersicht über intelligente Warnhinweise
uuid: b9bf75ad-bb6f-49fe-8c55-355ea3c50a71
translation-type: tm+mt
source-git-commit: ca9f1ed00295b556250894ae4e7fa377ef8a593d

---


# Übersicht über intelligente Warnhinweise

Intelligente Warnhinweise ermöglichen eine genauere Steuerung der Warnhinweise und integrieren die Anomalieerkennung in das Warnhinweissystem.

[Intelligente Warnhinweise auf YouTube](https://www.youtube.com/watch?v=UVH9xr_2REA) (5:34)

## Überblick

Die neuen Funktionen „Warnhinweiserstellung“ und „Warnhinweis-Manager“ in Analysis Workspace ersetzen die bisherigen Funktionen in Reports &amp; Analytics. Mithilfe intelligenter Warnhinweise können Sie:

* Warnhinweise erstellen, die auf Anomalien basieren (90-%-, 95-%-, 99-%-, 99,75-%- und 99,9-%-Schwellen, Änderungen in %, darüber/darunter)
* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken
* Erstellen von "gestapelten"Warnhinweisen, die mehrere Metriken in einem einzigen Warnhinweis erfassen

Es gibt vier Möglichkeiten, in die Warnhinweiserstellung zu gelangen:

* Direkt zum Warnhinweiserstellung wechseln:  **[!UICONTROL Komponenten]** &gt; **[!UICONTROL Warnungen]**
* Verwenden des Tastaturbefehls in Workspace: `Ctrl + Shift + A` (Windows) oder `Cmd + Shift + A` (Mac)
* Selecting one or more freeform table line item/s, right-clicking and selecting **[!UICONTROL Create Alert from Selection]**. Dadurch wird der Warnhinweiserstellung geöffnet und die entsprechenden Metriken und angewendeten Filter werden vorab ausgefüllt. Sie können die Warnung bei Bedarf bearbeiten.

   ![Warnhinweis aus Auswahl erstellen](assets/create-alert-from-selection.png)

* From within a Reports &amp; Analytics report, by going to  **[!UICONTROL More]** &gt; **[!UICONTROL Add Alert]** . Dadurch wird die Warnhinweiserstellung geöffnet und die entsprechenden Metriken und angewendeten Filter aus dem Bericht werden vorausgefüllt. Sie können die Warnung bei Bedarf bearbeiten.

   ![Warnung hinzufügen](assets/add-alert.png)

Die Prozentwerte sind Standardabweichungen. Beispiel: 95 % = 2 Standardabweichungen und 99 % = 3 Standardabweichungen. Je nach der von Ihnen ausgewählten Zeitgranularität [werden verschiedene Modelle](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) verwendet, um zu berechnen, wie weit jeder Punkt von der Norm entfernt ist (Anzahl der Standardabweichungen). Wenn Sie einen niedrigeren Schwellenwert festlegen (z. B. 90 %), erhalten Sie mehr Anomalien als bei einem höheren Schwellenwert (99,75 %).

> [!IMPORTANT] Die Verwendung von Daten mit Zeitstempel zum Erstellen von Warnungen kann dazu führen, dass Warnungen falsch ausgelöst werden. Adobe empfiehlt die Verwendung von Daten ohne Zeitstempel für intelligente Warnhinweise.

## Anomalische Suche nach Warnungen

Wenn ein Warnhinweis eine Anomalieerkennung verwendet, hängt der Schulungszeitraum von der für den Warnhinweis ausgewählten Granularität ab.

* Monatliche Granularität: 15 Monate + gleicher Bereich im letzten Jahr
* Wöchentliche Granularität: 15 Wochen + gleicher Bereich im letzten Jahr
* Tägliche Granularität: 35 Tage + gleicher Bereich im letzten Jahr
* Stündliche Granularität: 336 Stunden

Weitere Informationen finden Sie unter [Statistische Verfahren zur Anomalieerkennung](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) .
