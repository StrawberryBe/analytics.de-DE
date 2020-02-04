---
title: Akquise-Berichte in Adobe Analytics
description: Erfahren Sie, wie Sie Berichte mit dem Analysis Workspace erstellen.
translation-type: tm+mt
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# Akquise-Berichte

Akquise-Berichte zeigen Ihnen, wie Sie Besucher auf Ihre Site bringen.

In Adobe Analytics werden diese Berichte als **Marketingkanäle** bezeichnet. Sie erfordern eine grundlegende Ersteinrichtung, ermöglichen jedoch eine wesentlich benutzerspezifischere Ansicht der Kanäle.

> [!IMPORTANT]
>
> Richten Sie Ihre Marketingkanal-Verarbeitungsregeln zur Verwendung dieser Berichte ein. Informationen zur bestmöglichen Konfiguration von Marketingkanälen in Ihrem Unternehmen finden Sie unter [Erste Schritte mit Marketingkanälen](/help/components/c-marketing-channels/c-getting-started-mchannel.md) .

Auf dieser Seite wird davon ausgegangen, dass der Benutzer über grundlegende Kenntnisse in der Verwendung des Analysis Workspace verfügt. Siehe [Erstellen eines einfachen Berichts im Analysis Workspace für Google Analytics-Benutzer](create-report.md) , wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Gesamter Traffic - Kanäle

Zeigt eine aggregierte Ansicht aller Kanäle, die Besucher zum Erreichen Ihrer Site verwenden.

1. Suchen Sie im Menü Komponenten die Dimension **Marketingkanal** und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &#39;Dimension hier ablegen&#39;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

## Gesamter Traffic - Treemaps

Zeigt eine Treppe des Kanalverkehrs an. Dieser Bericht ähnelt dem Bericht &quot;Alle Traffic - Kanäle&quot;, wird jedoch anders angezeigt.

1. Klicken Sie auf das Symbol Visualisierungen auf der linken Seite und ziehen Sie die Treemap-Visualisierung auf den Arbeitsbereich über der leeren Freiformtabelle.
2. Klicken Sie auf das Symbol Komponenten links und ziehen Sie dann die Dimension **Marketingkanal** in den großen Freiform-Tabellenbereich mit der Bezeichnung &#39;Dimension hier ablegen&#39;.
3. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.
4. Beachten Sie, dass zusätzliche Metriken zusätzliche Treemaps erstellen. Wenn nur eine Treemap gewünscht wird:
   1. Klicken Sie auf die oberste Zelle der gewünschten Metrik, um die Treemap darzustellen.
   2. Klicken Sie bei gedrückter Umschalttaste auf die letzte Zelle derselben Metrikspalte, um die Spalte blau zu markieren. Wenn dies korrekt ausgeführt wird, ist eine Treemap in der Visualisierung vorhanden.
   3. Klicken Sie auf den farbigen Punkt in der oberen rechten Ecke der Treemap-Visualisierung und dann auf das Kontrollkästchen Auswahl sperren.

Treemaps können auf jede Dimension angewendet werden, nicht nur auf Marketingkanäle.

## Gesamter Traffic - Quelle/Mittel

Quell- und mittlere Berichte zeigen die Domänen an, die den Traffic zu Ihrer Site geleitet haben.

* Die primäre Dimension &quot; **Quelle** &quot;ist im Arbeitsbereich für Analysen als **Referrerdomäne** verfügbar.
* Die **primäre Dimension &quot;Mittel** &quot;ist im Arbeitsbereich für Analysen als **Referrer-Typ** verfügbar.
* Die primäre Dimension &quot; **Suchbegriff** &quot;ist im Arbeitsbereich für Analysen als Dimension &quot; **Suchbegriff** &quot;verfügbar.

1. Suchen Sie im Komponentenmenü die oben angegebene gewünschte Dimension und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen zu den jeweiligen Dimensionen finden Sie auf den folgenden Seiten im Komponenten-Benutzerhandbuch:

* [Verweisende Domäne](/help/components/c-variables/dimensionslist/reports-referring-domains.md)
* [Typ der verweisenden Stelle](/help/components/c-variables/dimensionslist/reports-ref-types.md)
* [Keywords](/help/components/c-variables/dimensionslist/reports-search-keywords.md)

## Alle Traffic - Verweise

* Die primäre Dimension &quot; **Quelle** &quot;ist im Arbeitsbereich für Analysen als **Referrerdomäne** verfügbar.
* Die primäre Dimension &quot; **Einstiegsseite** &quot;ist im Arbeitsbereich für Analysen als **Einstiegsseite** verfügbar.

1. Suchen Sie im Komponentenmenü die Dimension &quot; **Verweisende Domäne** &quot;oder &quot; **Entrypage** &quot;und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen finden Sie unter [Verweisende Domäne](/help/components/c-variables/dimensionslist/reports-referring-domains.md) im Komponenten-Benutzerhandbuch.

## Google Ad-Berichte und Search Console-Berichte

Adobe verwendet eine Funktion im Analysis Workspace, Advertising Analytics, um Werbe- und Suchdaten von mehreren Plattformen, einschließlich Google, einzubringen.

Die Funktion für die Werbeanalyse erfordert eine Konfiguration, um Daten zurückgeben zu können. Weitere Informationen zur Aktivierung dieser zusätzlichen Dimensionen im Analysis Workspace finden Sie in der Hilfe[ zu ](/help/integrate/c-advertising-analytics/overview.md)Werbeanalysen.

## Social-Berichte

Social-Berichte enthalten ähnliche Informationen wie der jeweilige Verhaltensbericht, außer im Kontext sozialer Netzwerke. Diese Daten stehen im Analysis Workspace zur Verfügung, indem eine Dimension mit einem Segment kombiniert wird.

Manchmal erreichen Besucher Ihre Site über mehrere Kanäle in derselben Sitzung. Ein Besucher klickt beispielsweise auf eine Social-Media-Seite und dann einige Minuten später auf eine Suchmaschine, um Ihre Site zu erreichen. In diesen Fällen können nicht-soziale Domänen in diesem Bericht angezeigt werden. Wenn Sie nicht soziale Domänen ausschließen möchten, sortieren Sie den Bericht nach Besuchen oder erstellen Sie eine Kopie des Segments, das auf Treffern statt Besuchen basiert. See [Segmentation Containers](/help/components/c-segmentation/seg-overview.md) in the Components user guide for more information.

### Social - Netzwerkverweise

Der Bericht &quot;Netzwerkverweise&quot;zeigt an, welche sozialen Netzwerkdomänen den Traffic zu Ihrer Site geleitet haben. Diese Daten sind im Arbeitsbereich für Analysen verfügbar und verwenden die Dimension **Verweisende Domäne** und das Segment **Besuche von Social-Sites** .

1. Suchen Sie im Menü &quot;Komponenten&quot;die Dimension &quot; **Verweisende Domäne** &quot;und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot;.
2. Suchen Sie im Menü Komponenten das Segment **Besuche von Social-Sites** und ziehen Sie es in den kleinen Bereich direkt über der Freiformtabelle mit der Bezeichnung &#39;Segment hier ablegen&#39;.
3. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

### Social - Einstiegsseiten

Der Bericht &quot;Einstiegsseiten&quot;zeigt an, auf welchen Seiten Besucher nach dem Klicken auf einen Link über ein soziales Netzwerk gelangt sind. Diese Daten sind im Arbeitsbereich für Analysen verfügbar und verwenden die Dimension **Einstiegsseite** und **Besuche von Social-Sites** .

1. Suchen Sie im Menü &quot;Komponenten&quot;die Dimension &quot; **Entrypage** &quot;und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot;.
2. Suchen Sie im Menü Komponenten das Segment **Besuche von Social-Sites** und ziehen Sie es in den kleinen Bereich direkt über der Freiformtabelle mit der Bezeichnung &#39;Segment hier ablegen&#39;.
3. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

### Social - Konversionen

Der Umrechnungsbericht zeigt E-Commerce-Daten im Kontext sozialer Netzwerke an. Zur Verwendung dieser Berichte auf beiden Plattformen ist eine zusätzliche Implementierung erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt für den Analysis Workspace konfiguriert sind.

### Social - Plugins

Der Bericht &quot;Plugins&quot;zeigt an, wie Besucher mit eingebetteten Social Media-Plug-Ins auf Ihrer Site interagieren. Für die Verwendung im Analysis Workspace ist eine zusätzliche Implementierung erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt erfasst werden.

### Social - Benutzerfluss

Der Bericht &quot;Benutzerfluss&quot;zeigt Pfaddaten im Zusammenhang mit Besuchern an, die über ein soziales Netzwerk ankommen.

1. Klicken Sie auf das Symbol Visualisierungen links und ziehen Sie eine Flussvisualisierung auf den Arbeitsbereich über der Freiformtabelle
2. Klicken Sie auf das Symbol Komponenten links und ziehen Sie dann das Segment **Besuche von Social-Sites** in den kleinen Bereich direkt über der Flussvisualisierung mit der Bezeichnung &#39;Segment hier ablegen&#39;.
3. Suchen Sie die Dimension &quot; **Seiten** &quot;und klicken Sie dann auf das Pfeilsymbol, um die Seitenwerte anzuzeigen. Dimensionswerte sind gelb.
4. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den Bereich mit der Bezeichnung &quot;Dimension oder Element&quot;in der Mitte
5. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

## Kampagnen - Alle

Der Kampagnenbericht ist im Analysis Workspace unter Verwendung der Dimension **Rückverfolgungscode** verfügbar. Beachten Sie, dass die Verwendung der Tracking-Code-Dimension eine zusätzliche Implementierung zur Datenerfassung erfordert.

Es ist möglich, UTM-Parameter in Adobe Analytics mithilfe von benutzerspezifischen Variablen (eVars) zu erfassen. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass Trackingcodewerte in Adobe Analytics genau erfasst werden.

1. Suchen Sie im Menü Komponenten die Dimension **Trackingcode** und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &#39;Dimension hier ablegen&#39;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

## Kampagnen - Gebührenpflichtige Suchbegriffe

Der Bericht zu gebührenpflichtigen Suchbegriffen zeigt die Leistung der einzelnen Suchbegriffe an, nachdem ein Besucher auf einen Link zur gebührenpflichtigen Suche in einer Suchmaschine geklickt hat. Die Dimension &quot; **Suchbegriffe - Gebührenpflichtig** &quot;ist im Arbeitsbereich für Analysen verfügbar, erfordert jedoch eine einmalige Einrichtung der gebührenpflichtigen Sucherkennung, um Daten zu erfassen. Weitere Informationen zum Einrichten finden Sie unter [Gebührenpflichtige Sucherkennung](/help/admin/admin/paid-search-detection/paid-search-detection.md) im Admin-Benutzerhandbuch.

1. Suchen Sie im Menü Komponenten die Dimension **Suchbegriff - Gebührenpflichtig** und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &#39;Dimension hier ablegen&#39;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

## Kampagnen - Kostenlose Suchbegriffe

Der Bericht zu kostenlosen Suchbegriffen zeigt an, wie die einzelnen Suchbegriffe funktionieren, wenn ein Besucher auf einen kostenlosen Suchlink von einer Suchmaschine klickt. Die Dimension **&quot;Suchbegriffe - Kostenlos** &quot;ist im Arbeitsbereich für Analysen verfügbar. Beachten Sie, dass bei nicht eingerichteter gebührenpflichtiger Sucherkennung diese Dimension sowohl gebührenpflichtige als auch kostenlose Suchbegriffe erfasst.

1. Suchen Sie im Menü Komponenten die Dimension **Suchbegriff - Kostenlos** und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &#39;Dimension hier ablegen&#39;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

## Kostenanalyse

Dieser Bericht zeigt Daten zur Besuchs-, Kosten- und Umsatzleistung Ihrer gebührenpflichtigen Marketingkanäle an. Adobe bietet ein spezielles Produkt zur Bereitstellung von Insight, die Adobe Advertising Cloud. Wenn Ihr Unternehmen an der Verwendung dieses Produkts interessiert ist, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens.
