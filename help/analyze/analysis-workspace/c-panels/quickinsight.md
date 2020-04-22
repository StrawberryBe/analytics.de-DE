---
description: 'null'
title: Quick Insight Builder
translation-type: tm+mt
source-git-commit: 77b126b2add78113c266265f413240f27f89bced

---


# Quick Insight Builder

>[!IMPORTANT]
>
>Quick Insights befindet sich derzeit im Beta-Test und steht noch nicht generell allen Adobe Analytics-Kunden zur Verfügung.

Quick Insights bietet Nichtanalysten und neuen Benutzern von Analyse Workspace Anleitungen, wie Sie Geschäftsfragen schnell und einfach beantworten können. Es ist auch ein großartiges Werkzeug für fortgeschrittene Benutzer, die eine einfache Frage schnell beantworten möchten, ohne selbst eine Tabelle erstellen zu müssen.

Wenn Sie diesen Arbeitsbereich für Analysen zum ersten Beginn verwenden, fragen Sie sich vielleicht, welche Visualisierungen am nützlichsten sind, welche Dimensionen und Metriken Einblicke ermöglichen, wo Elemente per Drag &amp; Drop eingefügt werden können, wo ein  erstellt werden kann usw.

Um dies zu unterstützen, verwendet Quick Insights einen Algorithmus, der auf der Grundlage der Nutzung von Datenkomponenten durch Ihre eigene Firma in Analyse Workspace die beliebtesten Dimensionen, Metriken, Segmente und Datumsbereiche Ihrer Firma darstellt.

Quick Insights hilft Ihnen

* Erstellen Sie eine Datentabelle und die zugehörige Visualisierung in Analyse Workspace ordnungsgemäß.
* Erfahren Sie mehr über die Terminologie und das Vokabular für Grundelemente und Analyse Workspace.
* Machen Sie einfache Aufschlüsselungen von Dimensionen, fügen Sie mehrere Metriken hinzu oder vergleichen Sie Segmente einfach in einer Freiform-Tabelle.
* Ändern Sie die verschiedenen Visualisierungstypen oder versuchen Sie es auszuprobieren, um das Suchwerkzeug für Ihre Analyse schnell und intuitiv zu finden.

## Grundlegende Terminologie

Im Folgenden finden Sie einige grundlegende Begriffe, mit denen Sie vertraut sein müssen. Jede Datentabelle besteht aus zwei oder mehr Bausteinen, die Sie zur Erzählung Ihrer Datenstory verwenden.

| Baustein | Definition |
|---|---|
| Dimension | Dimensionen sind Beschreibungen oder Merkmale von Metrikdaten, die in einem Projekt angezeigt, aufgeschlüsselt und verglichen werden können. Es handelt sich um nicht-numerische Werte und Daten, die in Dimensionselemente unterteilt werden. Beispielsweise sind &quot;browser&quot;oder &quot;page&quot;Dimensionen. |
| Dimensionselement | Dimensionselemente sind individuelle Werte für eine Dimension. Beispielsweise wären Dimensionselemente für die Browserdimension &quot;Chrome&quot;, &quot;Firefox&quot;, &quot;Edge&quot;usw. |
| Metrik | Metriken sind quantitative Informationen über Besucheraktivitäten wie Ansichten, Clickthroughs, Neuladungen, durchschnittliche Besuchszeit, Einheiten, Bestellungen, Umsatz usw. |
| Visualisierung | Workspace Angebot [eine Reihe von Visualisierungen](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md) , um visuelle Darstellungen Ihrer Daten zu erstellen. |
| Segment | Mit Segmenten können Sie Untergruppen von Besuchern anhand von Merkmalen oder Website-Interaktionen identifizieren. Sie können beispielsweise Besucher-Segmente basierend auf Attributen erstellen: Browsertyp, Gerät, Anzahl der Besuche, Land, Geschlecht oder basierend auf Interaktionen: Kampagnen, Suchbegriffssuche, Suchmaschinen oder auf der Grundlage von Ausstiegen und Einstiegen: Besucher aus Facebook, einer definierten Landingpage, einer verweisenden Domäne oder basierend auf benutzerspezifischen Variablen: Formularfeld, definierte Kategorien, Kunden-ID. |

## Erste Schritte mit Quick Insights

1. Melden Sie sich mit den angegebenen Anmeldeinformationen bei Adobe Analytics an.
1. Gehen Sie zu [!UICONTROL Workspace] und klicken Sie auf **[!UICONTROL Create New Project]** und dann auf **[!UICONTROL Quick Insights Builder]**.

   ![](assets/qibuilder.png)

1. Wenn Sie den ersten Beginn abschließen, führen Sie das kurze Lernprogramm durch, in dem Sie einige der Grundlagen des Quick Insight Builder kennenlernen. Oder klicken Sie auf **[!UICONTROL Skip Tutorial]**.
1. Wählen Sie die Bausteine aus (auch als Komponenten bezeichnet): Dimensionen (orange), Metriken (grün), Segmente (blau) oder Datumsbereiche (violett) Sie müssen mindestens eine Dimension und eine Metrik auswählen, damit eine Tabelle automatisch erstellt wird.

   ![](assets/qibuilder2.png)

   Sie haben drei Möglichkeiten, die Bausteine auszuwählen:
   * Ziehen Sie sie per Drag &amp; Drop aus der linken Leiste
   * Wenn Sie wissen, was Sie suchen: Beginn, die den Namen eingeben, und Quick Insights füllen die Lücken für Sie aus
   * Klicken Sie auf die Dropdownliste und suchen Sie die Liste

1. Wenn Sie mindestens eine Dimension und eine Metrik hinzugefügt haben, wird Folgendes erstellt:

   * Eine Freiform-Tabelle mit der Dimension links (vertikal) und den Metriken oben (horizontal). Sehen Sie sich diese Tabelle an:

1. (Optional) Führen Sie einen Drilldown zu Dimensionen durch und sehen Sie Dimensionselemente, indem Sie auf den Pfeil > rechts neben der Dimension klicken.



## Bekannte Einschränkungen

Wenn Sie versuchen, direkt in der Tabelle zu bearbeiten, führt dies dazu, dass der Quick Insight Builder (das leere Füllwerkzeug) nicht mehr synchron ist. Sie können die vorherigen Quick Insight-Einstellungen wiederherstellen. Ist dies nicht der Fall, führt das Erstellen direkt dazu, dass sich die Tabelle jetzt als herkömmliche Freiform-Tabelle verhält.

