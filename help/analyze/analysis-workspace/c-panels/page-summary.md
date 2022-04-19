---
description: Das Bedienfeld "Seitenzusammenfassung"zeigt zusammenfassende Informationen für eine von Ihnen ausgewählte Seite an.
title: Seitenzusammenfassungsbereich
feature: Panels
role: User, Admin
source-git-commit: 4bb950350d258b8d608f6d95d37d7d860e23ed2c
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 9%

---


# Seitenzusammenfassungsbereich

Die [!UICONTROL Seitenzusammenfassung] wurde in Reports &amp; Analytics als Bericht unter Berichte > Interaktion > Seitenanalyse > Seitenzusammenfassung gestartet. Es handelt sich jetzt auch um einen Arbeitsbereich-Bereich. In diesem Bedienfeld können Sie einfach Schlüsselstatistiken zu bestimmten Seiten durchsuchen.

## Zugriff auf den Bereich

Sie können über [!UICONTROL Berichte] oder innerhalb [!UICONTROL Arbeitsbereich].

| Zugangspunkt | Beschreibung |
| --- | --- |
| [!UICONTROL Berichte] | <ul><li>Das Bedienfeld wurde bereits in einem Projekt abgelegt.</li><li>Die linke Leiste ist ausgeblendet.</li><li>Es wird nur die Dimension Seite unterstützt.</li><li>Eine Standardeinstellung wurde bereits angewendet, in diesem Fall wurde die am häufigsten besuchte Seite für die[!UICONTROL Seite] Dimension. Sie können diese Einstellung ändern.</li></ul> |
| Workspace | Erstellen Sie ein neues Projekt und wählen Sie in der linken Leiste das Bedienfeldsymbol aus. Ziehen Sie die [!UICONTROL Seitenzusammenfassung] oberhalb der Freiformtabelle angezeigt. Beachten Sie, dass die Seite [!UICONTROL Dimension] leer ist. Wählen Sie ein Dimensionselement aus der Dropdownliste aus. |

## Bedienfeldeingaben {#Input}

Sie können die [!UICONTROL Nächstes oder vorheriges Element] Bedienfeld mit den folgenden Eingabeeinstellungen:

| Einstellung | Beschreibung |
| --- | --- |
| Dropzone Segment (oder andere Komponente) | Sie können Segmente oder andere Komponenten per Drag-and-Drop verschieben, um die Ergebnisse Ihrer Bedienfelder weiter zu filtern. |
| Seitendimensionselement | Wählen Sie aus der Dropdownliste das Dimensionselement aus, dessen Schlüsselstatistiken Sie untersuchen möchten. |

{style=&quot;table-layout:auto&quot;}

Klicken **[!UICONTROL Build]** , um das Bedienfeld zu erstellen.

## Bedienfeldausgabe {#output}

Die [!UICONTROL Seitenzusammenfassung] -Bedienfeld gibt einen umfangreichen Satz an Metrikdaten und Visualisierungen zurück, damit Sie Statistiken über bestimmte Seiten besser verstehen können.

| Metrik/Visualisierung | Beschreibung |
| --- | --- |
| [!UICONTROL Seitenansichten] - Aktueller Monat, bisher | Anzahl der Seitenansichten für diese Seite im aktuellen Monat. |
| [!UICONTROL Seitenansichten] - 4 Wochen vorher | Anzahl der Seitenansichten für diese Seite im letzten Monat. |
| [!UICONTROL Seitenansichten] - 52 Wochen zuvor | Anzahl der Seitenansichten für diese Seite im letzten Jahr. |
| [!UICONTROL Trend] | Ein Trend-Seitenansichtsdiagramm für diesen Monat, 4 Wochen zuvor und 52 Wochen zuvor. |
| [!UICONTROL Prozentsatz aller Seitenansichten] | Eine Zusammenfassungsnummer für den Prozentsatz aller Seitenansichten, die auf diese Seite gelangt sind. |
| [!UICONTROL Besuchszeit pro Seite] | Ein horizontales Balkendiagramm mit der auf dieser Seite verbrachten Zeit. |
| [!UICONTROL Einzelseitenbesuche] | Eine Zusammenfassungsnummer, die die Anzahl der Seitenansichten auflistet, bei denen dies die einzige besuchte Seite war. |
| [!UICONTROL Neuladungen] | Die [!UICONTROL Neuladungen] gibt an, wie oft ein Dimensionselement während einer Neuladung vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen. |
| [!UICONTROL Einträge] | Die [!UICONTROL Einträge] gibt an, wie oft ein bestimmtes Dimensionselement als erster Wert bei einem Besuch erfasst wird. |
| [!UICONTROL Ausstiege] | Die [!UICONTROL Ausstiege] gibt an, wie oft ein bestimmtes Dimensionselement als letzter Wert bei einem Besuch erfasst wird. |
| [!UICONTROL Fluss] | Ein Flussdiagramm mit der ausgewählten Seite als Fokuspunkt. Sie können wie bei jeder [Flussdiagramm](/help/analyze/analysis-workspace/visualizations/c-flow/creating-flow-report.md). |

{style=&quot;table-layout:auto&quot;}
