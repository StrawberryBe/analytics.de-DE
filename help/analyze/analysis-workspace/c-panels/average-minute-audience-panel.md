---
title: Bereich "Zielgruppendurchschnitt pro Minute"
description: Verwendung und Interpretation des Bereichs Zielgruppendurchschnitt pro Minute in Analysis Workspace.
feature: Panels
role: User, Admin
exl-id: be8371ee-8bc6-4a99-8527-dd94eab8a7f9
source-git-commit: 86f546da8a5eaded5abb4ee2ce8d4a536818574a
workflow-type: tm+mt
source-wordcount: '1320'
ht-degree: 11%

---

# Bereich &quot;Zielgruppendurchschnitt pro Minute&quot;

>[!NOTE]
>
>Diese Funktion wird derzeit eingeschränkt getestet.

Media Analytics-Kunden können das durchschnittliche Minutenzielgruppen-Bedienfeld verwenden, um den durchschnittlichen Verbrauch ihrer Inhalte besser zu verstehen. Die Zielgruppe &quot;Durchschnittliche Minute&quot;ermöglicht Vergleiche der Programmierung beliebiger Länge oder Genres. Darüber hinaus können Kunden diese durchschnittliche Minutenzielgruppe für digitale Sendungen mit linearen TV-Durchschnittsminuten-Metriken vergleichen oder anhängen. Dieses Bedienfeld bietet mehr Flexibilität, um die durchschnittliche Zielgruppe für benutzerdefinierte Zeiträume sowie den Zeitpunkt zu messen, zu dem die Classification der Dauer nach der Tatsache aktualisiert wurde. Die Metrik für die aktuelle durchschnittliche Minute-Zielgruppe funktioniert nur, wenn die Dauer zur Verarbeitungszeit verfügbar ist.

In Analysis Workspace bezeichnet die durchschnittliche Minutenzielgruppe die Zeit, die mit der Anzeige Ihres Medienstreams verbracht wurde, geteilt durch die Inhaltsdauer oder die Gesamtauswahl des Zeitraums und die ausgewählte Granularität.

Das Bedienfeld Zielgruppendurchschnitt pro Minute für Medien bietet eine durchschnittliche Minute für Zielgruppenanalysen nach dem ausgewählten spezifischen Inhalt, wenn die Dauer mithilfe von Klassifizierungen zur Verfügung gestellt wird.
Das Bedienfeld Zielgruppendurchschnitt pro Minute bietet außerdem Analysen über einen ausgewählten Zeitraum, die nach bestimmten Inhalten gefiltert werden können - unabhängig davon, ob die Dauer mit Classifications verfügbar ist oder nicht. Um auf das Bedienfeld Zielgruppendurchschnitt pro Minute für Medien zuzugreifen, navigieren Sie zu einer Report Suite mit aktivierten Media Analytics-Komponenten. Klicken Sie dann auf das Panel-Symbol ganz links und ziehen Sie das Panel in Ihr Analysis Workspace-Projekt.

<!-- For more information, see the Media Average Minute Audience introduction video:
<< replace with AMA video when available >> -->

<!-- >[!VIDEO](https://video.tv.adobe.com/v/330177/?quality=12) -->

## Bedienfeldeingaben {#Input}

Sie können das Bedienfeld &quot;Zielgruppendurchschnitt pro Minute&quot;mit den folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
|---------|------------|
| Datumsbereich der Bedienfelder | Der Datumsbereich des Panels ist standardmäßig „Heute“. Sie können ihn so verändern, dass Sie einen einzelnen Tag oder viele Monate auf einmal betrachten können. <br></br> Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Ziehen Sie ein Segment hierher (oder beliebige andere Komponenten) | Wie andere Bedienfelder filtert diese Einstellung Ihre Auswahl anhand von Segmenten, die Sie erstellt haben. Dies ist eine hervorragende Möglichkeit, bestimmte Plattformen, Live-Streams oder andere gängige Mediensegmente anzusehen. |
| Metrik berechnen für | Mit dieser Einstellung können Sie durch Auswahl von *spezifischer Inhalt* oder wenn Sie die durchschnittliche Minutenzielgruppe für einen bestimmten Zeitraum anzeigen möchten, indem Sie *benutzerdefinierter Zeitraum*. <br></br>Bestimmte Inhalte funktionieren nur, wenn die Dauer mithilfe von Classifications aktualisiert wurde. Wenn die Dauer nicht verfügbar ist oder Sie die durchschnittliche Minutenzielgruppe für eine Zeitreihe mit mehreren Inhalten oder Inhalten ohne bestimmte Dauer anzeigen möchten (z. B. während eines Live-Streams oder -Ereignisses), sollten Sie einen benutzerdefinierten Zeitraum auswählen. Diese Einstellung ändert den Workflow und die Berichtsausgabe. |

### Bestimmter Inhalt

| Einstellung | Beschreibung |
|---------|------------|
| Berichtsdimensionen | Bei der Auswahl bestimmter Inhalte können Sie die Berichtsausgabe auswählen, um entweder die Felder für Videoname oder Inhalts-ID zu verwenden und den Inhalt und die zugehörige durchschnittliche Minutenzielgruppe für den ausgewählten Zeitraum anzuzeigen. |
| Content filtern nach (optional) | Sie können den spezifischen Inhalt nach der gewünschten Ansicht oder der Struktur Ihrer Daten filtern. |
| Sendung, Staffel, Folge | Wenn Sie &quot;Anzeigen, Staffel, Folge&quot;auswählen, werden Ihre verfügbaren Sendungen im Dropdown-Menü angezeigt, die Sie mithilfe einer Suche filtern können (oder indem Sie den Anzeigennamen aus der linken Spalte ziehen und ablegen). Sie können Ihre Auswahl dort beenden, um alle Jahreszeiten Ihrer Sendung zu sehen, oder Sie können nach einzelnen Jahreszeiten und dann nach einzelnen Episoden filtern. Diese Einstellung zeigt die Daten für diese Sendungen, Jahreszeiten oder Episoden aus dem ausgewählten Zeitraum an. |
| Benutzerdefinierte Dimension | Wenn Ihr Anzeigename unter einer benutzerdefinierten Dimension liegt, können Sie ihn entweder durch Suchen in der Dropdown-Liste &quot;Dimension&quot;(optional) oder durch Verwenden der linken Spaltensuche finden. Das Dimensionselement wird basierend auf dieser Auswahl automatisch ausgefüllt und als Folge behandelt. |
| Keine | Sie können *Keines* um alle Videonamen anzuzeigen, die durchschnittliche Minutenzielgruppendaten für die ausgewählte Auswahl enthalten. |

### Erweiterte Einstellungen für spezifischen Inhalt

| Einstellung | Beschreibung |
|---------|------------|
| Tabelleneinstellungen | Die Standardeinstellung zeigt die Berechnungswerte in der Tabelle an, die den Zähler und Nenner der durchschnittlichen Minutenzielgruppe als die vorangehenden Spalten in der Tabelle anzeigt. Wenn Sie diese Option deaktivieren, werden diese beiden Spalten entfernt, sodass nur die durchschnittliche Minutenzielgruppe neben dem Videonamen oder der Inhalts-ID verbleibt. |
| Besuchszeitmetrik | Sie können die standardmäßige Besuchszeit für den Inhalt auswählen, die nur die Inhaltsdauer enthält, oder die Medienzeit verwenden, die Inhalt und Anzeigenzeit zusammen als Zählerberechnung für die durchschnittliche Minutenzielgruppe enthält. |

### Benutzerdefinierter Zeitraum

| Einstellung | Beschreibung |
|---------|------------|
| Granularität | Die Standardgranularität beträgt 5 Minuten. Sie können jedoch eine der Granularitäten auswählen, die als Nenner für die Zeitreihe innerhalb der Gesamtzeitraumauswahl, die in der Kalenderauswahl vorgenommen wird, verwendet werden. Wenn Sie beispielsweise 12:00 Uhr bis 23:30 Uhr mit einer Granularität von 5 Minuten auswählen, erhalten Sie die durchschnittliche Minutenzielgruppe über die gesamte halbe Stunde sowie sechs Zeilen mit der durchschnittlichen Minutenzielgruppe für jeden 5-minütigen Zeitraum. Diese Zeilen werden als Datenpunkte für das Zeitreihendiagramm verwendet. |
| Content filtern nach (optional) | Sie können den spezifischen Inhalt nach der gewünschten Ansicht oder der Struktur Ihrer Daten filtern. |
| Sendung, Staffel, Folge | Auswählen *Einblenden, Staffel, Folge* zeigt Ihre verfügbaren Anzeigen in der Dropdown-Liste an, die Sie per Suche filtern können (oder indem Sie den Anzeigennamen aus der linken Spalte ziehen und ablegen). Sie können Ihre Auswahl dort beenden, um alle Jahreszeiten Ihrer Sendung zu sehen, oder Sie können nach einzelnen Jahreszeiten und dann nach einzelnen Episoden filtern. Diese Einstellung zeigt die Daten für diese Sendungen, Jahreszeiten oder Episoden aus dem ausgewählten Zeitraum an. |
| Benutzerdefinierte Dimension | Wenn Ihr Anzeigename unter einer benutzerdefinierten Dimension liegt, können Sie ihn entweder durch Suchen in der Dropdown-Liste &quot;Dimension&quot;(optional) oder durch Verwenden der linken Spaltensuche finden. Das Dimensionselement wird basierend auf dieser Auswahl automatisch ausgefüllt und als Folge behandelt. |
| Keine | Sie können *Keines* um alle Videonamen über den ausgewählten Zeitraum anzuzeigen. |

### Erweiterte Einstellungen für benutzerdefinierte Zeiträume

| Einstellung | Beschreibung |
|---------|------------|
| Tabelleneinstellungen | Die Standardeinstellung zeigt die Berechnungswerte in der Tabelle an, die den Zähler und Nenner der durchschnittlichen Minutenzielgruppe als die vorangehenden Spalten in der Tabelle anzeigt. Wenn Sie diese Option deaktivieren, werden die beiden Spalten entfernt, sodass neben dem Zeitraum nur die Zielgruppe mit der durchschnittlichen Minute verbleibt. |


## Bestimmte Inhaltsbereichsausgabe

Das Bedienfeld Zielgruppendurchschnitt pro Minute für Medien gibt Folgendes zurück:

* Durchschnittliche Gesamtanzahl der Zielgruppen pro Minute für Ihre gesamte Auswahl
* Filter und durchschnittliche Minutenzielgruppe für die einzelnen Videos, die in einer Tabelle angezeigt werden
* Besuchszeit für Inhalt und Videolänge (Dauer), wenn diese erweiterte Einstellung ausgewählt wurde

Um das Bedienfeld jederzeit zu bearbeiten und neu zu erstellen, klicken Sie oben rechts auf den Stift zum Bearbeiten .

![Standardansicht](assets/specific-content-panel-output.png)


### Bestimmte Inhaltsdatenquelle

Die einzige Metrik, die in diesem Bereich verwendet werden kann, ist &quot;Zielgruppendurchschnitt pro Minute&quot;.

| Metrik | Beschreibung |
|--------|-------------|
| Zielgruppendurchschnitt pro Minute | Die Zeit, die mit der Anzeige Ihres Medien-Streams verbracht wurde, dividiert durch die Videolänge (Dauer), die über Classifications bereitgestellt wird. |

## Ausgabe des Bedienfelds &quot;Benutzerdefinierter Zeitraum&quot; {#custom-time-period-output}

Das Bedienfeld Zielgruppendurchschnitt pro Minute für Medien gibt die durchschnittliche Zielgruppe pro Minute für Ihre gesamte Auswahl, die maximale und minimale durchschnittliche Minute-Zielgruppe sowie das Liniendiagramm mit der durchschnittlichen Minutenzielgruppe über die gesamte Auswahl zurück. Die nachstehende Tabelle zeigt die Filter und die durchschnittliche Minutenzielgruppe für die Granularitäten sowie die Besuchszeit für den Inhalt und Granularität für jeden Zeitraum, wenn diese erweiterte Einstellung ausgewählt wurde.

Um das Bedienfeld jederzeit zu bearbeiten und neu zu erstellen, klicken Sie oben rechts auf den Stift zum Bearbeiten .

![Output von gleichzeitigen Betrachtern](assets/custom-time-period-panel-output.png)

### Datenquelle für den benutzerdefinierten Zeitraum

Die einzige Metrik, die in diesem Bedienfeld verwendet werden kann, ist &quot;Zielgruppendurchschnitt pro Minute&quot;:

| Metrik | Beschreibung |
|---|---|
| Zielgruppendurchschnitt pro Minute | Die mit der Anzeige Ihres Medien-Streams verbrachte Zeit dividiert durch die Gesamtauswahl oder die ausgewählte Granularität in Minuten. |



<!-- For more information about Media Average Minute Audience, visit [MA doc page]( https://url). -->
