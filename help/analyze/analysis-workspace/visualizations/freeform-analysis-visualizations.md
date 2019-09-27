---
description: Weitere Informationen zu Visualisierungen und Visualisierungseinstellungen in Analysis Workspace.
keywords: Analysis Workspace
seo-description: Weitere Informationen zu Visualisierungen und Visualisierungseinstellungen in Analysis Workspace.
seo-title: Visualisierungsübersicht
solution: Analytics
title: Visualisierungsübersicht
topic: Reports and Analytics
uuid: 318dea64-6277-4ec3-ad48-4dfcb7a54555
translation-type: tm+mt
source-git-commit: 3c5cc9275c9978caf57e4e29704e23405ac24b65

---


# Visualisierungsübersicht

Weitere Informationen zu Visualisierungen und Visualisierungseinstellungen in Analysis Workspace.

[Visualisierungstypen im Analysis Workspace auf YouTube](https://www.youtube.com/watch?v=b1zLEywRa6w&index=39&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (2:57)

## Visualizations panel {#section_DC07F032FBEF4046A40F7B95C28DA018}

Klicken Sie im seitlichen Bedienfeld auf **[!UICONTROL Visualisierungen], um den Visualisierungsbereich zu öffnen.**

![Schritt Ergebnis](assets/visualizations.png)

Wenn Sie Adobe Analytics verwenden, werden Sie mit den meisten Visualisierungsarten (z. B. Flächen-, Balken-, Donut- und Liniendiagramme) bereits vertraut sein. Analysis Workspace verfügt jedoch über Visualisierungseinstellungen sowie viele neue und einzigartige Visualisierungsarten mit interaktiven Funktionen.

## Visualization settings {#section_D3BB5042A92245D8BF6BCF072C66624B}

Um auf die [!UICONTROL Visualisierungseinstellungen] zuzugreifen, ziehen Sie eine Visualisierung in das [!UICONTROL Freiformfeld], und klicken Sie dann auf das Zahnrad-Symbol [!UICONTROL Visualisierungseinstellungen].

>[!IMPORTANT]
>
>Welche Visualisierungseinstellungen sichtbar sind, hängt von der Visualisierung ab. Nicht alle Einstellungen gelten für alle Visualisierungen. Zudem treten einige erweiterte Einstellungen **nur** bei bestimmten Visualisierungen in Erscheinung. Dies ist z. B. bei den [Histogrammeinstellungen](../../../analyze/analysis-workspace/visualizations/histogram.md#section_09D774C584864D4CA6B5672DC2927477) der Fall.

![](assets/visualization_settings.png)

<table id="table_E0695243886046979EE609FAE5D6EA00"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Einstellung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Prozentsatz </p> </td> 
   <td colname="col2"> <p>Zeigt Werte als Prozentzahlen an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>100 % gestapelt </p> </td> 
   <td colname="col2"> <p>Mit dieser Einstellung für die Visualisierungen „Bereich gestapelt“, „Balken gestapelt“ und „Horizontalbalken gestapelt“ wandeln Sie Diagramme in zu „100 % gestapelte“ Visualisierungen um. Beispiel: </p> <p><img  src="assets/stacked_100_percent.png" placement="break" width="400px" id="image_1B60D53F7EB84571B1580BC3A1E603EE" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Legende eingeblendet </p> </td> 
   <td colname="col2"> <p>Hiermit können Sie den Text zu Filterdetails für die Visualisierung „Zusammenfassungsnummer/Zusammenfassungsänderung“ ausblenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Grenzwert für max. Anzahl Elemente </p> </td> 
   <td colname="col2"> <p>Hiermit können Sie die Anzahl der Elemente begrenzen, die in einer Visualisierung angezeigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Y-Achse bei null verankern </p> </td> 
   <td colname="col2"> <p> Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Normalisierung </p> </td> 
   <td colname="col2"> <p>Erzwingt Metriken für gleiche Anteile. Siehe <a href="https://marketing.adobe.com/resources/help/en_US/reference/normalization.html" format="https" scope="external"> Normalisierung</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zwei Achsen anzeigen </p> </td> 
   <td colname="col2"> <p>Only applies if you have two metrics - you can have a y-axis on the left (for one metric) and on the right (for the other metric). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anomalien anzeigen </p> </td> 
   <td colname="col2"> <p>Reichert Liniendiagramme und Freiform-Tabellen so an, dass sie auch Datenanomalien anzeigen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Create Visual icon {#section_9C11D9DEDC42413AA53E69A71A509DFC}

Wenn Sie nicht sicher sind, welche Visualisierung Sie auswählen sollen, klicken Sie in einer beliebigen Tabellenzeile auf das Symbol **[!UICONTROL Visualisierung erstellen].** Dieses Symbol wird angezeigt, wenn Sie den Mauszeiger auf die Tabellenzeile bewegen. Wenn Sie darauf klicken, sucht Analysis Workspace nach der Visualisierung, die aufgrund der vorhandenen Fakten am besten zu Ihren Daten passt. Wenn Sie z. B. bis zu 3 Segmente ausgewählt haben, wird ein Venn-Diagramm erstellt. Bei mehr als 3 Segmenten wird ein Balkendiagramm erstellt. Für andere Datentypen wird eventuell ein Kantengraph erstellt usw.

![](assets/create-visual.png)

## Right-click visualization/panel menu {#section_05B7914D4C9E443F97E2BFFDEC70240C}

Auf Einstellungen, die sich auf eine Grafik beziehen, können Sie per Rechtsklick neben der Überschrift einer Visualisierung oder eines Felds zugreifen. Einige oder alle der folgenden Einstellungen sind dann verfügbar:

![](assets/right-click_menu.png)

| Einstellung | Beschreibung |
|--- |--- |
| Kopierte Visualisierung/Kopiertes Feld einfügen | Sie können das kopierte Element an einer anderen Stelle innerhalb des Projekts oder in ein ganz anderes Projekt einfügen. |
| Visualisierung/Fenster kopieren | Sie können per Rechtsklick eine Visualisierung oder ein Fenster kopieren. |
| Visualisierung/Fenster duplizieren | Fertigt ein exaktes Duplikat der aktuellen Visualisierung an, das Sie dann bearbeiten können. |
| Alle Leisten ausblenden | Alle Projektleisten werden ausgeblendet. |
| Alle Darstellungen in Leiste ausblenden | Alle Visualisierungen in dieser Projektleiste werden ausgeblendet. |
| Alle Leisten einblenden | Alle Projektleisten werden eingeblendet. |
| Alle Visualisierungen in Leiste einblenden | Alle Visualisierungen in dieser Projektleiste werden eingeblendet. |
| Beschreibung bearbeiten | Hiermit können Sie einen Text zur Beschreibung der Visualisierung oder des Bedienfeldes hinzufügen (oder bearbeiten). Diese Beschreibung wird in Projekt &gt; Projektinfo und Einstellungen angezeigt . |
| Bereichslink abrufen | Sie können Personen zu einem bestimmten Bereich innerhalb eines Projekts leiten. |
| Visualisierungslink anfordern | Hiermit können Sie diesen Link kopieren und freigeben, um andere Personen direkt zu dieser Visualisierung zu leiten. Benutzer müssen sich hierzu anmelden. |
| Neu starten | (Funktioniert bei Fluss, Venn, Histogramm) Löscht die Konfiguration für die aktuelle Visualisierung und öffnet ein neues Bedienfeld, in dem Sie diese neu konfigurieren können. |

## Edit legend labels {#section_94F1988CB4B9434BA1D9C6034062C3DE}

Sie können Seriennamen in Visualisierungslegenden (Fallout, Bereich, Bereich gestapelt, Balken, Balken gestapelt, Ringdiagramm, Histogramm, Horizontalbalken, Horizontalbalken gestapelt, Linie, Streuung, Venn) umbenennen, um die Visualisierungen zugänglicher zu gestalten.

Die Legendenbearbeitung ist für die folgenden Elemente **nicht** möglich: Treemap, Linear, Zusammenfassungsänderung oder -nummer, Text, Freiform, Histogramm, Kohorte oder Fluss-Visualisierungen.

Wenn Sie beispielsweise eine Legendenbeschriftung für ein Liniendiagramm bearbeiten möchten,

1. klicken Sie mit der rechten Maustaste auf die Legendenbeschriftungen.
1. Klicken Sie auf **[!UICONTROL Bezeichnung bearbeiten]**.

   ![](assets/edit-label.png)

1. Geben Sie den neuen Beschriftungstext ein.
1. Drücken Sie zum Speichern die **[!UICONTROL Eingabetaste].**

Hier finden Sie einen [Link zu einem Video](https://www.youtube.com/watch?v=mry3vDrTml0&index=61&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) zu diesem Thema.
