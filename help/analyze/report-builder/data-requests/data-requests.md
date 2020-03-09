---
description: 'null'
title: 'Datenanforderungen – Anforderungs-Assistent: Schritt 1'
uuid: 717542c3-e4aa-4e00-b0ca-cadecd219d13
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Datenanforderungen – Anforderungs-Assistent: Schritt 1

Im Dialogfeld „Anforderungs-Assistent: Schritt 1“ wählen Sie die Report Suite, den Berichtstyp sowie die Segmente aus und konfigurieren Datumswerte.

![](assets/rw1_overview.png)

1. **[!UICONTROL Report Suite:]** Die Liste der für Sie aufgrund Ihrer Anmeldeangeben verfügbaren Report Suites. Siehe [Report Suites auswählen](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **Bereichsauswahl:** Hier können Sie eine Report Suite-ID aus einer Zelle in Excel auswählen. Siehe [Report Suites auswählen](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **Segment**: Segmente sind benutzerspezifische Teildatensätze oder Daten, die durch eigens erstellte Regeln gefiltert wurden. Segmente basieren auf Treffern, Besuchen und Besuchern. Weitere Informationen zu Segmenten finden Sie im [Analytics-Segmentierungsleitfaden](https://marketing.adobe.com/resources/help/de_DE/analytics/segment/).

   Beispiel: Sie führen einen [!UICONTROL Seitenbericht] aus und wenden dann ein Segment „Erstbesuche“ an.

1. **Veröffentlichungsliste darf außer Kraft gesetzt werden:** Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungsliste auswählen, die für die Verteilung verwendet werden soll. Veröffentlichungslisten werden unter **[!UICONTROL Analytics]** > **[!UICONTROL Admin Tools]** eingerichtet. Die Report Suite für diese Anforderung wird durch die Report Suite mit der ID ersetzt, die den einzelnen Empfängern in der Veröffentlichungsliste zugeordnet ist. Siehe [Veröffentlichungsliste darf außer Kraft gesetzt werden](/help/analyze/report-builder/data-requests/allow-publishing-list-overrides.md).

1. **Berichtstyp**: Hier wird der Basisbericht festgelegt, der in der Datenanforderung ausgeführt werden soll. Es wird ein Bericht pro Anforderung ausgeführt, und dieser Bericht kann 1:n Dimensionen und 1:n Metriken enthalten. Metriken und Dimensionen für einen Berichtstyp werden im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2] angezeigt. Siehe [Berichtstypen auswählen](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md).

1. **Datumsbereiche**: Hier wird die von der Anforderung abgedeckte Zeitspanne festgelegt. Es sind verschiedene Arten von Zeiträumen verfügbar, z. B. vordefinierte, feste und rollierende. Es sind maximal 366 Zeiträume erlaubt. Sie können außerdem einen Datumsbereich wählen, der durch eine Zelle festgelegt wird, und Datumsbereiche als Vorlagen zur späteren Verwendung speichern.  Siehe [Berichtsdaten konfigurieren](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md).

1. **Granularität anwenden**: Hier wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben. Siehe [Granularität](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md).

>[!MORELIKETHIS]
>
>* [Eine Datenanforderung erstellen](/help/analyze/report-builder/data-requests/t-create-a-data-request.md)

