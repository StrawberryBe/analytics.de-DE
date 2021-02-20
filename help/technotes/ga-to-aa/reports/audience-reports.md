---
title: Zielgruppenberichte in Adobe Analytics
description: Erfahren Sie, wie Sie mit Analysis Workspace zielgruppenbasierte Berichte erstellen.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 97%

---


# Zielgruppenberichte

Zielgruppenberichte zeigen Informationen über die Typen von Personen an, die Ihre Site besuchen.

Auf dieser Seite wird davon ausgegangen, dass der Anwender über grundlegende Kenntnisse in der Verwendung von Analysis Workspace verfügt. Siehe [Basisbericht in Analysis Workspace für GA-Anwender erstellen](create-report.md), wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Aktive Nutzer

„Aktive Nutzer“ zeigt die kumulative Anzahl der Anwender Ihrer Site in den letzten 1, 7, 14 oder 28 Tagen an. Adobe verfügt zwar nicht über die exakte Berechnung, die in Google Analytics verwendet wird, Sie können jedoch die Metrik „Unique Visitors“ verwenden, um eine deduplizierte Anzahl von Anwendern auf Ihrer Site für den ausgewählten Datumsbereich anzuzeigen.

So erstellen Sie einen Kantengraphen für Unique Visitors:

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie die Linienvisualisierung auf den Arbeitsbereich über der leeren Freiformtabelle.
2. Klicken Sie links auf das Symbol „Komponenten“ und ziehen Sie dann die Metrik **Unique Visitors** in den kleineren Bereich namens „Metrik hier ablegen“.
3. Wenn eine andere Granularität gewünscht wird, ziehen Sie den gewünschten Datumsbereich (z. B. **Tag**, **Woche**, **Monat** usw.) oberhalb der vorhandenen Datendimensionskopfzeile.

Weitere Informationen zur Berechnung von Unique Visitors durch Adobe finden Sie unter [Unique Visitors](/help/components/metrics/unique-visitors.md) im Benutzerhandbuch zu Komponenten.

## Lebenszeitwert

Der Lebenszeitwert ist eine Funktion, die eine zusätzliche spezielle Implementierung auf beiden Plattformen erfordert. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um diese Daten zu erhalten.

## Kohortenanalyse

Die Kohortenanalyse zeigt, wie oft dieselben Anwender zu Ihrer Site zurückkehren.

So erstellen Sie eine Kohortentabelle:

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie Visualisierung „Kohortentabelle“ in den Arbeitsbereich.
2. Klicken Sie links auf das Symbol „Komponenten“ und ziehen Sie dann die Metrik **Besuche** sowohl auf die Aufnahme- als auch die Rückgabekriterien.
3. Klicken Sie auf Erstellen.

Weitere Informationen zu zusätzlichen Anpassungen der Kohortenvisualisierung finden Sie unter [Kohortenanalyse](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) im Benutzerhandbuch zu Analysis Workspace.

## Zielgruppen

Der Zielgruppenbericht in Google Analytics erfordert die Einrichtung von Zielgruppen. Zielgruppen müssen auch in Adobe Audience Manager konfiguriert werden. Weitere Informationen finden Sie im Adobe Audience Manager-Benutzerhandbuch.

## Nutzer-Explorer

Der Nutzer-Explorer-Bericht ermöglicht es Analysten, einzelne Besuche über anonymisierte IDs anzuzeigen. Adobe deckt nicht die Backend-IDs außerhalb der Daten-Feeds auf, bei denen es sich um Rohdatenexporte auf Trefferebene handelt.

* Wenn diese Daten in Analysis Workspace gewünscht werden, ist es möglich, mit einem Implementierungsberater zusammenzuarbeiten, um den Wert des anonymisierten Cookies für die eindeutige Kennung an eine eVar zu übergeben. Beachten Sie, dass dies nur bei kleineren Implementierungen funktioniert, die weniger als eine Million Unique Visitors pro Monat umfassen.
* Wenn diese Daten in Daten-Feeds gewünscht werden, sind die verketteten Spalten `visid_high` und `visid_low` die gängigsten Methoden zur Identifizierung von Unique Visitors. Weitere Informationen zu [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) finden Sie im Benutzerhandbuch zu Exporten.

## Demografie- und Interessenberichte

Demografie- und Interessendaten liefern Informationen über Alter, Geschlecht und Interessen der Site-Anwender. Diese Daten werden von Google über Site-übergreifende Tracking-Funktionen erfasst.

Demografie- und Interessensdaten werden von Adobe nicht automatisch erfasst. Wenn Ihr Unternehmen diese Daten jedoch erhält, können Sie hierfür Kundenattribute verwenden, eine Funktion innerhalb der Adobe Experience Cloud-Plattform. Sie ermöglicht die vollständige Kontrolle über die Organisation der Daten nach Attributen und ist nicht auf Demografie oder Interessen beschränkt.

Weitere Informationen finden Sie in der Hilfe zu Kundenattributen.

## Geografie – Sprache

Der Geografie-Sprachenbericht zeigt den Site-Traffic aufgeschlüsselt nach Spracheinstellung im Browser des Besuchers an.

So erstellen Sie einen Sprachenbericht:

1. Suchen Sie im Menü „Komponenten“ die Dimension **Sprache** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen finden Sie im Abschnitt zur Dimension [Sprache](/help/components/dimensions/language.md) im Benutzerhandbuch zu Komponenten.

## Geografie – Standort

Der Geografie-Standortbericht bietet eine weltweite Kartenansicht, in der die Daten nach Ländern aufgeschlüsselt werden.

So erstellen Sie einen Geografie-Standortbericht:

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie die Kartenvisualisierung auf den Arbeitsbereich über der leeren Freiformtabelle.
2. Klicken Sie links auf das Symbol „Komponenten“ und ziehen Sie dann die Metrik **Unique Visitors** in den Bereich namens „Metrik hinzufügen“.
3. Klicken Sie auf Erstellen.

Wenn die Tabelle zusätzlich zur Karte gewünscht wird:

1. Suchen Sie im Menü „Komponenten“ die Dimension **Länder** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen finden Sie in den Dimensionen [Länder](/help/components/dimensions/countries.md) im Komponenten-Benutzerhandbuch.

## Verhalten – Neu und wiederkehrend

Der Bericht zum Vergleich neuer und wiederkehrender Besucher bietet eine vereinfachte Ansicht der ersten Sitzungen (neue Besuche) im Vergleich zu nachfolgenden Sitzungen (erneute Besuche).

So erstellen Sie einen Bericht zum Vergleich neuer und wiederkehrender Besucher:

1. Suchen Sie im Menü „Komponenten“ das Segment **Erstbesuche** und ziehen Sie es in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“. Beachten Sie, dass **Erstbesuche** ein Segment ist, während Workspace in der Regel Dimensionen zur Darstellung von Zeilen verwendet.
2. Suchen Sie das Segment **Erneute Besuche** und ziehen Sie es auf die Kopfzeile der Segmentzeile. Dadurch wird das Segment als Dimension unterhalb der Erstbesuche hinzugefügt, was einen einfachen Vergleich ermöglicht.
3. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Wenn auch ein Kantengraph gewünscht wird:

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie die Linienvisualisierung auf den Arbeitsbereich über der Freiformtabelle.
2. Halten Sie die Strg- (Windows) oder Befehlstaste (Mac) gedrückt und klicken Sie auf jede Zeile in der Freiformtabelle, um sie zu markieren. Dadurch können beide Trends in der Linienvisualisierung angezeigt werden.
3. Klicken Sie auf den kleinen runden farbigen Punkt in der oberen linken Ecke der Linienvisualisierung und dann auf das Kontrollkästchen „Auswahl sperren“.

## Verhalten – Häufigkeit und Recency

Der Bericht „Häufigkeit und Recency“ entspricht ungefähr der Dimension **Besuchsnummer** in Analysis Workspace.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Besuchsnummer** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen finden Sie im Abschnitt zur Dimension [Besuchsnummer](/help/components/dimensions/visit-number.md) im Benutzerhandbuch zu Komponenten.

## Verhalten – Interaktionen

Der Interaktionsbericht entspricht ungefähr der Dimension **Zeit pro Besuch – Zusammengefasst**.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Zeit pro Besuch – Zusammengefasst** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen finden Sie im Abschnitt zur Dimension [Zeit pro Besuch](/help/components/dimensions/time-spent-per-visit.md) im Benutzerhandbuch zu Komponenten.

## Technologie – Browser und Betriebssystem

Es sind mehrere primäre Dimensionen im Browser- und Betriebssystem-Bericht verfügbar.

* Die primäre Dimension **Browser** steht auch in Analysis Workspace als Dimension zur Verfügung.
* Die primäre Dimension **Betriebssystem** ist ebenfalls in Analysis Workspace als Dimension verfügbar.
* Die primäre Dimension **Bildschirmauflösung** ist in Analysis Workspace als **Bildschirmauflösung** verfügbar.
* Die primäre Dimension **Bildschirmfarben** ist in Analysis Workspace als **Farbtiefe** verfügbar.
* Die primäre Dimension **Flash-Version** steht in Adobe Analytics nicht zur Verfügung. Diese Daten können jedoch bei Bedarf von einer eVar erfasst werden.

1. Suchen Sie im Menü „Komponenten“ die oben angegebene gewünschte Dimension und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen zu den jeweiligen Dimensionen finden Sie auf den folgenden Seiten im Benutzerhandbuch zu Komponenten:

* [Browser](/help/components/dimensions/browser.md)
* [Betriebssystem](/help/components/dimensions/operating-systems.md)
* [Bildschirmauflösung](/help/components/dimensions/monitor-resolution.md)
* [Farbtiefe](/help/components/dimensions/color-depth.md)

## Technologie – Netzwerk

Der Netzwerkbericht ähnelt der Dimension **Domäne**.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Domäne** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen finden Sie im Abschnitt zur Dimension [Domäne](/help/components/dimensions/domain.md) im Benutzerhandbuch zu Komponenten.

## Mobil – Übersicht

Der Übersichtsbericht für Mobilgeräte entspricht ungefähr der Dimension **Mobilgerätetyp**. Beachten Sie, dass der Wert „Sonstige“ dem Desktop-Traffic entspricht.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Mobilgerätetyp** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen finden Sie in der Dimension [Mobilgerätetyp](/help/components/dimensions/mobile-dimensions.md) im Komponenten-Benutzerhandbuch.

## Mobil – Geräte

Der Mobilgerätebericht entspricht ungefähr der Dimension **Mobilgerät**.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Mobilgerät** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Weitere Informationen finden Sie in der Dimension [Mobilgerät](/help/components/dimensions/mobile-dimensions.md) im Komponenten-Benutzerhandbuch.

## Benutzerspezifisch

Benutzerspezifische Berichte werden pro Implementierung definiert. Wenden Sie sich an den Analytics-Administrator und/oder Implementierungsberater Ihres Unternehmens, um diese Berichte zu interpretieren. Normalerweise pflegt ein Unternehmen ein [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md), um benutzerspezifische Variablenwerte und deren Füllung zu verfolgen.

## Benchmarking

Mithilfe von Benchmarking-Berichten können Sie sehen, wie die verschiedenen Facetten Ihrer Daten im Vergleich zum Branchendurchschnitt dastehen. Adobe gibt derzeit keine Benchmarking-Daten zwischen seinen Kunden frei.

## Nutzerfluss

Der Flussbericht ist auf beiden Plattformen verfügbar. So erstellen Sie einen Flussbericht:

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie die Flussvisualisierung auf den Arbeitsbereich über der Freiformtabelle.
2. Suchen Sie die Dimension **Seiten** und klicken Sie dann auf das Pfeilsymbol, um die Seitenwerte anzuzeigen. Dimensionen sind gelb gefärbt.
3. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den mittigen Bereich namens „Dimension oder Element“.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.
