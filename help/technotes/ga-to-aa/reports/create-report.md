---
title: Erstellen eines einfachen Berichts im Analysis Workspace
description: Erfahren Sie, wie Sie einen einfachen Bericht in Analysis Workspace in einem Format erstellen, das auf Benutzer ausgerichtet ist, die mit Drittanbieter-Tools wie Google Analytics vertraut sind.
translation-type: tm+mt
source-git-commit: 099662d021c1919f0760e79154536cfd0e23e959

---


# Erstellen eines einfachen Berichts im Analysis Workspace für Google Analytics-Benutzer

Der Arbeitsbereich für Analysen (eine der Hauptfunktionen in Adobe Analytics) bietet einem Benutzer einen robusten Bereich, um Einblicke in erfasste Daten zu erhalten. Die Berichterstellung unterscheidet sich sehr von Google Analytics und Adobe Analytics:

* Mit der Berichtsstruktur in Google Analytics können Sie einen bestimmten Datentyp auswählen, z. B. Geolocation oder Verweisverkehr. Die Plattform verwendet eine vorgefertigte Berichtansicht, die auf der erwarteten besten Methode zur Ansicht dieser Daten basiert.
* Die Berichtsstruktur im Analysis Workspace bietet eine leere Arbeitsfläche und bietet mehr Flexibilität bei der Erfüllung exakter Berichtsanforderungen.

Da Analysis Workspace mehr wie eine Arbeitsfläche als vorgefertigte Berichte funktioniert, ist es einfach eine Frage der Erstellung von Berichten aus Google Analytics, die richtigen Visualisierungen und Komponenten zu verwenden.

## Schlüsselbegriffe, die in Workspace verwendet werden

* **Bedienfelder** sind die übergeordneten Bausteine von Workspace. In fast allen Szenarien wird ein Freiformbedienfeld verwendet.
* **Visualisierungen** bilden alle Freiformbedienfelder. Ihr Zweck besteht darin, Daten in verschiedenen Formaten darzustellen. Meistens handelt es sich bei diesem Format um eine Tabelle, aber manchmal kann es sich um Dinge wie einen Donut oder ein Liniendiagramm handeln. Viele Berichte in Google Analytics entsprechen zwei Visualisierungen: ein Liniendiagramm und eine Freiformtabelle.
* **Komponenten** werden in einer Visualisierung platziert, um Daten zurückzugeben. Komponenten können auf viele verschiedene Arten gemischt werden, um Berichtanforderungen zu erfüllen.
   * **Dimensionen** sind Variablenwerte, die normalerweise Text enthalten. Beispiele sind der Seitenname, die verweisende Stelle oder das geografische Land. Sie werden meist als Zeilen in einer Tabelle aufgeführt.
   * **Metriken** bezeichnen normalerweise ein Ereignis oder eine Konversion einer Sortierung. Beispiele sind häufig auftretende Ereignisse wie Seitenansichten oder etwas Wichtigeres wie ein Kauf oder eine Registrierung. Sie werden meist als Spalten in Tabellen angesehen, um anzuzeigen, wie oft das Ereignis pro Dimension aufgetreten ist.
   * **Segmente** sind eine Untergruppe Ihrer Daten und verhalten sich ähnlich wie Segmente in Google Analytics. Sie ermöglichen es Ihnen, benutzerspezifische Filter zu erstellen, sodass Sie sich auf einen bestimmten Teil Ihrer Daten konzentrieren können.
   * **Mit Datumsbereichen** können Sie Daten nach dem Zeitpunkt des Ereignisses organisieren. Sie sind das Rückgrat der Anzeige von Trends im Zeitverlauf und werden normalerweise mit einer Metrik gepaart.

## Erstellen eines einfachen Berichts in Workspace

Erstellen Sie einen Bericht &quot;Alle Seiten&quot;(ähnlich dem Bericht in Google Analytics), indem Sie die richtigen Komponenten auf eine Arbeitsfläche ziehen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
1. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
1. Klicken Sie in der oberen Navigationsleiste auf „Workspace“.
1. Klicken Sie auf die Schaltfläche „Neues Projekt erstellen“.
1. Stellen Sie im modalen Popup sicher, dass „Leeres Projekt“ ausgewählt ist, und klicken Sie dann auf „Erstellen“.
1. Links wird eine Liste mit Dimensionen, Metriken, Segmenten und Datumsbereichen angezeigt. Suchen Sie die Dimension &quot;Seiten&quot;(farbig orange) und ziehen Sie sie auf die Arbeitsfläche mit der Bezeichnung &quot;Dimension hier ablegen&quot;.
1. Ein Bericht mit den wichtigsten Seiten für diesen Monat ist abrufbar. Analysis Workspace automatically populates the report with the [Occurrences](/help/components/c-variables/c-metrics/metrics-occurrences.md) metric.
1. Eine Tabelle in Google Analytics enthält in der Regel 7-8 Metriken. Suchen Sie die Absprungratenmetrik (grün gefärbt) und ziehen Sie sie neben die Kopfzeile der Metrik &quot;Vorfälle&quot;. Wenn Sie die Metrik &quot;Absprungrate&quot;neben &quot;Vorfälle&quot;ziehen, werden beide Metriken nebeneinander angezeigt.
1. Viele Metriken können nebeneinander platziert werden, indem Sie Metriken neben vorhandene Metriküberschriften ziehen. Informationen zum Abrufen von Metriken, die normalerweise in Google Analytics verwendet werden, finden Sie unter [häufig verwendete Metriken](common-metrics.md) .

   ![Neue Metrik](/help/technotes/ga-to-aa/assets/new_metric.png)

## Beginnen Sie mit einer vordefinierten Berichtsvorlage in Workspace

Erstellen Sie die Vorlage &quot;Inhaltskonsum&quot;(ähnlich dem Bericht &quot;Alle Seiten&quot;in Google Analytics), indem Sie auf eine Projektvorlage zugreifen.

1. Klicken Sie auf die Schaltfläche „Neues Projekt erstellen“.
1. Doppelklicken Sie auf das Symbol &quot;Inhaltskonsum (Web)&quot;unter &quot;Alle Vorlagen&quot;.
1. Durchsuchen Sie alle vordefinierten Visualisierungen: Einstiegsseitenfluss, Tabelle der Top-Seiten, Ausstiegsseitenfluss, Einstiegsseitenfluss und Tabelle der Top-Site-Abschnitte.

   ![Vorlagenauswahl](/help/technotes/ga-to-aa/assets/content_consumption_template.png)

## Mit dem Werkzeug experimentieren

Da Analysis Workspace ein Berichtswerkzeug ist, hat dies keine Auswirkungen auf die Datenerfassung. Komponenten wahllos in ein Projekt zu ziehen, um zu sehen, was funktioniert, hat keine weiteren Folgen. Ziehen Sie verschiedene Kombinationen von Dimensionen und Metriken in Ihr Workspace-Projekt, um zu sehen, welche Möglichkeiten Sie haben.

Wenn Sie versehentlich eine ungültige Komponente in Ihr Workspace-Projekt ziehen oder einen Schritt zurückgehen möchten, drücken Sie Strg+Z (Windows) oder Befehl+Z (Mac), um die letzte durchgeführte Aktion rückgängig zu machen. You can also start with a clean slate by clicking *[!UICONTROL Project]>[!UICONTROL New]*in the upper left menu.

Adobe hat im Kontextmenü mit der rechten Maustaste eine Reihe von Funktionen in Analysis Workspace platziert. Die meisten Visualisierungen und Komponenten können mit der rechten Maustaste angeklickt werden, um eine detailliertere Analyse und Interaktion zu erhalten. Wenn Sie mit der rechten Maustaste auf Komponenten in Ihrem Arbeitsbereich klicken, sehen Sie, welche Optionen verfügbar sind.

## Zu verwendende Dimensionen und Metriken verstehen

Wenn Sie mit Analysis Workspace vertraut sind und einen bestimmten Bericht erstellen möchten, der normalerweise in Google Analytics angezeigt wird, suchen Sie den Bericht auf der entsprechenden Seite:

* [Echtzeitberichte](realtime-reports.md)
* [Zielgruppenberichte](audience-reports.md)
* [Akquise-Berichte](acquisition-reports.md)
* [Verhaltensberichte](behavior-reports.md)
* [Konversionsberichte](conversions-reports.md)
