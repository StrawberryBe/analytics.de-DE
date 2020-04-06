---
description: Nachdem Sie einen Bericht ausgeführt haben, können Sie den Bericht an Ihre Ansicht anpassen und die Daten entsprechend Ihren Anforderungen analysieren. Sie können Berichtsdaten filtern, die grafische Darstellung der Daten ändern, die Datumsgranularität ändern usw.
title: Übersicht über das Anpassen von Berichten
topic: Reports and analytics
uuid: 37d221b7-50fd-4425-b2ba-f40911b72a2f
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Übersicht über das Anpassen von Berichten

Nachdem Sie einen Bericht ausgeführt haben, können Sie den Bericht an Ihre Ansicht anpassen und die Daten entsprechend Ihren Anforderungen analysieren. Sie können Berichtsdaten filtern, die grafische Darstellung der Daten ändern, die Datumsgranularität ändern usw.

## Benutzerspezifische Berichte erstellen {#task_BA6EACA3039C40AEA5605E1D8C76E646}

Schritte, die beschreiben, wie die aktuelle Konfiguration eines Berichts als neuer benutzerdefinierter Bericht gespeichert wird, der allen Benutzern zur Verfügung steht.

<!-- 

t_reports_custom.xml

 -->

Nur Administratoren können einen benutzerspezifischen Bericht erstellen. Wenn Sie einen benutzerspezifischen Bericht erstellen, wird er dem Hauptmenü des Berichte neben dem Bericht hinzugefügt, auf dem er basiert.

**So erstellen Sie einen benutzerspezifischen Bericht**

1. Führen Sie einen Bericht aus und konfigurieren Sie ihn nach Bedarf.
1. Klicken Sie auf **[!UICONTROL More]** > **[!UICONTROL Create Custom Report]**.
1. Name the report, then click **[!UICONTROL Save.]**

   Vergewissern Sie sich, dass Sie keinen vorhandenen Berichtsnamen duplizieren.

>[!MORELIKETHIS]
>
>* [Menüanpassung](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/customize-menus.translate.html)


## Datum oder Datumsbereich auswählen {#task_9BEF7D4D839A4748B76E8500D1406C34}

In diesen Schritten wird beschrieben, wie Sie die Zeiträume für Ihre Berichtsdaten auswählen.

<!-- 

t_reports_select_date.xml

 -->

Sie können bestimmte Tage, Wochen, Monate oder Jahre auswählen. Sie können auch Vergleichsberichte ausführen.

Wenn Sie ein Dashboard mit Reportlets mit unterschiedlichen Datumsbereichen öffnen, können Sie einen neuen Datumsbereich im Kalender auswählen. Die Änderungen gelten für alle Reportlets im Dashboard.

**So wählen Sie einen Datumsbereich aus**

1. Einen Bericht ausführen.
1. Klicken Sie oben rechts auf das Kalendersymbol.
1. Wählen Sie ein Datum aus.

   Sie können:

   * Ansichten-, Monats- oder Jahreszeiträume (bis zu drei).
   * Ziehen Sie den Cursor über Daten, um einen Bereich auszuwählen.
   * Geben Sie Datumsangaben manuell ein.
   * Klicken Sie auf einen Monatsnamen, um einen Monat auszuwählen.
   * Klicken Sie auf **[!UICONTROL Select Preset]** , um ein voreingestelltes Datum auszuwählen.
   * Sie können Datumswerte vergleichen.

1. Klicken Sie auf **[!UICONTROL Run Report]**.

## Datum vergleichen {#task_95155C3700774B709F5FB81AE96B0824}

Schritte, die beschreiben, wie Sie den Kalender verwenden können, um Datumsvergleiche zwischen Rangberichten auszuführen.

<!-- 

t_reports_comparing_dates.xml

 -->

Datumsvergleiche zwischen Trendberichten sind nicht möglich.

>[!NOTE] Wenn Sie einen Datumsvergleich bei Schlüsselmetriken in einem Dashboard durchführen möchten, können Sie die Daten mit zwei separaten Anforderungen in [Report Builder](https://marketing.adobe.com/resources/help/de_DE/arb/) übertragen. Dann können Sie benutzerdefinierte Formeln in Excel verwenden, um den Unterschied zwischen den beiden Werten zu analysieren.

So vergleichen Sie Datumsangaben zwischen Rangberichten in Reports &amp; Analysen:

1. Einen Bericht ausführen.
1. Klicken Sie oben rechts auf den Kalender.
1. Klicken Sie auf **[!UICONTROL Compare Dates]**.
1. Wählen Sie die Datumswerte aus, die Sie verwenden möchten.
1. Klicken Sie auf **[!UICONTROL Run Report]**.

## Prozentwerte als Diagramm anzeigen {#task_BC28CA19A4834AF6BFE68B5B5AEFE75D}

In diesen Schritten wird beschrieben, wie Sie angeben, ob der Prozentsatz in einer Berichtstabelle als Diagramm angezeigt werden soll.

<!-- 

t_reports_graph_percent.xml

 -->

Diese Visualisierung ist auch in Dashboard-Reportlets verfügbar.

1. Run a report that supports percentages, such as a [!UICONTROL Pages Report].
1. Klicken Sie auf **[!UICONTROL Percent Shown As: Graph]**.

## Berichtsdaten normalisieren {#task_8005B55E59BD479DA67BC618FF8BC94A}

Schritte, die beschreiben, wie Berichtdaten normalisiert werden.

<!-- 

t_reports_normalize.xml

 -->

Nachdem Sie einen Bericht mit verglichenen Daten oder einen A/B-Vergleich ausgeführt haben, können Sie die Daten normalisieren, um den Prozentsatz der Änderungen zwischen den Berichten anzuzeigen. Der sekundäre Datensatz wird angepasst, um Unterschiede bei der Anzahl der ausgewählten Tage oder bei unterschiedlichen Traffic-Aufträgen auszugleichen.

**So normalisieren Sie Berichtsdaten**

1. Führen Sie einen Bericht aus, der Datenvergleiche unterstützt.
1. Klicken Sie auf **[!UICONTROL Compare Dates]** und geben Sie dann Ihren Datumsvergleich an.
1. Klicken Sie auf **[!UICONTROL Run Report]**.
1. Klicken Sie auf **[!UICONTROL Normalize Data: Yes]**.

## Seitenauswahl für einen Bericht {#task_5CAC3B76BD4C4208B8D53DD972D4771F}

In diesen Schritten wird beschrieben, wie Sie eine bestimmte Seite aus den Seiten Ihrer Website für einen Bericht auswählen.

<!-- 

t_reports_select_page.xml

 -->

1. Erstellen Sie einen Bericht, z. B. [!UICONTROL Page Views Report] ( **[!UICONTROL Reports]** > **[!UICONTROL Site Metrics]** > **[!UICONTROL Page Views]**).
1. Click the **[!UICONTROL Selected Page]** link.
1. On [!UICONTROL Choose Page], select the pages you want to display.
1. Suchen Sie die Seite.
1. Klicken Sie auf **[!UICONTROL OK.]**

## Report Suites vergleichen {#task_6BEBEB2D4F36497C9DA5B18ADAD35546}

In diesen Schritten wird beschrieben, wie Sie Berichte aus zwei Report Suites im gleichen Bericht anzeigen.

<!-- 

t_reports_compare_suites.xml

 -->

Neben der grafischen Darstellung bietet die Tabelle des Berichts einen prozentualen Vergleich. Die folgenden Berichte können mit Vergleichen ausgeführt werden:

* Site-Content
* Mobile
* Traffic-Quellen
* Kampagnen
* Produkte
* Besuchertreue
* Besucherprofil
* Benutzerspez. Konversion
* Benutzerspezifischer Traffic
* Target
* Umfrage

**So vergleichen Sie Report Suites**

1. Erstellen Sie einen Bericht, der Ihnen den Vergleich von Berichten ermöglicht.
1. Click the **[!UICONTROL Compare to Site]** link.
1. Suchen Sie die Report Suite.
1. Klicken Sie auf **[!UICONTROL OK.]**

## Berichtsgranularität festlegen {#task_7ED3EEC9E1704A918B25D06ADA3412E0}

Schritte, die beschreiben, wie Ansichten Gesamtzahlen auf Stunden-, Tages-, Wochen-, Monats-, Quartals- oder Jahresbasis melden.

<!-- 

t_reports_granularity.xml

 -->

Der Zeitraum des Berichts legt fest, welche Granularitätsoptionen verfügbar sind. Sie können beispielsweise nur auswählen, **[!UICONTROL Hourly]** wenn Sie einen ein- oder zweitägigen Zeitraum ausgewählt haben. Sie können nur **[!UICONTROL Yearly]** Granularität auswählen, wenn Sie mehr als ein Jahr ausgewählt haben.

**So legen Sie die Berichtsgranularität fest**

1. Erstellen Sie einen Trendbericht, z. B. **[!UICONTROL Site Content]** > **[!UICONTROL Pages.]**
1. Click the **[!UICONTROL View by]** link, then click a granularity.

## Wochentagsbericht ausführen {#task_67CC818ACC3749839B69BDB2ED9AE6B8}

In diesen Schritten wird beschrieben, wie Sie Berichte an einem bestimmten Wochentag ausführen, z. B. an jedem Montag in einem bestimmten Datumsbereich.

<!-- 

t_reports_day_of_week.xml

 -->

Diese Funktion gilt nur für Trendberichte, die nach einem Datumsbereich von Woche oder Tag gefiltert werden.

1. Führen Sie einen Trendbericht über einen festgelegten Datumsbereich aus.
1. Klicken Sie auf den **[!UICONTROL Day of Week]** Link und dann auf einen Tag.

## Schaltfläche „In Arbeitsbereich ausprobieren“{#concept_DA41E22460B94BD9ADF63B1CEE2714A7}

Wenn Sie auf die **[!UICONTROL Try In Workspace]** Schaltfläche oben in einem Bericht klicken, wird derselbe Bericht in Analyse Workspace geladen.

<!-- 

try_in_workspace.xml

 -->

Die meisten Berichte in Reports &amp; Analysen enthalten jetzt die Schaltfläche &quot;In Arbeitsbereich ausprobieren&quot;, mit der Sie die aktuelle Ansicht im Arbeitsbereich für Analysen für weitere Anpassungen reproduzieren können.

Derzeit ist die Schaltfläche nur verfügbar, wenn Ihr Benutzername über die volle Berechtigung für Analyse Workspace verfügt.

Weitere Informationen zu allen Möglichkeiten zum Anpassen Ihres Berichts finden Sie im Handbuch [Analyse Workspace](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/) .
