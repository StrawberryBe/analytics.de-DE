---
description: Vergleich zwischen Terminologie und Aufgaben bei Ad Hoc Analysis und Analysis Workspace.
title: Analysis Workspace im Vergleich mit Ad Hoc Analysis
uuid: e4b3e40f-2b08-49a0-95f1-384d85c1640d
translation-type: tm+mt
source-git-commit: 0c934b0e1d6c1e862094737ad7ac504574c0c0d2
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 86%

---


# Analysis Workspace im Vergleich mit Ad Hoc Analysis

>[!IMPORTANT]
>
>Die Adobe bringt Ad Hoc Analysis am 1. März 2021 in den Status als lebensbedrohlich. [Weitere Infos...](https://adobe.ly/discoverworkspace).

Vergleich zwischen Terminologie und Aufgaben bei Ad Hoc Analysis und Analysis Workspace.

Analysis Workspace bringt viele Funktionen von Ad Hoc Analysis in den Arbeitsablauf im Browser. Einige Begriffe und Funktionen werden zwischen den Produkten übernommen, doch es gibt auch einige neue Begriffe und Ansätze für Analysen, die in Analysis Workspace neu eingeführt werden.

Einen technischen Vergleich der wichtigsten Funktionen und der Systemanforderungen der beiden Produkte finden Sie [hier](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-overview/analytics-product-comparison.html).

## Vergleich der Schlüsselbegriffe {#section_6109406B83B043A18E46D38F130B1D2E}

| Ad Hoc Analysis | Analysis Workspace |
|--- |--- |
| Projekt | Workspace oder Projekt |
| Workspace | Bereich |
| Bericht | Freiformtabelle |
| Diagramm/Diagramm | Visualisierung |
| Hierarchie: Projekt > Workspace > Berichte | Hierarchie: Projekt > Bedienfelder > Tabellen |
| Berichtsvorlagen „Bewerteter Bericht“, „Trendbericht“, „Summenbericht“ | Freiformtabellen-Visualisierung |
| Flussvorlage | Flussvisualisierung |
| Fallout | Fallout-Visualisierung |

## Vergleich der wichtigsten Aufgaben {#section_F31446F1DFA742D794A30D713E223440}

<table id="table_90D4461F04F34D70844C5E3FBB0BBE44"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ad Hoc Analysis Aufgabe </th> 
   <th colname="col2" class="entry"> Aufgabe in Analysis Workspace </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Dimensionen und Segmente zu Metrikspalten hinzufügen </p> </td> 
   <td colname="col2"> <p>Sie können Dimensionselemente oder Segmente als Spaltenüberschriften hinzufügen, um Vergleichsansichten von Metriken zu erstellen. <a href="https://www.youtube.com/watch?v=P9W0hhIHhCs"  > Video: Umgang mit Dimensionen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Segmente anwenden </p> </td> 
   <td colname="col2"> <p>Segmente sind im Komponentenmenü „Segment“ verfügbar und können in Analysis Workspace an drei Stellen angewandt werden: </p> 
    <ol id="ol_800D81FE2C84459B94B085C51E140330"> 
     <li id="li_F2E050902F9A4831BBA57F466E07DEAE">Auf der <b>Bereichsebene</b>, wo sie auf viele Visualisierungen im Bereich angewandt werden. Dies ähnelt dem Anwenden eines Segments auf einen Workspace in den Ad-hoc-Analysen. </li> 
     <li id="li_2D88E43E0161485C95B08DC3C593EFD9">Als <b>Zeilen in einer Tabelle</b>. Dies ähnelt dem Hinzufügen von Segmenten zum Abschnitt „Zeilen/Aufschlüsselungen“ im Tabellenersteller in den Ad-hoc-Analysen. </li> 
     <li id="li_102E1A1DAA9247C08FC46C5AB3D78113">Als <b>Spalten einer Tabelle</b>. Dies ähnelt dem Hinzufügen von Segmenten zum Abschnitt „Spalten“ im Tabellenersteller oder dem Anwenden eines Segments auf Berichtsebene in den Ad Hoc Analysis. </li> 
    </ol> <p><a href="https://www.youtube.com/watch?v=QlUCdQDnni4"  > Video: Verwendung von Segmenten in Workspace</a> </p> <p><a href="https://www.youtube.com/watch?v=YjaRlJoQqRA"  > Video: Anwenden von Segmenten auf einen Bereich</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Erstellen von temporären ("Ad-hoc") Segmenten </p> </td> 
   <td colname="col2"> <p>You can <a href="/help/analyze/analysis-workspace/components/t-freeform-project-segment.md"  > create instant, temporary ("ad-hoc") segments</a> in Analysis Workspace by dragging dimension items into the segment drop zone at the top of the panel. Darüber hinaus können Dropdown-Filter in der Dropzone des Bedienfelds hinzugefügt werden, um viele temporäre Segmente gleichzeitig zu erstellen und so kontrollierte Projektinteraktionen zu ermöglichen. </p> <p><a href="https://www.youtube.com/watch?v=NKm7Rj23TtE"  > Video: Ad-hoc-Segmente in Analysis Workspace</a> </p> <p><a href="https://www.youtube.com/watch?v=vpJywtsFVPI"  > Video: Dropdown-Filter in Analysis Workspace</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datumsbereiche und Granularitäten auswählen </p> </td> 
   <td colname="col2"> <p>Datumsbereiche und Granularitäten sind im Komponentenmenü „Zeit“ verfügbar und können auf drei Arten verwendet werden: </p> 
    <ol id="ol_8B57C8A840694A879B22B809C58E7482"> 
     <li id="li_58FAE6A87B494A5C9007CD35BB101608">Datumsbereiche können auf Spalten/Zeilen angewandt werden und überschreiben den für den Bereich ausgewählten Datumsbereich. Dies ähnelt Datumsbereichen auf Berichtsebene. </li> 
     <li id="li_85BB89EFF9C8466A992815BB7804EA37">Mit „Übernehmen“ wird ein Datumsbereich auf alle Visualisierungen in einem Bereich angewandt. Dies ähnelt einem Datumsbereich für einen Workspace in den Ad Hoc Analysis. </li> 
     <li id="li_BC18564A8FBB48F4A522BCAC60838759">Mit „In alle Bedienfelder übernehmen“ wird ein Datumsbereich auf alle Bereiche in einem Workspace-Projekt angewandt. Dies ähnelt einem Datumsbereich für ein Projekt in den Ad Hoc Analysis. </li> 
    </ol> <p><a href="https://www.youtube.com/watch?v=ybmv6EBmhn0"  > Video: Umgang mit Daten in Analysis Workspace</a> </p> <p><a href="https://www.youtube.com/watch?v=L4FSrxr3SDA"  > Video: Benutzerdefinierte Datumsbereiche</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fallout- und Konversionstrichter verwenden </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md"  > Fallout-Visualisierungen</a> sind in Analysis Workspace im Komponentenmenü „Visualisierung“ verfügbar. Ähnlich wie bei Ad Hoc Analysis: </p> 
    <ol id="ol_625FF45AED4E403DBEE1A906282E8531"> 
     <li id="li_7B6C5F2682774641B82D2021786AE5C4">Fallout kann für einen Besuch oder Besucher gelten. Optional kann „Alle Besuche“ einbezogen werden. Für Fallout kann über das Kontextmenü schnell ein Trend erstellt werden. </li> 
     <li id="li_CFBDDAB8E96A445DB0624640AEB25994">Dimensionselemente können mit einem ODER-Operator verknüpft werden (ähnlich wie Gruppen) und Ereignisse können im Trichter verwendet werden. </li> 
     <li id="li_6638E6A62C744A27B2C066E5F9EC62C0">Die nächsten Fallthrough- und Fallout-Schritte können auch über das Kontextmenü gerendert werden. </li> 
    </ol> <p>Außerdem können Sie mit der Fallout-Funktion in Analysis Workspace <a href="/help/analyze/analysis-workspace/visualizations/fallout/configuring-interdimensional-fallout.md"  > gemischte Dimensionen</a> innerhalb von Schritten verwenden, was eine Verbesserung gegenüber Ad Hoc Analysis darstellt. Gemischte Dimensionen in Schritten werden mit einem UND-Operator verwendet. </p> <p><a href="https://www.youtube.com/watch?v=VcrfHSyIoj8"  > Video: Fallout und Trichter</a> </p> <p><a href="https://www.youtube.com/watch?v=EeLV366pQag"  > Video: Verwendung mehrerer Fallout-Dimensionen</a> </p> <p><a href="https://www.youtube.com/watch?v=H-oT3QZlyZQ"  > Video: Vergleich von Segmenten in Fallout</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fluss untersuchen (Pfade) </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/visualizations/c-flow/flow.md"  > Flussvisualisierungen</a> sind in Analysis Workspace im Komponentenmenü „Visualisierung“ verfügbar. Ähnlich wie bei Ad Hoc Analysis: </p> 
    <ul id="ul_42D259310823496499F7D1474E1639AF"> 
     <li id="li_5DE6980EF66A49E58B8946A0422BC02C">Der Fluss kann für einen Besuch oder Besucher gelten. </li> 
     <li id="li_70A692266D32416BA3D70C1F8999F837">Die wichtigsten Statistiken werden als prozentuale Pfadansichten gezeigt. </li> 
    </ul> <p>Außerdem ermöglicht der Fluss <a href="/help/analyze/analysis-workspace/visualizations/c-flow/multi-dimensional-flow.md"  > gemischte Dimensionen</a> sowie die Fähigkeit, mit der rechten Maustaste zu klicken und ein Segment zu erstellen, was eine Verbesserung gegenüber Ad Hoc Analysis darstellt. </p> <p>Derzeit <b>kann Flow in Analysis Workspace Benutzern die Auswahl eines Ereignisses nicht</b> erlauben. </li> 
    </ul> <p><a href="https://www.youtube.com/watch?v=3R1HTM7y_RM"  > Video: Übersicht der Flussvisualisierung</a> </p> <p><a href="https://www.youtube.com/watch?v=m1Wa6inC1rQ"  > Video: Mehrdimensionaler Fluss</a> </p> <p><a href="https://www.youtube.com/watch?v=XrJoNQy6RaQ"  > Video: Segmente aus einem Fluss erstellen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Unbegrenzt Aufschlüsselungen erstellen </p> </td> 
   <td colname="col2"> <p>Mit Analysis Workspace können Sie im Browser einen unbegrenzten Drilldown durchführen. Segmente und Dimensionen lassen sich kombinieren. Mehrere Dimensionselemente können gleichzeitig aufgeschlüsselt werden, indem Sie eine Aufschlüsselungsdimension mehrfach auswählen und dann daran ziehen. </p> <p><a href="https://www.youtube.com/watch?v=3mQ2HN7-lIc"  > Video: Verbesserte Aufschlüsselungen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Trends für Daten schnell erstellen </p> </td> 
   <td colname="col2"> <p>Über das Diagramm-Symbol in der Berichtzeile lassen sich Daten schnell visualisieren. Außerdem werden diese Schnellvisualisierungen mit der Quelltabelle verknüpft, sodass Sie von einem Wert zum nächsten wechseln können und das Diagramm automatisch aktualisiert wird. </p> <p><a href="https://www.youtube.com/watch?v=kzlPjsBVYFQ"  > Video: Live-Verknüpfung von Diagrammdimensionen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Suites auswählen </p> </td> 
   <td colname="col2"> <p>In Analysis Workspace können einem Projekt mehrere Report Suites hinzugefügt werden.  </p> <p><a href="https://www.youtube.com/watch?v=kRPTBDNLJKk"  > Video: Mehrere Report Suites in Workspace</a> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attribution IQ </p> </td> 
   <td colname="col2"> <p>Mit <a href="/help/analyze/analysis-workspace/attribution/overview.md"  >Attribution IQ</a> in Analysis Workspace können Sie Freiformtabellen, Visualisierungen und berechneten Metriken viele neue Attributionsmodelltypen hinzufügen. Es umfasst 10 mehr regelbasierte und algorithmische Modelle. </p>  <p><a href="https://www.youtube.com/watch?v=aYbGcQvAN1E"  > Video: Attribution IQ in Freiform-Tabellen</a> </p> </td> 
  </tr>  
 </tbody> 
</table>

