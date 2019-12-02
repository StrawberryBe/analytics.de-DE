---
title: Zielgruppenberichte in Adobe Analytics
description: Erfahren Sie, wie Sie mit dem Analysis Workspace zielgruppenbasierte Berichte erstellen.
translation-type: tm+mt
source-git-commit: 6217430bf0ae9c0f9c6426e4bb2a8101257068e7

---


# Zielgruppenberichte

Zielgruppenberichte zeigen Informationen über die Typen von Personen an, die Ihre Site besuchen.

Auf dieser Seite wird davon ausgegangen, dass der Benutzer über grundlegende Kenntnisse in der Verwendung des Analysis Workspace verfügt. Siehe [Erstellen eines einfachen Berichts im Analysis Workspace für Google Analytics-Benutzer](create-report.md) , wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Aktive Benutzer

Aktive Benutzer zeigen die kumulative Anzahl der Benutzer Ihrer Site in den letzten 1, 7, 14 oder 28 Tagen an. Adobe verfügt zwar nicht über die exakte Berechnung, die in Google Analytics verwendet wird, Sie können jedoch die Metrik "Unique Visitors"verwenden, um eine deduplizierte Anzahl von Benutzern auf Ihrer Site basierend auf dem ausgewählten Datumsbereich anzuzeigen.

So erstellen Sie ein Liniendiagramm individueller Besucher:

1. Klicken Sie auf das Symbol Visualisierungen auf der linken Seite und ziehen Sie die Linienvisualisierung auf den Arbeitsbereich über der leeren Freiformtabelle.
2. Klicken Sie auf das Symbol Komponenten links und ziehen Sie dann die Metrik **Individuelle Besucher** in den kleineren Bereich mit der Bezeichnung 'Metrik hier ablegen'.
3. Wenn eine andere Granularität gewünscht wird, ziehen Sie den gewünschten Datumsbereich (z. B. **Tag**, **Woche**, **Monat** usw.) oben auf der vorhandenen Datendimensionsüberschrift.

Weitere Informationen zur Berechnung individueller Besucher durch Adobe finden Sie unter [Unique Visitors](/help/components/c-variables/c-metrics/metrics-unique-visitors.md) im Komponenten-Benutzerhandbuch.

## Lebenszeitwert

Der Lebenszeitwert ist eine Funktion, die eine zusätzliche spezielle Implementierung auf beiden Plattformen erfordert. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um diese Daten zu erhalten.

## Kohortenanalyse

Die Kohortenanalyse zeigt, wie oft dieselben Benutzer zu Ihrer Site zurückkehren.

So erstellen Sie eine Kohortentabelle:

1. Klicken Sie auf das Visualisierungssymbol links und ziehen Sie die Kohortentabellen-Visualisierung auf den Arbeitsbereich.
2. Klicken Sie auf das Symbol Komponenten auf der linken Seite und ziehen Sie dann die Metrik **Besuche** sowohl auf Aufnahmekriterien als auch auf Rückgabekriterien.
3. Klicken Sie auf Erstellen.

Weitere Informationen zu zusätzlichen Anpassungen der Kohortenvisualisierung finden Sie unter [Kohortenanalyse](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) im Benutzerhandbuch des Analysis Workspace.

## Zielgruppen

Der Zielgruppenbericht in Google Analytics erfordert die Einrichtung von Zielgruppen. Zielgruppen müssen auch über Adobe Audience Manager konfiguriert werden. Weitere Informationen finden Sie im Adobe Audience Manager-Benutzerhandbuch.

## Benutzer-Explorer

Der Bericht "Benutzer-Explorer"ermöglicht es einem Analysten, einzelne Besuche über anonymisierte IDs anzuzeigen. Adobe deckt die Backend-IDs nicht außerhalb von Data Feeds auf, bei denen es sich um Rohdatenexporte auf Trefferebene handelt.

* Wenn diese Daten in Analysis Workspace gewünscht werden, ist es möglich, mit einem Implementierungsberater zusammenzuarbeiten, um den Wert des anonymisierten Cookies für die eindeutige Kennung an eine eVar weiterzugeben. Beachten Sie, dass dies nur bei kleineren Implementierungen funktioniert, die aus weniger als 1 Million Unique Visitors pro Monat bestehen.
* Wenn diese Daten in Datenfeeds gewünscht werden, sind die verketteten Spalten `visid_high` und `visid_low` die gängigsten Methoden zur Identifizierung individueller Besucher. Weitere Informationen zu [Datenfeeds](/help/export/analytics-data-feed/data-feed-overview.md) finden Sie im Benutzerhandbuch zum Exportieren.

## Berichte zu Demografie und Interessen

Die demografischen Daten und Interessensdaten liefern Informationen über Alter, Geschlecht und Interessen der Site-Benutzer. Diese Daten werden von Google über ihre Site-übergreifenden Verfolgungsfähigkeiten erfasst.

Demografische Daten und Interessensdaten werden nicht automatisch von Adobe erfasst. Wenn Ihr Unternehmen diese Daten jedoch erhält, können Sie Kundenattribute verwenden, eine Funktion innerhalb der Adobe Experience Cloud-Plattform. Es ermöglicht die vollständige Kontrolle über die Organisation der Daten nach Attributen und ist nicht auf Demografie oder Interessen beschränkt.

Weitere Informationen finden Sie in der Hilfe zu Kundenattributen.

## Geo - Sprache

Der Bericht zur geografischen Sprache zeigt den Site-Traffic nach der Spracheinstellung im Browser des Besuchers an.

So erstellen Sie einen Sprachenbericht:

1. Suchen Sie im Menü "Komponenten"die Dimension " **Sprache** "und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen finden Sie unter [Sprachdimension](/help/components/c-variables/dimensionslist/reports-languages.md) im Komponenten-Benutzerhandbuch.

## Geo - Standort

Der Geo-Standortbericht bietet eine weltweite Kartenansicht, in der die Daten nach Ländern aufgeschlüsselt werden.

So erstellen Sie einen Geolocation-Bericht:

1. Klicken Sie auf das Symbol Visualisierungen auf der linken Seite und ziehen Sie die Imagemap-Visualisierung auf den Arbeitsbereich über der leeren Freiformtabelle.
2. Klicken Sie auf das Symbol Komponenten auf der linken Seite und ziehen Sie dann die Metrik **Unique Visitors** in den Bereich mit der Bezeichnung 'Metrik hinzufügen'.
3. Klicken Sie auf Erstellen.

Wenn die Tabelle zusätzlich zur Karte gewünscht wird:

1. Suchen Sie im Menü "Komponenten"die Dimension " **Länder** "und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen finden Sie unter [Geosegmentation](/help/components/c-variables/dimensionslist/reports-geosegmentation.md) -Dimensionen im Komponenten-Benutzerhandbuch.

## Verhalten - Neu im Vergleich zum Zurückkehren

Der neue vs. zurückkehrende Bericht bietet eine vereinfachte Ansicht der ersten Sitzungen (neue Besuche) im Vergleich zu nachfolgenden Sitzungen (wiederkehrende Besuche).

So erstellen Sie einen neuen oder einen Bericht über wiederkehrende Besuche:

1. Suchen Sie im Komponentenmenü das Segment **Erstbesuche** und ziehen Sie es in den großen Freiform-Tabellenbereich mit der Bezeichnung 'Dimension hier ablegen'. Beachten Sie, dass **Erstbesuche** ein Segment sind, während Workspace in der Regel Dimensionen zur Darstellung von Zeilen verwendet.
2. Suchen Sie das Segment " **Rückkehrende Besucher** "und ziehen Sie es auf die Kopfzeile der Segmentzeile. Dadurch wird das Segment als Dimension unterhalb der Erstbesuche hinzugefügt, was einen einfachen Vergleich ermöglicht.
3. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Wenn ein Liniendiagramm gewünscht wird:

1. Klicken Sie auf das Visualisierungssymbol links und ziehen Sie eine Linienvisualisierung auf den Arbeitsbereich über der Freiformtabelle
2. Verwenden Sie STRG+Klick (Windows) oder Cmd+Klick (Mac) für jede Zeile in der Freiform-Tabelle, um sie zu markieren. Dadurch können beide Trends in der Linienvisualisierung angezeigt werden.
3. Klicken Sie auf den kleinen runden farbigen Punkt in der oberen linken Ecke der Linienvisualisierung und dann auf das Kontrollkästchen Auswahl sperren.

## Verhalten - Häufigkeit und Aktualität

Der Häufigkeits- und Neuigkeitsbericht entspricht ungefähr der Dimension **Besuchsnummer** im Arbeitsbereich für Analysen.

1. Suchen Sie im Komponentenmenü die Dimension " **Besuchsnummer** "und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen finden Sie unter [Besuchsnummer](/help/components/c-variables/dimensionslist/reports-visitor-number.md) im Komponenten-Benutzerhandbuch.

## Verhalten - Interaktion

Der Einsatzbericht entspricht ungefähr der Dimension **Zeit pro Besuch - Zusammengefasst** .

1. Suchen Sie im Komponentenmenü die Dimension " **Zeit pro Besuch - Zusammengefasst** "und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen finden Sie in der Dimension " [Zeit pro Besuch](/help/components/c-variables/dimensionslist/reports-time-spent-per-visit.md) "im Komponenten-Benutzerhandbuch.

## Technologie - Browser und Betriebssystem

Es sind mehrere primäre Dimensionen im Browser- und OS-Bericht verfügbar.

* Die primäre Dimension " **Browser** "steht auch im Arbeitsbereich für Analysen als Dimension zur Verfügung.
* Die primäre Dimension **Betriebssystem** ist auch im Arbeitsbereich für Analysen als Dimension verfügbar.
* Die primäre Dimension **Bildschirmauflösung** ist im Arbeitsbereich für Analysen als Dimension für die **Bildschirmauflösung** verfügbar.
* Die primäre Dimension " **Bildschirmfarben** "ist im Arbeitsbereich für Analysen als **Farbtiefe** verfügbar.
* Die primäre Dimension " **Flash-Version** "steht in Adobe Analytics nicht zur Verfügung. Diese Daten können jedoch bei Bedarf von einer eVar erfasst werden.

1. Suchen Sie im Komponentenmenü die oben angegebene gewünschte Dimension und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen zu den jeweiligen Dimensionen finden Sie auf den folgenden Seiten im Komponenten-Benutzerhandbuch:

* [Browser](/help/components/c-variables/dimensionslist/reports-browsers.md)
* [Betriebssystem](/help/components/c-variables/dimensionslist/reports-operating-system.md)
* [Bildschirmauflösung](/help/components/c-variables/dimensionslist/reports-technology.md)
* [Farbtiefe](/help/components/c-variables/dimensionslist/reports-color-depth.md)

## Technologie - Netzwerk

Der Netzwerkbericht ist ungefähr gleich der Dimension **Domäne** .

1. Suchen Sie im Komponentenmenü die Dimension " **Domäne** "und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen finden Sie unter [Domänendimension](/help/components/c-variables/dimensionslist/reports-domains.md) im Komponenten-Benutzerhandbuch.

## Mobil - Übersicht

Der Übersichtsbericht für Mobilgeräte entspricht ungefähr der Dimension **"Mobilgerätetyp"** . Beachten Sie, dass der Wert "Sonstige"dem Desktop-Traffic entspricht.

1. Suchen Sie im Komponentenmenü die Dimension " **Mobilgerätetyp** "und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung "Dimension hier ablegen".
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen finden Sie unter Dimension " [Mobilgerätetyp](/help/components/c-variables/dimensionslist/reports-device-types.md) "im Benutzerhandbuch "Komponenten".

## Mobil - Geräte

Der Mobilgerätebericht entspricht ungefähr der Dimension **Mobilgerät** .

1. Suchen Sie im Komponentenmenü die Dimension **Mobilgerät** und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung 'Dimension hier ablegen'.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik " **Vorfälle** "in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Weitere Informationen finden Sie unter [Dimension "Mobilgerät](/help/components/c-variables/dimensionslist/reports-devices.md) "im Benutzerhandbuch "Komponenten".

## Benutzerspezifisch

Benutzerspezifische Berichte werden pro Implementierung definiert. Wenden Sie sich an den Analytics-Administrator und/oder Implementierungsberater Ihres Unternehmens, um diese Berichte zu interpretieren. Normalerweise unterhält ein Unternehmen ein [Lösungsdesigndokument](/help/implement/prepare/solution-design.md) , um benutzerdefinierte Variablenwerte und deren Füllung zu verfolgen.

## Benchmarking

Mithilfe von Benchmarking-Berichten können Sie sehen, wie die Facetten Ihrer Daten im Vergleich zum Branchendurchschnitt aussehen. Adobe gibt derzeit keine Benchmarking-Daten zwischen seinen Kunden frei.

## Benutzerfluss

Der Flussbericht ist auf beiden Plattformen verfügbar. So erstellen Sie einen Flussbericht:

1. Klicken Sie auf das Symbol Visualisierungen links und ziehen Sie eine Flussvisualisierung auf den Arbeitsbereich über der Freiformtabelle
2. Suchen Sie die Dimension " **Seiten** "und klicken Sie dann auf das Pfeilsymbol, um die Seitenwerte anzuzeigen. Dimensionswerte sind gelb.
3. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den Bereich mit der Bezeichnung "Dimension oder Element"in der Mitte
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.
