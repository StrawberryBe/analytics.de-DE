---
description: Quick Insight Builder ist ein Tool für neue Workspace-Benutzer, das diese beim Erstellen von Datentabellen und Visualisierungen unterstützt.
title: Quick Insights Builder
translation-type: tm+mt
source-git-commit: 446026850794e6fba3ccf04562221f2ca907a390
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 2%

---


# Quick Insights Builder

>[!IMPORTANT]
>
>**[!UICONTROL Quick Insights]** wird derzeit nur eingeschränkt getestet. [Mehr Infos...](https://docs.adobe.com/content/help/en/analytics/landing/an-releases.html)

[!UICONTROL Quick Insights] bietet Nichtanalysten und neuen Benutzern von [!UICONTROL Analyse Workspace] Anleitungen, wie Sie Geschäftsfragen schnell und einfach beantworten können. Es ist auch ein großartiges Werkzeug für fortgeschrittene Benutzer, die eine einfache Frage schnell beantworten möchten, ohne selbst eine Tabelle erstellen zu müssen.

Wenn Sie diesen Arbeitsbereich [!UICONTROL für]Analysen zum ersten Beginn verwenden, fragen Sie sich vielleicht, welche Visualisierungen am nützlichsten sind, welche Dimensionen und Metriken Einblicke erleichtern können, wo Elemente per Drag &amp; Drop eingefügt werden können, wo ein Segment erstellt wird usw.

Um dies zu unterstützen und basierend auf der Nutzung von Datenkomponenten durch Ihre eigene Firma im [!UICONTROL Analyse Workspace], verwendet [!UICONTROL Quick Insights] einen Algorithmus, der Ihnen die beliebtesten Dimensionen, Metriken, Segmente und Datumsbereiche, die Ihre Firma verwendet, präsentiert.

[!UICONTROL Quick Insights] hilft Ihnen

* Erstellen Sie eine Datentabelle und eine zugehörige Visualisierung in [!UICONTROL Analyse Workspace].
* Erfahren Sie mehr über die Terminologie und das Vokabular für Grundelemente und Bestandteile von [!UICONTROL Analyse Workspace].
* Machen Sie einfache Aufschlüsselungen von Dimensionen, fügen Sie mehrere Metriken hinzu oder vergleichen Sie Segmente einfach in einer [!UICONTROL Freiformtabelle].
* Ändern Sie die verschiedenen Visualisierungstypen oder versuchen Sie es auszuprobieren, um das Suchwerkzeug für Ihre Analyse schnell und intuitiv zu finden.

## Grundlegende Terminologie

Im Folgenden finden Sie einige grundlegende Begriffe, mit denen Sie vertraut sein müssen. Jede Datentabelle besteht aus zwei oder mehr Bausteinen (Komponenten), die Sie zum Erzählen Ihrer Datenstory verwenden.

| Baustein (Komponente) | Definition |
|---|---|
| [!UICONTROL Dimension] | Dimensionen sind Beschreibungen oder Merkmale von Metrikdaten, die in einem Projekt angezeigt, aufgeschlüsselt und verglichen werden können. Es handelt sich um nicht-numerische Werte und Daten, die in Dimensionselemente unterteilt werden. Beispielsweise sind &quot;browser&quot;oder &quot;page&quot;Dimensionen. |
| [!UICONTROL Dimensionselement] | Dimensionselemente sind individuelle Werte für eine Dimension. Beispielsweise wären Dimensionselemente für die Browserdimension &quot;Chrome&quot;, &quot;Firefox&quot;, &quot;Edge&quot;usw. |
| [!UICONTROL Metrik] | Metriken sind quantitative Informationen über Besucheraktivitäten wie Ansichten, Clickthroughs, Neuladungen, durchschnittliche Besuchszeit, Einheiten, Bestellungen, Umsatz usw. |
| [!UICONTROL Visualization] | Workspace Angebot [eine Reihe von Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) , um visuelle Darstellungen Ihrer Daten zu erstellen, z. B. Balkendiagramme, Ringdiagramme, Histogramme, Liniendiagramme, Karten, Streudiagramme und andere. |
| [!UICONTROL Dimensionsaufschlüsselung] | Eine Dimensionsaufschlüsselung ist eine Möglichkeit, eine Dimension buchstäblich nach anderen Dimensionen zu unterteilen. In unserem Beispiel könnten Sie die US-Bundesstaaten nach Mobilgeräten unterteilen, um die Besuche der Mobilgeräte pro Bundesland zu erhalten, oder Sie könnten Mobilgeräte nach Mobilgerätetypen, Regionen, internen Kampagnen usw. unterteilen. |
| [!UICONTROL Segment] | Mit Segmenten können Sie Untergruppen von Besuchern anhand von Merkmalen oder Website-Interaktionen identifizieren. Sie können beispielsweise [!UICONTROL Besucher] -Segmente basierend auf Attributen erstellen: Browsertyp, Gerät, Anzahl der Besuche, Land, Geschlecht oder basierend auf Interaktionen: Kampagnen, Suchbegriffssuche, Suchmaschinen oder auf der Grundlage von Ausstiegen und Einstiegen: Besucher aus Facebook, einer definierten Landingpage, einer verweisenden Domäne oder basierend auf benutzerspezifischen Variablen: Formularfeld, definierte Kategorien, Kunden-ID. |

## Erste Schritte mit Quick Insights

1. Melden Sie sich mit den angegebenen Anmeldeinformationen bei Adobe Analytics an.
1. Wechseln Sie zu [!UICONTROL Workspace] und klicken Sie auf Neues Projekt **** erstellen und dann auf **[!UICONTROL Schnelleinblicke]**. (Sie können auf dieses Bedienfeld auch über das Menü &quot; **[!UICONTROL Bedienfeld]** &quot;in der linken Leiste zugreifen.)

   ![](assets/qibuilder.png)

   ![](assets/qi-panel.png)

1. Wenn Sie den ersten Beginn verbringen, führen Sie das kurze Lernprogramm durch, in dem Sie einige der Grundlagen des [!UICONTROL Quick Insight-Bedienfelds] kennenlernen. Sie können auch auf &quot;Übung **[!UICONTROL überspringen&quot;klicken]**.
1. Wählen Sie die Bausteine aus (auch als Komponenten bezeichnet): Dimensionen (orange), Metriken (grün), Segmente (blau) oder Datumsbereiche (violett) Sie müssen mindestens eine Dimension und eine Metrik auswählen, damit eine Tabelle automatisch erstellt wird.

   ![](assets/qibuilder2.png)

   Sie haben drei Möglichkeiten, die Bausteine auszuwählen:
   * Ziehen Sie sie per Drag &amp; Drop aus der linken Leiste.
   * Wenn Sie wissen, was Sie suchen: Beginn eingeben und [!UICONTROL Quick Insight] füllen die Lücken aus.
   * Klicken Sie auf die Dropdown-Liste und suchen Sie die Liste.

1. Wenn Sie mindestens eine Dimension und eine Metrik hinzugefügt haben, wird Folgendes erstellt:

   * Eine Freiform-Tabelle mit der Dimension (hier, US-Bundesstaaten) und der Metrik (hier, Besuche) horizontal oben. Sehen Sie sich diese Tabelle an:
   ![](assets/qibuilder3.png)

   * Eine begleitende Visualisierung, in diesem Fall ein [Balkendiagramm](/help/analyze/analysis-workspace/visualizations/bar.md). Die erstellte Visualisierung basiert auf dem Datentyp, den Sie der Tabelle hinzugefügt haben. Zeitbasierte Daten (z. B. [!UICONTROL Besuche] pro Tag/Monat) verwenden standardmäßig ein [!UICONTROL Liniendiagramm] . Alle nicht zeitbasierten Daten (z. B. [!UICONTROL Besuche] pro [!UICONTROL Gerät]) verwenden standardmäßig ein [!UICONTROL Balkendiagramm] . Sie können den Visualisierungstyp ändern, indem Sie auf den Dropdown-Pfeil neben dem Visualisierungstyp klicken.


1. (Optional) Führen Sie einen Drilldown zu Dimensionen durch und sehen Sie Dimensionselemente, indem Sie auf den Pfeil > rechts neben der Dimension klicken.

1. Versuchen Sie, einige weitere Verfeinerungen hinzuzufügen, wie nachfolgend unter &quot;Weitere Tipps&quot;beschrieben.

1. Speichern Sie das Projekt, indem Sie auf **[!UICONTROL Projekt > Speichern]** klicken.

## Mehr Tipps

Weitere nützliche Hinweise werden im [!UICONTROL Quick Insight Builder]angezeigt, einige davon abhängig von Ihrer letzten Aktion.

* Vervollständigen Sie zunächst das Tutorial **[!UICONTROL Mehr Tipps]** : Greifen Sie über die Hilfe zu (?) neben dem Titel [!UICONTROL Quick Insights] angezeigt. Dieses Tutorial zeigt Ihnen 24 Stunden nach Erstellung eines Projekts mit mindestens einer Dimension und einer Metrik.

   ![](assets/qibuilder4.png)

* **Aufschlüsselung nach**: Sie können bis zu drei Stufen von Aufschlüsselungen für Dimensionen verwenden, um einen Drilldown zu den Daten durchzuführen, die Sie wirklich benötigen.

   ![](assets/qibuilder5.png)

* **Hinzufügen weitere Metriken**: Mithilfe des UND-Operators können Sie bis zu 2 weitere Metriken hinzufügen.

   ![](assets/qibuilder6.png)

* **Hinzufügen weitere Segmente**: Sie können bis zu 2 weitere Segmente hinzufügen, indem Sie die UND- oder ODER-Operatoren verwenden, um sie der Tabelle hinzuzufügen. Sehen Sie sich an, was mit der Tabelle passiert, wenn Sie Mobilbenutzer ODER Treue Besucher hinzufügen. Sie stehen nebeneinander, über den Metriken. Wenn Sie &quot;Mobilbenutzer UND treue Besucher&quot;hinzufügen, sehen Sie die Ergebnisse beider Segmente zusammen und sie werden übereinander in der Tabelle gestapelt.

   ![](assets/qibuilder7.png)

## Bekannte Einschränkungen

Wenn Sie versuchen, die Datei direkt in der Tabelle zu bearbeiten, führt dies dazu, dass das [!UICONTROL Quick Insight] -Bedienfeld (das Blindwerkzeug) nicht mehr synchron ist. Sie können die vorherigen Einstellungen für [!UICONTROL Schnelleinblicke] wiederherstellen, indem Sie oben rechts im Bedienfeld auf &quot; **[!UICONTROL Aufbau neu synchronisieren&quot;klicken]** .

![](assets/qibuilder9.png)

Sie erhalten eine Warnung, bevor Sie etwas direkt zur Tabelle hinzufügen:

![](assets/qibuilder8.png)

Andernfalls führt das direkte Erstellen dazu, dass sich die Tabelle jetzt als herkömmliche Freiform-Tabelle ohne die nützlichen Funktionen für neue Benutzer verhält.

