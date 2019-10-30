---
description: 'null'
seo-description: 'null'
seo-title: 'Datenanforderungen – Anforderungs-Assistent: Schritt 1'
title: 'Datenanforderungen – Anforderungs-Assistent: Schritt 1'
uuid: 717542c3-e4aa-4e00-b0ca-cadecd219d13
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Datenanforderungen – Anforderungs-Assistent: Schritt 1

Im Dialogfeld „Anforderungs-Assistent: Schritt 1“ wählen Sie die Report Suite, den Berichtstyp sowie die Segmente aus und konfigurieren Datumswerte.

![](assets/rw1_overview.png)

1. **[!UICONTROL Report Suite:]** Die Liste der für Sie aufgrund Ihrer Anmeldeangeben verfügbaren Report Suites. See [Select Report Suites](../../../analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md#task_59444416F6F042D1998217AE91580913).

1. **Bereichsauswahl:** Hier können Sie eine Report Suite ID aus einer Zelle in Excel auswählen. See [Select Report Suites](../../../analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md#task_59444416F6F042D1998217AE91580913).

1. **Segment**: Segmente sind benutzerspezifische Teildatensätze oder Daten, die durch eigens erstellte Regeln gefiltert wurden. Segmente basieren auf Treffern, Besuchen und Besuchern. Weitere Informationen zu Segmenten finden Sie im [Analytics-Segmentierungsleitfaden](https://marketing.adobe.com/resources/help/en_US/analytics/segment/).

   Beispiel: Sie führen einen [!UICONTROL Seitenbericht] aus und wenden dann ein Segment „Erstbesuche“ an.

1. **Veröffentlichungsliste darf außer Kraft gesetzt werden:** Wenn Sie einen Bericht planen, können Sie eine Veröffentlichungsliste auswählen, die für die Verteilung verwendet werden soll. Publishing lists are set up in **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin tools]**. Die Report Suite für diese Anforderung wird durch die Report Suite mit der ID ersetzt, die den einzelnen Empfängern in der Veröffentlichungsliste zugeordnet ist. Siehe [Veröffentlichungsliste darf außer Kraft gesetzt werden](../../../analyze/report-builder/data-requests/allow-publishing-list-overrides.md#concept_BCB19A20DC4B4B8D984F9670EE018D8C).

1. **Berichtstyp**: Hier wird der Basisbericht festgelegt, der in der Datenanforderung ausgeführt werden soll. Es wird ein Bericht pro Anforderung ausgeführt, und dieser Bericht kann 1:n Dimensionen und 1:n Metriken enthalten. Metriken und Dimensionen für einen Berichtstyp werden im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2] angezeigt. Siehe Berichtstypen [auswählen](../../../analyze/report-builder/data-requests/c-report-types/select-report-types.md#concept_C711B27E6FB64C18AC564EE142FC7EFC).

1. **Datumsbereiche**: Hier wird die von der Anforderung abgedeckte Zeitspanne festgelegt. Es sind verschiedene Arten von Zeiträumen verfügbar, z. B. vordefinierte, feste und rollierende. Es sind maximal 366 Zeiträume erlaubt. Sie können außerdem einen Datumsbereich wählen, der durch eine Zelle festgelegt wird, und Datumsbereiche als Vorlagen zur späteren Verwendung speichern.  Siehe Berichtsdaten [konfigurieren](../../../analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md)

1. **Granularität anwenden**: Hier wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben. Siehe [Granularität](../../../analyze/report-builder/data-requests/configuring-report-dates/granularity.md#concept_A13CBA2962E24FF882456135431B7ADB).

>[!MORE_LIKE_THIS]
>
>* [Eine Datenanforderung erstellen](/help/analyze/report-builder/data-requests/t-create-a-data-request.md)