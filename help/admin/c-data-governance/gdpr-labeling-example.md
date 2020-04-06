---
description: 'null'
title: Beschriftungsbeispiel
uuid: a9a5b937-dbde-4f0f-a171-005ef4c79df9
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Beschriftungsbeispiel

## Beispieltrefferdaten

Angenommen, Sie haben die folgenden Trefferdaten:

* Die erste Zeile enthält die Beschriftungen für jede Variable.
* Die zweite Zeile ist der Name der Variablen. Wenn eine ID-Bezeichnung vorhanden ist, enthält sie den zugewiesenen Namensraum in Klammern.
* Trefferdaten-Beginn in der dritten Zeile.

| Bezeichnungen | I2<br>ID-PERSON<br>DEL-PERSON<br>ACC-PERSON | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|---|---|---|---|---|---|
| **Variablenname **<br>**(Namespace)** | **MyProp1 **<br>**(Benutzer)** | **Besucher-ID **<br>**(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3 **<br>**(xyz)** |
| Trefferdaten | Mary | 77 | A | Mo | X |
|  | Mary | 88 | B | N | Y |
|  | Mary | 99 | C | O | Z |
|  | John | 77 | D | P | Mi |
|  | John | 88 | E | N | U |
|  | John | 44 | Fr | Q | V |
|  | John | 55 | G | R | X |
|  | Alice | 66 | A | N | Z |

## Beispielzugriffsanforderung

Wenn Sieh eine Zugriffsanfrage senden, enthält die Zusammenfassungsdatei die in der Tabelle unten angegebenen Werte. Eine Anfrage kann nur eine Gerätedatei, eine Personendatei oder je eine von beiden zurückgeben. Zwei Zusammenfassungsdateien werden nur zurückgegeben, wenn eine Personen-ID verwendet wird und &quot;developIds&quot;den Wert &quot;true&quot;hat.

| API-Werte | API-Werte | Dateityp | Daten in der <br>Zusammenfassungsdatei für den Zugriff | Daten in der <br>Zusammenfassungsdatei für den Zugriff | Daten in der <br>Zusammenfassungsdatei für den Zugriff | Daten in der <br>Zusammenfassungsdatei für den Zugriff | Daten in der <br>Zusammenfassungsdatei für den Zugriff |
|--- |--- |--- |---|---|---|---|---|
| **Namensraum/ID** | **expandIDs** |  | **MyProp1** | **Besucher-ID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| AAID=77 | false (falsch) | device | Variable nicht vorhanden | 77 | Variable nicht vorhanden | M, P | X, W |
| AAID=77 | true (wahr) | device | Variable nicht vorhanden | 77 | Variable nicht vorhanden | M, P | X, W |
| user=Mary | false (falsch) | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true (wahr) | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true (wahr) | device | nicht vorhanden | 77, 88 | nicht vorhanden | N, P | U, W |
| user=Mary  AAID=66 | true (wahr) | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary  AAID=66 | true (wahr) | device | nicht vorhanden | 66, 77, 88 | nicht vorhanden | N, P | U, W, Z |
| xyz=X | false (falsch) | device | nicht vorhanden | 55, 77 | nicht vorhanden | M, R | X |
| xyz=X | true (wahr) | device | nicht vorhanden | 55, 77 | nicht vorhanden | M, P, R | W, X |

Beachten Sie, dass die Einstellung für &quot;expandeIDs&quot;keine Auswirkungen auf die Ausgabe hat, wenn eine Cookie-ID verwendet wird.

## Musterlöschanforderung

Bei einer Löschanforderung mit den API-Werten in der ersten Tabellenzeile wird die Treffertabelle aktualisiert, sodass sie wie folgt aussieht:

| AAID=77 expandIDs value<br>does not matter | AAID=77 expandIDs value<br>does not matter | AAID=77 expandIDs value<br>does not matter | AAID=77 expandIDs value<br>does not matter | AAID=77 expandIDs value<br>does not matter |
|---|---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Mary | 42 | A | Datenschutz-7398 | Datenschutz-9152 |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 42 | D | Datenschutz-1866 | Datenschutz-8216 |
| John | 88 | E | N | U |
| John | 44 | Fr | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | Mi |

>[!NOTE] Dies hat nur Einfluss auf Zellen in Zeilen, die „AAID = 77“ und eine DEL-DEVICE-Beschriftung enthalten.

| user=Mary<br>expandIDs=false | user=Mary<br>expandIDs=false | user=Mary<br>expandIDs=false | user=Mary<br>expandIDs=false | user=Mary<br>expandIDs=false |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Datenschutz-0523 | 77 | Datenschutz-1866 | Datenschutz-3681 | X |
| Datenschutz-0523 | 88 | Datenschutz-2178 | Datenschutz-1975 | Y |
| Datenschutz-0523 | 99 | Datenschutz-9045 | Datenschutz-2864 | Z |
| John | 77 | D | P | Mi |
| John | 88 | E | N | U |
| John | 44 | Fr | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | Mi |

>[!NOTE] Dies hat nur Einfluss auf Zellen in Zeilen, die „user = Mary“ und eine DEL-PERSON-Beschriftung enthalten. In der Praxis würde es sich zudem bei der Variablen mit dem A_ID-Wert wahrscheinlich um ein Prop- oder eVar-Objekt handeln, und der zugehörige Ersatzwert wäre wahrscheinlich eine Zeichenfolge, die mit „Privacy Service-“ gefolgt von einer zufälligen Nummer (GUID) beginnt, statt dass der numerische Wert durch einen anderen, zufälligen numerischen Wert ersetzt wird.

| user=Mary<br>expandIDs=true | user=Mary<br>expandIDs=true | user=Mary<br>expandIDs=true | user=Mary<br>expandIDs=true | user=Mary<br>expandIDs=true |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Datenschutz-5782 | 09 | Datenschutz-0859 | Datenschutz-8183 | Datenschutz-9152 |
| Datenschutz-5782 | 16 | Datenschutz-6104 | Datenschutz-2911 | Datenschutz-6821 |
| Datenschutz-5782 | 83 | Datenschutz-2714 | Datenschutz-0219 | Datenschutz-4395 |
| John | 09 | D | Datenschutz-8454 | Datenschutz-8216 |
| John | 16 | E | Datenschutz-2911 | Datenschutz-2930 |
| John | 44 | Fr | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | Mi |

Beachten Sie Folgendes:

* Zellen in Zeilen, die `user=Mary` und die Beschriftung `DEL-DEVICE` oder `DEL-PERSON` enthalten, sind ebenso betroffen wie Zellen mit der Beschriftung `DEL-DEVICE` in Zeilen mit einer beliebigen Besucher-ID, die in einer Zeile mit dem Wert `user=Mary` auftritt.
* `MyEvar2` in der vierten und fünften Zeile wird aktualisiert, weil diese Zeilen dieselben Besucher-ID-Werte wie die in der ersten und zweiten Zeile enthalten. Demzufolge werden sie bei der ID-Erweiterung für Löschvorgänge auf Geräteebene einbezogen.
* Die Werte für `MyEvar2` in den Zeilen zwei und fünf stimmen vor und nach dem Löschvorgang überein. Sie stimmen jedoch nach dem Löschvorgang nicht mehr mit dem Wert N in der letzten Zeile überein, da diese Zeile im Rahmen der Löschanfrage nicht aktualisiert wurde.
* `MyEvar3` verhält sich mit ID-Erweiterung anders als ohne, da ohne ID-Erweiterung keine `ID-DEVICES` übereingestimmt haben. Jetzt stimmt `AAID` in den ersten fünf Zeilen überein.
