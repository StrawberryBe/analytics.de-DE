---
description: Dieser Bericht ordnet die Seiten Ihrer Site anhand der Seiten mit dem höchsten Traffic-Aufkommen. Falls Sie im Rahmen Ihrer Geschäftstätigkeit quantitative Daten über Seiten benötigen, kann dieser Bericht mithilfe der richtigen Metrik diese Daten für Sie ermitteln.
seo-description: Dieser Bericht ordnet die Seiten Ihrer Site anhand der Seiten mit dem höchsten Traffic-Aufkommen. Falls Sie im Rahmen Ihrer Geschäftstätigkeit quantitative Daten über Seiten benötigen, kann dieser Bericht mithilfe der richtigen Metrik diese Daten für Sie ermitteln.
seo-title: Seiten
solution: Analytics
title: Seiten
topic: 'Berichte    '
uuid: 6435 e 262-e 734-4 c 15-af 5 b -173799 d 5 cc 43
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Seiten

Dieser Bericht ordnet die Seiten Ihrer Site anhand der Seiten mit dem höchsten Traffic-Aufkommen. Falls Sie im Rahmen Ihrer Geschäftstätigkeit quantitative Daten über Seiten benötigen, kann dieser Bericht mithilfe der richtigen Metrik diese Daten für Sie ermitteln.

## Zuordnung, Ablauf und spezielle Werte {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

Beachten Sie, dass die Metriken im Seitenbericht in Reports &amp; Analytics eine lineare Zuordnung verwenden. Der Umsatz wird beispielsweise auf alle Seiten aufgeteilt, die vor dem Kaufergebnis aufgerufen wurden. Dies führt möglicherweise zu Unklarheiten bei manchen Metriken, die normalerweise nur auf einer Seite vorkommen, wie etwa bei einem Zusatz zum Warenkorb.

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry">Reports &amp; <p>Analysen </p> </th> 
   <th colname="col3" class="entry"> Ad Hoc Analysis </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
   <th colname="col5" class="entry"> Analysis Workspace </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Metrikzuordnung </td> 
   <td colname="col2"> Linear </td> 
   <td colname="col3"> Die Zuordnung ist für die einzelnen Dimensionen spezifisch. Als Standard gilt die Zuordnung „Letztkontakt“. Die Dimension „pagename“ bildet jedoch eine Ausnahme. Wenn Sie auf „pagename“ ein benutzerspezifisches Ereignis anwenden, ist die Zuordnung der genaue Treffer. </td> 
   <td colname="col4"> <p>Auf derselben Seitenansicht festgelegte Werte </p> </td> 
   <td colname="col5"> <p>Auf derselben Seitenansicht festgelegte Werte </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Werte laufen ab nach </td> 
   <td colname="col2"> Seitenansicht </td> 
   <td colname="col3"> Seitenansicht </td> 
   <td colname="col4"> Seitenansicht </td> 
   <td colname="col5"> Seitenansicht </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Wertgrenzen </td> 
   <td colname="col2"> <p>Erste 500.000 individuell pro Monat + neue Werte mit Traffic </p> </td> 
   <td colname="col3"> <p>Erste 500.000 individuell pro Monat + neue Werte mit Traffic </p> </td> 
   <td colname="col4"> Keine </td> 
   <td colname="col5"> <p>Erste 500.000 individuell pro Monat + neue Werte mit Traffic </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Spezielle Werte </td> 
   <td colname="col2"> <p>(geringer Traffic) repräsentiert Werte über die ersten 500.000 hinaus, die nicht ausreichend Traffic empfangen haben, um verzeichnet zu werden. </p> </td> 
   <td colname="col3"> <p>(geringer Traffic) repräsentiert Werte über die ersten 500.000 hinaus, die nicht ausreichend Traffic empfangen haben, um verzeichnet zu werden. </p> </td> 
   <td colname="col4"> Keine </td> 
   <td colname="col5"> <p>(geringer Traffic) repräsentiert Werte über die ersten 500.000 hinaus, die nicht ausreichend Traffic empfangen haben, um verzeichnet zu werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn Sie in Reports &amp; Analytics ein benutzerspezifisches Ereignis als Metrik in einem Seitenbericht anwenden, erfolgt eine lineare Zuordnung.

Dies bedeutet, dass das Ereignis, selbst wenn mit einem s.tl()-Aufruf gesendet wurde, die lineare Zuordnung des vorherigen s.t()-Aufrufs erhält. Beispiel:

| Seitenname | Page_event | Ereignisse |
|---|---|---|
| Seite 1 | **s.t()** |  |
| Seite 1 | s.tl() | Ereignis 1 |
| Seite 1 | s.tl() | Ereignis 1 |
| Seite 1 | s.tl() | Ereignis 1 |
| Seite 2 | **s.t()** |  |
| Seite 2 | **s.t()** |  |
| Seite 2 | s.tl() | Ereignis 1 |

Für dieses Szenario erhalten wir im Seitenbericht die folgende Zuordnung:

| Seiten | Seitenansichten | Ereignis 1 |
|---|---|---|
| Seite 1 | 1 | 1+1+1+1/3 = 3,33 |
| Seite 2 | 2 | 2/3 = 0,67 |

Auch wenn das Ereignis über einen s.tl-Aufruf gesendet wird, erhält die vor dem gesendeten Ereignis (s.t()-Aufruf) angesehene Seite einen Teil der Gutschrift.

## Hinweise {#section_47B0F4746D4847AC9E8697127063F4D0}

* Wenn kein Seitenname vorhanden ist, wird die URL verwendet.
* Falls Sie einen Treffer haben, bei dem kein Seitenname, keine URL der Seite oder keine Ereignisliste (kein kommerzielles Ereignis) vorhanden ist, dann wird der Treffer ausgeschlossen.
* Aufschlüsselungen zu Seiten zeigen, dass alle Seiten, die über einen Wert verfügten, persistent waren.

