---
title: Basisbericht in Analysis Workspace erstellen
description: Erfahren Sie, wie Sie einen einfachen Bericht in Analysis Workspace in einem Format erstellen, das auf Anwender ausgerichtet ist, die mit Drittanbieter-Tools wie Google Analytics vertraut sind.
exl-id: 513da3f1-ad24-4d5b-bc35-dbcd3694cbdf
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '854'
ht-degree: 100%

---

# Basisbericht in Analysis Workspace für GA-Anwender erstellen

Analysis Workspace (eine der Hauptfunktionen in Adobe Analytics) bietet Anwendern einen leistungsstarken Bereich, um Einblicke in erfasste Daten zu erhalten. Das Reporting in Adobe Analytics unterscheidet sich stark von Google Analytics:

* Mit der Berichtsstruktur in Google Analytics können Sie einen bestimmten Datentyp auswählen, z. B. Geostandort oder Verweis-Traffic. Die Plattform verwendet eine vorgefertigte Berichtansicht, die auf der erwarteten besten Methode zur Ansicht dieser Daten basiert.
* Die Berichtsstruktur in Analysis Workspace bietet eine leere Arbeitsfläche und mehr Flexibilität bei der Erfüllung exakter Berichtsanforderungen.

Da Analysis Workspace eher wie eine Arbeitsfläche als ein vorgefertigter Bericht funktioniert, müssen einfach nur die Berichte aus Google Analytics mit den richtigen Visualisierungen und Komponenten in Analysis Workspace nachgebildet werden.

## Schlüsselbegriffe in Workspace

* **Bedienfelder** sind die übergeordneten Bausteine von Workspace. In fast allen Szenarien wird ein Freiformbedienfeld verwendet.
* **Visualisierungen** bilden alle Freiformbedienfelder. Ihr Zweck besteht darin, Daten in verschiedenen Formaten darzustellen. Meistens handelt es sich bei diesem Format um eine Tabelle, aber manchmal kann es sich um Dinge wie ein Ring- oder ein Liniendiagramm handeln. Viele Berichte in Google Analytics entsprechen zwei Visualisierungen: einem Liniendiagramm und einer Freiformtabelle.
* **Komponenten** werden in einer Visualisierung platziert, um Daten zurückzugeben. Komponenten können auf viele verschiedene Arten gemischt werden, um Berichtsanforderungen zu erfüllen.
   * **Dimensionen** sind Variablenwerte, die normalerweise Text enthalten. Beispiele sind der Seitenname, der Referrer und das Land. Sie werden meist als Zeilen in einer Tabelle aufgeführt.
   * **Metriken** bezeichnen normalerweise ein Ereignis oder eine Konversion beliebiger Art. Beispiele sind häufig auftretende Ereignisse wie Seitenansichten oder etwas Wichtigeres wie ein Kauf oder eine Registrierung. Sie werden meist als Spalten in Tabellen angezeigt, um darzustellen, wie oft das Ereignis pro Dimension aufgetreten ist.
   * **Segmente** sind eine Untergruppe Ihrer Daten und verhalten sich ähnlich wie Segmente in Google Analytics. Mit ihnen können Sie benutzerspezifische Filter erstellen, um sich auf einen bestimmten Teil Ihrer Daten konzentrieren zu können.
   * **Datumsbereiche** bieten Ihnen die Möglichkeit, Daten nach dem Zeitpunkt eines Ereignisses zu organisieren. Sie sind das Fundament der Trend-Anzeige im Zeitverlauf und werden normalerweise mit einer Metrik gekoppelt.

## Basisbericht in Workspace erstellen

Erstellen Sie einen „Alle Seiten“-Bericht (ähnlich dem Bericht in Google Analytics), indem Sie die richtigen Komponenten auf eine Arbeitsfläche ziehen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
1. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
1. Klicken Sie in der oberen Navigationsleiste auf „Workspace“.
1. Klicken Sie auf die Schaltfläche „Neues Projekt erstellen“.
1. Stellen Sie im modalen Popup sicher, dass „Leeres Projekt“ ausgewählt ist, und klicken Sie dann auf „Erstellen“.
1. Links wird eine Liste mit Dimensionen, Metriken, Segmenten und Datumsbereichen angezeigt. Suchen Sie die Dimension „Seiten“ (orange markiert) und ziehen Sie sie auf die Arbeitsfläche mit der Angabe „Dimension hier ablegen“.
1. Es wird ein Bericht mit den wichtigsten Seiten für diesen Monat angezeigt. Analysis Workspace füllt den Bericht automatisch mit der Metrik [Vorfälle](/help/components/metrics/occurrences.md).
1. Eine Tabelle in Google Analytics enthält in der Regel sieben bis acht Metriken. Suchen Sie die Metrik „Absprungrate“ (grün markiert) und ziehen Sie sie neben die Kopfzeile der Metrik „Vorfälle“. Wenn Sie die Metrik „Absprungrate“ neben „Vorfälle“ ziehen, werden beide Metriken nebeneinander angezeigt.
1. Viele Metriken können nebeneinander platziert werden, indem Sie Metriken neben vorhandene Metrikkopfzeilen ziehen. Informationen zum Abrufen von Metriken, die normalerweise in Google Analytics verwendet werden, finden Sie unter [Häufig verwendete Metriken](common-metrics.md).

   ![Neue Metrik](/help/technotes/ga-to-aa/assets/new_metric.png)

## Mit einer vordefinierten Berichtsvorlage in Workspace beginnen

Erstellen Sie die Vorlage für Content-Verbrauch (ähnlich dem Bericht „Alle Seiten“ in Google Analytics), indem Sie auf eine Projektvorlage zugreifen.

1. Klicken Sie auf die Schaltfläche „Neues Projekt erstellen“.
1. Doppelklicken Sie auf das Symbol für Nutzung von Inhalten (Web) unter „Alle Vorlagen“.
1. Durchsuchen Sie alle vordefinierten Visualisierungen: Entrypage-Fluss, Tabelle der Top-Seiten, Exitpage-Fluss, Einstiegsbereichsfluss und Tabelle der Top-Einstiegsbereiche.

   ![Vorlagenauswahl](/help/technotes/ga-to-aa/assets/content_consumption_template.png)

## Mit dem Werkzeug experimentieren

Da Analysis Workspace ein Berichtswerkzeug ist, hat dies keine Auswirkungen auf die Datenerfassung. Komponenten wahllos in ein Projekt zu ziehen, um zu sehen, was funktioniert, hat keine weiteren Folgen. Ziehen Sie verschiedene Kombinationen von Dimensionen und Metriken in Ihr Workspace-Projekt, um zu sehen, welche Möglichkeiten Sie haben.

Wenn Sie versehentlich eine ungültige Komponente in Ihr Workspace-Projekt ziehen oder einen Schritt zurückgehen möchten, drücken Sie Strg+Z (Windows) oder Befehl+Z (Mac), um die letzte durchgeführte Aktion rückgängig zu machen. Sie können auch mit einem leeren Arbeitsbereich beginnen, indem Sie im Menü oben links auf *[!UICONTROL Projekt] > [!UICONTROL Neu]* klicken.

In Analysis Workspace finden sich in den Kontextmenüs, die sich über die rechte Maustaste aufrufen lassen, eine Menge nützlicher Funktionen. Die meisten Visualisierungen und Komponenten können mit der rechten Maustaste angeklickt werden, um eine detailliertere Analyse und Interaktion zu erhalten. Wenn Sie mit der rechten Maustaste auf Komponenten in Ihrem Arbeitsbereich klicken, sehen Sie, welche Optionen verfügbar sind.

## Zu verwendende Dimensionen und Metriken verstehen

Wenn Sie mit Analysis Workspace vertraut sind und einen bestimmten Bericht erstellen möchten, der normalerweise in Google Analytics angezeigt wird, suchen Sie den Bericht auf der entsprechenden Seite:

* [Echtzeitberichte](realtime-reports.md)
* [Zielgruppenberichte](audience-reports.md)
* [Akquiseberichte](acquisition-reports.md)
* [Verhaltensberichte](behavior-reports.md)
* [Konversionsberichte](conversions-reports.md)
