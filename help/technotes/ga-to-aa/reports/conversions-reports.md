---
title: Konversionsberichte in Adobe Analytics
description: Erfahren Sie, wie Sie Konversionsberichte in Adobe Analytics verwenden.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 99%

---


# Konversionsberichte

Eine Konversion ist eine Aktion, die ein Besucher auf Ihrer Site durchführt und die direkt in die Schlüsselindikatoren Ihres Unternehmens übersetzt wird. Konversionsberichte zeigen Details dazu an, wie die Konversion der Besucher stattfindet.

Auf dieser Seite wird davon ausgegangen, dass der Anwender über grundlegende Kenntnisse in der Verwendung von Analysis Workspace verfügt. Siehe [Basisbericht in Analysis Workspace für GA-Anwender erstellen](create-report.md), wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Zielberichte

Zielvorhaben bieten Google Analytics-Anwendern eine Möglichkeit, die Konversion einer Website zu definieren. Sie sind die Standardmethode zum Erstellen von Trichtern, umgekehrtem Verhaltensfluss, Multi-Channel-Trichtern und Attribution. Zielvorhaben in Google Analytics gelten nicht rückwirkend und können nur auf der Admin-Seite eingerichtet werden. Darüber hinaus basieren sie nur auf einer Seite, einem Ereignis, einer Besuchszeit oder einer durchschnittlichen Anzahl von Seiten.

In Adobe Analytics ist das Konzept eines Ziels nicht erforderlich, da Metriken in jedem Kontext angewendet werden können. Solange Ihre Implementierung die Ereignisse berücksichtigt, die Sie verfolgen möchten, können Sie jeden Konversionsbericht anpassen und sofort Ergebnisse für Verlaufsdaten erhalten.

### Trichtervisualisierung

Der Trichter-Visualisierungsbericht hilft Analysten, sich auf eine bestimmte Reihe von Schritten zu konzentrieren, die zur Konversion erforderlich sind. Um auf einer E-Commerce-Site einen Kauf zu tätigen, müssen Besucher beispielsweise erst die Seiten für den Einkaufswagen, für Abrechnung und Versand, Zahlung sowie für die Bestellübersicht durchlaufen.

In Analysis Workspace können diese Daten mithilfe der Fallout-Visualisierung angezeigt werden.

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie die Fallout-Visualisierung auf den Arbeitsbereich über der Freiformtabelle.
2. Klicken Sie auf das Symbol „Komponenten“ auf der linken Seite und suchen Sie dann die Dimension **Seiten**.
3. Klicken Sie auf das Pfeilsymbol neben der Dimension „Seiten“, um die Seitenwerte anzuzeigen. Dimensionen sind gelb gefärbt.
4. Suchen Sie die gewünschte Seite, die als erster Touchpoint fungiert, und ziehen Sie sie in den Bereich „Touchpoint hinzufügen“ in der Visualisierung.
5. Fügen Sie weitere gewünschte Touchpoints hinzu, indem Sie die Seitenwerte in die Visualisierung ziehen.

Die Fallout-Visualisierung ist nicht auf die Dimension „Seiten“ beschränkt. Jede Dimension, Metrik und jedes Segment kann verwendet werden, um Ihren Fallout-bericht an die Anforderungen Ihres Unternehmens anzupassen.

![Fallout-Visualisierung](/help/technotes/ga-to-aa/assets/fallout.png)

## E-Commerce-Berichte

E-Commerce-Berichte werden in der Regel von Sites verwendet, die Produkte oder Services anbieten, um Bestellungen und den Umsatz durch gekaufte Artikel zu messen. Diese Funktion ist in Adobe Analytics verfügbar und wird als „Produktberichte“ bezeichnet.

Sowohl E-Commerce-Berichte in Google Analytics als auch Produktberichte in Adobe Analytics erfordern benutzerspezifische Implementierungsänderungen. Weitere Informationen finden Sie im Abschnitt zur Dimension [Produkte](/help/components/dimensions/product.md) im Benutzerhandbuch zu Komponenten.

## Multi-Channel-Trichterberichte

Multi-Channel-Trichterberichte bieten zusätzliche Marketing-Kanaldaten, die über das hinausgehen, was Akquiseberichte bieten. Diese Berichte konzentrieren sich auf die Konversion der Besucher statt darauf, wie Besucher zu Ihrer Site gelangen.

>[!NOTE]
>
> Die Verwendung von Multi-Channel-Berichten in Adobe Analytics erfordert sowohl die Einrichtung von Marketing-Kanälen als auch eine benutzerspezifische Implementierung, um die Produktvariable und das Kaufereignis aufzunehmen. Adobe empfiehlt die Zusammenarbeit mit einem Implementierungsberater, wenn diese Funktionen noch nicht für Ihre Report Suite konfiguriert sind.

### Multi-Channel – Vorbereitete Conversions

„Vorbereitete Conversions“ zeigt, wie oft jeder Kanal eine Konversion unterstützt hat. In Analysis Workspace kann hierfür die Metrik **Bestellhilfen** verwendet werden.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Marketing-Kanal** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die Metrik **Bestellhilfen** auf die automatisch erstellte Metrik **Vorfälle**, um sie zu ersetzen. Zusätzliche Metriken können bei Bedarf in den Arbeitsbereich gezogen werden.

### Multi-Channel – Top-Conversion-Pfade

Der Bericht zu den Top-Konversionspfaden zeigt die wichtigsten Kanalpfade an, die ein Anwender vor der Konversion verwendet. Analysis Workspace verwendet einen Flussbericht zur Visualisierung der Top-Konversionspfade.

1. Klicken Sie auf das Symbol „Bedienfelder“ auf der linken Seite und ziehen Sie ein Bedienfeld „Attribution“ über die Freiformtabelle.
2. Klicken Sie links auf das Symbol „Komponenten“, suchen Sie die Dimension **Marketing-Kanal** und ziehen Sie sie in das Feld „Dimension hinzufügen“.
3. Suchen Sie das gewünschte Konversionsereignis unter Metriken (z. B. Bestellungen) und ziehen Sie es in das Feld „Metrik hinzufügen“. Beachten Sie, dass berechnete Metriken für das Fenster „Attribution“ nicht unterstützt werden.
4. Klicken Sie auf Erstellen.
5. Suchen Sie im resultierenden Bericht die Visualisierung „Kanalfluss“. Dieser Fluss zeigt die wichtigsten Pfade an, die ein Besucher vor einem Kauf aufgerufen hat.

Diese Flussvisualisierung ist interaktiv. Klicken Sie auf jeden Kanal, um den Fluss in beide Richtungen zu erweitern.

![Flussvisualisierung](/help/technotes/ga-to-aa/assets/flow.png)

### Multi-Channel – Zeitintervall

Der Zeitintervallbericht zeigt die Zeit in Tagen an, die ein Besucher auf Ihrer Site für die Konversion benötigt hat. In Analysis Workspace stehen diese Daten mit der Dimension **Tage bis Erstkauf** zur Verfügung. Sie steht nur im Zusammenhang mit einem korrekt implementierten Kaufereignis zur Verfügung.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Tage bis Erstkauf** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Adobe empfiehlt die Verwendung der Metriken **Bestellungen**, **Einheiten** oder **Umsatz** mit dieser Dimension.

Für andere Konversionstypen, einschließlich benutzerspezifischer Ereignisse, ist die Dimension **Zeit vor Ereignis** verfügbar. Sie zeigt die Zeit in Minuten an, die ein Besucher brauchte, um das Ereignis während des Besuchs auszulösen.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Zeit vor Ereignis** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Adobe empfiehlt, diese Dimension neben benutzerspezifischen Ereignissen oder Kaufereignissen zu verwenden.

### Multi-Channel – Pfadlänge

Der Pfadlängenbericht zeigt die Anzahl der Kanäle an, die vor einem Konversionsereignis genutzt wurden. In Analysis Workspace enthält das Fenster „Attribution“ diese Daten in einer seiner Visualisierungen.

1. Klicken Sie auf das Symbol „Bedienfelder“ auf der linken Seite und ziehen Sie ein Bedienfeld „Attribution“ über die Freiformtabelle.
2. Klicken Sie links auf das Symbol „Komponenten“, suchen Sie die Dimension **Marketing-Kanal** und ziehen Sie sie in das Feld „Dimension hinzufügen“.
3. Suchen Sie das gewünschte Konversionsereignis unter Metriken (z. B. Bestellungen) und ziehen Sie es in das Feld „Metrik hinzufügen“. Beachten Sie, dass berechnete Metriken für das Fenster „Attribution“ nicht unterstützt werden.
4. Klicken Sie auf Erstellen.
5. Suchen Sie im resultierenden Bericht die Visualisierung „Touchpoints pro Journey“. Dieses Histogramm zeigt die Anzahl der Kanäle an, die ein Besucher vor einem Kauf genutzt hat.
