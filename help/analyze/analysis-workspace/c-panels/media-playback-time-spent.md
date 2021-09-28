---
title: Bedienfeld "Besuchszeit für Medienwiedergabe"
description: Verwendung und Interpretation des Bedienfelds "Besuchszeit für Medienwiedergabe"in Analysis Workspace.
feature: Panels
role: User, Admin
exl-id: null
source-git-commit: 74ef44c4afba6d2dffb2b10fa473baee3be16a23
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 49%

---

# Bedienfeld &quot;Besuchszeit für Medienwiedergabe&quot;

Media Analytics-Kunden können die Wiedergabedauer analysieren, um zu verstehen, wo Spitzenzeiten von gleichzeitigen Vorgängen auftraten oder wo es zu Abbrüchen kam. So erhalten Sie wertvolle Einblicke in die Qualität von Inhalten und die Interaktion mit Betrachtern und können bei der Fehlerbehebung oder Planung von Volumen oder Skalierung helfen.

In Analysis Workspace bezeichnet die Wiedergabedauer die Zeit, die mit der Anzeige Ihrer Medien-Streams zu einem bestimmten Zeitpunkt verbracht wurde. Sie umfasst Pause, Pufferung und Startzeit.

Das Bedienfeld &quot;Besuchszeit für Medienwiedergabe&quot;ermöglicht die Analyse der Wiedergabe im Zeitverlauf mit Details zu Spitzenzeiten bei gleichzeitiger Wiedergabe und der Möglichkeit, diese aufzuschlüsseln und zu vergleichen. Um auf das Bedienfeld &quot;Besuchszeit für Medienwiedergabe&quot;zuzugreifen, navigieren Sie zu einer Report Suite mit aktivierten Media Analytics-Komponenten. Klicken Sie dann auf das Bedienfeldsymbol ganz links und ziehen Sie das Bedienfeld in Ihr Analysis Workspace-Projekt.

Dieses Bedienfeld enthält auch neue Funktionen im Kalender, mit denen Sie weniger als 24 Stunden auswählen und anzeigen können. Sie können dies für den gesamten Bereich tun oder Sie können Segmente mithilfe aufeinander folgender Zeiträume erstellen, damit Sie die Anmeldung/das Opt-in-Ereignis für die Zuschauer über Programme oder Programmabschnitte hinweg verfolgen können. Nachdem Sie mindestens zwei dieser Datumssegmente platziert haben, sehen Sie ein Optionsfeld für die Datumssequenzanzeige, das die Zeilen entweder mit einem gemeinsamen X-Achsen-Start überlagert oder sie nacheinander mit ihrem jeweiligen X-Achsen-Start anzeigt.

## Bedienfeldeingaben {#Input}

Sie können das Bedienfeld &quot;Besuchszeit für Medienwiedergabe&quot;mit den folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
|---|---|
| Datumsbereich der Bedienfelder | Der Datumsbereich des Bedienfelds ist standardmäßig „Heute“.  Sie können ihn so verändern, dass Sie einen einzelnen Tag oder viele Monate auf einmal betrachten können.<br>Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Granularität | Die Standardeinstellung für die Granularität ist „Minute“. <br>Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Zusammenfassende Zahlen der Bedienfelder | Um Datums- oder Uhrzeitdetails für die Wiedergabedauer anzuzeigen, ist eine Zusammenfassungsnummer verfügbar. Das Maximum zeigt Details zu Spitzenzeiten von gleichzeitigen Ansichten an. Das Minimum zeigt Details zum Tiefpunkt an. Summe addiert die Gesamtwiedergabedauer für die Auswahl. Der Bereich zeigt standardmäßig nur Maximum an. Sie können ihn jedoch ändern, um Minimum, Summe oder eine beliebige Kombination der drei anzuzeigen.<br>Wenn Sie Aufschlüsselungen verwenden, wird jeweils eine Zusammenfassungsnummer angezeigt. |
| Serienaufschlüsselung | Optional können Sie Ihre Visualisierung nach Segmenten, Dimensionen, Dimensionselementen oder Datumsbereichen unterteilen.<p>– Sie können bis zu 10 Zeilen auf einmal ansehen. Aufschlüsselungen sind auf eine einzelne Ebene beschränkt.</p><p>– Beim Ziehen einer Dimension werden die oberen Dimensionselemente automatisch anhand des im Bedienfelds ausgewählten Datumsbereichs ausgewählt.</p>– Ziehen Sie zum Vergleichen von Datumsbereichen zwei oder mehr Datumsbereiche in den Filter für die Aufschlüsselung der Serie. |
| Zeitformat | Sie können die Wiedergabedauer entweder in Stunden:Minutes:Sekunden (Standard) oder in Minuten anzeigen (in Ganzzahlen, auf 0,5 aufgerundet). |
| Anzeige der Datumsreihe | Wenn Sie mindestens zwei Datumsbereichssegmente als Serienaufschlüsselungen platziert haben, sehen Sie die Option zur Auswahl einer Überlagerung (Standard) oder einer sequenziellen Überlagerung. Die Überlagerung zeigt die Linien mit einem gemeinsamen X-Achsen-Start an, sodass sie parallel ausgeführt werden, während die Linien mit ihrem jeweiligen X-Achsen-Start sequenziell angezeigt werden. Wenn die Daten aufgerollt sind (z. B. Segment 1 um 20:44 Uhr und Segment 2 um 20:45 Uhr), werden die Zeilen nacheinander angezeigt. |

### Standardansicht

![Standardansicht](assets/mpts_default_view.png)

## Bedienfeldausgabe {#Output}

Das Bedienfeld &quot;Besuchszeit für Medienwiedergabe&quot;gibt ein Liniendiagramm und Zusammenfassungsnummern zurück, die Details zur maximalen, minimalen und/oder Summe der Wiedergabedauer enthalten. Oben im Bedienfeld wird eine Zusammenfassungszeile angezeigt, die Sie an die ausgewählten Bedienfeldeinstellungen erinnert.

Sie können das Bedienfeld jederzeit bearbeiten oder erneut erstellen, indem Sie oben rechts auf den Stift zum Bearbeiten klicken.

Wenn Sie Serienaufschlüsselung ausgewählt haben, wird für jeden der folgenden Punkte eine Zeile im Liniendiagramm und eine Zusammenfassungsnummer angezeigt:

![Ausgabe der Medienwiedergabe](assets/mpts_outputs1.png)

### Datenquelle

Die einzige Metrik, die in diesem Bedienfeld verwendet werden kann, ist die Wiedergabedauer.

| Metrik | Beschreibung |
|---|---|
| Besuchszeit für Wiedergabe | Gesamtstunden:minutes:Sekunden (oder Minuten) des Inhalts, der während der ausgewählten Granularität angezeigt wurde, einschließlich Pause, Pufferung und Startzeit. |

## Häufig gestellte Fragen (FAQ) {#FAQ}

| Frage | Antwort |
|---|---|
| Wo ist die Freiformtabelle? Wie kann ich die Datenquelle anzeigen? | <p></p><p>Die Freiformtabelle ist in dieser Ansicht nicht verfügbar. Sie können die Datenquelle herunterladen, indem Sie mit der rechten Maustaste auf das Liniendiagramm klicken und die CSV-Datei herunterladen.</p> |
| <p>Warum hat sich meine Granularität verändert?</p> | <p>Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch aktualisiert, um den vollständigen Datumsbereich aufzunehmen.</p><p></p><p>Wenn Sie von einem größeren auf einen kleineren Datumsbereich wechseln, wird die Granularität auf das niedrigste zulässige Detail aktualisiert, sobald der Datumsbereich geändert wird. Um eine höhere Granularität zu sehen, bearbeiten Sie das Bedienfeld und erstellen Sie es erneut.</p> |
| <p></p><p>Wie vergleiche ich Videonamen, Segmente, Inhaltstypen usw.?</p> | <p>Um diese in einer einzigen Visualisierung zu vergleichen, ziehen Sie Segmente, Dimensionen oder bestimmte Dimensionselemente in den Filter für die Serienaufschlüsselung.</p><p></p><p>Die Ansicht ist auf 10 Aufschlüsselungen beschränkt. Um mehr als 10 ansehen zu können, müssen Sie mehrere Bedienfelder verwenden.</p> |
| Wie vergleiche ich Datumsbereiche? | Um Datumsbereiche in einer einzigen Visualisierung zu vergleichen, verwenden Sie die Serienaufschlüsselungen, indem Sie zwei oder mehr Datumsbereiche ziehen. Diese Datumsbereiche setzen den Datumsbereich des Bedienfelds außer Kraft. |
| Wie ändere ich den Visualisierungstyp? | <p></p><p>Dieses Bedienfeld ermöglicht nur die Linienvisualisierung für die Zeitreihen.</p> |
| Kann ich die Anomalieerkennung ausführen? | <p></p><p>Nein. Die Anomalieerkennung ist für dieses Bedienfeld nicht verfügbar.</p> |
