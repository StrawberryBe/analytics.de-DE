---
description: Die Zeileneinstellungen variieren je nachdem, welche Komponente Sie in die Tabelle gezogen haben.
title: Zeileneinstellungen
uuid: f30c31d5-1fd4-4b93-94c3-ca441099fe2e
translation-type: tm+mt
source-git-commit: 5c2f2d098398927d8379f2eb9ea69ca9acbfd726

---


# Zeileneinstellungen

Die Zeileneinstellungen variieren je nachdem, welche Komponente Sie in die Tabelle gezogen haben.

Sie können außerdem die ausgewählte(n) Zeile(n) mit den [Rechtsklickaktionen in einer Tabelle](/help/analyze/analysis-workspace/visualizations/freeform-table.md) verwalten.

Um auf die Tabellenzeileneinstellungen zuzugreifen, klicken Sie auf das Einstellungs-Symbol neben einer Dimension, einem Segment, einer Metrik, einem Zeitraum oder einer Aufschlüsselung im jeweiligen Element:

![](assets/row-settings.png)

<table id="table_7ACE6413DB1F40349ED2860020F92E55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Zeileneinstellung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="/help/analyze/analysis-workspace/components/calendar-date-ranges/time-comparison.md"  > Datumsvergleiche</a> </p> </td> 
   <td colname="col2"> <p><b>Richten Sie die Daten in allen Spalten so aus, dass sie alle in derselben Zeile beginnen. </b> </p> <p>Wenn Sie z. B. die Daten in einem Monatsvergleich zwischen Oktober und September 2016 ausrichten, beginnt die linke Spalte mit dem 1. Oktober und die rechte Spalte mit dem 1. September: </p> <p><img placement="break"  src="assets/add-time-period-column3.png" width="500px" id="image_99398B13FEDA4715B8B818DF6093CA37" /> </p> <p>Standardmäßig deaktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Prozentsatz </p> </td> 
   <td colname="col2"> <p><b>Prozentsätze nach Zeile berechnen</b> </p> <p>Erzwingt, dass die Freiformtabelle die Zellprozentsätze über die gesamte Zeile berechnet, anstatt die Spalte nach unten zu verschieben. Dies ist besonders nützlich für die Trend-Darstellung von Prozentangaben. Die Option ist standardmäßig aktiviert, wenn Sie das Symbol <span class="uicontrol">Visualisieren</span> verwenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Spaltensummen </p> </td> 
   <td colname="col2"> <p>Diese Einstellungen werden nur bei  <a href="/help/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md"  > manuellen (statischen) Zeilen</a> (wenn Sie eine endliche Gruppe aus Elementen ausgewählt haben) angezeigt und nicht bei dynamischen Zeilen (wenn Sie eine Dimension einfügen, die alle Elemente anzeigt). <p>Hinweis: Bei <i>metrischen</i> manuellen Zeilen ist diese Einstellung deaktiviert, da es nicht sinnvoll ist, andere Metriken als die aktuellen Zeilen einer Tabelle zu summieren. </p> </p> <p><b>Berechnen Sie die Summen durch Addieren der Werte, die sich zurzeit in jeder Spalte befinden (standardmäßig aktiviert):</b> </p> <p>Diese Option berechnet nur die aktuell in der Tabelle vorhandenen Spalten. (Clientseitige Berechnung) </p> <p><b>Berechnen Sie die Summen anhand aller Zeilen für jede Metrik (standardmäßig deaktiviert):</b> </p> <p>Diese Option bezieht alle Dimensionselemente für diese Dimension ein, auch dann, wenn diese nicht in der Tabelle aufgeführt sind. (Serverseitige Berechnung) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aufschlüsselung </p> </td> 
   <td colname="col2"> <p><b>Aufschlüsselung nach Position:</b> </p> <p>Sie können Aufschlüsselungen nach fester Position in einer Freiformtabelle durchführen. Sie können z. B. festlegen, dass die ersten sieben Zeilen immer aufgeschlüsselt werden. </p> <p>(Zuvor war die Liste mit den Werten in der Aufschlüsselung „gesperrt“. Dies konnte z. B. dazu führen, dass Sie eine Aufschlüsselung des <span class="term">Datums</span> nach <span class="term">Seite</span> durchführten und die ersten 50 Seiten für den ausgewählten Datumsbereich erhielten. Wenn Sie diesen Bericht speicherten und ihn einen Monat später erneut durchführen wollten, hätten sich die ersten 50 Seiten wahrscheinlich geändert. In Analysis Workspace werden jedoch die Ergebnisse der ursprünglichen Aufschlüsselung verwendet und dieselben Seiten angezeigt, aber mit dem aktuellen Monat als Zeitraum.) </p> <p>Ausführung einer Aufschlüsselung anhand einer festen Position: </p> 
    <ol id="ol_A396A11566AA4F52BC3ABBC373CEF477"> 
     <li id="li_BDAB1E9A48D44944A4F7C31F1182B923">Schlüsseln Sie einige Zeilen in Ihrer Tabelle auf. </li> 
     <li id="li_C5610437D3714CCEB9F3C771864B4336">Klicken Sie auf das Einstellungs-Symbol (Zahnrad) neben der Tabellenzeile, die Sie fixieren möchten. </li> 
     <li id="li_675E429DC3B94201978166F9408D30B1">Aktivieren Sie das Kästchen neben <span class="uicontrol">Aufschlüsselung nach Position</span>. </li> 
     <li id="li_E8A417D0D6D1438CAE825843BA0A7060">Ändern Sie die Sortierungsreihenfolge oder den Datumsbereich. Die Aufschlüsselungen sind jetzt an die Zeilenposition und nicht die hartcodierten Zeilen gebunden. </li> 
    </ol> <p>Standardmäßig deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

| Zeileneinstellung | Beschreibung |
|--- |--- |
| Datumsvergleiche | Richten Sie die Daten in allen Spalten so aus, dass sie alle in derselben Zeile beginnen.   Wenn Sie z. B. die Daten in einem Monatsvergleich zwischen Oktober und September 2016 ausrichten, beginnt die linke Spalte mit dem 1. Oktober und die rechte Spalte mit dem 1. September.<br>Standardmäßig deaktiviert. |
| Prozentsatz | Prozentsätze pro Zeile berechnen Erzwingt, dass in der Freiformtabelle die Zellprozentsätze über die Zeile anstatt für die Spalte berechnet werden. Dies ist besonders nützlich für die Trend-Darstellung von Prozentangaben.<br>Standardmäßig aktiviert, wenn Sie das Symbol „Visualisieren“ verwenden. |
| Spaltensummen | Diese Einstellungen werden nur bei  [manuellen (statischen) Zeilen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.html) (wenn Sie eine endliche Gruppe aus Elementen ausgewählt haben) angezeigt und nicht bei dynamischen Zeilen (z. B. wenn Sie eine Dimension einfügen, die alle Elemente anzeigt).<ul><li>**[!UICONTROL Show sum of current rows as the total]** - Zeigt eine clientseitige Summe der Tabellenzeilen an. Das bedeutet, dass die Gesamtsumme die Duplikat-Metriken wie Besuche oder Besucher **nicht** löscht.</li><li>**[!UICONTROL Show Grand Total]** - dies zeigt eine serverseitige Summe an, d. h. die Gesamtsumme löscht Duplikat-Metriken wie Besuche oder Besucher.</li></ul> |
| Aufschlüsselung | **[!UICONTROL Breakdown by position]**:  Sie können Aufschlüsselungen nach fester Position in einer Freiformtabelle durchführen. Sie können z. B. festlegen, dass die ersten sieben Zeilen immer aufgeschlüsselt werden.<br>(Zuvor war die Liste mit den Werten in der Aufschlüsselung „gesperrt“. Dies konnte z. B. dazu führen, dass wenn Sie eine Aufschlüsselung des Datums nach Seite durchführten, Sie die ersten 50 Seiten für den ausgewählten Datumsbereich erhielten. Wenn Sie diesen Bericht speicherten und ihn einen Monat später erneut durchführen wollten, hätten sich die ersten 50 Seiten wahrscheinlich geändert. In Analysis Workspace werden jedoch die Ergebnisse der ursprünglichen Aufschlüsselung verwendet und dieselben Seiten angezeigt, aber mit dem aktuellen Monat als Zeitraum.)<br>Ausführung einer Aufschlüsselung anhand einer festen Position: 1. Schlüsseln Sie einige Zeilen in Ihrer Tabelle auf. 2. Klicken Sie auf das Einstellungs-Symbol (Zahnrad) neben der Tabellenzeile, die Sie fixieren möchten. 3. Aktivieren Sie das Kästchen neben „Aufschlüsselung nach Position“. 4. Ändern Sie die Sortierungsreihenfolge oder den Datumsbereich. Die Aufschlüsselungen sind jetzt an die Zeilenposition und nicht die hartcodierten Zeilen gebunden.<br>Standardmäßig deaktiviert. |