---
title: Panel „Verbrachte Zeit bei der Medienwiedergabe“
description: Verwendung und Interpretation des Panels „verbrachten Zeit bei der Medienwiedergabe“ in Analysis Workspace.
feature: Panels
role: User, Admin
exl-id: null
source-git-commit: 74ef44c4afba6d2dffb2b10fa473baee3be16a23
workflow-type: ht
source-wordcount: '981'
ht-degree: 100%

---

# Panel „Verbrachte Zeit bei der Medienwiedergabe“

Media Analytics-Kunden können die verbrachte Zeit bei der Medienwiedergabe analysieren, um zu verstehen, wo besonders viele gleichzeitige Aufrufe stattfanden oder wo es zu Abbrüchen kam. So erhalten sie wertvolle Einblicke in die Qualität von Inhalten und die Interaktion von Betrachtern, was bei der Fehlerbehebung und der Planung von Volumen oder Skalierung helfen kann.

In Analysis Workspace bezeichnet die verbrachte Zeit bei der Medienwiedergabe die Zeit, die mit der Anzeige Ihrer Medien-Streams zu einem bestimmten Zeitpunkt verbracht wurde. Sie beinhaltet auch Pausen, die Pufferung und die Zeit bis zum Start.

Das Panel „Verbrachte Zeit bei der Medienwiedergabe“ ermöglicht die Analyse der Medienwiedergabe im Zeitverlauf und bietet Details zu Spitzenzeiten, in denen besonders viele gleichzeitige Aufrufe stattfanden, sowie die Möglichkeit von Aufschlüsselungen und Vergleichen. Um auf das Panel „Verbrachte Zeit bei der Medienwiedergabe“ zuzugreifen, navigieren Sie zu einer Report Suite, während die Media Analytics-Komponenten aktiviert sind. Klicken Sie dann auf das Panel-Symbol ganz links und ziehen Sie das Panel in Ihr Analysis Workspace-Projekt.

Dieses Panel enthält auch neue Funktionen im Kalender, mit denen Sie weniger als 24 Stunden auswählen und anzeigen können. Sie können dies für das gesamte Panel tun oder aber Segmente mithilfe aufeinanderfolgender Zeiträume erstellen, damit Sie den Ein- und Ausstieg von Zuschauern in allen Programmen oder Programmabschnitten verfolgen können. Nachdem Sie mindestens zwei dieser Datumssegmente platziert haben, sehen Sie ein Optionsfeld für die Datumssequenzanzeige. Darin werden die Linien entweder mit einem gemeinsamen X-Achsen-Beginn überlagert dargestellt oder sie werden nacheinander mit ihrem jeweiligen X-Achsen-Beginn anzeigt.

## Panel-Eingaben {#Input}

Sie können das Panel „Verbrachte Zeit bei der Medienwiedergabe“ mithilfe der folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
|---|---|
| Datumsbereich der Bedienfelder | Der Datumsbereich des Panels ist standardmäßig „Heute“. Sie können ihn so verändern, dass Sie einen einzelnen Tag oder viele Monate auf einmal betrachten können.<br>Diese Visualisierung ist auf 1.440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Granularität | Die Standardeinstellung für die Granularität ist „Minute“.<br>Diese Visualisierung ist auf 1.440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Zusammenfassende Zahlen der Bedienfelder | Um Details zu Datum und Uhrzeit für die verbrachte Zeit bei der Medienwiedergabe anzuzeigen, steht eine zusammenfassende Zahl zur Verfügung. Das Maximum zeigt Details zu Spitzenzeiten von gleichzeitigen Aufrufen an. Das Minimum zeigt Details zum Tiefstand an. In der Summe wird die gesamte Wiedergabezeit für diese Auswahl dargestellt. Im Panel wird standardmäßig nur der maximale Wert angezeigt. Sie können dies jedoch ändern, sodass das Minimum, die Summe oder eine beliebige Kombination der drei Werte angegeben wird.<br>Wenn Sie Aufschlüsselungen verwenden, wird jeweils eine Zusammenfassungsnummer angezeigt. |
| Serienaufschlüsselung | Optional können Sie Ihre Visualisierung nach Segmenten, Dimensionen, Dimensionselementen oder Datumsbereichen unterteilen.<p>– Sie können bis zu 10 Zeilen auf einmal ansehen. Aufschlüsselungen sind auf eine einzelne Ebene beschränkt.</p><p>– Beim Ziehen einer Dimension werden die oberen Dimensionselemente automatisch anhand des im Panels ausgewählten Datumsbereichs ausgewählt.</p>– Ziehen Sie zum Vergleichen von Datumsbereichen zwei oder mehr Datumsbereiche in den Filter für die Aufschlüsselung der Serie. |
| Zeitformat | Sie können die Wiedergabedauer entweder in Stunden:Minutes:Sekunden (Standard) oder in Minuten anzeigen (in Ganzzahlen, auf 0,5 aufgerundet). |
| Anzeige der Datumsreihe | Wenn Sie mindestens zwei Datumsbereichssegmente als Serienaufschlüsselungen platziert haben, sehen Sie die Option zur Auswahl einer Überlagerung (Standard) oder einer Sequenz. Bei der Überlagerung werden die Linien mit einem gemeinsamen X-Achsen-Beginn gezeigt, sodass sie parallel laufen, während bei der Sequenz die Linien mit ihrem jeweiligen X-Achsen-Beginn dargestellt werden. Wenn die Daten aufeinanderfolgend sind (z. B. Segment 1 endet um 20:44 Uhr und Segment 2 startet um 20:45 Uhr), werden die Zeilen nacheinander dargestellt. |

### Standardansicht

![Standardansicht](assets/mpts_default_view.png)

## Panel-Ausgabe {#Output}

Das Panel „Verbrachte Zeit bei der Medienwiedergabe“ gibt ein Liniendiagramm und zusammenfassende Zahlen zurück, die Details zur maximalen Wiedergabedauer, minimalen Wiedergabedauer und/oder der Summe der Wiedergabedauer enthalten. Oben im Bedienfeld wird eine Zusammenfassungszeile angezeigt, die Sie an die ausgewählten Bedienfeldeinstellungen erinnert.

Sie können das Bedienfeld jederzeit bearbeiten oder erneut erstellen, indem Sie oben rechts auf den Stift zum Bearbeiten klicken.

Wenn Sie Serienaufschlüsselung ausgewählt haben, wird für jeden der folgenden Punkte eine Zeile im Liniendiagramm und eine Zusammenfassungsnummer angezeigt:

![Ausgabe der verbrachten Zeit bei der Medienwiedergabe](assets/mpts_outputs1.png)

### Datenquelle

Die einzige Metrik, die in diesem Panel verwendet werden kann, ist „Wiedergabedauer“.

| Metrik | Beschreibung |
|---|---|
| Wiedergabedauer | Summe der Stunden:minutes:Sekunden (oder Minuten) des Inhalts, der während der ausgewählten Granularität betrachtet wurde, einschließlich Pausen, Pufferung und der Zeit bis zum Start. |

## Häufig gestellte Fragen (FAQ) {#FAQ}

| Frage | Antwort |
|---|---|
| Wo ist die Freiformtabelle? Wie kann ich die Datenquelle anzeigen? | <p></p><p>Die Freiformtabelle ist in dieser Ansicht nicht verfügbar. Sie können die Datenquelle herunterladen, indem Sie mit der rechten Maustaste auf das Liniendiagramm klicken und die CSV-Datei herunterladen.</p> |
| <p>Warum hat sich meine Granularität verändert?</p> | <p>Diese Visualisierung ist auf 1.440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn die Kombination aus Datumsbereich und Granularität mehr als 1.440 Zeilen ergibt, wird die Granularität automatisch aktualisiert, um den vollständigen Datumsbereich zu erfassen.</p><p></p><p>Wenn Sie von einem größeren auf einen kleineren Datumsbereich wechseln, wird die Granularität auf das niedrigste zulässige Detail aktualisiert, sobald der Datumsbereich geändert wird. Um eine höhere Granularität zu sehen, bearbeiten Sie das Bedienfeld und erstellen Sie es erneut.</p> |
| <p></p><p>Wie vergleiche ich Videonamen, Segmente, Inhaltstypen usw.?</p> | <p>Um diese in einer einzigen Visualisierung zu vergleichen, ziehen Sie Segmente, Dimensionen oder bestimmte Dimensionselemente in den Filter für die Serienaufschlüsselung.</p><p></p><p>Die Ansicht ist auf 10 Aufschlüsselungen beschränkt. Um mehr als 10 ansehen zu können, müssen Sie mehrere Bedienfelder verwenden.</p> |
| Wie vergleiche ich Datumsbereiche? | Um Datumsbereiche in einer einzigen Visualisierung zu vergleichen, verwenden Sie die Serienaufschlüsselungen, indem Sie zwei oder mehr Datumsbereiche in das Panel ziehen. Diese Datumsbereiche setzen den Datumsbereich des Bedienfelds außer Kraft. |
| Wie ändere ich den Visualisierungstyp? | <p></p><p>Dieses Bedienfeld ermöglicht nur die Linienvisualisierung für die Zeitreihen.</p> |
| Kann ich die Anomalieerkennung ausführen? | <p></p><p>Nein. Die Anomalieerkennung ist für dieses Panel nicht verfügbar.</p> |
