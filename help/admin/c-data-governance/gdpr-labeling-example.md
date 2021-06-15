---
description: Zeigt Beispiele zum Beschriften von Daten für Trefferdaten, Zugriffsanfragen und Löschanfragen
title: Beschriftungsbeispiel
uuid: a9a5b937-dbde-4f0f-a171-005ef4c79df9
exl-id: 9bea8636-c79c-4998-8952-7c66d31226e3
source-git-commit: 3ff221b8715ecde6923310b6818904c697a2b003
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 87%

---

# Beschriftungsbeispiel

## Treffer-Beispieldaten

Angenommen, es liegen die folgenden Trefferdaten vor:

* Die erste Zeile enthält die Beschriftungen für die einzelnen Variablen.
* Die zweite Zeile entspricht dem Namen der Variable. Wenn sie eine ID-Beschriftung aufweist, enthält sie den zugewiesenen Namespace in Klammern.
* Die Trefferdaten beginnen in der dritten Reihe.

| Bezeichnungen | I2<br>ID-PERSON<br>DEL-PERSON<br>ACC-PERSON | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|---|---|---|---|---|---|
| **Variablenname** <br> **(Namespace)** | **MyProp1** <br> **(user)** | **Besucher-ID** <br> **(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3** <br> **(xyz)** |
| Trefferdaten | Mary | 77 | A | M | X |
|  | Mary | 88 | B | N | Y |
|  | Mary | 99 | C | O | Z |
|  | John | 77 | D | P | W |
|  | John | 88 | E | N | U |
|  | John | 44 | F | Q | V |
|  | John | 55 | G | R | X |
|  | Alice | 66 | A | N | Z |

## Beispiel einer Zugriffsanfrage

Wenn ich eine Zugriffsanfrage sende, enthält die Zusammenfassungsdatei die in der folgenden Tabelle angegebenen Werte. Eine Anfrage kann nur eine Gerätedatei, eine Personendatei oder je eine von beiden zurückgeben. Zwei Zusammenfassungsdateien werden nur dann zurückgegeben, wenn eine Personen-ID verwendet wird und wenn die Option „expandIDs“ auf „true“ festgelegt ist.

<table>
  <tr>
    <th colspan="2" style="text-align:center">API-Werte</th>
    <th rowspan="2">Zurückgegeben<br>Dateityp</th>
    <th colspan="5" style="text-align:center">Daten in der Zusammenfassungsdatei für den Zugriff</th>
  </tr>
  <tr>
    <th>Namensraum/ID</th>
    <th>expandIDs</th>
    <th>MyProp1</th>
    <th>Visitor ID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>AAID=77</td>
    <td>false (falsch)</td>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>77</td>
    <td>nicht vorhanden</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>AAID=77</td>
    <td>true (wahr)</td>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>77</td>
    <td>nicht vorhanden</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>user=Mary</td>
    <td>false (falsch)</td>
    <td>Person</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A,B,C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary</td>
    <td rowspan="2">true (wahr)</td>
    <td>Person</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A,B,C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>77, 88</td>
    <td>A,B,C</td>
    <td>N, P</td>
    <td>U, W</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary<br>AAID=66</td>
    <td rowspan="2">true (wahr)</td>
    <td>Person</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A,B,C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>66, 77, 88</td>
    <td>A,B,C</td>
    <td>N, P</td>
    <td>U, W, Z</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>false (falsch)</td>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>55, 77</td>
    <td>nicht vorhanden</td>
    <td>M, R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>true (wahr)</td>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>55,77</td>
    <td>nicht vorhanden</td>
    <td>M, P, R</td>
    <td>W, X</td>
  </tr>
</table>

Beachten Sie, dass die Einstellung für „expandIDs“ keinen Einfluss auf die Ausgabe hat, wenn eine Cookie-ID verwendet wird.

## Beispiellöschanfragen

Wenn für eine Löschanfrage die API-Werte in der ersten Zeile der Tabelle verwendet werden, wird die Treffertabelle aktualisiert und sieht dann folgendermaßen aus:

<table>
  <tr>
    <th colspan="5" style="text-align:center">AAID=77 <br>(expandIDs value does not matter)</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Mary</td>
    <td>42</td>
    <td>A</td>
    <td>Datenschutz-7398</td>
    <td>Datenschutz-9152</td>
  </tr>
  <tr>
    <td>Mary</td>
    <td>88</td>
    <td>B</td>
    <td>N</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>Mary</td>
    <td>99</td>
    <td>C</td>
    <td>O</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>John</td>
    <td>42</td>
    <td>D</td>
    <td>Datenschutz-1866</td>
    <td>Datenschutz-8216</td>
  </tr>
  <tr>
    <td>John</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>Dies hat nur Einfluss auf Zellen in Zeilen, die „AAID = 77“ und eine DEL-DEVICE-Beschriftung enthalten.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary<br>expandIDs=false</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Datenschutz-0523</td>
    <td>77</td>
    <td>Datenschutz-1866</td>
    <td>Datenschutz-3681</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Datenschutz-0523</td>
    <td>88</td>
    <td>Datenschutz-2178</td>
    <td>Datenschutz-1975</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>Datenschutz-0523</td>
    <td>99</td>
    <td>Datenschutz-9045</td>
    <td>Datenschutz-2864</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>John</td>
    <td>77</td>
    <td>D</td>
    <td>P</td>
    <td>W</td>
  </tr>
  <tr>
    <td>John</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>Dies hat nur Einfluss auf Zellen in Zeilen, die „user = Mary“ und eine DEL-PERSON-Beschriftung enthalten. In der Praxis würde es sich zudem bei der Variablen mit dem A_ID-Wert wahrscheinlich um ein Prop- oder eVar-Objekt handeln, und der zugehörige Ersatzwert wäre wahrscheinlich eine Zeichenfolge, die mit „Privacy-“ gefolgt von einer zufälligen Nummer (GUID) beginnt, statt dass der numerische Wert durch einen anderen, zufälligen numerischen Wert ersetzt wird.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary<br>expandIDs=true</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Datenschutz-5782</td>
    <td>09</td>
    <td>Datenschutz-0859</td>
    <td>Datenschutz-8183</td>
    <td>Datenschutz-9152</td>
  </tr>
  <tr>
    <td>Datenschutz-5782</td>
    <td>16</td>
    <td>Datenschutz-6104</td>
    <td>Datenschutz-2911</td>
    <td>Datenschutz-6821</td>
  </tr>
  <tr>
    <td>Datenschutz-5782</td>
    <td>83</td>
    <td>Datenschutz-2714</td>
    <td>Datenschutz-0219</td>
    <td>Datenschutz-4395</td>
  </tr>
  <tr>
    <td>John</td>
    <td>09</td>
    <td>D</td>
    <td>Datenschutz-8454</td>
    <td>Datenschutz-8216</td>
  </tr>
  <tr>
    <td>John</td>
    <td>16</td>
    <td>E</td>
    <td>Datenschutz-2911</td>
    <td>Datenschutz-2930</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

Beachten Sie Folgendes:

* Zellen in Zeilen, die die Beschriftung `user=Mary` und die Beschriftung `DEL-DEVICE` oder `DEL-PERSON` enthalten, sind ebenso betroffen wie Zellen mit der Beschriftung `DEL-DEVICE` in Zeilen, die eine beliebige Besucher-ID (AAID) enthalten, die in einer Zeile mit `user=Mary` aufgetreten ist.
* Die Einstellung &quot;expandIDs&quot;wird nicht auf den Aufruf erweitert, um in MyEvar3 vorhandene Werte einzuschließen, die eine ID-DEVICE-Beschriftung haben, wenn `user=Mary` verwendet wird. &quot;ExpandIDs&quot;erweitert sich nur, um Besucher-IDs (in diesem Beispiel AAIDs, aber auch die ECID) in Zeilen mit `user=Mary` einzuschließen.
* `MyEvar2` in der vierten und fünften Zeile wird aktualisiert, weil diese Zeilen dieselben Besucher-ID-Werte wie die in der ersten und zweiten Zeile enthalten. Demzufolge werden sie bei der ID-Erweiterung für Löschvorgänge auf Geräteebene einbezogen.
* Die Werte für `MyEvar2` in den Zeilen zwei und fünf stimmen vor und nach dem Löschvorgang überein. Sie stimmen jedoch nach dem Löschvorgang nicht mehr mit dem Wert N in der letzten Zeile überein, da diese Zeile im Rahmen der Löschanfrage nicht aktualisiert wurde.
* `MyEvar3` verhält sich mit ID-Erweiterung anders als ohne, da ohne ID-Erweiterung keine `ID-DEVICES` übereingestimmt haben. Jetzt stimmt `AAID` in den ersten fünf Zeilen überein.
