---
description: Verwenden Sie die Flussvisualisierung in einem Workspace-Projekt.
title: Flussvisualisierung konfigurieren
feature: Visualizations
role: User, Admin
exl-id: c2fdcc96-81ac-4d3b-b255-ff805b6ff0ea
source-git-commit: bef175d9675134f4932407a0b9e4a3c67b1d27a5
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 23%

---

# Flussvisualisierung konfigurieren

>[!NOTE]
>
>Diese neue Version der [!UICONTROL Fluss] Die Visualisierung wird derzeit nur eingeschränkt getestet.

Mit der aktualisierten Flussvisualisierung können Sie die Journey verstehen, die von einem bestimmten Konversionsereignis auf Ihrer Website oder in Ihrer App ausgehen oder dazu führen. Sie verfolgt einen Pfad durch Ihre Dimensionen (und Dimensionselemente) oder Metriken. Mit &quot;Fluss&quot;können Sie den Anfang oder das Ende des Pfades konfigurieren, an dem Sie interessiert sind, oder alle Pfade analysieren, die durch eine Dimension oder ein Dimensionselement fließen.

Die neue [!UICONTROL Fluss] Erlebnis verbessert Ihren Workflow auf verschiedene Weise:

* Sie können jetzt Ihren Pfad mit der Kombination aus einer Metrik und einer Pfaddimension starten oder beenden.
* Enthält [!UICONTROL Erweiterte Einstellungen] , damit Sie die [!UICONTROL Fluss].
* Mit der neuen Schaltfläche &quot;Erstellen&quot;sparen Sie Zeit in der Analyse, indem Sie die Journey alle gleichzeitig konfigurieren, dann Abfragen und dann automatisch mehrere Spalten und Knoten gleichzeitig &#x200B; erstellen können.

![Neue Fluss-Benutzeroberfläche](assets/new-flow.png)

## Konfigurationsschritte {#configure}

1. Um ein Flussdiagramm zu erstellen, fügen Sie ein leeres Bedienfeld zu Ihrem Projekt hinzu und klicken Sie in der linken Leiste auf das Symbol für Visualisierungen . Ziehen Sie dann die Flussvisualisierung in das Bedienfeld. Oder ziehen Sie die [!UICONTROL Fluss] Visualisierung in ein vorhandenes Projekt.

1. Sie können Ihre Flussvisualisierung mit einer von drei Optionen verankern:

   * [!UICONTROL Beginnt mit] (Metriken, Dimensionen oder Elemente) oder
   * [!UICONTROL Enthält] (Dimensionen oder Elemente) oder
   * [!UICONTROL Endet in] (Metriken, Dimensionen oder Elemente)

   Jede dieser Kategorien wird auf dem Bildschirm als eine „Dropzone“ (Ablagebereich) angezeigt. Sie können die Dropzone auf drei Arten füllen:

   * Verwenden Sie das Dropdown-Menü, um Metriken oder Dimensionen auszuwählen.
   * Ziehen Sie Elemente aus der Dimensionen- oder Metrikliste.
   * Verwenden Sie die Suche, um die gewünschten Metriken oder Dimensionen zu finden.

   Nehmen wir beispielsweise an, Sie möchten alles nachverfolgen, was zu einem Checkout-Ereignis führt. Sie würden eine mit dem Checkout zusammenhängende Dimension oder Metrik ziehen (z. B. [!UICONTROL Reihenfolge vorhanden]) in die **[!UICONTROL Endet in]** Dropzone.

1. Wenn Sie eine Metrik auswählen, müssen Sie auch eine [!UICONTROL Pathing-Dimension], wie hier gezeigt, verwenden Sie zum Erstellen des Pfads. Der Standardwert ist [!UICONTROL Seite].

   ![Pfaddimension](assets/pathing-dim.png)

   >[!IMPORTANT]
   >
   >Berechnete Metriken können nicht im  **[!UICONTROL Beginnt mit]** oder **[!UICONTROL Endet in]** Ablageflächen.

1. (Optional) Klicken Sie auf **[!UICONTROL Erweiterte Einstellungen anzeigen]** zum Konfigurieren der erweiterten Einstellungen:

   ![Erweiterte Einstellungen](assets/adv-settings.png)

   | Einstellung | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Umbruch-Bezeichnungen]** | Die Bezeichnungen der Flusselemente werden üblicherweise aus Platzgründen auf dem Bildschirm abgeschnitten. Aktivieren Sie dieses Kontrollkästchen, um die gesamte Bezeichnung anzuzeigen.  Standard = deaktiviert. |
   | **[!UICONTROL Wiederholungsinstanzen einschließen]** | Flussvisualisierungen basieren auf Instanzen einer Dimension. Diese Einstellung gibt Ihnen die Möglichkeit, wiederholte Instanzen ein- oder auszuschließen, z. B. Seitenneuladungen. Wiederholungen können jedoch nicht aus Flussvisualisierungen entfernt werden, die Dimensionen mit mehreren Werten enthalten, wie listVars, listProps, s.product, Merchandising-eVars usw. Standard = deaktiviert. |
   | **[!UICONTROL Begrenzung auf erstes/letztes Auftreten]** | Begrenzen Sie Pfade auf Pfade, die mit dem ersten/letzten Vorkommen einer Dimension/eines Elements/einer Metrik beginnen/enden. Eine ausführlichere Erläuterung finden Sie im folgenden Abschnitt mit dem Titel &quot;Beispielszenario für die Beschränkung auf das erste/letzte Auftreten&quot;. |
   | **[!UICONTROL Anzahl der Spalten]** | Legt fest, wie viele Spalten Sie in Ihrem Flussdiagramm anzeigen möchten. |
   | **[!UICONTROL Elemente pro Spalte erweitert]** | Wie viele Elemente Sie in jeder Spalte anzeigen möchten. |
   | **[!UICONTROL Fluss-Container]** | <ul><li>Besuch</li><li>Besucher.</li></ul> Hiermit können Sie bei der Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Mithilfe dieser Einstellungen können Sie Einblicke in Besucheraktivitäten auf der Besucherebene (besuchsübergreifend) erhalten oder die Analyse auf einen einzelnen Besuch einschränken. |

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Flussausgabe anzeigen und ändern {#output}

![Flussausgabe](assets/flow-output.png)

Eine Zusammenfassung der Flusskonfiguration wird oben im Diagramm angezeigt. Die Pfade in dem Diagramm sind proportional. Pfade mit mehr Aktivität werden dicker dargestellt.

Um die Daten weiter zu untersuchen, haben Sie mehrere Möglichkeiten:

* Das Flussdiagramm ist interaktiv. Wenn Sie den Mauszeiger über das Diagramm halten, werden jeweils andere Details angezeigt.

* Wenn Sie auf einen Knoten in dem Diagramm klicken, werden die zugehörigen Details zu diesem Knoten angezeigt. Klicken Sie erneut auf den Knoten, um ihn zu reduzieren.

   ![node-details](assets/node-details.png)

* Sie können eine Spalte so filtern, dass nur bestimmte Ergebnisse angezeigt werden, z. B. das Ein- und Ausschließen, die Angabe von Kriterien usw.

* Klicken Sie links auf das Pluszeichen (+), um eine Spalte zu erweitern.

* Verwenden Sie die unten erläuterten Rechtsklickoptionen, um die Ausgabe weiter anzupassen.

* Klicken Sie auf das Stiftsymbol neben der Konfigurationsübersicht, um den Fluss weiter zu bearbeiten oder ihn mit verschiedenen Optionen neu zu erstellen.

* Sie können Ihr Flussdiagramm als Teil der .CSV-Datei eines Projekts auch exportieren und weiter analysieren, indem Sie **[!UICONTROL Projekt]** > **[!UICONTROL CSV herunterladen]** aufrufen.

## Filtern

Über jeder Spalte wird ein Filter angezeigt, wenn Sie den Mauszeiger darüber bewegen. Wenn Sie auf den Filter klicken, erhalten Sie dasselbe Filterdialogfeld, das auch heute in der Freiformtabelle vorhanden ist. Dieser Filter funktioniert genauso wie in der Freiformtabelle.

* Verwenden Sie erweiterte Einstellungen, um bestimmte Kriterien in unsere Benutzerliste aufzunehmen oder auszuschließen.
* Nachdem Sie ein Element aus der Liste gefiltert haben, spiegelt diese Spalte die Filterung wider. (Der Filter reduziert ihn entweder, um nur das im Filter zulässige Element anzuzeigen, oder er entfernt alle Elemente mit Ausnahme des Elements, das Sie im Filter verwenden möchten.
* Alle nachgelagerten und vorgelagerten Spalten sollten beibehalten werden, solange Daten in die verbleibenden Knoten fließen.
* Nach der Anwendung wird das Filtersymbol in Blau über der Spalte angezeigt, in der es gefiltert wird.
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
| [!UICONTROL Element ausschließen]/[!UICONTROL Ausgeschlossene Elemente wiederherstellen] | Entfernt einen bestimmten Knoten aus der Spalte und erstellt ihn automatisch als Filter oben in der Spalte. Um das ausgeschlossene Element wiederherzustellen, klicken Sie erneut mit der rechten Maustaste und wählen Sie **[!UICONTROL Ausgeschlossenes Element wiederherstellen]**. Sie können den Filter auch oben in der Spalte öffnen und die Säule mit dem Element entfernen, das Sie gerade ausgeschlossen haben. |

## Beispielszenario für &quot;Beschränkung auf das erste/letzte Vorkommen&quot;

Beachten Sie bei Verwendung dieser Option Folgendes:

* **[!UICONTROL Auf das erste/letzte Vorkommen beschränken]** zählt nur das erste/letzte Vorkommen in der Reihe. Alle anderen Vorkommen der **[!UICONTROL Beginnt mit]** oder **[!UICONTROL Endet in]** -Kriterien verworfen werden.
* Bei Verwendung mit **[!UICONTROL Beginnt mit]** fließen, wird nur das erste Vorkommen einbezogen, das den Startkriterien entspricht.
* Bei Verwendung mit **[!UICONTROL Endet in]** fließen, wird nur das letzte Vorkommen einbezogen, das den Endkriterien entspricht.
* Die verwendete Serie unterscheidet sich je nach Container. Wenn Sie **[!UICONTROL Besuch]** -Container ist, wird die Trefferreihe die Sitzung sein. Wenn Sie **[!UICONTROL Besucher]** -Container enthält, sind alle Treffer aus der Trefferreihe eines bestimmten Benutzers im bereitgestellten Datumsbereich.
* Die **[!UICONTROL Auf das erste/letzte Vorkommen beschränken]** kann in den erweiterten Einstellungen konfiguriert werden, wenn eine Metrik oder ein Element der Dimension in den Feldern &quot;Beginnt mit&quot;oder &quot;Endet mit&quot;verwendet wird.

Beispielreihe von Treffern:

Startseite > Produkte > Zum Warenkorb hinzufügen > Produkte > Zum Warenkorb hinzufügen > Rechnungsstellung > Bestellbestätigung

### Ziehen Sie eine Flussanalyse mit den folgenden Einstellungen in Erwägung:

* Beginnen mit[!UICONTROL  Zum Warenkorb hinzufügen] (Dimension Item)
* [!UICONTROL Seite] Pfaddimension
* [!UICONTROL Besuch] container

Wenn &quot;Auf das erste/letzte Vorkommen beschränken&quot;deaktiviert ist, würde diese einzelne Trefferreihe zwei Vorkommen von &quot;Zum Warenkorb hinzufügen&quot;zählen.
Erwartete Flussausgabe: &quot;Zum Warenkorb hinzufügen&quot;(2) —> &quot;Produkte&quot;(1) -> &quot;Rechnungsstellung&quot;(1)

Wenn jedoch &quot;Auf das erste/letzte Vorkommen begrenzen&quot;aktiviert ist, wird nur das erste Vorkommen von &quot;Zum Warenkorb hinzufügen&quot;in die Analyse aufgenommen.
Erwartete Flussausgabe: &quot;Zum Warenkorb hinzufügen&quot;(1) —> &quot;Produkte&quot;(1)

### Betrachten Sie die gleiche Reihe von Treffern, verwenden Sie jedoch die folgenden Einstellungen:

* Endet in [!UICONTROL Zum Warenkorb hinzufügen] (Dimension Item)
* [!UICONTROL Seite] Pfaddimension
* [!UICONTROL Besuch] container

Wenn **[!UICONTROL Auf das erste/letzte Vorkommen beschränken]** is *disabled*festgelegt ist, würde diese einzelne Trefferreihe zwei Vorkommen von &quot;Zum Warenkorb hinzufügen&quot;zählen.
Erwartete Flussausgabe: &quot;Products&quot; (2) &lt;— &quot;Add to cart&quot; (2)

Wenn **[!UICONTROL Auf das erste/letzte Vorkommen beschränken]** is *enabled*, nur das letzte Vorkommen von [!UICONTROL Zum Warenkorb hinzufügen] in die Analyse einbezogen werden.
Erwartete Flussausgabe: &quot;Produkte&quot;(1) &lt;— &quot;Zum Warenkorb hinzufügen&quot;(1)
