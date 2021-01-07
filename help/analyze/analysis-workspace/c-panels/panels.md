---
description: Ein Bereich ist eine Sammlung von Tabellen und Visualisierungen
title: Übersicht über Bedienfelder
translation-type: tm+mt
source-git-commit: 272c50040a009d2b69885924e7b1f402636e8889
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 11%

---


# Übersicht über Bedienfelder

Ein [!UICONTROL Bedienfeld] ist eine Sammlung von Tabellen und Visualisierungen. Sie können auf Bedienfelder über das Symbol oben links in Workspace oder über ein [leeres Bedienfeld](blank-panel.md) zugreifen. Bedienfelder sind hilfreich, wenn Sie Ihre Projekte nach Zeiträumen, Report Suites oder Anwendungsfällen für Analysen organisieren möchten. Die folgenden Bedienfeldtypen sind in Analysis Workspace verfügbar:

| Name des Bedienfelds | Beschreibung |
| --- | --- |
| [Leeres Bedienfeld](blank-panel.md) | Wählen Sie aus den verfügbaren Bereichen und Visualisierungen, um Ihre Analyse Beginn. |
| [Bedienfeld „Quick Insights“](quickinsight.md) | Sie können rasch eine Freiformtabelle und eine entsprechende Visualisierung erstellen, um Einblicke schneller zu analysieren und bereitzustellen. |
| [Analytics for Target-Bedienfeld](a4t-panel.md) | Target-Aktivitäten und Erlebnisse in Analysis Workspace analysieren. |
| [Attributionsbedienfeld](attribution.md) | Vergleichen und visualisieren Sie schnell eine beliebige Anzahl von Zuordnungsmodellen mit einer beliebigen Dimension und Konversionsmetrik. |
| [Freiform-Bedienfeld](freeform-panel.md) | Führen Sie unbegrenzte Vergleiche und Aufschlüsselungen durch und fügen Sie dann Visualisierungen hinzu, um eine umfangreiche Datengeschichte zu erzählen. |
| [Bedienfeld „Gleichzeitige Medienbetrachter“](media-concurrent-viewers.md) | Analysieren Sie gleichzeitige Betrachter über einen längeren Zeitraum. Sie erhalten Details zum maximalen gleichzeitigen Zugriff und die Möglichkeit, aufzuschlüsseln und zu vergleichen. |
| [Bedienfeld „Segmentvergleich“](c-segment-comparison/segment-comparison.md) | Vergleichen Sie schnell zwei Segmente über alle Datenpunkte hinweg, um automatisch relevante Unterschiede zu ermitteln. |

![](assets/panel-overview.png)

[!UICONTROL Quick Insights],   Blankand   FreeformPanels sind großartige Orte zum Beginn Ihrer Analyse, während  [!UICONTROL Analytics für Zielgruppe],  [!UICONTROL Attribution IQ],  [!UICONTROL Media Concurrent-] Viewer und   Segment-Vergleich sich zu fortgeschrittenen Analysen eignen. In Projekten steht eine `"+"`-Schaltfläche zur Verfügung, mit der Sie jederzeit leere Bedienfelder hinzufügen können.

Das Standard-Startbedienfeld ist das Bedienfeld [!UICONTROL Freiform]. Sie können jedoch auch das leere Bedienfeld [als Standard festlegen.](/help/analyze/analysis-workspace/c-panels/blank-panel.md)

## Report Suite {#report-suite}

Tabellen und Visualisierungen innerhalb eines Bedienfelds leiten Daten von der [!UICONTROL Report Suite] ab, die oben rechts im Bedienfeld ausgewählt wurde. Die Report Suite bestimmt auch, welche Komponenten in der linken Leiste verfügbar sind. In einem Projekt können Sie je nach Anwendungsfällen Ihrer Analyse eine oder [viele Report Suites](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html?lang=de-DE) verwenden. Um eine einzelne Report Suite auf alle Bereiche in einem Projekt anzuwenden, klicken Sie **mit der rechten Maustaste auf Bereichsüberschrift > Report Suite auf alle Bereiche anwenden**.

Die Liste der Report Suites wird nach Relevanz sortiert. Die Adobe richtet sich danach, wie oft und wie oft die Suite vom aktuellen Benutzer verwendet wurde und wie oft die Suite in der Organisation verwendet wird.

![](assets/panel-report-suite.png)

## Kalender {#calendar}

Der Bedienfeldkalender steuert den Tabellenbereich und die Visualisierungen innerhalb eines Berichte.

Hinweis: Wenn eine (violette) Komponente des Datumsbereichs in einer Tabelle, Visualisierung oder einem Bereich-Dropzone verwendet wird, wird der Bereichskalender überschrieben.

![](assets/panel-calendar.png)

## Dropzone {#dropzone}

Mit dem Bedienfeld-Dropzone können Sie Segment- und Dropdown-Filter auf alle Tabellen und Visualisierungen innerhalb eines Bedienfelds anwenden. Sie können einen oder mehrere Filter auf einen Bereich anwenden. Der Titel über jedem Filter kann geändert werden, indem Sie auf den Stift bearbeiten klicken, oder Sie können mit der rechten Maustaste klicken, um ihn ganz zu entfernen.

### Filter segmentieren

Ziehen Sie ein beliebiges Segment aus der linken Leiste in den Ablagebereich des Bedienfelds, um mit dem Filtern des Bedienfelds zu beginnen.

![](assets/segment-filter.png)

### Ad-hoc-SegmentFilter

Nicht-Segmentkomponenten können auch direkt in die Dropzone gezogen werden, um Ad-hoc-Segmente zu erstellen. So sparen Sie Zeit und Mühe beim Aufrufen des Segmentaufbaus. Auf diese Weise erstellte Segmente werden automatisch als Segmente auf Trefferebene definiert. Diese Definition kann geändert werden, indem Sie auf das Informationssymbol (i) neben dem Segment klicken, dann auf das Bleistiftsymbol zum Bearbeiten und im Segmentaufbau bearbeiten.

Ad-hoc-Segmente sind lokal im Projekt und werden nicht in der linken Leiste angezeigt, es sei denn, Sie veröffentlichen sie.

![](assets/adhoc-segment-filter.png)

### Dropdown-Filter {#dropdown-filter}

Neben Segmentdaten ermöglichen Ihnen Dropdown-Filter die kontrollierte Interaktion mit den Filtern. Sie können beispielsweise einen Dropdown-Filter für Mobilgerätetypen hinzufügen, damit Sie das Bedienfeld nach Tablet, Mobiltelefon oder Desktop segmentieren können.

Dropdown-Filter können auch verwendet werden, um viele Projekte zu einem zu konsolidieren. Wenn Sie beispielsweise mehrere Versionen desselben Projekts mit unterschiedlichen Ländersegmenten verwenden, können Sie alle Versionen in einem Projekt zusammenfassen und einen Dropdown-Filter &quot;Land&quot;hinzufügen.

![](assets/dropdown-filter-intro.png)

So erstellen Sie Dropdown-Filter:

1. Wenn Sie einen Dropdownfilter mit [!UICONTROL Dimensionen] erstellen möchten, z. B. Werte innerhalb der Dimension [!UICONTROL Marketing-Kanal], klicken Sie in der linken Leiste auf das Pfeilsymbol neben Ihrer Dimension. Dadurch werden alle verfügbaren Elemente verfügbar gemacht. Wählen Sie ein oder mehrere Komponentenelemente aus der linken Leiste aus und legen Sie sie im Bedienfeld-Dropzone **ab, während Sie die Umschalttaste** gedrückt halten. Dadurch werden die Komponenten zu einem Dropdown-Filter und nicht zu einem einzigen Segment.
1. Wenn Sie einen Dropdown-Filter mit einer anderen Komponente wie Metriken, Segmente oder Datumsbereichen erstellen möchten, wählen Sie in der linken Leiste einen Komponententyp aus und legen Sie die Dropzone **im Bedienfeld ab, während Sie die Umschalttaste** gedrückt halten.
1. Wählen Sie eine der Optionen aus dem Dropdownmenü aus, um die Daten im Bedienfeld zu ändern. Sie können auch festlegen, dass keine der Bereichsdaten gefiltert werden, indem Sie **[!UICONTROL Kein Filter]** auswählen.

![](assets/create-dropdown.png)

[Sehen Sie sich das ](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/using-panels/using-panels-to-organize-your-analysis-workspace-projects.html) Video an, um mehr über das Hinzufügen von Dropdown-Filtern zu Ihrem Projekt zu erfahren.

## Rechtsklick auf Menü {#right-click}

Zusätzliche Funktionen für ein Bedienfeld sind verfügbar, wenn Sie mit der rechten Maustaste auf die Bereichsüberschrift klicken.

![](assets/right-click-menu.png)

Die folgenden Einstellungen sind verfügbar:

| Einstellung | Beschreibung |
| --- | --- |
| Kopiertes Bedienfeld/Visualisierung einfügen | Ermöglicht das Einfügen (&quot;Einfügen&quot;) eines kopierten Bereichs oder einer Visualisierung an eine andere Stelle im Projekt oder in ein komplett anderes Projekt. |
| Bedienfeld kopieren | Hiermit können Sie mit der rechten Maustaste klicken und einen Bereich kopieren, sodass Sie ihn an einer anderen Stelle im Projekt oder in ein komplett anderes Projekt einfügen können. |
| Report Suite auf alle Bereiche anwenden | Damit können Sie die Report Suite des aktiven Bereichs auf alle Bereiche im Projekt anwenden. |
| Duplikat | Erstellt ein exaktes Duplikat des aktuellen Bedienfelds, das Sie dann ändern können. |
| Alle Bedienfelder reduzieren/erweitern | Reduziert und erweitert alle Projektfenster. |
| Alle Visualisierungen im Bedienfeld reduzieren/erweitern | Reduziert und erweitert alle Visualisierungen im aktuellen Bedienfeld. |
| Beschreibung bearbeiten | hinzufügen (oder bearbeiten) Sie eine Textbeschreibung für das Bedienfeld. |
| Bereichslink abrufen | Sie können Personen zu einem bestimmten Bereich innerhalb eines Projekts leiten. Wenn auf den Link geklickt wird, muss sich der Empfänger anmelden, bevor er zu dem exakten Bereich weitergeleitet wird, mit dem er verknüpft ist. |
