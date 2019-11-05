---
title: Konversionsberichte in Adobe Analytics
description: Erfahren Sie, wie Sie Konversionsberichte in Adobe Analytics verwenden.
translation-type: tm+mt
source-git-commit: 3ce18f3f222286aed08c81dd2c958dab7e443df3

---


# Konversionsberichte

Eine "Konversion"ist eine Aktion, die ein Besucher auf Ihrer Site durchführt und die direkt in die Schlüsselindikatoren Ihres Unternehmens übersetzt wird. Konversionsberichte zeigen Details zur Konvertierung durch Besucher an.

Auf dieser Seite wird davon ausgegangen, dass der Benutzer über grundlegende Kenntnisse in der Verwendung des Analysis Workspace verfügt. Siehe [Erstellen eines einfachen Berichts im Analysis Workspace für Google Analytics-Benutzer](create-report.md) , wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Zielberichte

Ziele bieten Google Analytics-Benutzern eine Möglichkeit, die Konvertierung einer Website zu definieren. Sie sind die Standardmethode zum Erstellen von Trichtern, umgekehrtem Verhaltensfluss, Multikanal-Trichter und Zuordnungen. Ziele in Google Analytics sind nicht rückwirkend und können nur auf der Admin-Seite eingerichtet werden. Darüber hinaus basieren sie nur auf einer Seite, einem Ereignis, einer Besuchszeit oder einer durchschnittlichen Anzahl von Seiten.

In Adobe Analytics ist das Konzept eines Ziels nicht erforderlich, da Metriken in jedem Kontext angewendet werden können. Solange Ihre Implementierung die Ereignisse berücksichtigt, die Sie verfolgen möchten, können Sie jeden Konversionsbericht anpassen und sofort Ergebnisse für historische Daten erhalten.

### Trichtervisualisierung

Der Trichtervisualisierungsbericht hilft Analysten, sich auf eine bestimmte Reihe von Schritten zu konzentrieren, die zur Konvertierung erforderlich sind. Vor dem Kauf muss beispielsweise ein Besucher auf einer E-Commerce-Site auf die Einkaufswagen-, Abrechnungs- und Versandseite, die Zahlungsseite und die Seite zur Überprüfung der Bestellung zugreifen.

In Analysis Workspace können diese Daten mithilfe der Fallout-Visualisierung angezeigt werden.

1. Klicken Sie auf das Visualisierungssymbol links und ziehen Sie eine Fallout-Visualisierung auf den Arbeitsbereich über der Freiformtabelle
2. Klicken Sie auf das Symbol Komponenten auf der linken Seite und suchen Sie dann die Dimension **Seiten** .
3. Klicken Sie auf das Pfeilsymbol neben der Seitendimension, um die Seitenwerte anzuzeigen. Dimensionswerte sind gelb.
4. Suchen Sie die gewünschte Seite, die als erster Touchpoint fungiert, und ziehen Sie sie in den Bereich mit der Bezeichnung "Touchpoint hinzufügen"in der Visualisierung.
5. Fügen Sie weitere gewünschte Touchpoints hinzu, indem Sie die Seitenwerte in die Visualisierung ziehen.

Die Fallout-Visualisierung ist nicht auf die Dimension "Seiten"beschränkt. Jede Dimension, Metrik oder jedes Segment kann verwendet werden, um Ihren Trichteranalysebericht an die Anforderungen Ihres Unternehmens anzupassen.

![Fallout-Visualisierung](/help/technotes/ga-to-aa/assets/fallout.png)

## E-Commerce-Berichte

E-Commerce-Berichte werden in der Regel von Sites verwendet, die Produkte oder Dienstleistungen verkaufen, um Bestellungen und Umsatz auf gekauften Artikeln zu messen. Diese Funktion ist in Adobe Analytics verfügbar und wird als Produktberichte bezeichnet.

Sowohl E-Commerce-Berichte in Google Analytics als auch Produktberichte in Adobe Analytics erfordern benutzerspezifische Implementierungsänderungen. Weitere Informationen finden Sie in der Dimension " [Produkte](/help/components/c-variables/dimensionslist/reports-products.md) "im Benutzerhandbuch "Komponenten".

## Berichte zu Multikanal-Trichter

Mehrkanaltrichterberichte bieten zusätzliche Marketingkanaldaten, die über das hinausgehen, was Akquise-Berichte bieten. Diese Berichte konzentrieren sich darauf, wie Besucher umrechnen, anstatt wie Besucher zu Ihrer Site gelangen.

> [!NOTE]
>
> Die Verwendung von Mehrkanal-Berichten in Adobe Analytics erfordert sowohl die Einrichtung von Marketingkanälen als auch eine benutzerdefinierte Implementierung, um die Produktvariable und das Kaufereignis aufzunehmen. Adobe empfiehlt die Zusammenarbeit mit einem Implementierungsberater, wenn diese Funktionen noch nicht für Ihre Report Suite konfiguriert sind.

### Mehrkanal - Unterstützte Konvertierungen

Unterstützte Konvertierungen zeigen, wie oft jeder Kanal eine Konvertierung unterstützt hat. Im Arbeitsbereich für Analysen kann die Metrik " **Bestellhilfen** "verwendet werden.

1. Suchen Sie im Menü Komponenten die Dimension **Marketingkanal** und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung 'Dimension hier ablegen'.
2. Ziehen Sie die Metrik " **Bestellhilfen** "auf die automatisch erstellte Metrik " **Vorfälle** ", um sie zu ersetzen. Zusätzliche Metriken können bei Bedarf in den Arbeitsbereich gezogen werden.

### Mehrkanal - Top-Umrechnungspfade

Der Bericht zu den Top-Konversionspfaden zeigt die wichtigsten Kanalpfade an, die ein Benutzer vor der Konvertierung verwendet. Der Arbeitsbereich für Analysen verwendet einen Flussbericht zur Visualisierung der Top-Konversionspfade.

1. Klicken Sie auf das Symbol "Bedienfelder"auf der linken Seite und ziehen Sie ein Bedienfeld "Zuordnung"über die Freiform-Tabelle.
2. Klicken Sie auf das Symbol Komponenten links, suchen Sie die Dimension **Marketingkanal** und ziehen Sie sie in das Feld Dimension hinzufügen.
3. Suchen Sie das gewünschte Konversionsereignis unter Metriken (z. B. Bestellungen) und ziehen Sie es in das Feld "Metrik hinzufügen". Beachten Sie, dass berechnete Metriken für das Fenster Zuordnung nicht unterstützt werden.
4. Klicken Sie auf Erstellen.
5. Suchen Sie im resultierenden Bericht die Kanalflussvisualisierung. Dieser Fluss zeigt die wichtigsten Pfade an, die ein Besucher vor einem Kauf aufgerufen hat.

Diese Flussvisualisierung ist interaktiv. Klicken Sie auf jeden Kanal, um den Fluss in beide Richtungen zu erweitern.

![Flussvisualisierung](/help/technotes/ga-to-aa/assets/flow.png)

### Mehrkanal - Zeitverzögerung

Der Zeitzonenbericht zeigt die Zeit in Tagen an, die ein Besucher auf Ihrer Site umgerechnet hat. Im Arbeitsbereich für Analysen stehen diese Daten mit der Dimension **Tage bis Erstkauf** zur Verfügung. Sie steht nur im Zusammenhang mit einem korrekt implementierten Kaufereignis zur Verfügung.

1. Suchen Sie im Menü "Komponenten"die Dimension " **Tage bis Erstkauf** "und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Adobe empfiehlt die Verwendung der **Bestellungen**-, **Einheiten**- oder **Umsatzmetriken** mit dieser Dimension.

Für andere Konversionstypen, einschließlich benutzerspezifischer Ereignisse, ist die Dimension " **Zeit vor Ereignis** "verfügbar. Er zeigt die Zeit in Minuten an, die ein Besucher brauchte, um das Ereignis während des Besuchs auszulösen.

1. Suchen Sie im Menü "Komponenten"die Dimension " **Zeit vor Ereignis** "und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Adobe empfiehlt, diese Dimension neben benutzerspezifischen Ereignissen oder Kaufereignissen zu verwenden.

### Mehrkanal - Pfadlänge

Der Pfadlängenbericht zeigt die Anzahl der Kanäle an, die vor einem Konversionsereignis berührt wurden. Im Analysis Workspace enthält das Fenster Zuordnung diese Daten in einer seiner Visualisierungen.

1. Klicken Sie auf das Symbol "Bedienfelder"links und ziehen Sie ein Bedienfeld "Zuordnung"über die Freiform-Tabelle
2. Klicken Sie auf das Symbol Komponenten links, suchen Sie die Dimension **Marketingkanal** und ziehen Sie sie in das Feld Dimension hinzufügen.
3. Suchen Sie das gewünschte Konversionsereignis unter Metriken (z. B. Bestellungen) und ziehen Sie es in das Feld "Metrik hinzufügen". Beachten Sie, dass berechnete Metriken für das Fenster Zuordnung nicht unterstützt werden.
4. Klicken Sie auf Erstellen.
5. Suchen Sie im resultierenden Bericht die "Touchpoints per Journey"-Visualisierung. Dieses Histogramm zeigt die Anzahl der Kanäle an, die ein Besucher vor einem Kauf aufgerufen hat.
