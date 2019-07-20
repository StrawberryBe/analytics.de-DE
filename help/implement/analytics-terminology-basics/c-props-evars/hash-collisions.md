---
description: Beschreibt, was eine Hash-Kollision ist und wie sie manifestiert werden kann.
keywords: Analytics-Implementierung; hash; Kollision; prop; evar; Hash
seo-description: Beschreibt, was eine Hash-Kollision ist und wie sie manifestiert werden kann.
seo-title: Hash-Kollisionen
solution: Analytics
title: Hash-Kollisionen
topic: Entwickler und Implementierung
uuid: 7 dfd 6 e 64-4 a 62-4087-bc 28-fb 667 ec 2 b 1 b 6
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Hash-Kollisionen

Beschreibt, was eine Hash-Kollision ist und wie sie manifestiert werden kann.

Adobe behandelt prop- und eVar-Werte standardmäßig als Zeichenfolgen, auch wenn der Wert eine Zahl ist. Manchmal sind diese Zeichenfolgen Hunderte von Zeichen lang, manchmal sind sie kurz. Um Platz zu sparen, die Leistung zu verbessern und alles einheitlich zu gestalten, werden die Zeichenfolgen nicht direkt in den verarbeitenden Tabellen verwendet. Stattdessen wird für jeden Wert ein 32-Bit- oder 64-Bit-Hash berechnet. Alle Berichte werden auf diesen Hash-Werten ausgeführt, bis die Daten angezeigt werden. Jeder Hash wird dabei durch den Originaltext ersetzt. Ohne diese Komprimierung könnten Berichte innerhalb weniger Minuten ausgeführt werden.

Bei den meisten Feldern wird die Zeichenfolge zuerst komplett in Kleinschreibung konvertiert (reduziert die Anzahl einzigartiger Werte). Hash-Werte werden auf Monatsbasis vergeben (bei der ersten Anzeige pro Monat). Von Monat zu Monat besteht eine geringe Möglichkeit, dass zwei einzigartige Variablenwerte denselben Hash-Wert erhalten. Dieses Ereignis wird als *Hash-Kollision* bezeichnet.

Hash-Kollisionen können sich wie folgt im Bericht manifestieren:

* Wenn Sie einen Trend für einen Wert erstellen und in einem Monat eine Spitze verzeichnen, haben vermutlich andere Werte für diese Variable denselben Hash-Wert erhalten wie der Wert, den Sie gerade prüfen.
* Dasselbe passiert mit Segmenten für einen bestimmten Wert.

<p class="head"> <b>Beispiel für Hash-Kollision</b> </p>

Die Wahrscheinlichkeit von Hash-Kollisionen steigt analog zur Anzahl an einzigartigen Werten in einer Dimension (eVar). Beispielsweise könnte einer der Werte, die gegen Ende des Monats eingehen, denselben Hash-Wert erhalten, der bereits einem anderen Wert in diesem Monat zugewiesen wurde. Die folgenden Beispiele veranschaulichen, wie sich dies auf Segmentergebnisse auswirken kann. Nehmen wir an, eVar62 wird am 18. Februar den Wert 100 zugewiesen. Analytics pflegt eine Tabelle, die wie folgt aussehen kann:

<table id="table_6A49D1D5932E485DB2083154897E5074"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar62-Zeichenfolgenwert </th> 
   <th colname="col2" class="entry"> Hash </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Wert 99 </p> </td> 
   <td colname="col2"> <p> 111 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> Wert 100</b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wert 101 </p> </td> 
   <td colname="col2"> <p> 222 </p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn Sie ein Segment erstellen, das auf Besuche mit eVar62="value 500" prüft, ermittelt Analytics, ob „value 500“ ein Hash enthält. Da „value 500“ nicht vorhanden ist, gibt Analytics null Besuche zurück. Am 23. Februar erhält eVar62 den Wert „value 500“, und der Hash dafür lautet ebenfalls 123. Die Tabelle sieht folgendermaßen aus:

<table id="table_5FCF0BCDA5E740CCA266A822D9084C49"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar62-Zeichenfolgenwert </th> 
   <th colname="col2" class="entry"> Hash </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Wert 99 </p> </td> 
   <td colname="col2"> <p> 111 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> Wert 100</b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wert 101 </p> </td> 
   <td colname="col2"> <p> 222 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> Wert 500 </b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn das Segment erneut ausgeführt wird, prüft es den Hash von „value 500“, findet 123, und der Bericht gibt alle Besuche mit dem Hash 123 zurück. Auf diese Weise werden Besuche am 18. Februar in den Ergebnissen eingebunden.

Diese Situation kann bei der Verwendung von Analytics Probleme verursachen. Adobe sucht weiter nach Wegen, die Wahrscheinlichkeit von Hash-Kollisionen in der Zukunft zu verringern. Um diese Situation zu vermeiden, müssen Wege gefunden werden, die einzigartigen Werte zwischen Variablen zu verteilen, nicht erforderliche Werte mit Verarbeitungsregeln zu entfernen oder die Anzahl an Werten pro Variable anderweitig zu verringern.
