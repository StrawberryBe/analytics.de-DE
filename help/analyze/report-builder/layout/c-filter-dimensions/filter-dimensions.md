---
description: Sie können Dimensionen filtern, die Sie dem Raster „Zeilenbezeichnungen“ hinzugefügt haben. Filter engen die von Anforderungen zurückgegebenen Daten ein und können sowohl auf Pivot- als auch auf benutzerdefinierte Layouts angewendet werden. Wenn Sie die Filterung von Dimensionen im Pivot-Layout konfigurieren, können Sie zusätzlich die Anzahl der Einträge von einer Zelle angeben.
title: Übersicht über Filterdimensionen
uuid: c54d5add-f278-476d-8f14-73f1c2e37671
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 98%

---


# Übersicht über Filterdimensionen

Sie können Dimensionen filtern, die Sie dem Raster „Zeilenbezeichnungen“ hinzugefügt haben. Filter engen die von Anforderungen zurückgegebenen Daten ein und können sowohl auf Pivot- als auch auf benutzerdefinierte Layouts angewendet werden. Wenn Sie die Filterung von Dimensionen im Pivot-Layout konfigurieren, können Sie zusätzlich die Anzahl der Einträge von einer Zelle angeben.

Das Formular „Ausgewählter Filter“ wird auf der Grundlage des Elements und der Metrik vorbelegt, die in der Report Builder-Anfrage ausgewählt sind.

## Filter definieren – Werte und Sonderzeichen {#section_15840216A4044C40974945FAA435AD93}

Informationen über Filter im Bereich **[!UICONTROL Am meisten bevorzugte Filter]** > **[!UICONTROL Filter definieren]**.

![](assets/define_filter.png)

Die folgenden Tabellen enthalten Beispiele und Informationen über Filter:

<table id="table_8AC3A26FF02143DBA949B30F2A46CF11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Filter </th> 
   <th colname="col02" class="entry"> Beschreibung </th> 
   <th colname="col2" class="entry"> Beispielfilter </th> 
   <th colname="col3" class="entry"> Übereinstimmungsergebnisse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Enthält alle Begriffe </p> </td> 
   <td colname="col02"> <p>Enthält jeden durch Leerzeichen getrennten Wert in jeder beliebigen Reihenfolge. </p> </td> 
   <td colname="col2"> <p>a b c </p> </td> 
   <td colname="col3"> <p>Stimmt überein mit <span class="term"> a b c</span> und <span class="term"> b a c</span> usw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enthält einen der Begriffe </p> </td> 
   <td colname="col02"> <p>Enthält mindestens einen der Filter (durch Leerzeichen getrennt). </p> </td> 
   <td colname="col2"> <p>A B C </p> </td> 
   <td colname="col3"> <p>Stimmt überein mit <span class="term"> A1</span>, <span class="term"> B2</span>, <span class="term"> C3</span>, aber nicht mit<span class="term"> D4</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enthält die Wortgruppe </p> </td> 
   <td colname="col02"> <p>Enthält den Suchfilter und mögliche andere Begriffe. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Stimmt überein mit <span class="term"> abc</span> und <span class="term"> abc def</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enthält keine Begriffe </p> </td> 
   <td colname="col02"> <p>Gibt alles zurück, sofern es keinen von Ihnen eingegebenen Wert enthält. </p> </td> 
   <td colname="col2"> <p>a b c </p> </td> 
   <td colname="col3"> <p>Stimmt überein mit <span class="term"> d e f</span>, aber nicht mit<span class="term"> c d e f</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enthält nicht die Wortgruppe </p> </td> 
   <td colname="col02"> <p>Gibt alles zurück, das nicht Ihre Wortgruppe enthält. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Ausgeschlossen sind <span class="term"> abc</span>, <span class="term"> abc def</span> und stimmt überein mit <span class="term"> def</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gleich </p> </td> 
   <td colname="col02"> <p>Gibt einen exakten Treffer zurück. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p> <span class="term"> abc</span> wird zurückgegeben, nichts anderes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ist nicht gleich </p> </td> 
   <td colname="col02"> <p>Gibt alles zurück, das nicht genau Ihrem Eintrag entspricht. </p> </td> 
   <td colname="col2"> <p>a </p> </td> 
   <td colname="col3"> <p>Stimmt nicht überein mit <span class="term"> a</span>. </p> <p>Stimmt überein mit<span class="term"> a b c</span>. </p> <p>Stimmt überein mit<span class="term"> abc</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beginnt mit </p> </td> 
   <td colname="col02"> <p>Gibt Ergebnisse zurück, die mit einem bestimmten Wert beginnen. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Stimmt überein mit <span class="term"> abcd</span>, aber nicht mit <span class="term"> 1abc</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Endet mit </p> </td> 
   <td colname="col02"> <p>Gibt Ergebnisse zurück, die mit einem bestimmten Wert enden. </p> </td> 
   <td colname="col2"> <p>xyz </p> </td> 
   <td colname="col3"> <p>Sucht nach <span class="term"> wxyz</span> aber nicht <span class="term"> wxyz0</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Erweitert (Sonderzeichen) </p> </td> 
   <td colname="col02"> <p>Ermöglicht die Suche nach Zeichen in regulären Ausdrücken: </p> <p> <code> "", ^, -, *, $, | </code> </p> </td> 
   <td colname="col2"> <p>"^Home*Page$" | Sport </p> </td> 
   <td colname="col3"> <p> Dadurch wird ein Filter definiert, der mit <span class="term"> Home</span> beginnt, anschließend nach null oder mehr Zeichen sucht, und dann mit <span class="term">Page</span> endet. </p> <p>Auch jede Seite mit <span class="term">Sport</span> darin wird erfasst. </p> <p>Beispiele für Treffer sind: </p> 
    <ul id="ul_72D76C5AFEAF405E8A0E4E3C604D10AE"> 
     <li id="li_4D490059B667450DA8A0103167C7B391">HomePage </li> 
     <li id="li_1351619156274092AEB2771D882AD357">Home und (andere Zeichen) Page </li> 
     <li id="li_940EAA99A8CF49308E8471065EB317B1">Home Sport </li> 
     <li id="li_50A895F14A454BE9BF06EE0F07F99B3B">Sport Page </li> 
     <li id="li_F3CE0D07941D4C2485D2DE0B73E00677">Sport </li> 
     <li id="li_E84C15C061824A5D922D9900392F2996">xyz Sport abc </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_8BBB06C8860745DEA41B39673699DC0F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Sonderzeichen </th> 
   <th colname="col2" class="entry"> Zweck </th> 
   <th colname="col3" class="entry"> Hinweise </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> " " </td> 
   <td colname="col2"> Gleich </td> 
   <td colname="col3"> <p>Nicht mit einem Escapezeichen versehen, sofern es nicht mit einem anderen Anführungszeichen verwendet wird. Beispiel: <span class="term">17"-Display</span> ist keine Wortgruppe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> * </td> 
   <td colname="col2"> Platzhalterzeichen </td> 
   <td colname="col3"> <p>Entspricht dem Sternchen in einem regulären Ausdruck. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ^ </td> 
   <td colname="col2"> Beginnt mit </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> $ </td> 
   <td colname="col2"> Endet mit </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> – </td> 
   <td colname="col2"> Nicht </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> | </td> 
   <td colname="col2"> Oder </td> 
   <td colname="col3"> <p>Nur unterstützt im <span class="term"> Erweiterter Filter (Sonderzeichen)</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
