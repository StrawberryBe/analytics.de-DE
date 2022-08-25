---
description: Verwenden Sie die Flussvisualisierung in einem Workspace-Projekt.
title: Flussvisualisierung konfigurieren
feature: Visualizations
role: User, Admin
exl-id: c2fdcc96-81ac-4d3b-b255-ff805b6ff0ea
source-git-commit: c0e590dab9e45768cf8f8bd20f17d7f5306f41bd
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 96%

---

# Flussvisualisierung konfigurieren

>[!NOTE]
>
>Diese neue Version der [!UICONTROL Flussvisualisierung] wird derzeit eingeschränkt getestet.

Die aktualisierte Flussvisualisierung hilft Ihnen, die Journey zu verstehen, die von einem bestimmten Konversionsereignis auf Ihrer Website oder in Ihrer Mobile App ausgeht oder dazu führt. Die Flussvisualisierung folgt einem Pfad durch Ihre Dimensionen (und Dimensionselemente) oder Metriken. Mit der Flussvisualisierung können Sie den Anfang oder das Ende des Pfads konfigurieren, an dem Sie interessiert sind, oder alle Pfade analysieren, die durch eine Dimension oder ein Dimensionselement führen.

Die neue [!UICONTROL Fluss]-Funktion verbessert Ihren Workflow auf mehrfache Weise:

* Sie können jetzt Ihren Pfad mit der Kombination aus einer Metrik und einer Pfaddimension beginnen oder beenden.
* Die Fluss-Funktion enthält [!UICONTROL erweiterte Einstellungen], über die Sie den [!UICONTROL Fluss] zusätzlich anpassen können.
* Mit der neuen Schaltfläche „Erstellen“ sparen Sie Zeit bei der Analyse, indem Sie die Journey auf einmal konfigurieren, dann Abfragen durchführen und danach automatisch mehrere Spalten und Knoten gleichzeitig erstellen.

![Neue Fluss-Benutzeroberfläche](assets/new-flow.png)

## Konfigurationsschritte {#configure}

1. Um ein Flussdiagramm zu erstellen, fügen Sie ein leeres Bedienfeld zu Ihrem Projekt hinzu und klicken Sie in der linken Leiste auf das Visualisierungssymbol. Ziehen Sie dann die Flussvisualisierung in das Bedienfeld. Oder ziehen Sie die [!UICONTROL Flussvisualisierung] in ein vorhandenes Projekt.

1. Sie können Ihre Flussvisualisierung mithilfe einer von drei Optionen verankern:

   * [!UICONTROL Beginnt mit] (Metriken, Dimensionen oder Elemente) oder
   * [!UICONTROL Enthält] (Dimensionen oder Elemente) oder
   * [!UICONTROL Endet mit] (Metriken, Dimensionen oder Elemente)

   Jede dieser Kategorien wird auf dem Bildschirm als ein Ablagebereich angezeigt. Sie können den Ablagebereich auf drei Arten füllen:

   * Verwenden Sie das Dropdown-Menü, um Metriken oder Dimensionen auszuwählen.
   * Ziehen Sie Elemente aus der Dimensionen- oder Metrikliste.
   * Verwenden Sie die Suche, um die gewünschten Metriken oder Dimensionen zu finden.

   Nehmen wir beispielsweise an, Sie möchten alle Etappen nachverfolgen, die zu einem Checkout-Ereignis führen. In diesem Fall würden Sie eine mit dem Checkout zusammenhängende Dimension oder Metrik (z. B. [!UICONTROL Bestellung vorhanden]) in die Ablagefläche **[!UICONTROL Endet mit]** ziehen.

1. Wenn Sie eine Metrik auswählen, müssen Sie auch eine [!UICONTROL Pfaddimension], wie hier gezeigt, angeben, die Sie zum Erstellen des Pfads verwenden werden. Die Standardeinstellung ist [!UICONTROL Seite].

   ![Pfaddimension](assets/pathing-dim.png)

   >[!IMPORTANT]
   >
   >Berechnete Metriken können nicht im Ablagebereich **[!UICONTROL Beginnt mit]** oder **[!UICONTROL Endet mit]** abgelegt werden.

1. (Optional) Klicken Sie auf **[!UICONTROL Erweiterte Einstellungen anzeigen]**, um die erweiterten Einstellungen zu konfigurieren:

   ![Erweiterte Einstellungen](assets/adv-settings.png)

   | Einstellung | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Beschriftungen umbrechen]** | Die Bezeichnungen der Flusselemente werden üblicherweise aus Platzgründen auf dem Bildschirm abgeschnitten. Aktivieren Sie dieses Kontrollkästchen, um die gesamte Bezeichnung anzuzeigen.  Standard = deaktiviert. |
   | **[!UICONTROL Wiederholungsinstanzen einschließen]** | Flussvisualisierungen basieren auf Instanzen einer Dimension. Diese Einstellung gibt Ihnen die Möglichkeit, wiederholte Instanzen ein- oder auszuschließen, z. B. Seitenneuladungen. Wiederholungen können jedoch nicht aus Flussvisualisierungen entfernt werden, die Dimensionen mit mehreren Werten enthalten, wie listVars, listProps, s.product, Merchandising-eVars usw. Standard = deaktiviert. |
   | **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** | Begrenzen Sie Pfade auf jene, die mit dem ersten/letzten Vorkommen einer Dimension/eines Elements/einer Metrik beginnen/enden. Eine ausführlichere Erläuterung finden Sie im folgenden Abschnitt unter dem Titel „Beispielszenario für die Beschränkung auf das erste/letzte Auftreten“. |
   | **[!UICONTROL Anzahl der Spalten]** | Gibt an, wie viele Spalten Sie in Ihrem Flussdiagramm anzeigen möchten. |
   | **[!UICONTROL Erweiterte Elemente pro Spalte]** | Wie viele Elemente Sie in jeder Spalte anzeigen möchten. |
   | **[!UICONTROL Fluss-Container]** | <ul><li>Besuch</li><li>Besucher.</li></ul> Hiermit können Sie bei der Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Mithilfe dieser Einstellungen können Sie Einblicke in Besucheraktivitäten auf der Besucherebene (besuchsübergreifend) erhalten oder die Analyse auf einen einzelnen Besuch einschränken. |

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Flussausgabe anzeigen und ändern {#output}

![Flussausgabe](assets/flow-output.png)

Eine Zusammenfassung der Flusskonfiguration wird oben im Diagramm angezeigt. Die Pfade in dem Diagramm sind proportional. Pfade mit mehr Aktivität werden dicker dargestellt.

Um die Daten weiter zu untersuchen, haben Sie mehrere Möglichkeiten:

* Das Flussdiagramm ist interaktiv. Wenn Sie den Mauszeiger über das Diagramm halten, werden jeweils andere Details angezeigt.

* Wenn Sie auf einen Knoten in dem Diagramm klicken, werden die zugehörigen Details zu diesem Knoten angezeigt. Klicken Sie erneut auf den Knoten, um ihn wieder zu reduzieren.

   ![Knoten-Details](assets/node-details.png)

* Sie können eine Spalte so filtern, dass nur bestimmte Ergebnisse angezeigt werden, z. B. das Ein- und Ausschließen, die Angabe von Kriterien usw.

* Klicken Sie links auf das Pluszeichen (+), um eine Spalte zu erweitern.

* Verwenden Sie die unten erläuterten Rechtsklickoptionen, um die Ausgabe weiter anzupassen.

* Klicken Sie auf das Stiftsymbol neben der Konfigurationsübersicht, um den Fluss weiter zu bearbeiten oder ihn mit verschiedenen Optionen neu zu erstellen.

* Sie können Ihr Flussdiagramm als Teil der .CSV-Datei eines Projekts auch exportieren und weiter analysieren, indem Sie **[!UICONTROL Projekt]** > **[!UICONTROL CSV herunterladen]** aufrufen.

## Filtern

Über jeder Spalte wird ein Filter angezeigt, wenn Sie den Mauszeiger darüber bewegen. Wenn Sie auf den Filter klicken, sehen Sie dasselbe Filterdialogfeld, das heute auch in der Freiformtabelle vorhanden ist. Dieser Filter funktioniert genauso wie in der Freiformtabelle.

* Verwenden Sie die erweiterten Einstellungen, um bestimmte Kriterien in die Benutzerliste aufzunehmen oder auszuschließen.
* Nachdem Sie ein Element aus der Liste gefiltert haben, spiegelt diese Spalte die Filterung wider. (Der Filter reduziert sie entweder, um nur das im Filter zulässige Element anzuzeigen, oder er entfernt alle Elemente mit Ausnahme des Elements, das Sie im Filter verwenden möchten.
* Alle nachgelagerten und vorgelagerten Spalten sollten beibehalten werden, solange Daten in die verbleibenden Knoten fließen.
* Nach der Anwendung wird das Filtersymbol in Blau über der Spalte angezeigt, die gefiltert wird.
* Um einen Filter zu entfernen, klicken Sie auf das Filtersymbol, um das Filtermenü zu öffnen. Entfernen Sie alle angewendeten Filter und klicken Sie dann auf **[!UICONTROL Speichern]**. Der Fluss sollte zum vorherigen, ungefilterten Status zurückkehren.

## Rechtsklick-Optionen {#right-click}

| Option | Beschreibung |
|--- |--- |
| [!UICONTROL Auf diesen Knoten fokussieren] | Wechselt den Fokus auf den ausgewählten Knoten. Der Fokusknoten wird in der Mitte des Flussdiagramms angezeigt. |
| [!UICONTROL Neu starten] | Bringt Sie wieder zurück in den Freiform-Diagramm-Builder, in dem Sie ein neues Flussdiagramm erstellen können. |
| [!UICONTROL Segment von diesem Punkt im Fluss aus erstellen] | Erstellen eines Segments. Hiermit gelangen Sie in den Segment Builder, in dem Sie das neue Segment einrichten können. |
| [!UICONTROL Aufschlüsselung] | Hiermit können Sie den Knoten nach verfügbaren Dimensionen, Metriken oder Zeiten aufschlüsseln. |
| [!UICONTROL Trend] | Mit dieser Option erstellen Sie ein Trenddiagramm für den Knoten. |
| [!UICONTROL Gesamte Spalte erweitern] | Hiermit erweitern Sie eine Spalte so, dass alle Knoten angezeigt werden. In der Standardeinstellung werden nur die obersten fünf Knoten angezeigt. |
| [!UICONTROL Gesamte Spalte reduzieren] | Diese Option blendet alle Knoten in einer Spalte aus. |
| [!UICONTROL Element ausschließen]/[!UICONTROL Ausgeschlossene Elemente wiederherstellen] | Entfernt einen bestimmten Knoten aus der Spalte und erstellt daraus automatisch einen Filter oben in der Spalte. Um das ausgeschlossene Element wiederherzustellen, klicken Sie erneut mit der rechten Maustaste und wählen Sie **[!UICONTROL Ausgeschlossenes Element wiederherstellen]**. Sie können den Filter auch oben in der Spalte öffnen und die Box mit dem Element entfernen, das Sie gerade ausgeschlossen haben. |

## Beispielszenario für „Beschränkung auf das erste/letzte Vorkommen“

Beachten Sie bei Verwendung dieser Option Folgendes:

* **[!UICONTROL Auf das erste/letzte Vorkommen beschränken]** zählt nur das erste/letzte Vorkommen in der Reihe. Alle anderen Vorkommen der Kriterien **[!UICONTROL Beginnt mit]** oder **[!UICONTROL Endet mit]** werden verworfen.
* Bei Verwendung mit einem Fluss des Typs **[!UICONTROL Beginnt mit]** wird nur das erste Vorkommen einbezogen, das den Startkriterien entspricht.
* Bei Verwendung mit einem Fluss des Typs **[!UICONTROL Endet mit]** wird nur das letzte Vorkommen einbezogen, das den Endkriterien entspricht.
* Die verwendete Reihe unterscheidet sich je nach Container. Bei Verwendung des Containers **[!UICONTROL Besuch]** wird die Trefferreihe die Sitzung sein. Bei Verwendung des Containers **[!UICONTROL Besucher]** besteht die Trefferreihe aus allen Treffern einer bestimmten benutzenden Person im bereitgestellten Datumsbereich.
* Die Option **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** kann in den erweiterten Einstellungen konfiguriert werden, wenn eine Metrik oder ein Element der Dimension in den Feldern „Beginnt mit“ oder „Endet mit“ verwendet wird.

Beispielreihe von Treffern:

Startseite > Produkte > Zum Warenkorb hinzufügen > Produkte > Zum Warenkorb hinzufügen > Rechnungsstellung > Bestellbestätigung

### Betrachten Sie eine Flussanalyse mit den folgenden Einstellungen:

* Beginn mit [!UICONTROL Zum Warenkorb hinzufügen] (Dimensionselement)
* Pfaddimension [!UICONTROL Seite]
* Container [!UICONTROL Besuch]

Wenn **[!UICONTROL Auf das erste/letzte Vorkommen beschränken]** is *disabled*und dann zählt diese einzelne Trefferreihe zwei Instanzen von &quot;Zum Warenkorb hinzufügen&quot;.
Erwartete Flussausgabe: 
„Zum Warenkorb hinzufügen“ (2) —> „Produkte“ (1)
-> „Rechnungsstellung“ (1)

Wenn **[!UICONTROL Auf das erste/letzte Vorkommen beschränken]** is *enabled*, wird nur das erste Vorkommen von &quot;Zum Warenkorb hinzufügen&quot;in die Analyse aufgenommen.
Erwartete Flussausgabe:
„Zum Warenkorb hinzufügen“ (1) —> „Produkte“ (1)

### Betrachten Sie die gleiche Reihe von Treffern, jedoch unter Verwendung der folgenden Einstellungen:

* Endet mit [!UICONTROL Zum Warenkorb hinzufügen] (Dimensionselement)
* Pfaddimension [!UICONTROL Seite]
* Container [!UICONTROL Besuch]

Wenn die Option **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** *deaktiviert* ist, würde diese einzelne Trefferreihe zwei Vorkommnisse von „Zum Warenkorb hinzufügen“ zählen.
Erwartete Flussausgabe: 
„Produkte“ (2) &lt;— „Zum Warenkorb hinzufügen“ (2)

Wenn jedoch **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** *aktiviert* ist, würde nur das letzte Auftreten von [!UICONTROL Zum Warenkorb hinzufügen] in die Analyse einbezogen.
Erwartete Flussausgabe: 
„Produkte“ (1) &lt;— „Zum Warenkorb hinzufügen“ (1)
