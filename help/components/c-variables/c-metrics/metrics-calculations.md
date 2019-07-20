---
description: Metriken werden nach den Methoden „Standard“, Beitrag, „Zuletzt“ und „Lineare Zuordnung“ berechnet. Jede Methode berechnet Werte unterschiedlich auf Grundlage von Formeln.
seo-description: Metriken werden nach den Methoden „Standard“, Beitrag, „Zuletzt“ und „Lineare Zuordnung“ berechnet. Jede Methode berechnet Werte unterschiedlich auf Grundlage von Formeln.
seo-title: Metrikberechnungen
solution: Analytics
title: Metrikberechnungen
topic: Metriken
uuid: 2 af 58 f 1 e -12 c 5-4828-ae 39-c 9 aeaef 6 b 705
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Metrikberechnungen

Metriken werden nach den Methoden „Standard“, Beitrag, „Zuletzt“ und „Lineare Zuordnung“ berechnet. Jede Methode berechnet Werte unterschiedlich auf Grundlage von Formeln.

<table id="table_6F81A12174D84124B7FD81FBBEDF18A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Berechnung der Metrik </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Original </td> 
   <td colname="col2"> <p>Der Erfolg wird dem ersten Variablenwert gutgeschrieben, der mit dem Erfolgsereignis verbunden ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zuletzt </td> 
   <td colname="col2"> <p>Der Erfolg wird dem letzten Variablenwert gutgeschrieben, der mit dem Erfolgsereignis verbunden ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Linear </td> 
   <td colname="col2"> <p>Wenn die lineare Zuordnung ausgewählt ist, werden die Erfolgserlebnisse gleichmäßig auf alle Variablenwerte im Besuch aufgeteilt. Bei numerischen Ereignissen und bei Währungsereignissen, beispielsweise <span class="term"> Umsatz</span>wird der Geldbetrag aufgeteilt. For counter events such as <span class="term"> Orders</span>, a fraction of the event is awarded to each variable value in the visit. Diese Bruchteile werden bei der Berichterstellung summiert und dann auf die nächste Ganzzahl gerundet. </p> <p>Beispiel: Wenn bei einem Besuch vier Seiten aufgerufen werden, bevor ein Erfolgsereignis eintritt, erhält jede Seite eine Gutschrift von 25 % für das Ereignis. Falls <span class="varname"> -kampagne</span> zwei Werte enthielt, würde jeder Kampagnenwert 50% der Gutschrift für das Ereignis erhalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beitrag </td> 
   <td colname="col2"> <p>Schreibt den Erfolg jedem Variablenwert gut, der zu einem Erfolgsereignis bei einem Besuch beigetragen hat. Diese Berechnung kann auch übergreifend auf mehrere Besuchersitzungen angewandt werden, wenn Sie besuchsübergreifende Beitragsmetriken verwenden. </p> <p>Siehe <a href="../../../components/c-variables/c-metrics/metrics-participation.md#concept_8E6B39106A244CB49E055150B291B477" format="dita" scope="local"> Beitrag</a> finden Sie weitere Informationen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel – Metrikberechnung {#section_4CE01DA35108418D9909823A7ECC4B45}

Angenommen, Ihre Site bietet eine interne Suche, die mithilfe einer Konversionsvariable (eVar) nachverfolgt wird. Der Benutzer führt mehrere interne Suchvorgänge durch und kauft dann Waren im Wert von $100 ein:

*`Pet`* &gt; *`Feline`* &gt; *`Cat`* &gt; *`Kitten`* &gt; $ 100 Einkauf

Die Gutschrift wird im Bericht wie folgt zugeordnet:

<table id="table_91A7244E77854838A8392B49366FB445"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar-Wert </th> 
   <th colname="col2" class="entry"> Erste/r </th> 
   <th colname="col3" class="entry"> Letzte/r </th> 
   <th colname="col4" class="entry"> Linear </th> 
   <th colname="col5" class="entry"> Beitrag </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Haustier </p> </td> 
   <td colname="col2"> <p>100 $ </p> </td> 
   <td colname="col3"> <p>0 $ </p> </td> 
   <td colname="col4"> <p>25 $ </p> </td> 
   <td colname="col5"> <p>100 $ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Katze </p> </td> 
   <td colname="col2"> <p>0 $ </p> </td> 
   <td colname="col3"> <p>0 $ </p> </td> 
   <td colname="col4"> <p>25 $ </p> </td> 
   <td colname="col5"> <p>100 $ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hauskatze </p> </td> 
   <td colname="col2"> <p>0 $ </p> </td> 
   <td colname="col3"> <p>0 $ </p> </td> 
   <td colname="col4"> <p>25 $ </p> </td> 
   <td colname="col5"> <p>100 $ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Junges Kätzchen </p> </td> 
   <td colname="col2"> <p>0 $ </p> </td> 
   <td colname="col3"> <p>100 $ </p> </td> 
   <td colname="col4"> <p>25 $ </p> </td> 
   <td colname="col5"> <p>100 $ </p> </td> 
  </tr> 
 </tbody> 
</table>

