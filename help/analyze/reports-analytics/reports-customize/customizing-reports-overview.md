---
description: Nachdem Sie einen Bericht ausgeführt haben können Sie diesen benutzerdefiniert anpassen, um die Daten nach Ihren Wünschen anzuzeigen und zu analysieren. Sie haben die Möglichkeit Berichtsdaten zu filtern, die Art und Weise der grafischen Präsentation zu ändern, die Datums-Granularität zu ändern usw.
title: Übersicht über das Anpassen von Berichten
uuid: 37d221b7-50fd-4425-b2ba-f40911b72a2f
feature: Grundlagen zu Reports & Analysen
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 99%

---


# Übersicht über das Anpassen von Berichten

Nachdem Sie einen Bericht ausgeführt haben können Sie diesen benutzerdefiniert anpassen, um die Daten nach Ihren Wünschen anzuzeigen und zu analysieren. Sie haben die Möglichkeit Berichtsdaten zu filtern, die Art und Weise der grafischen Präsentation zu ändern, die Datums-Granularität zu ändern usw.

## Benutzerspezifische Berichte erstellen {#task_BA6EACA3039C40AEA5605E1D8C76E646}

In diesen Schritten wird beschrieben, wie Sie die aktuelle Konfiguration eines Berichts als neuen benutzerspezifischen Bericht speichern, den alle Benutzer anzeigen können.

<!-- 

t_reports_custom.xml

 -->

Benutzerspezifische Berichte können nur durch Administratoren erstellt werden. Wenn Sie einen benutzerspezifischen Bericht erstellen, wird dieser im Hauptberichtsmenü neben dem Bericht hinzugefügt, auf dem er beruht.

**So erstellen Sie einen benutzerspezifischen Bericht**

1. Führen Sie einen Bericht aus und konfigurieren Sie ihn nach Bedarf.
1. Klicken Sie auf **[!UICONTROL Mehr]** > **[!UICONTROL Benutzerspezifischen Bericht erstellen]**.
1. Benennen Sie den Bericht und klicken Sie auf **[!UICONTROL Speichern]**.

   Vergewissern Sie sich, dass Sie keinen vorhandenen Berichtsnamen duplizieren.

>[!MORELIKETHIS]
>
>* [Menüanpassung](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/customize-menus.html)


## Datum oder Datumsbereich auswählen {#task_9BEF7D4D839A4748B76E8500D1406C34}

In diesen Schritten wird beschrieben, wie Sie die Zeiträume für Ihre Berichtsdaten auswählen.

<!-- 

t_reports_select_date.xml

 -->

So z. B. bestimmte Tage, Wochen, Monate oder Jahre. Sie können außerdem Vergleichsberichte ausführen.

Wenn Sie ein Dashboard mit Reportlets mit unterschiedlichen Datumsbereichen öffnen, können Sie einen neuen Datumsbereich im Kalender festlegen. Die Änderungen gelten für alle Reportlets im Dashboard.

**So wählen Sie einen Datumsbereich aus**

1. Einen Bericht ausführen.
1. Klicken Sie oben rechts auf das Kalendersymbol.
1. Wählen Sie ein Datum aus.

   Sie können:

   * Sie können bis zu drei Tages-, Monats- oder Jahreszeiträume anzeigen.
   * Sie können mit dem Cursor einen Datenbereich auswählen.
   * Sie können Datumsangaben manuell eingeben.
   * Sie können einen Monat auswählen, indem Sie auf ihn klicken.
   * Sie können durch Klicken auf **[!UICONTROL Voreinstellung auswählen]** ein voreingestelltes Datum auswählen.
   * Sie können Datumswerte vergleichen.

1. Klicken Sie auf **[!UICONTROL Bericht ausführen]**.

## Datum vergleichen {#task_95155C3700774B709F5FB81AE96B0824}

In diesen Schritten wird beschrieben, wie Sie den Kalender verwenden können, um Datumsvergleiche zwischen Rangberichten auszuführen.

<!-- 

t_reports_comparing_dates.xml

 -->

Datumsvergleiche aus Trendberichten sind nicht möglich.

>[!NOTE]
>
>Wenn Sie einen Datumsvergleich bei Schlüsselmetriken in einem Dashboard durchführen möchten, können Sie die Daten mit zwei separaten Anforderungen in [Report Builder](https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/home.html) übertragen. Dann können Sie benutzerdefinierte Formeln in Excel verwenden, um den Unterschied zwischen den beiden Werten zu analysieren.

So führen Sie Datumsvergleiche zwischen Rangberichten in Reports &amp; Analytics aus:

1. Einen Bericht ausführen.
1. Klicken Sie oben rechts auf den Kalender.
1. Klicken Sie auf **[!UICONTROL Datum vergleichen]**.
1. Wählen Sie die Datumswerte aus, die Sie verwenden möchten.
1. Klicken Sie auf **[!UICONTROL Bericht ausführen]**.

## Prozentwerte als Diagramm anzeigen {#task_BC28CA19A4834AF6BFE68B5B5AEFE75D}

In diesen Schritten wird beschrieben, wie Sie festlegen können, ob Prozentwerte in einer Berichtstabelle als Diagramm angezeigt werden sollen.

<!-- 

t_reports_graph_percent.xml

 -->

Diese Art der Visualisierung ist auch in Dashboard-Reportlets verfügbar.

1. Führen Sie einen Bericht aus, der Prozentwerte unterstützt, wie zum Beispiel [!UICONTROL Seitenberichte].
1. Klicken Sie auf **[!UICONTROL Prozentwert angezeigt als: Diagramm]**.

## Berichtsdaten normalisieren {#task_8005B55E59BD479DA67BC618FF8BC94A}

In diesen Schritten wird beschrieben, wie Sie Berichtsdaten normalisieren.

<!-- 

t_reports_normalize.xml

 -->

Nachdem Sie einen Bericht mit verglichenen Datumswerten oder für A/B-Vergleiche ausgeführt haben, können Sie die Daten normalisieren, um die prozentuale Änderung zwischen den Berichten anzuzeigen. Der sekundäre Datensatz wird angepasst, um für Abweichungen in der Anzahl der gewählten Tage oder aufgrund unterschiedlichen Traffic-Aufkommens zu kompensieren.

**So normalisieren Sie Berichtsdaten**

1. Führen Sie einen Bericht aus, der Datenvergleiche unterstützt.
1. Klicken Sie auf **[!UICONTROL Datumsvergleich]** und legen Sie Ihren Datumsvergleich fest.
1. Klicken Sie auf **[!UICONTROL Bericht ausführen]**.
1. Klicken Sie auf **[!UICONTROL Daten normalisieren: Ja]**.

## Seitenauswahl für einen Bericht {#task_5CAC3B76BD4C4208B8D53DD972D4771F}

In diesen Schritten wird beschrieben, wie Sie eine bestimmte Seite aus den Seiten Ihrer Website für einen Bericht auswählen.

<!-- 

t_reports_select_page.xml

 -->

1. Erstellen Sie einen Bericht, zum Beispiel einen [!UICONTROL Bericht „Seitenanzeigen“] (**[!UICONTROL Berichte]** > **[!UICONTROL Site-Metriken]** > **[!UICONTROL Seitenansichten]**).
1. Klicken Sie auf den Link **[!UICONTROL Gewählte Seite]**.
1. Wählen Sie unter [!UICONTROL Seite auswählen] die Seiten aus, die Sie anzeigen möchten.
1. Suchen Sie die Seite.
1. Klicken Sie auf **[!UICONTROL OK]**.

## Report Suites vergleichen {#task_6BEBEB2D4F36497C9DA5B18ADAD35546}

In diesen Schritten wird beschrieben, wie Sie Berichte aus zwei Report Suites im selben Bericht anzeigen.

<!-- 

t_reports_compare_suites.xml

 -->

Neben der grafischen Darstellung bietet die Tabelle des Berichts einen prozentualen Vergleich. Folgende Berichte können als Vergleich ausgeführt werden:

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
1. Klicken Sie auf den Link **[!UICONTROL Mit Site vergleichen]**.
1. Suchen Sie die Report Suite.
1. Klicken Sie auf **[!UICONTROL OK]**.

## Berichtsgranularität festlegen {#task_7ED3EEC9E1704A918B25D06ADA3412E0}

In diesen Schritten wird beschrieben, wie Sie Summen aus Berichten auf stündlicher, täglicher, wöchentlicher, monatlicher, quartalsmäßiger oder jährlicher Basis anzeigen.

<!-- 

t_reports_granularity.xml

 -->

Der Zeitraum eines Berichts bestimmt, welche Granularitätsoptionen verfügbar sind. So können Sie z. B. nur **[!UICONTROL Stündlich]** auswählen, wenn Sie einen ein- oder zweitägigen Zeitrahmen ausgewählt haben. Die Granularität **[!UICONTROL Jährlich]** können Sie nur auswählen, wenn Sie mehr als ein Jahr ausgewählt haben.

**So geben Sie die Berichtsgranularität an**

1. Erstellen Sie einen Trendbericht, wie zum Beispiel **[!UICONTROL Site-Content]** > **[!UICONTROL Seiten]**.
1. Klicken Sie auf **[!UICONTROL Ansicht nach]** und anschließend auf Granularität.

## Wochentagsbericht ausführen {#task_67CC818ACC3749839B69BDB2ED9AE6B8}

In diesen Schritten wird beschrieben, wie Sie Berichte an einem bestimmten Wochentag ausführen, z. B. jeden Montag im angegebenen Datumsbereich.

<!-- 

t_reports_day_of_week.xml

 -->

Diese Funktion gilt nur für Trendberichte, die nach dem Datumsbereich „Woche“ oder „Tag“ gefiltert sind.

1. Führen Sie einen Trendbericht über einen festgelegten Datumsbereich aus.
1. Klicken Sie auf den Link **[!UICONTROL Wochentag]** und klicken Sie anschließend einen Link an.

## Schaltfläche „In Arbeitsbereich ausprobieren“ {#concept_DA41E22460B94BD9ADF63B1CEE2714A7}

Durch einen Klick auf die Schaltfläche **[!UICONTROL In Arbeitsbereich ausprobieren]** oben im Report wird der Bericht in Analysis Workspace geladen.

<!-- 

try_in_workspace.xml

 -->

Die meisten Berichte in Reports &amp; Analytics beinhalten jetzt die Schaltfläche „In Arbeitsbereich ausprobieren“, über die Sie die aktuelle Ansicht in Analysis Workspace reproduzieren können, um weitere Anpassungen vorzunehmen.

Aktuell ist die Schaltfläche nur verfügbar, wenn Ihrem Benutzernamen vollständige Berechtigungen in Analysis Workspace zugewiesen sind.

Weitere Informationen zu den Möglichkeiten, Ihren Bericht anzupassen, finden Sie im Handbuch zu [Analysis Workspace](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/home.html).
