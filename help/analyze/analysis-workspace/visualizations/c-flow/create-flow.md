---
description: Verwenden Sie die Flussvisualisierung in einem Workspace-Projekt.
title: Konfigurieren einer Flussvisualisierung
feature: Visualizations
role: User, Admin
exl-id: c2fdcc96-81ac-4d3b-b255-ff805b6ff0ea
source-git-commit: ec466d2a503278b05d19eda09e2a2244897ce1f3
workflow-type: ht
source-wordcount: '1417'
ht-degree: 100%

---

# Konfigurieren einer Flussvisualisierung

Flussvisualisierungen helfen Ihnen, die Journey zu verstehen, die von einem bestimmten Konversionsereignis auf Ihrer Website oder in Ihrer Mobile App ausgeht oder dazu führt. Die Flussvisualisierung folgt einem Pfad durch Ihre Dimensionen (und Dimensionselemente) oder Metriken.

Mit Flussvisualisierungen können Sie den Anfang oder das Ende des Pfads konfigurieren, an dem Sie interessiert sind, oder alle Pfade analysieren, die durch eine Dimension oder ein Dimensionselement führen.

![Neue Fluss-Benutzeroberfläche](assets/new-flow.png)

## Erstellen einer Flussvisualisierung {#configure}

1. Fügen Sie ein leeres Bedienfeld zu Ihrem Projekt hinzu und klicken Sie in der linken Leiste auf das Visualisierungssymbol.

   Oder

   Fügen Sie eine Visualisierung mit einer der Methoden hinzu, die im Abschnitt „Hinzufügen von Visualisierungen zu einem Bedienfeld“ in [Überblick über Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) beschrieben sind.

1. Sie können Ihre Flussvisualisierung mithilfe einer der folgenden Optionen verankern:

   * [!UICONTROL **Beginnt mit**] (Metriken, Dimensionen oder Elemente) oder
   * [!UICONTROL **Enthält**] (Dimensionen oder Elemente) oder
   * [!UICONTROL **Endet mit**] (Metriken, Dimensionen oder Elemente)

   Jede dieser Kategorien wird auf dem Bildschirm als ein Ablagebereich angezeigt. Sie können den Ablagebereich auf drei Arten füllen:

   * Verwenden Sie das Dropdown-Menü, um Metriken oder Dimensionen auszuwählen.
   * Ziehen Sie Dimensionen oder Metriken aus der linken Leiste.
   * Beginnen Sie mit der Eingabe des Namens einer Dimension oder Metrik und wählen Sie sie dann aus, wenn sie in der Dropdown-Liste angezeigt wird.

   >[!IMPORTANT]
   >
   >Berechnete Metriken können nicht im Feld **[!UICONTROL Beginnt mit]** oder **[!UICONTROL Endet mit]** verwendet werden.

1. Wenn Sie eine Metrik auswählen, müssen Sie auch eine [!UICONTROL **Pfaddimension**] bereitstellen, die als Pfad verwendet wird, der zu Ihrer ausgewählten Komponente führt oder von dieser weg führt, wie hier dargestellt. Die Standardeinstellung ist [!UICONTROL **Seite**].

   ![Pfaddimension](assets/pathing-dim.png)

1. (Optional) Wählen Sie **[!UICONTROL Erweiterte Einstellungen anzeigen]** aus, um eine der folgenden Optionen zu konfigurieren:

   ![Erweiterte Einstellungen](assets/adv-settings.png)

   | Einstellung | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Beschriftungen umbrechen]** | Die Bezeichnungen der Flusselemente werden üblicherweise aus Platzgründen auf dem Bildschirm abgeschnitten. Aktivieren Sie dieses Kontrollkästchen, um die gesamte Bezeichnung anzuzeigen.  Standard = deaktiviert. |
   | **[!UICONTROL Wiederholungsinstanzen einschließen]** | Flussvisualisierungen basieren auf Instanzen einer Dimension. Diese Einstellung gibt Ihnen die Möglichkeit, wiederholte Instanzen ein- oder auszuschließen, z. B. Seitenneuladungen. Wiederholungen können jedoch nicht aus Flussvisualisierungen entfernt werden, die Dimensionen mit mehreren Werten enthalten, wie listVars, listProps, s.product, Merchandising-eVars usw. <p>Standardmäßig ist diese Option deaktiviert.</p> |
   | **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** | Begrenzen Sie Pfade auf jene, die mit dem ersten/letzten Vorkommen einer Dimension/eines Elements/einer Metrik beginnen/enden. Eine ausführlichere Erläuterung finden Sie im nachfolgenden Abschnitt [Beispielszenario für die Beschränkung auf das erste/letzte Auftreten](#example-scenario-for-limit-to-firstlast-occurrence). |
   | **[!UICONTROL Anzahl der Spalten]** | Die Anzahl der Spalten, die Ihr Flussdiagramm enthalten soll. Sie können maximal 5 Spalten angeben. |
   | **[!UICONTROL Erweiterte Elemente pro Spalte]** | Die Anzahl der Elemente, die jede Spalte enthalten soll. Sie können pro Spalte maximal 10 erweiterte Elemente angeben. |
   | **[!UICONTROL Fluss-Container]** | <ul><li>Besuch</li><li>Besucher.</li></ul> Hiermit können Sie bei der Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Mithilfe dieser Einstellungen können Sie Einblicke in Besucheraktivitäten auf der Besucherebene (besuchsübergreifend) erhalten oder die Analyse auf einen einzelnen Besuch einschränken. |

   >[!IMPORTANT]
   >
   >Die Kombination von **[!UICONTROL Anzahl der Spalten]** und **[!UICONTROL Erweiterte Elemente pro Spalte]** bestimmt die Anzahl der zugrunde liegenden Anfragen, die zum Erstellen der Flussvisualisierung erforderlich sind. Je höher diese Zahlen sind, desto länger dauert das Rendern einer Visualisierung.

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

>[!INFO]
>
>**Beispiel:** Angenommen, Sie möchten den Pfad verfolgen, den Benutzende zu und von den beliebtesten Seiten Ihrer Site eingeschlagen haben.
>
>Dazu gehen Sie wie folgt vor:
> 
>1. Erstellen Sie eine Flussvisualisierung, wie oben beschrieben.
>1. Ziehen Sie die Dimension [!UICONTROL **Seite**] in das Feld **[!UICONTROL Enthält]** und wählen Sie [!UICONTROL **Erstellen**] aus.
>1. Die Flussvisualisierung wird mit der am häufigsten angezeigten Seite erstellt, die im Fokusknoten in der Mitte der Visualisierung angezeigt wird. Sie sehen auch die Top-Seiten, die zu dieser Seite führen (links neben dem Fokusknoten), sowie die Top-Seiten, die aus dieser Fokusseite führen (rechts neben dem Fokusknoten).
>1. Analysieren Sie die Daten im Fluss, wie unter [Flussausgabe anzeigen und ändern](#view-and-change-the-flow-output) beschrieben.


## Flussausgabe anzeigen und ändern {#output}

![Flussausgabe](assets/flow-output.png)

Eine Zusammenfassung der Flusskonfiguration wird oben im Diagramm angezeigt. Die Anzeigedicke eines Pfads im Diagramm ist proportional zu seiner Aktivität, wobei Pfade mit mehr Aktivität dicker angezeigt werden als Pfade mit weniger Aktivität.

Um die Daten weiter zu untersuchen, haben Sie mehrere Möglichkeiten:

* Das Flussdiagramm ist interaktiv. Wenn Sie den Mauszeiger über das Diagramm halten, werden jeweils andere Details angezeigt.

* Wenn Sie einen Knoten in dem Diagramm auswählen, werden die zugehörigen Details zu diesem Knoten angezeigt. Wählen Sie den Knoten erneut aus, um ihn wieder zu reduzieren.

  ![Knoten-Details](assets/node-details.png)

* Sie können eine Spalte so filtern, dass nur bestimmte Ergebnisse angezeigt werden, z. B. das Ein- und Ausschließen, das Angeben von Kriterien usw.

* Wählen Sie links das Pluszeichen (+) aus, um eine Spalte zu erweitern.

* Verwenden Sie die unten erläuterten Rechtsklickoptionen, um die Ausgabe weiter anzupassen.

* Wählen Sie das Stiftsymbol neben der Konfigurationsübersicht aus, um den Fluss weiter zu bearbeiten oder ihn mit verschiedenen Optionen neu zu erstellen.

* Sie können Ihr Flussdiagramm als Teil der CSV-Datei eines Projekts auch exportieren und weiter analysieren, indem Sie **[!UICONTROL Projekt]** > **[!UICONTROL CSV herunterladen]** aufrufen.

## Filtern

Über jeder Spalte wird ein Filter angezeigt, wenn Sie den Mauszeiger darüber bewegen. Wenn Sie den Filter auswählen, sehen Sie dasselbe Filterdialogfeld, das heute auch in der Freiformtabelle vorhanden ist. Dieser Filter funktioniert genauso wie in der Freiformtabelle.

* Verwenden Sie die erweiterten Einstellungen, um bestimmte Kriterien in die Benutzerliste aufzunehmen oder auszuschließen.
* Nachdem Sie ein Element aus der Liste gefiltert haben, spiegelt diese Spalte die Filterung wider. (Der Filter reduziert sie entweder, um nur das im Filter zulässige Element anzuzeigen, oder er entfernt alle Elemente mit Ausnahme des Elements, das Sie im Filter verwenden möchten.
* Alle nachgelagerten und vorgelagerten Spalten sollten beibehalten werden, solange Daten in die verbleibenden Knoten fließen.
* Nach der Anwendung wird das Filtersymbol in Blau über der Spalte angezeigt, die gefiltert wird.
* Um einen Filter zu entfernen, klicken Sie auf das Filtersymbol. Daraufhin wird das Filtermenü geöffnet. Entfernen Sie alle angewendeten Filter und wählen Sie **[!UICONTROL Speichern]** aus. Der Fluss sollte zum vorherigen, ungefilterten Status zurückkehren.

## Rechtsklick-Optionen {#right-click}

| Option | Beschreibung |
|--- |--- |
| [!UICONTROL Neu starten] | Bringt Sie wieder zurück in den Freiform-Diagramm-Builder, in dem Sie ein neues Flussdiagramm erstellen können. |
| [!UICONTROL Segment für diesen Pfad erstellen] | Erstellen eines Segments. Hiermit gelangen Sie in den Segment Builder, in dem Sie das neue Segment einrichten können. |
| [!UICONTROL Aufschlüsselung] | Hiermit können Sie den Knoten nach verfügbaren Dimensionen, Metriken oder Zeiten aufschlüsseln. |
| [!UICONTROL Trend] | Mit dieser Option erstellen Sie ein Trenddiagramm für den Knoten. |
| Nächste Spalte anzeigen/Vorherige Spalte anzeigen | Zeigt die nächste (rechte) oder vorherige (linke) Spalte der Visualisierung an. |
| Spalte ausblenden | Blendet die ausgewählte Spalte aus der Visualisierung aus. |
| [!UICONTROL Gesamte Spalte erweitern] | Hiermit erweitern Sie eine Spalte so, dass alle Knoten angezeigt werden. In der Standardeinstellung werden nur die obersten fünf Knoten angezeigt. |

## Beispielszenario für „Beschränkung auf das erste/letzte Vorkommen“

Beachten Sie bei Verwendung dieser Option Folgendes:

* **[!UICONTROL Auf das erste/letzte Vorkommen beschränken]** zählt nur das erste/letzte Vorkommen in der Reihe. Alle anderen Vorkommen der Kriterien **[!UICONTROL Beginnt mit]** oder **[!UICONTROL Endet mit]** werden verworfen.
* Bei Verwendung mit einem Fluss des Typs **[!UICONTROL Beginnt mit]** wird nur das erste Vorkommen einbezogen, das den Startkriterien entspricht.
* Bei Verwendung mit einem Fluss des Typs **[!UICONTROL Endet mit]** wird nur das letzte Vorkommen einbezogen, das den Endkriterien entspricht.
* Die verwendete Reihe unterscheidet sich je nach Container. Bei Verwendung des Containers **[!UICONTROL Besuch]** wird die Trefferreihe die Sitzung sein. Bei Verwendung des Containers **[!UICONTROL Besucher]** besteht die Trefferreihe aus allen Treffern einer bestimmten benutzenden Person im bereitgestellten Datumsbereich.
* Die Option **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** kann in den erweiterten Einstellungen konfiguriert werden, wenn ein Metrik- oder Dimensionselement in den Feldern „Beginnt mit“ oder „Endet mit“ verwendet wird.

Beispielreihe von Treffern:

Startseite > Produkte > Zum Warenkorb hinzufügen > Produkte > Zum Warenkorb hinzufügen > Rechnungsstellung > Bestellbestätigung

### Betrachten Sie eine Flussanalyse mit den folgenden Einstellungen:

* Beginn mit [!UICONTROL Zum Warenkorb hinzufügen] (Dimensionselement)
* Pfaddimension [!UICONTROL Seite]
* Container [!UICONTROL Besuch]

Wenn die Option **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** *deaktiviert* ist, zählt diese einzelne Trefferreihe als zwei Vorkommnisse von „Zum Warenkorb hinzufügen“.
Erwartete Flussausgabe: 
„Zum Warenkorb hinzufügen“ (2) —> „Produkte“ (1)
-> „Rechnungsstellung“ (1)

Wenn jedoch **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** *aktiviert* ist, wird nur das erste Vorkommnis von „Zum Warenkorb hinzufügen“ in die Analyse aufgenommen.
Erwartete Flussausgabe:
„Zum Warenkorb hinzufügen“ (1) —> „Produkte“ (1)

### Betrachten Sie die gleiche Reihe von Treffern, jedoch unter Verwendung der folgenden Einstellungen:

* Endet mit [!UICONTROL Zum Warenkorb hinzufügen] (Dimensionselement)
* Pfaddimension [!UICONTROL Seite]
* Container [!UICONTROL Besuch]

Wenn die Option **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** *deaktiviert* ist, zählt diese einzelne Trefferreihe als zwei Vorkommnisse von „Zum Warenkorb hinzufügen“.
Erwartete Flussausgabe: 
„Produkte“ (2) &lt;— „Zum Warenkorb hinzufügen“ (2)

Wenn jedoch **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** *aktiviert* ist, würde nur das letzte Auftreten von [!UICONTROL Zum Warenkorb hinzufügen] in die Analyse einbezogen.
Erwartete Flussausgabe: 
„Produkte“ (1) &lt;— „Zum Warenkorb hinzufügen“ (1)
