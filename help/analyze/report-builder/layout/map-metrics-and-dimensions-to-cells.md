---
description: Bevor Sie damit beginnen, einem Arbeitsblatt Elemente zuzuordnen, stellen Sie sicher, dass das Arbeitsblatt nicht schreibgeschützt ist. Wenn ein bestehender Schutz für das Arbeitsblatt die Benutzerinteraktion verhindert, können Sie keine Zellen darin auswählen. Heben Sie zunächst den Schreibschutz auf und beginnen Sie dann mit der Zuordnung von Elementen zu Zellen.
seo-description: Bevor Sie damit beginnen, einem Arbeitsblatt Elemente zuzuordnen, stellen Sie sicher, dass das Arbeitsblatt nicht schreibgeschützt ist. Wenn ein bestehender Schutz für das Arbeitsblatt die Benutzerinteraktion verhindert, können Sie keine Zellen darin auswählen. Heben Sie zunächst den Schreibschutz auf und beginnen Sie dann mit der Zuordnung von Elementen zu Zellen.
seo-title: Metriken und Dimensionen Zellen zuordnen
solution: Analytics
title: Metriken und Dimensionen Zellen zuordnen
topic: ReportBuilder
uuid: 50893 e 1 c -5 f 2 c -4558-8001-41 e 70 d 74 d 6 e 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Metriken und Dimensionen Zellen zuordnen

Bevor Sie damit beginnen, einem Arbeitsblatt Elemente zuzuordnen, stellen Sie sicher, dass das Arbeitsblatt nicht schreibgeschützt ist. Wenn ein bestehender Schutz für das Arbeitsblatt die Benutzerinteraktion verhindert, können Sie keine Zellen darin auswählen. Heben Sie zunächst den Schreibschutz auf und beginnen Sie dann mit der Zuordnung von Elementen zu Zellen.

Die Anzahl der Bereiche und Zellen, für die Zuordnungen zu erstellen sind, hängt von Ihrer Auswahl zu Granularität, Datumsbereich und Filtern ab. Wenn Sie beispielsweise [!UICONTROL Site-Metrik] &gt; [!UICONTROL Traffic-Bericht] wählen, die Granularität auf [!UICONTROL Woche] setzen und den Datumsbereich auf [!UICONTROL Letzte 2 Wochen] festlegen, werden Sie in [!UICONTROL Anforderungs-Assistent: Schritt 2] aufgefordert, eine Zuordnung für drei Zellen herzustellen (bei Verwendung von [!UICONTROL Benutzerdefiniertes Layout]). Durch die Abfrage werden Daten für die erste und die zweite Woche abgerufen, wobei jeder Datenpunktwert gleich dem Wert der Seitenaufrufe ist. Die dritte Zelle dient als Zeilenüberschrift, die Sie mit Hilfe der [!UICONTROL Formatoptionen] konfigurieren können.

Wenn Sie eine Zuordnung zu nicht kompatiblen Bereichen des Arbeitsblatts vornehmen, löst ReportBuilder einen Fehler aus.

Die folgenden Abschnitte enthalten weitere Informationen:

* [Zellenbereich auswählen](../../../analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_1E37FB46DA194FB7A1050B8833A48AC6)
* [Methoden für die Auswahl von Zellen](../../../analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_760421C3D7F84D67A639174710C93B22)
* [Probleme bei der Zuordnung](../../../analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_CC1BCF841291447EB3A994EB08F3A099)

## Select a Range of Cells {#section_1E37FB46DA194FB7A1050B8833A48AC6}

Wenn Sie in [!UICONTROL Anforderungs-Assistent: Schritt 2] die Option [!UICONTROL Benutzerdefiniertes Layout] für eine Trendanforderung verwenden, können Sie die Anforderung einem Bereich von Zellen zuordnen.

Click the **[!UICONTROL Range Selector]** ![select_cell_icon.png](assets/select_cell_icon.png)

neben dem Element, das Sie zuordnen möchten.

* ** All Cells in Range:** Requires you to select a group of cells for a [!UICONTROL Custom Layout] style request.

* ** First Cell of Range:** Lets you select the top-left cell of the range, and displays the [!UICONTROL Range] orientation to specify the horizontal or vertical orientation of input and output cells (column or row). Verwenden Sie diese Option, um die Zellen von ReportBuilder auswählen zu lassen.

* ** Bereichsausrichtung: ** Hiermit können Sie die Zellenbereiche als Spalten oder Zeilen ausrichten.
* **Position der obersten Zelle des Bereichs auswählen:** Zeigt die Zellreferenzen an.

## Techniques for selecting cells {#section_760421C3D7F84D67A639174710C93B22}

You select the data by clicking the **[!UICONTROL Range Selection]** icon  ![select_cell_icon.png](assets/select_cell_icon.png)

 und die Maus bei gedrückter Taste über den gewünschten Zellbereich im Arbeitsblatt ziehen. Eine durchgehende Auswahl wird schwarz umrahmt dargestellt.

![](assets/twenty_cells.gif)

Getrennt ausgewählte Zeilen weisen einen weißen Rahmen um die jeweiligen Zeilen auf.

![](assets/twoXten_cells_highlighted.gif)

Um getrennte Zeilen in einer einzigen Anforderung zuzuordnen, drücken Sie die [!UICONTROL Strg]-Taste und ziehen Sie den Cursor bei gedrückter Maustaste über die gewünschten Zellen. Dieses Verfahren kann eingesetzt werden, wenn Ihre Anforderung beispielsweise in vier Bereichen mit jeweils zehn Zellen angezeigt werden soll, nicht in 40 zusammenhängenden Zellen.

![](assets/map4.png)

Klicken Sie nach dem Auswählen von Zellen im Dialogfeld **[!UICONTROL Bereichsauswahl]** erneut auf das Symbol für die [!UICONTROL Bereichsauswahl], um zum Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2] zurückzukehren.

## Issues when mapping {#section_CC1BCF841291447EB3A994EB08F3A099}

Wenn Sie aus Versehen eine Zuordnung für eine Zelle wählen, für die bereits eine aktive Zuordnung vorliegt, wird im Textfeld neben dem Symbol für die Bereichsauswahl kein Zellenverweis angezeigt. Wenn Sie in diesem Fall auf [!UICONTROL OK] klicken, zeigt ReportBuilder die folgende Fehlermeldung an: „Der ausgewählte Bereich überschneidet sich mit dem Bereich einer anderen Anforderung. Ändern Sie Ihre Auswahl.“

* Wenn Sie die Zelle trotzdem benötigen, klicken Sie mit der rechten Maustaste darauf (und auf evtl. ebenfalls betroffene Zellen) und wählen Sie **[!UICONTROL Anforderung löschen]**.

Wenn Sie diese Fehlermeldung vermeiden möchten, haben Sie zwei Möglichkeiten:

* Planen des Berichtsformats durch Formatierung von Zellen mit Anforderungen und Zuordnungen
* Testen eines Arbeitsblatts, die Zuordnungen enthält

Ein Test auf Bereiche mit eingebetteten Anforderungen wird folgendermaßen durchgeführt:

* Starten Sie den [!UICONTROL Anforderungs-Manager] und klicken Sie auf die einzelnen in der Tabelle aufgeführten Anforderungen. Durch Klicken auf eine Anforderung werden die zugehörigen Bereiche im Arbeitsblatt markiert.
* Wählen Sie die Zellen in der Kalkulationstabelle aus, die für die neue Zuordnung verwendet werden sollen, und klicken Sie auf [!UICONTROL Aus Blatt]. Im [!UICONTROL Anforderungs-Manager] wird nun eine Anforderung, deren Ausgabeelemente sich mit der betreffenden Zelle überschneiden, hervorgehoben dargestellt. Wird keine Anforderung hervorgehoben, ist die Zelle verfügbar.

* Wählen Sie Zellen im Arbeitsblatt aus, klicken Sie mit der rechten Maustaste und überprüfen Sie, ob im Kontextmenü die Option [!UICONTROL Anforderung bearbeiten] verfügbar ist. Ist dies der Fall, ist eine mit den Zellen verknüpfte Anforderung vorhanden.

