---
description: Funktionen zur Barrierefreiheitsunterstützung im Arbeitsbereich für Analysen
title: Barrierefreiheit im Arbeitsbereich für Analysen
translation-type: tm+mt
source-git-commit: a8fa30ecd8f3f230dac98a6f69ff6334d996fb9c
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 4%

---


# Barrierefreiheit im Arbeitsbereich für Analysen

Erfahren Sie mehr über die Barrierefreiheitsunterstützung in [!UICONTROL Analyse Workspace], dem führenden Tool zur Analyse von Adobe Analytics.

Barrierefreiheit bedeutet, Produkte für Menschen mit Sehbehinderungen, Hörgeschäften, Kognitionsfähigkeiten, motorischen Störungen und anderen Behinderungen nutzbar zu machen. Beispiele für Barrierefreiheitsfunktionen für Softwareprodukte sind die Unterstützung von Bildschirmlesehilfen, Entsprechungen für Grafiken, Tastaturbefehle, die Änderung von Anzeigefarben in kontrastreiche Farben usw.

[!UICONTROL Analyse Workspace] bietet einige Tools, mit denen Sie auf die Verwendung zugreifen können:

## Navigieren in [!UICONTROL Workspace] mithilfe der Tastatur

Die Navigation in [!UICONTROL Analyse Workspace] funktioniert oben > unten und links > rechts. Die folgenden Navigationselemente erleichtern die Zugänglichkeit:

* Der `F6` Schlüssel ermöglicht richtungsweisende Verknüpfungen
* Die `Tab` Taste wechselt zwischen einzelnen Elementen.
* Wir wenden Fokusindikatoren an, sodass sehende Tastaturbenutzer einen klaren Hinweis darauf haben, welches UI-Element derzeit im Fokus ist. Der Indikator ist ein blauer Rand um das ausgewählte Element herum.

   ![Fokusindikator](assets/focus-indicator.png)

### Tastaturnavigation für Drag &amp; Drop-Interaktionen

[!UICONTROL Analyse Workspace] ist eine Drag &amp; Drop-Benutzeroberfläche. Benutzer können jedoch stattdessen Komponenten über die Tastatur hinzufügen:

1. Registerkarten zu einer Komponente in der linken Leiste.
1. Drücken Sie `Enter` die Eingabetaste.
1. Verwenden Sie die Pfeiltasten, um zu dem Bereich zu navigieren, in dem Sie die Komponente ablegen möchten.
1. Drücken Sie `Enter` die Eingabetaste, um die Komponente zu platzieren.

### Tastaturbefehle (Hotkeys)

[!UICONTROL Analyse Workspace] Angebot einen umfangreichen Satz [Tastaturbefehle](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.html) für einen nahtlosen Arbeitsablauf. Nachfolgend sind einige allgemeine Kurzbefehle für die Navigation, die Erstellung von Analysen und die Demokratisierung von Erkenntnissen aufgeführt.

#### Navigation

| Tastaturbefehl | Aktion |
|---|---|
| Alt + Umschalt + 1 / 2 / 3 | Wechseln zu verschiedenen Schienen: [!UICONTROL Bedienfelder], [!UICONTROL Visualisierungen]oder [!UICONTROL Komponenten] |
| Alt + Nach-links/Nach-rechts | Zwischen Bedienfeldern navigieren |
| Alt + M | Alle Bedienfelder reduzieren/erweitern |
| Alt+ Strg+M | Aktives Bedienfeld reduzieren/erweitern |
| Strg + / | Linke Leiste durchsuchen |

#### Erstellung von Analysen

| Tastaturbefehl | Aktion |
|---|---|
| Alt + 1 | Neue Freiformtabelle |
| Strg+Umschalt+C | Neue berechnete Metrik |
| Strg+Umschalt+D | Neuer Datumsbereich |
| Strg+Umschalt+E | Neues Segment |
| Strg+Z | Machen Sie Ihre Änderungen rückgängig |
| Umschalttaste gedrückt halten (im Dropzone des Bereichssegments) | Einen [Dropdownfilter erstellen](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html) |

#### Demokratisierung

| Tastaturbefehl | Aktion |
|---|---|
| Strg+S | Speichern |
| Strg+Umschalt+G | kuratieren |
| Strg+G | Freigabe |
| Alt + Umschalt + S | Plan |
| Alt + L | Link zum Projekt |
| Strg+Umschalt+B | PDF herunterladen |

## Unterstützung für Bildschirmlesehilfen und Vergrößerungssoftware

Eine Bildschirmlesehilfe liest Text, der auf dem Computerbildschirm angezeigt wird. Es werden auch nicht textuelle Informationen wie Schaltflächenbeschriftungen oder Bildbeschreibungen in der Anwendung gelesen, die in Tags oder Attributen zur Barrierefreiheit bereitgestellt werden.

## Farbpaletten und Kontrast

[!UICONTROL Analyse Workspace] strebt die Konformität mit WCAG 2.1 AA an, einschließlich der Anforderungen für den Farbkontrast.

Darüber hinaus können die Benutzer ihre eigene bevorzugte Farbpalette für ein Projekt unter **[!UICONTROL Projekt]** > **[!UICONTROL Projekteinstellungen]** > [Farbpalette](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes.html)festlegen.

## Erforderliche Feldüberprüfung in Komponenten-Buildern

Beim Erstellen einer Komponente werden die erforderlichen Felder beim Speichern überprüft. Wenn ein erforderliches Feld die Überprüfung nicht erfolgreich durchläuft, wird es rot mit einem Fehlersymbol gekennzeichnet. Es wird eine schriftliche Beschreibung des Problems angezeigt, das behoben werden muss.

Sobald eine Komponente vollständig validiert wurde, wird der Builder durch Drücken der Taste `Save` geschlossen.

![Fehler-Überprüfung](assets/error-validation.png)

## Unterstützung für Barrierefreiheitsfunktionen des Betriebssystems

Analyse Workspace unterstützt integrierte MS Windows- und macOS-Zugänglichkeitsfunktionen wie den Modus mit hohem Kontrast, fixierbare Schlüssel und langsame Schlüssel/Filterschlüssel. Es enthält auch Informationen über die Benutzeroberfläche des Betriebssystems, um die Interaktion mit Hilfstechnologien zu ermöglichen, einschließlich Bildschirmlesehilfen wie VoiceOver für macOS und NVDA unter Windows.