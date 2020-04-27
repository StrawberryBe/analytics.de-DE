---
description: Bevor Sie damit beginnen, einem Arbeitsblatt Elemente zuzuordnen, stellen Sie sicher, dass das Arbeitsblatt nicht schreibgeschützt ist. Wenn ein bestehender Schutz für das Arbeitsblatt die Benutzerinteraktion verhindert, können Sie keine Zellen darin auswählen. Heben Sie zunächst den Schreibschutz auf und beginnen Sie dann mit der Zuordnung von Elementen zu Zellen.
title: Metriken und Dimensionen Zellen zuordnen
topic: Report builder
uuid: 50893e1c-5f2c-4558-8001-41e70d74d6e7
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Metriken und Dimensionen Zellen zuordnen

Bevor Sie damit beginnen, einem Arbeitsblatt Elemente zuzuordnen, stellen Sie sicher, dass das Arbeitsblatt nicht schreibgeschützt ist. Wenn ein bestehender Schutz für das Arbeitsblatt die Benutzerinteraktion verhindert, können Sie keine Zellen darin auswählen. Heben Sie zunächst den Schreibschutz auf und beginnen Sie dann mit der Zuordnung von Elementen zu Zellen.

Die Anzahl der Bereiche und Zellen, für die Zuordnungen zu erstellen sind, hängt von Ihrer Auswahl zu Granularität, Datumsbereich und Filtern ab. Wenn Sie z. B. [!UICONTROL Site Metric] > [!UICONTROL Traffic Report], [!UICONTROL Week] Granularität einstellen und Datumsbereich für festlegen, werden Sie aufgefordert, drei Zellen (bei Verwendung [!UICONTROL Last 2 Weeks]) auf der [!UICONTROL Custom Layout][!UICONTROL Request Wizard: Step 2]Seite zuzuordnen. Durch die Abfrage werden Daten für die erste und die zweite Woche abgerufen, wobei jeder Datenpunktwert gleich dem Wert der Seitenaufrufe ist. Your third cell serves as the row heading, which you can configure using [!UICONTROL Format Options].

Wenn Sie eine Zuordnung zu nicht kompatiblen Bereichen des Arbeitsblatts vornehmen, löst ReportBuilder einen Fehler aus.

Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

* [Auswahl eines Zellenbereiches ](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_1E37FB46DA194FB7A1050B8833A48AC6)
* [Methoden für die Auswahl von Zellen ](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_760421C3D7F84D67A639174710C93B22)
* [Probleme bei der Zuordnung ](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_CC1BCF841291447EB3A994EB08F3A099)

## Auswahl eines Zellenbereiches {#section_1E37FB46DA194FB7A1050B8833A48AC6}

On the [!UICONTROL Request Wizard: Step 2], when you enable [!UICONTROL Custom Layout] for a trended request, you can map the request to a range of cells.

Klicken Sie auf **[!UICONTROL Range Selector]** ![select_cell_icon.png](assets/select_cell_icon.png)

neben dem Artikel, den Sie zuordnen möchten.

* **Alle Zellen im Bereich:** Erfordert die Auswahl einer Gruppe von Zellen für eine [!UICONTROL Custom Layout] Stilanforderung.
* **Erste Zelle des Bereichs:** Ermöglicht die Auswahl der Zelle links oben im Bereich und zeigt die [!UICONTROL Range] Ausrichtung an, um die horizontale oder vertikale Ausrichtung der Eingabe- und Ausgabezellen (Spalte oder Zeile) festzulegen. Verwenden Sie diese Option, um die Zellen von Report Builder auswählen zu lassen.
* **Bereichsausrichtung:** Wahlweise Orientierung des Zellenbereichs als Spalten oder Zeilen.
* **Position der obersten Zelle des Bereichs auswählen:** Zeigt die Zellreferenzen an.

## Methoden für die Auswahl von Zellen {#section_760421C3D7F84D67A639174710C93B22}

You select the data by clicking the **[!UICONTROL Range Selection]** icon  ![select_cell_icon.png](assets/select_cell_icon.png)

und die Maus bei gedrückter Taste über den gewünschten Zellbereich im Arbeitsblatt ziehen. Eine durchgehende Auswahl wird schwarz umrahmt dargestellt.

![](assets/twenty_cells.gif)

Getrennt ausgewählte Zeilen weisen einen weißen Rahmen um die jeweiligen Zeilen auf.

![](assets/twoXten_cells_highlighted.gif)

To map separate rows in one request, use the [!UICONTROL Control] key, then click and drag the cursor over the desired cells. Dieses Verfahren kann eingesetzt werden, wenn Ihre Anforderung beispielsweise in vier Bereichen mit jeweils zehn Zellen angezeigt werden soll, nicht in 40 zusammenhängenden Zellen.

![](assets/map4.png)

Nachdem Sie Zellen ausgewählt haben, klicken Sie erneut auf das **[!UICONTROL Range Selector]** Symbol im [!UICONTROL Range Selection] Formular, um zum Formular zurückzukehren [!UICONTROL Request Wizard: Step 2].

## Probleme bei der Zuordnung {#section_CC1BCF841291447EB3A994EB08F3A099}

Wenn Sie aus Versehen eine Zuordnung für eine Zelle wählen, für die bereits eine aktive Zuordnung vorliegt, wird im Textfeld neben dem Symbol für die Bereichsauswahl kein Zellenverweis angezeigt. Wenn Sie in diesem Fall auf [!UICONTROL OK] klicken, zeigt ReportBuilder die folgende Fehlermeldung an: „Der ausgewählte Bereich überschneidet sich mit dem Bereich einer anderen Anforderung. Ändern Sie Ihre Auswahl.&quot;

* If you still need to use the cell, right-click on the desired cell or cells, and select **[!UICONTROL Delete Request]**.

Wenn Sie diese Fehlermeldung vermeiden möchten, haben Sie zwei Möglichkeiten:

* Planen des Berichtsformats durch Formatierung von Zellen mit Anforderungen und Zuordnungen
* Testen eines Arbeitsblatts, die Zuordnungen enthält

Ein Test auf Bereiche mit eingebetteten Anforderungen wird folgendermaßen durchgeführt:

* Launch the [!UICONTROL Request Manager] and click on individual requests listed in the table. Durch Klicken auf eine Anforderung werden die zugehörigen Bereiche im Arbeitsblatt markiert.
* Select cells in the spreadsheet you intend to use for a new mapping and click [!UICONTROL From Sheet]. The [!UICONTROL Request Manager] selects the request in the list which has an output item that intersects the selected cell. Wird keine Anforderung hervorgehoben, ist die Zelle verfügbar.
* Select cells in the spreadsheet, right-click in the context menu and verify if [!UICONTROL Edit Request] is available. Ist dies der Fall, ist eine mit den Zellen verknüpfte Anforderung vorhanden.
