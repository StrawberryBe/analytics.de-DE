---
title: Akquiseberichte in Adobe Analytics
description: Erfahren Sie, wie Sie mit Analysis Workspace akquisebasierte Berichte erstellen.
exl-id: 2929d34b-8eb0-4105-a49c-02d536929fe0
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '1578'
ht-degree: 100%

---

# Akquiseberichte

Akquiseberichte zeigen Ihnen, wie Sie Besucher auf Ihre Site bringen.

In Adobe Analytics werden diese Berichte als **Marketing-Kanäle** bezeichnet. Sie erfordern eine grundlegende Ersteinrichtung, ermöglichen jedoch eine wesentlich benutzerspezifischere Ansicht der Kanäle.

>[!IMPORTANT]
>
> Richten Sie zur Verwendung dieser Berichte Ihre Marketing-Kanal-Verarbeitungsregeln ein. Informationen zur bestmöglichen Konfiguration von Marketing-Kanälen in Ihrem Unternehmen finden Sie unter [Erste Schritte mit Marketing-Kanälen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

Auf dieser Seite wird davon ausgegangen, dass der Anwender über grundlegende Kenntnisse in der Verwendung von Analysis Workspace verfügt. Siehe [Basisbericht in Analysis Workspace für GA-Anwender erstellen](create-report.md), wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Alle Zugriffe – Channels

Zeigt eine aggregierte Ansicht aller Kanäle, die Besucher zum Erreichen Ihrer Site verwenden.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Marketing-Kanal** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

## Alle Zugriffe – Treemaps

Zeigt eine Treemap des Kanal-Traffics an. Dieser Bericht ähnelt dem Bericht „Alle Zugriffe – Channels“, wird jedoch anders angezeigt.

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie die Treemap-Visualisierung auf den Arbeitsbereich über der leeren Freiformtabelle.
2. Klicken Sie links auf das Symbol „Komponenten“ und ziehen Sie dann die Dimension **Marketing-Kanal** in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
3. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).
4. Beachten Sie, dass zusätzliche Metriken zusätzliche Treemaps erstellen. Wenn nur eine Treemap gewünscht wird:
   1. Klicken Sie auf die oberste Zelle der gewünschten Metrik, um die Treemap darzustellen.
   2. Klicken Sie bei gedrückter Umschalttaste auf die letzte Zelle derselben Metrikspalte, um die Spalte blau zu markieren. Wenn dies korrekt ausgeführt wird, ist eine Treemap in der Visualisierung vorhanden.
   3. Klicken Sie auf den farbigen Punkt in der oberen rechten Ecke der Treemap-Visualisierung und dann auf das Kontrollkästchen „Auswahl sperren“.

Treemaps können auf jede Dimension angewendet werden, nicht nur auf Marketing-Kanäle.

## Alle Zugriffe – Quelle/Medium

Berichte zu Quellen und Medien zeigen die Domänen an, die den Traffic zu Ihrer Site geleitet haben.

* Die primäre Dimension **Quelle** ist in Analysis Workspace als Dimension **Referrer-Domäne** verfügbar.
* Die primäre Dimension **Medium** ist in Analysis Workspace als Dimension **Referrer-Typ** verfügbar.
* Die primäre Dimension **Keyword** ist in Analysis Workspace als Dimension **Suchbegriff** verfügbar.

1. Suchen Sie im Menü „Komponenten“ die oben angegebene gewünschte Dimension und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen zu den jeweiligen Dimensionen finden Sie auf den folgenden Seiten im Benutzerhandbuch zu Komponenten:

* [Verweisende Domäne](/help/components/dimensions/referring-domain.md)
* [Typ der verweisenden Stelle](/help/components/dimensions/referrer-type.md)
* [Keywords](/help/components/dimensions/search-keyword.md)

## Alle Zugriffe – Verweise

* Die primäre Dimension **Quelle** ist in Analysis Workspace als Dimension **Referrer-Domäne** verfügbar.
* Die primäre Dimension **Landingpage** ist in Analysis Workspace als Dimension **Entrypage** verfügbar.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Referrer-Domäne** oder **Entrypage** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen finden Sie im Abschnitt zur Dimension [Referrer-Domäne](/help/components/dimensions/referring-domain.md) im Benutzerhandbuch zu Komponenten.

## Google Ads- und Search Console-Berichte

Adobe verwendet in Analysis Workspace eine Funktion namens Advertising Analytics, um Werbe- und Suchdaten von mehreren Plattformen, einschließlich Google, einzuspeisen.

Die Funktion Advertising Analytics erfordert eine Konfiguration, um Daten zurückgeben zu können. Weitere Informationen zur Aktivierung dieser zusätzlichen Dimensionen in Analysis Workspace finden Sie in der [Advertising Analytics-Hilfe](/help/integrate/c-advertising-analytics/overview.md).

## Social-Berichte

Social-Berichte enthalten ähnliche Informationen wie der jeweilige Verhaltensbericht, jedoch im Kontext sozialer Netzwerke. Diese Daten stehen in Analysis Workspace zur Verfügung, indem eine Dimension mit einem Segment kombiniert wird.

Manchmal erreichen Besucher Ihre Site über mehrere Kanäle in derselben Sitzung. Ein Besucher klickt beispielsweise auf eine Social-Media-Seite und dann einige Minuten später auf eine Suchmaschine, um Ihre Site zu erreichen. In diesen Fällen werden möglicherweise Nicht-Social-Domänen in diesem Bericht angezeigt. Wenn Sie Nicht-Social-Domänen ausschließen möchten, sortieren Sie den Bericht nach Besuchen oder erstellen Sie eine Kopie des Segments, das auf Treffern statt Besuchen basiert. Weitere Informationen finden Sie unter [Segmentierungs-Container](/help/components/segmentation/seg-overview.md) im Benutzerhandbuch zu Komponenten.

### Social – Netzwerkverweise

Der Bericht zu Netzwerkverweisen zeigt an, welche Domänen von sozialen Netzwerken den Traffic zu Ihrer Site geleitet haben. Diese Daten sind in Analysis Workspace unter Verwendung der Dimension **Referrer-Domäne** und des Segments **Besuche von sozialen Websites** verfügbar.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Referrer-Domäne** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Suchen Sie im Menü „Komponenten“ das Segment **Besuche von sozialen Websites** und ziehen Sie es in den kleinen Bereich namens „Segment hier ablegen“ direkt über der Freiformtabelle.
3. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

### Social – Landing-Pages

Der Landing-Pages-Bericht zeigt, auf welche Seiten Besucher nach dem Klicken auf einen Link in einem sozialen Netzwerk gelangt sind. Diese Daten sind in Analysis Workspace unter Verwendung der Dimension **Entrypage** und des Segments **Besuche von sozialen Websites** verfügbar.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Entrypage** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Suchen Sie im Menü „Komponenten“ das Segment **Besuche von sozialen Websites** und ziehen Sie es in den kleinen Bereich namens „Segment hier ablegen“ direkt über der Freiformtabelle.
3. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

### Social – Conversions

Der Konversionsbericht zeigt E-Commerce-Daten im Kontext sozialer Netzwerke an. Zur Verwendung dieser Berichte ist auf beiden Plattformen eine zusätzliche Implementierung erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt für Analysis Workspace konfiguriert sind.

### Social – Plug-ins

Der Bericht „Plug-ins“ zeigt an, wie Besucher mit eingebetteten Social-Media-Plug-ins auf Ihrer Site interagieren. Für die Verwendung in Analysis Workspace ist eine zusätzliche Implementierung erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt erfasst werden.

### Social – Nutzerfluss

Der Bericht zum Benutzerfluss zeigt Pfaddaten im Zusammenhang mit Besuchern an, die über ein soziales Netzwerk ankommen.

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie die Flussvisualisierung auf den Arbeitsbereich über der Freiformtabelle.
2. Klicken Sie links auf das Symbol „Komponenten“ und ziehen Sie dann das Segment **Besuche von sozialen Websites** in den kleinen Bereich namens „Segment hier ablegen“ direkt über der Flussvisualisierung.
3. Suchen Sie die Dimension **Seiten** und klicken Sie dann auf das Pfeilsymbol, um die Seitenwerte anzuzeigen. Dimensionselemente sind gelb markiert.
4. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den mittigen Bereich namens „Dimension oder Element“.
5. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

## Kampagnen – Alle

Der Kampagnenbericht ist in Analysis Workspace unter Verwendung der Dimension **Trackingcode** verfügbar. Beachten Sie, dass die Verwendung der Dimension „Trackingcode“ eine zusätzliche Implementierung zur Datenerfassung erfordert.

Es ist möglich, UTM-Parameter in Adobe Analytics mithilfe von benutzerspezifischen Variablen (eVars) zu erfassen. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass Trackingcode-Werte in Adobe Analytics genau erfasst werden.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Trackingcode** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

## Kampagnen – Bezahlte Keywords

Der Bericht zu gebührenpflichtigen Keywords zeigt die Leistung der einzelnen Suchbegriffe an, nachdem ein Besucher in einer Suchmaschine auf einen Paid-Search-Link geklickt hat. Die Dimension **Suchbegriffe – Gebührenpflichtig** ist in Analysis Workspace verfügbar, erfordert jedoch eine einmalige Einrichtung der Paid-Search-Erkennung, um Daten zu erfassen. Weitere Informationen zur Einrichtung finden Sie unter [Paid-Search-Erkennung](/help/admin/admin/paid-search-detection/paid-search-detection.md) im Administratorhandbuch.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Suchbegriff – Gebührenpflichtig** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

## Kampagnen – Kostenlose Keywords

Der Bericht zu kostenlosen Keywords zeigt die Leistung der einzelnen Suchbegriffe an, nachdem ein Besucher in einer Suchmaschine auf einen normalen Such-Link geklickt hat. Die Dimension **Suchbegriffe – Kostenlos** ist in Analysis Workspace verfügbar. Beachten Sie, dass bei nicht eingerichteter Paid-Search-Erkennung diese Dimension sowohl gebührenpflichtige als auch kostenlose Suchbegriffe erfasst.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Suchbegriff – Kostenlos** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

## Kostenanalyse

Dieser Bericht zeigt Daten zur Besuchs-, Kosten- und Umsatzleistung Ihrer gebührenpflichtigen Marketing-Kanäle an. Adobe bietet ein spezielles Produkt zur Bereitstellung von Einblicken: Adobe Advertising Cloud. Wenn Ihr Unternehmen an der Verwendung dieses Produkts interessiert ist, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens.
