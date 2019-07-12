---
title: Akquise-Berichte in Adobe Analytics
description: Erfahren Sie, wie Sie akquise-Berichte mithilfe von Analysis Workspace erstellen.
translation-type: tm+mt
source-git-commit: 71899840dd5b401c6892b6ad5088d4a32fd07042

---


# Akquise-Berichte

Akquise-Berichte zeigen, wie Sie Besucher auf Ihrer Site abrufen.

In Adobe Analytics, these reports are known as **Marketing Channels**. Sie benötigen einige grundlegende Ersteinstellungen, lassen jedoch eine wesentlich mehr benutzerdefinierte Kanalansicht zu.

> [!IMPORTANT]
>
> Richten Sie Ihre Marketingkanal-Verarbeitungsregeln ein, um diese Berichte zu verwenden. See [Getting Started with Marketing Channels](../../../components/c-marketing-channels/c-getting-started-mchannel.md) for information on how to best configure Marketing Channels in your organization.

Diese Seite geht davon aus, dass der Benutzer über grundlegende Kenntnisse zur Verwendung des Analysis Workspace verfügt. See [Create a basic report in Analysis Workspace for Google Analytics users](create-report.md) if you are not yet familiar with the tool in Adobe Analytics.

## Gesamter Traffic - Kanäle

Zeigt eine aggregierte Ansicht aller Kanäle, die Besucher zum Erreichen Ihrer Site verwenden.

1. In the Components menu, locate the **Marketing Channel** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

## Gesamter Traffic - Treemaps

Zeigt eine Treemap des Kanaltraffics an. Dieser Bericht ähnelt dem gesamten Traffic - Kanäle, wird aber auf unterschiedliche Weise angezeigt.

1. Klicken Sie auf das Symbol Visualisierungen links und ziehen Sie die Treemap-Visualisierung auf den Arbeitsbereich oberhalb der leeren Freiform-Tabelle.
2. Click the Components icon on the left, then drag the **Marketing Channel** dimension onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
3. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.
4. Beachten Sie, dass zusätzliche Metriken zusätzliche Treemaps erstellen. Wenn nur eine Treemap gewünscht wird:
   1. Klicken Sie auf die obere Zelle der gewünschten Metrik, um die Treemap darzustellen.
   2. Klicken Sie auf die letzte Zelle derselben Metrik-Spalte, um die Spalte blau zu markieren. Wenn eine Treue korrekt ausgeführt wird, ist eine Treemap in der Visualisierung vorhanden.
   3. Klicken Sie in der rechten oberen Ecke der Treemap-Visualisierung auf den farbigen Punkt und anschließend auf das Kontrollkästchen &quot;Auswahl sperren&quot; .

Treemaps können auf alle Dimensionen angewendet werden, nicht nur auf Marketingkanäle.

## Gesamter Traffic - Quelle/Mittel

Quell- und mittlere Berichte zeigen die Domänen an, die Traffic zu Ihrer Site bringen.

* The **Source** primary dimension is available in Analysis Workspace as the **Referring Domain** dimension.
* The **Medium** primary dimension is available in Analysis Workspace as the  **Referrer Type** dimension.
* **Die primäre Keyword** -Dimension steht im Analysis Workspace als **Keyword-** Dimension zur Verfügung.

1. Suchen Sie im Komponentenmenü die gewünschte Dimension oben und ziehen Sie sie auf den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot; .
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

Weitere Informationen zu ihrer jeweiligen Dimension finden Sie auf den folgenden Seiten im Benutzerhandbuch für Komponenten:

* [Verweisende Domäne](../../../components/c-variables/dimensionslist/reports-referring-domains.md)
* [Typ der verweisenden Stelle](../../../components/c-variables/dimensionslist/reports-ref-types.md)
* [Keywords](../../../components/c-variables/dimensionslist/reports-search-keywords.md)

## Gesamter Traffic - Verweise

* The **Source** primary dimension is available in Analysis Workspace as the **Referring Domain** dimension.
* The **Landing Page** primary dimension is available in Analysis Workspace as the **Entry Page** dimension.

1. In the components menu, locate the **Referring Domain** or **Entry Page** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Referring Domain](../../../components/c-variables/dimensionslist/reports-referring-domains.md) dimension in the Components user guide for more information.

## Berichte zu Google Ads und Search Console

Adobe verwendet im Analysis Workspace eine Funktion namens Advertising Analytics, um Werbe- und Suchdaten von mehreren Plattformen, einschließlich Google, zu erfassen.

Die Anzeigenanalysefunktion erfordert die Konfiguration der Daten. See [Advertising Analytics Help](../../../integrate/c-advertising-analytics/overview.md) for details on how to enable these additional dimensions in Analysis Workspace.

## Social-Berichte

Social-Berichte liefern ähnliche Informationen wie der jeweilige Verhaltensbericht, außer im Kontext sozialer Netzwerke. Diese Daten sind im Analysis Workspace verfügbar, indem Sie eine Dimension mit einem Segment kombinieren.

Manchmal erreichen Besucher Ihre Site über mehrere Kanäle in derselben Sitzung. Ein Besucher klickt zum Beispiel auf eine Social Media-Seite und dann einige Minuten später auf eine Suchmaschine, um Ihre Site zu erreichen. In diesen Fällen können Nicht-Social-Domänen in diesem Bericht angezeigt werden. Wenn Sie Nicht-Social-Domänen ausschließen möchten, sortieren Sie den Bericht nach Besuchen oder erstellen Sie eine Kopie des Segments, die auf Treffern statt auf Besuchen basiert. See [Segmentation Containers](../../../components/c-segmentation/seg-overview.md) in the Components user guide for more information.

### Social - Netzwerkverweise

Der Bericht &quot;Netzwerkverweise&quot; zeigt an, welche sozialen Netzwerkdomänen den Traffic zu Ihrer Site bringen. This data is available in Analysis Workspace using the **Referring Domain** dimension and **Visits from Social Sites** segment.

1. In the Components menu, locate the **Referring Domain** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. In the Components menu, locate the **Visits from Social Sites** segment and drag in onto the small area just above the freeform table labeled &#39;Drop a segment here&#39;.
3. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

### Social - Einstiegsseiten

Der Bericht &quot;Einstiegsseiten&quot; zeigt an, auf welche Seiten Besucher gelangt sind, nachdem sie über ein soziales Netzwerk auf einen Link geklickt haben. This data is available in Analysis Workspace using the **Entry Page** dimension and **Visits from Social Sites** segment.

1. In the Components menu, locate the **Entry Page** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. In the Components menu, locate the **Visits from Social Sites** segment and drag in onto the small area just above the freeform table labeled &#39;Drop a segment here&#39;.
3. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

### Social - Konversionen

Der Umrechnungsbericht zeigt E-Commerce-Daten im Kontext sozialer Netzwerke an. Zur Verwendung dieser Berichte auf beiden Plattformen ist zusätzliche Implementierungen erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten für den Analysis Workspace richtig konfiguriert wurden.

### Social - Plugins

Der Bericht zu Plugins zeigt an, wie Besucher mit eingebetteten Social Media-Plugins auf Ihrer Site interagieren. Zusätzliche Implementierungen sind für die Verwendung in Analysis Workspace erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten genau erfasst werden.

### Social - Benutzerfluss

Der Bericht &quot;Benutzerfluss&quot; zeigt Pfaddaten im Kontext von Besuchern, die über ein soziales Netzwerk gelangen.

1. Klicken Sie links auf das Visualisierungssymbol und ziehen Sie eine Flussvisualisierung auf den Arbeitsbereich oberhalb der Freiformtabelle.
2. Click the Components icon on the left, then drag the **Visits from Social Sites** segment onto the small area just above the flow visualization labeled &#39;Drop a Segment here&#39;.
3. Locate the **Pages** dimension, then click the Arrow icon to reveal page values. Dimensionswerte sind gelb farbig.
4. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den Bereich mit der Bezeichnung &quot;Dimension oder Element&quot; in der Mitte.
5. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um die Flüsse auf die nachfolgenden oder vorherigen Seiten zu erweitern. Verwenden Sie das Rechtsklick-Menü, um Spalten zu erweitern oder zu minimieren. Innerhalb desselben Flussberichts können auch unterschiedliche Dimensionen verwendet werden.

## Kampagnen - Alle

The campaigns report is available in Analysis Workspace using the **Tracking Code** dimension. Beachten Sie, dass für die Verwendung der Rückverfolgungscode-Dimension zusätzliche Implementierungen zur Datenerfassung erforderlich sind.

Es ist möglich, UTM-Parameter in Adobe Analytics mithilfe von benutzerdefinierten Variablen (evars) zu erfassen. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass die Rückverfolgungscodewerte in Adobe Analytics genau erfasst werden.

1. In the Components menu, locate the **Tracking Code** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

## Kampagnen - Gebührenpflichtige Suchbegriffe

Der Bericht zu gebührenpflichtigen Suchbegriffen zeigt an, wie die einzelnen Suchbegriffe ausgeführt werden, nachdem ein Besucher auf einen gebührenpflichtigen Suchlink von einer Suchmaschine klickt. The **Search Keywords - Paid** dimension is available in Analysis Workspace, but requires a one-time setup of paid search detection to collect data. See [Paid Search Detection](../../../admin/admin/paid-search-detection/paid-search-detection.md) in the Admin user guide for setup details.

1. In the Components menu, locate the **Search Keyword - Paid** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

## Kampagnen - Kostenlose Suchbegriffe

Der Bericht zu organischen Suchbegriffen zeigt an, wie die einzelnen Suchbegriffe nach dem Klicken auf einen kostenlosen Suchlink aus einer Suchmaschine ausgeführt werden. The **Search Keywords - Natural** dimension is available in Analysis Workspace. Beachten Sie, dass diese Dimension, wenn keine gebührenpflichtige Sucherkennung eingerichtet ist, sowohl gebührenpflichtige als auch kostenlose Suchbegriffe erfasst.

1. In the Components menu, locate the **Search Keyword - Natural** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

## Kostenanalyse

Dieser Bericht zeigt die Daten zu Besuchen, Kosten und Umsatz für Ihre gebührenpflichtigen Marketingkanäle. Adobe bietet ein dediziertes Produkt, das Einblicke in die Adobe Advertising Cloud bietet. Wenn Ihr Unternehmen an der Nutzung dieses Produkts interessiert ist, wenden Sie sich an den Kundenbetreuer Ihrer Organisation.
