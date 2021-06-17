---
title: Bedienfeld „Gleichzeitige Medienbetrachter“
description: Verwendung und Interpretation des Bedienfelds „Gleichzeitige Medienbetrachter“ in Analysis Workspace.
feature: Bedienfelder
role: Business Practitioner, Administrator
exl-id: 29575b51-e319-4156-9834-aa0b671afb31
source-git-commit: 73161e10a2f70cd0e874d2c1de6d4f418b25aefb
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 100%

---

# Bedienfeld „Gleichzeitige Medienbetrachter“

Media Analytics-Kunden können gleichzeitige Betrachter analysieren, um zu verstehen, wo Spitzenzeiten mit gleichzeitigen Ansichten auftraten oder wo es zu Abbrüchen kam. So erhalten sie wertvolle Einblicke in die Qualität von Inhalten und die Interaktion mit Betrachtern, die bei der Fehlerbehebung, Planung von Volumen oder Skalierung helfen können.

In Analysis Workspace bezeichnet der Begriff „Gleichzeitige Betrachter“ die Anzahl der Unique Visitors, die sich Ihre Medien-Streams unabhängig von der Anzahl der Sitzungen zu einem bestimmten Zeitpunkt ansehen.

Das Bedienfeld „Gleichzeitige Medienbetrachter“ ermöglicht die Analyse von gleichzeitigen Betrachtern im Zeitverlauf mit Details zu Spitzenzeiten des gleichzeitigen Betrachtens und der Möglichkeit, Unterteilungen und Vergleiche vorzunehmen. Um auf das Bedienfeld „Gleichzeitige Medienbetrachter“ zuzugreifen, navigieren Sie zu einer Report Suite mit aktivierten Media Analytics-Komponenten. Klicken Sie dann auf das Bedienfeldsymbol ganz links und ziehen Sie das Bedienfeld in Ihr Analysis Workspace-Projekt.

## Bedienfeldeingaben {#Input}

Sie können das Bedienfeld „Gleichzeitige Medienbetrachter“ mithilfe der folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
|---|---|
| Datumsbereich der Bedienfelder | Der Datumsbereich des Bedienfelds ist standardmäßig „Heute“.  Sie können ihn so verändern, dass Sie einen einzelnen Tag oder viele Monate auf einmal betrachten können. <br> <br>Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene).  Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Granularität | Die Standardeinstellung für die Granularität ist „Minute“. <br> <br>Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene).  Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Zusammenfassende Zahlen der Bedienfelder | Um Details zu Datum und Uhrzeit für gleichzeitige Betrachter anzuzeigen, steht eine Zusammenfassungsnummer zur Verfügung. Das Maximum zeigt Details zu Spitzenzeiten von gleichzeitigen Ansichten an. Das Minimum zeigt Details zum Tiefpunkt an.  Die Standardeinstellung im Bedienfeld zeigt nur das Maximum an, Sie können diese Einstellung jedoch ändern, um nur das Minimum oder sowohl Maximum als auch Minimum anzuzeigen.<br><br>Wenn Sie Aufschlüsselungen verwenden, wird jeweils eine Zusammenfassungsnummer angezeigt. |
| Serienaufschlüsselung | Optional können Sie Ihre Visualisierung nach Segmenten, Dimensionen, Dimensionselementen oder Datumsbereichen unterteilen. <br><br>– Sie können bis zu 10 Zeilen auf einmal ansehen. Aufschlüsselungen sind auf eine einzelne Ebene beschränkt.<br><br>– Beim Ziehen einer Dimension werden die oberen Dimensionselemente automatisch anhand des im Bedienfelds ausgewählten Datumsbereichs ausgewählt.<br><br>– Ziehen Sie zum Vergleichen von Datumsbereichen zwei oder mehr Datumsbereiche in den Filter für die Aufschlüsselung der Serie. |

### Standardansicht

![Standardansicht](assets/concurrent-viewers-default.png)


### Serienaufschlüsselungsansicht

![Serienaufschlüsselungsansicht](assets/concurrent-viewers-series-breakdown.png)

## Bedienfeldausgabe {#Output}

Das Bedienfeld „Gleichzeitige Medienbetrachter“ gibt ein Liniendiagramm und Zusammenfassungsnummern zurück, die Details zu maximalen und/oder minimalen gleichzeitigen Betrachtern enthalten.  Oben im Bedienfeld wird eine Zusammenfassungszeile angezeigt, die Sie an die ausgewählten Bedienfeldeinstellungen erinnert.

Sie können das Bedienfeld jederzeit bearbeiten oder erneut erstellen, indem Sie oben rechts auf den Stift zum Bearbeiten klicken.

Wenn Sie Serienaufschlüsselung ausgewählt haben, wird für jeden der folgenden Punkte eine Zeile im Liniendiagramm und eine Zusammenfassungsnummer angezeigt:

![Output von gleichzeitigen Betrachtern](assets/concurrent-viewers-output.png)

### Datenquelle

Die einzige Metrik, die in diesem Bedienfeld verwendet werden kann, ist „Gleichzeitige Betrachter“:

| Metrik | Beschreibung |
|---|---|
| Gleichzeitige Betrachter | Anzahl der Unique Visitors, die Ihre(n) Medien-Stream(s) zu einem bestimmten Zeitpunkt angesehen haben, unabhängig von der Anzahl der Sitzungen.<br><br>Dies unterscheidet sich vom Bericht „Gleichzeitige Betrachter“ im Bereich „Berichte“, wo die gleichzeitigen aktiven Sitzungen zugrunde gelegt werden.  Durch die Verwendung der Unique Visitors werden unerwünschte „Spitzen“ in den Anzeige-Grenzbereichen (wo die Sitzungen gleichzeitig enden und beginnen) entfernt. |

Eine Freiformtabelle ist in dieser Ansicht nicht verfügbar.  Zur Ansicht der Datenquelle können Sie mit der rechten Maustaste auf das Liniendiagramm klicken und es als csv-Datei herunterladen.  Serienaufschlüsselungen werden einbezogen.


![Output von gleichzeitigen Betrachtern](assets/concurrent-viewers-download-csv.png)

## Häufig gestellte Fragen (FAQ) {#FAQ}

| Frage | Antwort |
|---|---|
| Wo ist die Freiformtabelle? Wie kann ich die Datenquelle anzeigen? | Die Freiformtabelle ist in dieser Ansicht nicht verfügbar.  Sie können die Datenquelle herunterladen, indem Sie mit der rechten Maustaste auf das Liniendiagramm klicken und die CSV-Datei herunterladen. |
| Warum hat sich meine Granularität verändert? | Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene).  Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch aktualisiert, um den vollständigen Datumsbereich aufzunehmen.<br><br>Wenn Sie von einem größeren auf einen kleineren Datumsbereich wechseln, wird die Granularität auf das niedrigste zulässige Detail aktualisiert, sobald der Datumsbereich geändert wird. Um eine höhere Granularität zu sehen, bearbeiten Sie das Bedienfeld und erstellen Sie es erneut. |
| Wie vergleiche ich Videonamen, Segmente, Inhaltstypen usw.? | Um diese in einer einzigen Visualisierung zu vergleichen, ziehen Sie Segmente, Dimensionen oder bestimmte Dimensionselemente in den Filter für die Serienaufschlüsselung.<br><br>Die Ansicht ist auf 10 Aufschlüsselungen beschränkt.  Um mehr als 10 ansehen zu können, müssen Sie mehrere Bedienfelder verwenden. |
| Wie vergleiche ich Datumsbereiche? | Um Datumsbereiche in einer einzigen Visualisierung zu vergleichen, verwenden Sie die Serienaufschlüsselungen, indem Sie zwei oder mehr Datumsbereiche ziehen.  Diese Datumsbereiche setzen den Datumsbereich des Bedienfelds außer Kraft. |
| Wie ändere ich den Visualisierungstyp? | Dieses Bedienfeld ermöglicht nur die Linienvisualisierung für die Zeitreihen. |
| Kann ich die Anomalieerkennung ausführen? | Nein.  Die Anomalieerkennung ist für dieses Bedienfeld nicht verfügbar. |
| Warum sollte ich Unique Visitors anstelle von aktiven Sitzungen verwenden? | Die Verwendung von Unique Visitors ermöglicht das Entfernen unerwünschter Spitzen in den Anzeige-Grenzbereichen (wo Sitzungen gleichzeitig enden und beginnen). |
| Was bedeutet es, parallele Betrachter mit einer Granularität von mehr als einer Minute zu haben? | Bei einer Granularität von mehr als einer Minute stellen gleichzeitige Betrachter die Summe der gleichzeitigen Unique Viewers für alle Minuten innerhalb dieses Zeitraums dar. Beispielsweise ist die Granularität gleichzeitiger Betrachter auf Stundenebene die Summe der gleichzeitigen Unique Viewers für alle Minuten innerhalb der Stunde. |
| Zeigt das Arbeitsbereich-Bedienfeld dieselben Informationen wie der Bericht zu gleichzeitigen Betrachtern? | Nein.  In Analysis Workspace bezeichnet der Begriff „Gleichzeitige Betrachter“ die Anzahl der Unique Visitors, die sich Ihre Medien-Streams zu einem bestimmten Zeitpunkt ansehen, unabhängig von der Anzahl der Sitzungen.<br><br>Dies unterscheidet sich vom Bericht „Gleichzeitige Betrachter“ im Bereich „Berichte“, wo die gleichzeitigen aktiven Sitzungen zugrunde gelegt werden.  Durch die Verwendung der Unique Visitors können unerwünschte Spitzen in den Anzeige-Grenzbereichen, wo die Sitzungen gleichzeitig enden und beginnen, entfernt werden. |

<!-- For more information about Media Concurrent Viewers, visit [MA doc page]( https://url). -->
