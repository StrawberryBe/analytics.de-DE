---
description: Vergleich zwischen Terminologie und Aufgaben bei Ad Hoc Analysis und Analysis Workspace.
title: Analysis Workspace im Vergleich mit Ad Hoc Analysis
uuid: e4b3e40f-2b08-49a0-95f1-384d85c1640d
translation-type: tm+mt
source-git-commit: 56ca9fa36db9d7dd126808280ba17f29f4b787d9
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 100%

---


# Analysis Workspace im Vergleich mit Ad Hoc Analysis

>[!IMPORTANT]
>
>Adobe stellt Ad Hoc Analysis am 1. März 2021 ein. [Weitere Infos](https://adobe.ly/discoverworkspace)

Vergleich zwischen Terminologie und Aufgaben bei Ad Hoc Analysis und Analysis Workspace.

Analysis Workspace bringt viele Funktionen von Ad Hoc Analysis in den Arbeitsablauf im Browser. Einige Begriffe und Funktionen werden zwischen den Produkten übernommen, doch es gibt auch einige neue Begriffe und Ansätze für Analysen, die in Analysis Workspace neu eingeführt werden.

Einen technischen Vergleich der wichtigsten Funktionen und der Systemanforderungen der beiden Produkte finden Sie [hier](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/analytics-product-comparison.html?lang=de-DE).

## Vergleich der Schlüsselbegriffe  {#section_6109406B83B043A18E46D38F130B1D2E}

| Ad Hoc Analysis | Analysis Workspace |
|--- |--- |
| Projekt | Workspace oder Projekt |
| Workspace | Bereich |
| Bericht | Freiformtabelle |
| Grafik/Diagramm | Visualisierung |
| Hierarchie: Projekt > Workspace > Berichte | Hierarchie: Projekt > Bedienfelder > Tabellen |
| Berichtsvorlagen „Bewerteter Bericht“, „Trendbericht“, „Summenbericht“ | Freiformtabellen-Visualisierung |
| Flussvorlage | Flussvisualisierung |
| Fallout | Fallout-Visualisierung |

## Vergleich der wichtigsten Aufgaben  {#section_F31446F1DFA742D794A30D713E223440}

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
   <td colname="col2"> <p>Sie können Dimensionselemente oder Segmente als Spaltenüberschriften hinzufügen, um Vergleichsansichten von Metriken zu erstellen. <a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/metrics/adding-dimensions-and-metrics-to-your-project-in-analysis-workspace.html?lang=de-DE"  > Video: Hinzufügen von Dimensionen und Metriken zu Ihrem Projekt in Analysis Workspace</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Segmente anwenden </p> </td> 
   <td colname="col2"> <p>Segmente sind im Komponentenmenü „Segment“ verfügbar und können in Analysis Workspace an drei Stellen angewandt werden: </p> 
    <ol id="ol_800D81FE2C84459B94B085C51E140330"> 
     <li id="li_F2E050902F9A4831BBA57F466E07DEAE">Auf der <b>Bereichsebene</b>, wo sie auf viele Visualisierungen im Bereich angewandt werden. Dies ähnelt dem Anwenden eines Segments auf einen Workspace in den Ad-hoc-Analysen. </li> 
     <li id="li_2D88E43E0161485C95B08DC3C593EFD9">Als <b>Zeilen in einer Tabelle</b>. Dies ähnelt dem Hinzufügen von Segmenten zum Abschnitt „Zeilen/Aufschlüsselungen“ im Tabellenersteller in den Ad-hoc-Analysen. </li> 
     <li id="li_102E1A1DAA9247C08FC46C5AB3D78113">Als <b>Spalten einer Tabelle</b>. Dies ähnelt dem Hinzufügen von Segmenten zum Abschnitt „Spalten“ im Tabellenersteller oder dem Anwenden eines Segments auf Berichtsebene in den Ad Hoc Analysis. </li> 
    </ol> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/applying-segments-to-your-analysis-workspace-project.html?lang=de-DE"  > Video: Verwendung von Segmenten in Workspace</a> </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/panel-level-segments.html?lang=de-DE"  > Video: Anwenden von Segmenten auf einen Bereich</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Temporäre Segmente („ad-hoc-Segmente“) erstellen </p> </td> 
   <td colname="col2"> <p>Sie können <a href="/help/analyze/analysis-workspace/components/t-freeform-project-segment.md"  >im Handumdrehen temporäre Segmente („Ad-hoc-Segmente“)</a> in Analysis Workspace erstellen, indem Sie Dimensionselemente in die Segment-Dropzone oben im Bedienfeld ziehen. Darüber hinaus können Dropdown-Filter in der Dropzone des Bedienfelds hinzugefügt werden, um viele temporäre Segmente gleichzeitig zu erstellen und so gesteuerte Projektinteraktionen zu ermöglichen. </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/ad-hoc-temporary-segments.html?lang=de-DE"  > Video: Ad-hoc-Segmente in Analysis Workspace</a> </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/using-drop-down-filters.html?lang=de-DE"  > Video: Dropdown-Filter in Analysis Workspace</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datumsbereiche und Granularitäten auswählen </p> </td> 
   <td colname="col2"> <p>Datumsbereiche und Granularitäten sind im Komponentenmenü „Zeit“ verfügbar und können auf drei Arten verwendet werden: </p> 
    <ol id="ol_8B57C8A840694A879B22B809C58E7482"> 
     <li id="li_58FAE6A87B494A5C9007CD35BB101608">Datumsbereiche können auf Spalten/Zeilen angewandt werden und überschreiben den für den Bereich ausgewählten Datumsbereich. Dies ähnelt Datumsbereichen auf Berichtsebene. </li> 
     <li id="li_85BB89EFF9C8466A992815BB7804EA37">Mit „Übernehmen“ wird ein Datumsbereich auf alle Visualisierungen in einem Bereich angewandt. Dies ähnelt einem Datumsbereich für einen Workspace in den Ad Hoc Analysis. </li> 
     <li id="li_BC18564A8FBB48F4A522BCAC60838759">Mit „In alle Bedienfelder übernehmen“ wird ein Datumsbereich auf alle Bereiche in einem Workspace-Projekt angewandt. Dies ähnelt einem Datumsbereich für ein Projekt in den Ad Hoc Analysis. </li> 
    </ol> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/using-dates-in-analysis-workspace.html?lang=de-DE"  > Video: Umgang mit Daten in Analysis Workspace</a> </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/creating-custom-date-ranges-in-analysis-workspace.html?lang=de-DE"  > Video: Benutzerdefinierte Datumsbereiche</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fallout- und Konversionstrichter verwenden </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md"  > Fallout-Visualisierungen</a> sind in Analysis Workspace im Komponentenmenü „Visualisierung“ verfügbar. Ähnlich wie bei Ad Hoc Analysis: </p> 
    <ol id="ol_625FF45AED4E403DBEE1A906282E8531"> 
     <li id="li_7B6C5F2682774641B82D2021786AE5C4">Fallout kann für einen Besuch oder Besucher gelten. Optional kann „Alle Besuche“ einbezogen werden. Für Fallout kann über das Kontextmenü schnell ein Trend erstellt werden. </li> 
     <li id="li_CFBDDAB8E96A445DB0624640AEB25994">Dimensionselemente können mit einem OR-Operator verknüpft werden (ähnlich wie Gruppen) und Ereignisse können im Trichter verwendet werden. </li> 
     <li id="li_6638E6A62C744A27B2C066E5F9EC62C0">Die nächsten Fallthrough- und Fallout-Schritte können auch über das Kontextmenü gerendert werden. </li> 
    </ol> <p>Außerdem können Sie mit der Fallout-Funktion in Analysis Workspace <a href="/help/analyze/analysis-workspace/visualizations/fallout/configuring-interdimensional-fallout.md"  > gemischte Dimensionen</a> innerhalb von Schritten verwenden, was eine Verbesserung gegenüber Ad Hoc Analysis darstellt. Gemischte Dimensionen in Schritten werden mit einem AND-Operator verwendet. </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/analyzing-customer-journeys/fallout-visualization.html?lang=de-DE"  > Video: Fallout-Visualisierung</a> </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/analyzing-customer-journeys/multi-dimensional-fallout.html?lang=de-DE"  > Video: Verwendung mehrerer Fallout-Dimensionen</a> </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/analyzing-customer-journeys/comparing-segments-in-fallout.html?lang=de-DE"  > Video: Vergleich von Segmenten in Fallout</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fluss untersuchen (Pfade) </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/visualizations/c-flow/flow.md"  > Flussvisualisierungen</a> sind in Analysis Workspace im Komponentenmenü „Visualisierung“ verfügbar. Ähnlich wie bei Ad Hoc Analysis: </p> 
    <ul id="ul_42D259310823496499F7D1474E1639AF"> 
     <li id="li_5DE6980EF66A49E58B8946A0422BC02C">Der Fluss kann für einen Besuch oder Besucher gelten. </li> 
     <li id="li_70A692266D32416BA3D70C1F8999F837">Die wichtigsten Statistiken werden als prozentuale Pfadansichten gezeigt. </li> 
    </ul> <p>Außerdem ermöglicht der Fluss <a href="/help/analyze/analysis-workspace/visualizations/c-flow/multi-dimensional-flow.md"  > gemischte Dimensionen</a> sowie die Fähigkeit, mit der rechten Maustaste zu klicken und ein Segment zu erstellen, was eine Verbesserung gegenüber Ad Hoc Analysis darstellt. </p> <p>Derzeit können Benutzer im Flow in Analysis Workspace <b>kein</b> Erfolgsereignis auswählen. </li> 
    </ul> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/analyzing-customer-journeys/flow-visualization.html?lang=de-DE"  > Video: Übersicht der Flussvisualisierung</a> </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/analyzing-customer-journeys/text-wrapping-and-multi-dimensional-flow.html?lang=de-DE"  > Video: Mehrdimensionaler Fluss</a> </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/analyzing-customer-journeys/expanding-on-flow-visualization.html?lang=de-DE"  > Video: Segmente aus einem Fluss erstellen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Unbegrenzt Aufschlüsselungen erstellen </p> </td> 
   <td colname="col2"> <p>Mit Analysis Workspace können Sie im Browser einen unbegrenzten Drilldown durchführen. Segmente und Dimensionen lassen sich kombinieren. Mehrere Dimensionselemente können gleichzeitig aufgeschlüsselt werden, indem Sie eine Aufschlüsselungsdimension mehrfach auswählen und dann daran ziehen. </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/dimension-breakdown-by-position.html?lang=de-DE"  > Video: Verbesserte Aufschlüsselungen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Trends für Daten schnell erstellen </p> </td> 
   <td colname="col2"> <p>Über das Diagramm-Symbol in der Berichtzeile lassen sich Daten schnell visualisieren. Außerdem werden diese Schnellvisualisierungen mit der Quelltabelle verknüpft, sodass Sie von einem Wert zum nächsten wechseln können und das Diagramm automatisch aktualisiert wird. </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/visualizations/dimension-graph-live-linking.html?lang=de-DE"  > Video: Live-Verknüpfung von Diagrammdimensionen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Suites auswählen </p> </td> 
   <td colname="col2"> <p>In Analysis Workspace können einem Projekt mehrere Report Suites hinzugefügt werden.  </p> <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/multiple-report-suites-in-analysis-workspace.html?lang=de-DE"  >Video: Mehrere Report Suites in Workspace</a> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attribution IQ </p> </td> 
   <td colname="col2"> <p>Mit <a href="/help/analyze/analysis-workspace/attribution/overview.md"  >Attribution IQ</a> in Analysis Workspace können Sie Freiform-Tabellen, Visualisierungen und berechneten Metriken viele neue Attributionsmodelltypen hinzufügen. Dies umfasst mehr als 10 regelbasierte und algorithmische Modelle. </p>  <p><a href="https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/attribution-iq/using-attribution-iq-in-freeform-tables.html?lang=de-DE"  >Video: Attribution IQ in Freiform-Tabellen</a> </p> </td> 
  </tr>  
 </tbody> 
</table>

