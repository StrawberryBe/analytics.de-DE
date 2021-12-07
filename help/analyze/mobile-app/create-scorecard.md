---
description: So erstellen Sie eine Scorecard für Adobe Analytics-Dashboards
title: Mobile-Scorecard erstellen
feature: Analytics Dashboards
role: User, Admin
source-git-commit: fca73532a83756062583d750b1727b5f2558718f
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 100%

---


# Mobile-Scorecard erstellen

Die folgenden Informationen liefern Kuratoren von Adobe Analytics-Daten eine Anleitung dazu, wie sie Mobile-Scorecards für Führungskräfte konfigurieren und darstellen können. Sehen Sie sich zunächst das Video zu Scorecard Builder von Adobe Analytics-Dashboards an:

>[!VIDEO](https://video.tv.adobe.com/v/34544)

Eine Adobe Analytics Scorecard stellt wie nachfolgend gezeigt wichtige Datenvisualisierungen für ausführende Benutzer in einem gekachelten Layout bereit:

![Beispiel-Scorecard](assets/intro_scorecard.png)

Als Kurator dieser Scorecard können Sie mit dem Scorecard Builder festlegen, welche Kacheln auf der Scorecard für den ausführenden Benutzer angezeigt werden. Sie können auch konfigurieren, wie die detaillierten Ansichten bzw. Aufschlüsselungen angepasst werden können, nachdem auf die Kacheln getippt wird. Hier sehen Sie die Scorecard Builder-Oberfläche:

![Scorecard Builder](assets/scorecard_builder.png)

Zur Erstellung der Scorecard führen Sie folgende Schritte aus:

1. Öffnen Sie die Vorlage für [!UICONTROL leere mobile Scorecards].
2. Konfigurieren Sie die Scorecard mit Daten und speichern Sie sie.

## Zugriff auf die Vorlage für [!UICONTROL leere mobile Scorecards]

Sie können die Vorlage [!UICONTROL Leere mobile Scorecard] öffnen, indem Sie entweder ein neues Projekt erstellen oder über das Menü „Tools“ zugreifen.

### Neues Projekt erstellen

1. Öffnen Sie Adobe Analytics und klicken Sie auf die Registerkarte **[!UICONTROL Arbeitsbereich]**.
1. Klicken Sie auf die Schaltfläche **[!UICONTROL Projekt erstellen]** und wählen Sie die Projektvorlage **[!UICONTROL Leere mobile Scorecard]** aus.
1. Klicken Sie auf **[!UICONTROL Erstellen]**.

![Scorecard-Vorlage](assets/new_template.png)

### Tools-Menü

1. Wählen Sie im Menü **[!UICONTROL Tools]** die Option **[!UICONTROL Analytics-Dashboards (Mobile App)]** aus.
1. Klicken Sie im nachfolgenden Bildschirm auf **[!UICONTROL Neue Scorecard erstellen]**.

## Scorecard mit Daten konfigurieren und speichern

So implementieren Sie die Scorecard-Vorlage:

1. Geben Sie unter **[!UICONTROL Eigenschaften]** (in der rechten Leiste) eine **[!UICONTROL Report Suite des Projekts]** an, aus der Sie Daten verwenden möchten.

   ![Report Suite-Auswahl](assets/properties_save.png)

1. Um Ihrer Scorecard eine neue Kachel hinzuzufügen, ziehen Sie eine Metrik aus dem linken Bereich und legen Sie sie im Bereich **[!UICONTROL Metriken hierher ziehen und ablegen]** ab. Sie können auch eine Metrik zwischen zwei Kacheln einfügen, indem Sie einen ähnlichen Workflow verwenden.

   ![Kacheln hinzufügen](assets/build_list.png)


1. Von jeder Kachel aus können Sie auf eine Detailansicht zugreifen, die zusätzliche Informationen über die Metrik anzeigt, wie z. B. die obersten Elemente in einer Liste verwandter Dimensionen.

## Dimensionen oder Metriken hinzufügen

Um einer Metrik eine verwandte Dimension hinzuzufügen, ziehen Sie eine Dimension aus dem linken Bereich und legen Sie sie auf einer Kachel ab.

Sie können beispielsweise geeignete Dimensionen (wie **[!DNL Marketing Channel]** in diesem Beispiel) zur Metrik **[!UICONTROL Unique Visitors]** hinzufügen, indem Sie sie auf die Kachel ziehen und dort ablegen. Aufschlüsselungen von Dimensionen werden im Abschnitt [!UICONTROL Drill Ins] (Aufschlüsselung) der kachelspezifischen **[!UICONTROL Eigenschaften]** angezeigt. Sie können jeder Kachel mehrere Dimensionen hinzufügen.

![Dimensionen hinzufügen](assets/layer_dimensions.png)

## Segmente anwenden

Um ein Segment auf einzelne Kacheln anzuwenden, ziehen Sie es aus dem linken Bereich und legen Sie es direkt auf der Kachel ab.

Wenn Sie das Segment auf alle Kacheln in der Scorecard anwenden möchten, legen Sie die Kachel oben auf der Scorecard ab. Sie können auch Segmente anwenden, indem Sie im Filtermenü unterhalb der Datumsbereiche Segmente auswählen. Sie [konfigurieren und wenden Filter für Ihre Scorecards](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html?lang=de) genauso wie in Adobe Analytics Workspace an.

![Segmente für Filter erstellen](assets/segment_ui.png)

## Datumsbereiche hinzufügen

Um Datumsbereichskombinationen, die in Ihrer Wertungsliste ausgewählt werden können, hinzuzufügen oder zu entfernen, wählen Sie die Dropdown-Liste „Datumsbereich“ aus.

![Neue Scorecard](assets/new_score_card.png)

Jede neue Scorecard Beginn mit 6 Datumsbereichskombinationen, die sich auf den Datumsbereich von heute und gestern konzentrieren. Sie können unnötige Datumsbereiche entfernen, indem Sie auf das „x“ klicken, oder Sie können jede Datumsbereichskombination durch Klicken auf den Stift bearbeiten.

![Neue Scorecard2](assets/new_score_card2.png)

Um ein Primärdatum zu erstellen oder zu ändern, wählen Sie über die Dropdown-Liste aus den verfügbaren Datumsbereichen aus oder ziehen Sie eine Datumskomponente aus der rechten Leiste in den Ablagebereich.

![Neue Scorecard3](assets/new_score_card3.png)

Um ein Vergleichsdatum zu erstellen, können Sie im Dropdown-Menü aus praktischen Voreinstellungen für gängige Zeitvergleiche auswählen. Sie können auch eine Datumskomponente aus der rechten Leiste ziehen und ablegen.

![Neue Scorecard4](assets/new_score_card4.png)

Wenn der gewünschte Datumsbereich noch nicht erstellt wurde, können Sie durch Klicken auf das Kalendersymbol einen neuen erstellen.

![Neue Scorecard5](assets/new_score_card5.png)

Dadurch gelangen Sie zum Generator für den Datumsbereich, in dem Sie eine neue Komponente für den Datumsbereich erstellen und speichern können.

## Visualisierungen anwenden

Video zu Visualisierungen für Mobile-Scorecards ansehen:

>[!VIDEO](https://video.tv.adobe.com/v/337570/?quality=12&learn=on)

Analytics-Dashboards verfügen über vier Visualisierungen, die Ihnen einen nützlichen Einblick in Dimensionselemente und -metriken bieten. Wenn Sie eine andere Visualisierung anwenden möchten, ändern Sie den [!UICONTROL Diagrammtyp] in den [!UICONTROL Eigenschaften] einer Kachel. Wählen Sie einfach die rechte Kachel aus und ändern Sie dann den Diagrammtyp.

![Kacheleigenschaften](assets/properties.png)

Oder klicken Sie auf das Symbol für [!UICONTROL Visualisierungen] in der linken Leiste und ziehen Sie die rechte Visualisierung per Drag &amp; Drop auf die Kachel:

![Visualisierungen](assets/vizs.png)

### [!UICONTROL Zusammenfassungszahl]

Verwenden Sie die Visualisierung der Zusammenfassungsnummer, um eine große Zahl hervorzuheben, die in einem Projekt wichtig ist.

![Zusammenfassungszahl](assets/summary-number.png)

### [!UICONTROL Ringdiagramm]

Ähnlich einem Tortendiagramm zeigt diese Visualisierung die Daten als Teile oder Segmente eines Ganzen. Ein Ringdiagramm kann für den Vergleich der Teile eines Ganzen verwendet werden. Nehmen wir beispielsweise an, Sie möchten sehen, welche Anzeigenplattform zur Gesamtzahl der Unique Visitors beigetragen hat:

![Ringvisualisierung](assets/donut-viz.png)

### [!UICONTROL Linie]

Die Linienvisualisierung stellt Metriken anhand einer Linie dar, die den Wertverlauf über einen bestimmten Zeitraum hinweg zeigt. Ein Liniendiagramm zeigt Dimensionen im Zeitverlauf an, funktioniert aber bei jeder Visualisierung. In diesem Beispiel visualisieren Sie die Dimension „Produktkategorie“.

![Linienvisualisierung](assets/line.png)


### [!UICONTROL Horizontalbalken]

Diese Visualisierung zeigt Horizontalbalken, die verschiedene Werte aus einer oder mehreren Metriken darstellen. Verwenden Sie zum Beispiel [!UICONTROL Horizontalbalken] als bevorzugte Visualisierung, um ganz leicht zu erkennen, welches Ihre Top-Produkte sind.

![Horizontaler Balken](assets/horizontal.png)

### Entfernen Sie [!UICONTROL nicht angegebene] Dimensionselemente

Wenn Sie [!UICONTROL nicht angegebene] Dimensionselemente aus Ihren Daten entfernen möchten, gehen Sie wie folgt vor:

1. Wählen Sie die richtige Kachel aus.
1. Wählen Sie in der rechten Leiste unter **[!UICONTROL Drill-ins]** den Rechtspfeil neben dem Dimensionselement aus, für das Sie Elemente des Typs **[!UICONTROL Nicht angegeben]** entfernen möchten.

   ![nicht angegeben](assets/unspecified.png)

1. Klicken Sie auf das Symbol neben **[!UICONTROL Nicht angegeben]**, um nicht spezifizierte Daten aus Ihrem Reporting zu entfernen. (Sie können auch jedes andere Dimensionselement entfernen.)

## Kacheleigenschaften anzeigen und konfigurieren

Wenn Sie im Scorecard Builder auf eine Kachel klicken, zeigt die rechte Leiste die Eigenschaften und Merkmale an, die mit dieser Kachel verbunden sind. In dieser Leiste können Sie einen neuen **[!UICONTROL Titel]** für die Kachel angeben. Anstatt die Kachel aus der linken Leiste zu ziehen und abzulegen können Sie sie auch konfigurieren, indem Sie Komponenten angeben.

![Kachel „Eigenschaften“](assets/properties_tile.png)

Wenn Sie auf Kacheln klicken, wird in einem dynamischen Popup angezeigt, wie die Aufschlüsselungsansicht für ausführende Benutzer in der App dargestellt wird. Wenn keine Dimension auf die Kachel angewendet wurde, werden je nach Standarddatumsbereich entweder **Stunden** oder **Tage** als Aufschlüsselungsdimension verwendet.

Aufschlüsselungen verbessern Ihre Analyse, indem sie Metriken und Dimensionen nach anderen Metriken und Dimensionen aufschlüsseln wie z. B. in diesem Beispiel eines Einzelhändlers:

* Metrik „Unique Visitors“ aufgeschlüsselt nach Anzeigenplattform (AMO-ID)
* Besuche aufgeschlüsselt nach Produktkategorie (Einzelhandel)
* Gesamtumsatz aufgeschlüsselt nach Produktnamen

![Aufschlüsselungsansicht](assets/break_view.png)

Jede der Kachel hinzugefügte Dimension wird in einer Dropdown-Liste in der Detailansicht der App angezeigt. Der ausführende Benutzer kann dann aus den in der Dropdown-Liste aufgelisteten Optionen auswählen.

## Komponenten entfernen

Um eine Komponente zu entfernen, die auf die gesamte Scorecard angewendet wird, klicken Sie auf eine beliebige Stelle außerhalb der Kacheln auf die Scorecard. Entfernen Sie die Komponente, indem Sie auf das **x** klicken, das angezeigt wird, wenn Sie den Mauszeiger über die Komponente bewegen, wie unten für das Segment **Erstbesuche** dargestellt:

![Komponenten entfernen](assets/new_remove.png)

## Scorecard benennen

Um die Scorecard zu benennen, klicken Sie auf den Namensbereich in der oberen linken Ecke des Bildschirms und geben Sie den neuen Namen ein.

![Scorecards benennen](assets/new_name.png)

## Scorecard freigeben

So geben Sie die Scorecard für einen ausführenden Benutzer frei:

1. Klicken Sie auf das Menü **[!UICONTROL Freigeben]** und wählen Sie **[!UICONTROL Scorecard freigeben]**.

1. Füllen Sie die Felder im Formular **[!UICONTROL Mobile Scorecard freigeben]** aus, indem Sie:

   * den Namen der Scorecard angeben
   * eine Beschreibung der Scorecard angeben
   * relevante Tags hinzufügen
   * die Empfänger der Scorecard angeben

1. Klicken Sie auf **[!UICONTROL Freigabe]**.

![Scorecards freigeben](assets/new_share.png)

Nachdem Sie eine Scorecard freigegeben haben, können die Empfänger in den Analytics-Dashboards darauf zugreifen. Wenn Sie in Scorecard Builder nachträgliche Änderungen an der Scorecard vornehmen, werden diese automatisch in der freigegebenen Scorecard aktualisiert. Ausführende Benutzer sehen die Änderungen, nachdem sie die Scorecard in ihrer App aktualisiert haben.

Wenn Sie die Scorecard durch Hinzufügen neuer Komponenten aktualisieren, sollten Sie die Scorecard erneut freigeben (und die Option zum **[!UICONTROL Freigeben eingebetteter Komponenten]** aktivieren), um sicherzustellen, dass die ausführenden Benutzer Zugriff auf diese Änderungen haben.