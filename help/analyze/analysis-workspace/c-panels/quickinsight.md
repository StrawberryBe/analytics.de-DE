---
description: 'null'
title: Quick Insights Builder
translation-type: tm+mt
source-git-commit: c8f482c21e6301ef34a221a73323cd7386921f2f

---


# Quick Insights Builder

>[!IMPORTANT]
>
>**[!UICONTROL Quick Insights]** befindet sich derzeit im Beta-Test und ist noch nicht generell für alle Adobe Analytics-Kunden verfügbar.

[!UICONTROL Quick Insights] bietet Analysten und Anwendern von Analyse Workspace Anleitungen, wie sie Geschäftsfragen schnell und einfach beantworten können. Es ist auch ein großartiges Werkzeug für fortgeschrittene Benutzer, die eine einfache Frage schnell beantworten möchten, ohne selbst eine Tabelle erstellen zu müssen.

Wenn Sie diesen Arbeitsbereich für Analysen zum ersten Beginn verwenden, fragen Sie sich vielleicht, welche Visualisierungen am nützlichsten sind, welche Dimensionen und Metriken Einblicke ermöglichen, wo Elemente per Drag &amp; Drop eingefügt werden können, wo ein  erstellt werden kann usw.

Um dies zu unterstützen und basierend auf der Nutzung von Datenkomponenten durch Ihre eigene Firma im Analyse Workspace einen Algorithmus zu verwenden, der Ihnen die beliebtesten Dimensionen, Metriken, Segmente und Datumsbereiche, die Ihre Firma verwendet, präsentiert. [!UICONTROL Quick Insights]

[!UICONTROL Quick Insights] hilft Ihnen

* Erstellen Sie eine Datentabelle und die zugehörige Visualisierung in Analyse Workspace ordnungsgemäß.
* Erfahren Sie mehr über die Terminologie und das Vokabular für Grundelemente und Analyse Workspace.
* Machen Sie einfache Aufschlüsselungen von Dimensionen, fügen Sie mehrere Metriken hinzu oder vergleichen Sie Segmente einfach in einer Freiform-Tabelle.
* Ändern Sie die verschiedenen Visualisierungstypen oder versuchen Sie es auszuprobieren, um das Suchwerkzeug für Ihre Analyse schnell und intuitiv zu finden.

## Grundlegende Terminologie

Im Folgenden finden Sie einige grundlegende Begriffe, mit denen Sie vertraut sein müssen. Jede Datentabelle besteht aus zwei oder mehr Bausteinen (Komponenten), die Sie zum Erzählen Ihrer Datenstory verwenden.

| Baustein (Komponente) | Definition |
|---|---|
| [!UICONTROL Dimension] | Dimensionen sind Beschreibungen oder Merkmale von Metrikdaten, die in einem Projekt angezeigt, aufgeschlüsselt und verglichen werden können. Es handelt sich um nicht-numerische Werte und Daten, die in Dimensionselemente unterteilt werden. Beispielsweise sind &quot;browser&quot;oder &quot;page&quot;Dimensionen. |
| [!UICONTROL Dimension item] | Dimensionselemente sind individuelle Werte für eine Dimension. Beispielsweise wären Dimensionselemente für die Browserdimension &quot;Chrome&quot;, &quot;Firefox&quot;, &quot;Edge&quot;usw. |
| [!UICONTROL Metric] | Metriken sind quantitative Informationen über Besucheraktivitäten wie Ansichten, Clickthroughs, Neuladungen, durchschnittliche Besuchszeit, Einheiten, Bestellungen, Umsatz usw. |
| Visualisierung | Workspace Angebot [eine Reihe von Visualisierungen](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md) , um visuelle Darstellungen Ihrer Daten zu erstellen, z. B. Balkendiagramme, Ringdiagramme, Histogramme, Liniendiagramme, Karten, Streudiagramme und andere. |
| [!UICONTROL Segment] | Mit Segmenten können Sie Untergruppen von Besuchern anhand von Merkmalen oder Website-Interaktionen identifizieren. Sie können beispielsweise [!UICONTROL Visitor] Segmente basierend auf Attributen erstellen: Browsertyp, Gerät, Anzahl der Besuche, Land, Geschlecht oder basierend auf Interaktionen: Kampagnen, Suchbegriffssuche, Suchmaschinen oder auf der Grundlage von Ausstiegen und Einstiegen: Besucher aus Facebook, einer definierten Landingpage, einer verweisenden Domäne oder basierend auf benutzerspezifischen Variablen: Formularfeld, definierte Kategorien, Kunden-ID. |

## Erste Schritte mit Quick Insights

1. Melden Sie sich mit den angegebenen Anmeldeinformationen bei Adobe Analytics an.
1. Gehen Sie zu [!UICONTROL Workspace] und klicken Sie auf **[!UICONTROL Create New Project]** und dann auf **[!UICONTROL Quick Insights Builder]**.

   ![](assets/qibuilder.png)

1. Wenn Sie den ersten Beginn abschließen, führen Sie das kurze Lernprogramm durch, in dem Sie einige der Grundlagen des Quick Insight Builder kennenlernen. Oder klicken Sie auf **[!UICONTROL Skip Tutorial]**.
1. Wählen Sie die Bausteine aus (auch als Komponenten bezeichnet): Dimensionen (orange), Metriken (grün), Segmente (blau) oder Datumsbereiche (violett) Sie müssen mindestens eine Dimension und eine Metrik auswählen, damit eine Tabelle automatisch erstellt wird.

   ![](assets/qibuilder2.png)

   Sie haben drei Möglichkeiten, die Bausteine auszuwählen:
   * Ziehen Sie sie per Drag &amp; Drop aus der linken Leiste.
   * Wenn Sie wissen, was Sie suchen: Beginn, die den Namen eingeben, und Quick Insights füllen die Lücken für Sie aus.
   * Klicken Sie auf die Dropdown-Liste und suchen Sie die Liste.

1. Wenn Sie mindestens eine Dimension und eine Metrik hinzugefügt haben, wird Folgendes erstellt:

   * Eine Freiform-Tabelle mit der Dimension (hier, US-Bundesstaaten) und der Metrik (hier, Besuche) horizontal oben. Sehen Sie sich diese Tabelle an:
   ![](assets/qibuilder3.png)

   * Eine begleitende Visualisierung, in diesem Fall ein [Balkendiagramm](/help/analyze/analysis-workspace/visualizations/bar.md). Die erstellte Visualisierung basiert auf dem Datentyp, den Sie der Tabelle hinzugefügt haben. Sie können den Visualisierungstyp ändern, indem Sie auf den Dropdown-Pfeil neben **[!UICONTROL Bar]**.


1. (Optional) Führen Sie einen Drilldown zu Dimensionen durch und sehen Sie Dimensionselemente, indem Sie auf den Pfeil > rechts neben der Dimension klicken.

1. Versuchen Sie, einige weitere Verbesserungen hinzuzufügen, wie nachfolgend unter &quot;Weitere hilfreiche Optionen&quot;beschrieben.

## Weitere hilfreiche Optionen

Weitere nützliche Hinweise werden im Quick Insights-Builder angezeigt, einige davon abhängig von Ihrer letzten Aktion.

* **Ziehen und Ablegen** versuchen: Wenn Sie z. B. den Baustein mithilfe der Dropdownliste ausgewählt haben, kann dies Popup-Fenster werden:

   ![](assets/qibuilder4.png)

* **Visualisierung**&#x200B;ändern: ermutigt Sie, verschiedene visuelle Darstellungen Ihrer Daten auszuprobieren, bis Sie die wirklich glänzende finden. Hier ein Beispiel für ein Liniendiagramm:

   ![](assets/qibuilder8.png)

* **Aufschlüsselung nach**: Sie können bis zu drei Stufen von Aufschlüsselungen für Dimensionen verwenden, um einen Drilldown zu den Daten durchzuführen, die Sie wirklich benötigen. Eine Aufschlüsselung ist eine Möglichkeit, die Dimension buchstäblich nach anderen Dimensionen zu unterteilen. In unserem Beispiel könnten Sie die US-Bundesstaaten nach Mobilgeräten aufschlüsseln, um die Besuche der Mobilgeräte nach Bundesland, Mobilgerätetypen oder Regionen, nach internen Kampagnen usw. zu erhalten.

   ![](assets/qibuilder5.png)

* **Hinzufügen weitere Metriken**: Mithilfe des UND-Operators können Sie bis zu 2 weitere Metriken hinzufügen.

   ![](assets/qibuilder6.png)

* **Hinzufügen weitere Segmente**: Sie können bis zu 2 weitere Segmente hinzufügen, indem Sie die UND- oder ODER-Operatoren verwenden, um sie der Tabelle hinzuzufügen. Sehen Sie sich an, was mit der Tabelle passiert, wenn Sie Mobilbenutzer ODER Treue Besucher hinzufügen. Sie stehen nebeneinander, über den Metriken. Wenn Sie &quot;Mobilbenutzer UND treue Besucher&quot;hinzufügen, sehen Sie die Ergebnisse beider Segmente zusammen und sie werden übereinander in der Tabelle gestapelt.

   ![](assets/qibuilder7.png)

## Bekannte Einschränkungen

Wenn Sie versuchen, direkt in der Tabelle zu bearbeiten, führt dies dazu, dass der Quick Insight-Builder (das leere Füllwerkzeug) nicht mehr synchron ist. Sie können die vorherigen Quick Insight-Einstellungen wiederherstellen, indem Sie zu der Tabelle navigieren **[!UICONTROL Help > Tutorials]** oder sie löschen, indem Sie oben rechts im Fenster &quot;Quick Insight&quot;auf **[!UICONTROL Clear]** klicken.

Andernfalls führt das direkte Erstellen dazu, dass sich die Tabelle jetzt als herkömmliche Freiform-Tabelle ohne die nützlichen Funktionen für neue Benutzer verhält.

