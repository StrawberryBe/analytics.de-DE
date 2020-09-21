---
description: 'null'
title: Beschriftungsbeispiel
uuid: a9a5b937-dbde-4f0f-a171-005ef4c79df9
translation-type: ht
source-git-commit: 322e2e87ab532d5e8a864dc06613a9b275c71df5
workflow-type: ht
source-wordcount: '802'
ht-degree: 100%

---


# Beschriftungsbeispiel

## Treffer-Beispieldaten

Angenommen, es liegen die folgenden Trefferdaten vor:

* Die erste Zeile enthält die Beschriftungen für die einzelnen Variablen.
* Die zweite Zeile entspricht dem Namen der Variable. Wenn sie eine ID-Beschriftung aufweist, enthält sie den zugewiesenen Namespace in Klammern.
* Die Trefferdaten beginnen in der dritten Reihe.

| Bezeichnungen | I2 <br> ID-PERSON <br> DEL-PERSON <br> ACC-PERSON | I2 <br> ID-DEVICE <br> DEL-DEVICE <br> ACC-ALL | I2 <br> DEL-PERSON <br> ACC-PERSON | I2 <br> DEL-DEVICE <br> DEL-PERSON <br> ACC-ALL | I2 <br> ID-DEVICE <br> DEL-DEVICE <br> ACC-ALL |
|---|---|---|---|---|---|
| **Variablenname** <br> **(Namespace)** | **MyProp1** <br> **(user)** | **Besucher-ID** <br> **(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3**  <br> **(xyz)** |
| Trefferdaten | Mary | 77 | A | M | X |
|  | Mary | 88 | B | N | Y |
|  | Mary | 99 | C | O | Z |
|  | John | 77 | D | P | W |
|  | John | 88 | E | N | U |
|  | John | 44 | F | Q | V |
|  | John | 55 | G | R | X |
|  | Alice | 66 | A | N | Z |

## Beispiel einer Zugriffsanfrage

Wenn Sieh eine Zugriffsanfrage senden, enthält die Zusammenfassungsdatei die in der Tabelle unten angegebenen Werte. Eine Anfrage kann nur eine Gerätedatei, eine Personendatei oder je eine von beiden zurückgeben. Zwei Zusammenfassungsdateien werden nur dann zurückgegeben, wenn eine Personen-ID verwendet wird und wenn die Option „expandIDs“ auf „true“ festgelegt ist.

| API-Werte | API-Werte | Zurückgegebener Dateityp | Daten in der <br>Zusammenfassungsdatei für den Zugriff | Daten in der <br>Zusammenfassungsdatei für den Zugriff | Daten in der <br>Zusammenfassungsdatei für den Zugriff | Daten in der <br>Zusammenfassungsdatei für den Zugriff | Daten in der <br>Zusammenfassungsdatei für den Zugriff |
|--- |--- |--- |---|---|---|---|---|
| **Namensraum/ID** | **expandIDs** |  | **MyProp1** | **Besucher-ID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| AAID=77 | false (falsch) | Gerät | Variable nicht vorhanden | 77 | Variable nicht vorhanden | M, P | X, W |
| AAID=77 | true (wahr) | Gerät | Variable nicht vorhanden | 77 | Variable nicht vorhanden | M, P | X, W |
| user=Mary | false (falsch) | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true (wahr) | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true (wahr) | Gerät | nicht vorhanden | 77, 88 | nicht vorhanden | N, P | U, W |
| user=Mary  AAID=66 | true (wahr) | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary  AAID=66 | true (wahr) | Gerät | nicht vorhanden | 66, 77, 88 | nicht vorhanden | N, P | U, W, Z |
| xyz=X | false (falsch) | Gerät | nicht vorhanden | 55, 77 | nicht vorhanden | M, R | X |
| xyz=X | true (wahr) | Gerät | nicht vorhanden | 55, 77 | nicht vorhanden | M, P, R | W, X |

Beachten Sie, dass die Einstellung für „expandIDs“ keinen Einfluss auf die Ausgabe hat, wenn eine Cookie-ID verwendet wird.

## Beispiel einer Löschanfrage

Wenn für eine Löschanfrage die API-Werte in der ersten Zeile der Tabelle verwendet werden, wird die Treffertabelle aktualisiert und sieht dann folgendermaßen aus:

| AAID=77 expandIDs value <br> does not matter | AAID=77 expandIDs value <br> does not matter | AAID=77 expandIDs value <br> does not matter | AAID=77 expandIDs value <br> does not matter | AAID=77 expandIDs value <br> does not matter |
|---|---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Mary | 42 | A | Datenschutz-7398 | Datenschutz-9152 |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 42 | D | Datenschutz-1866 | Datenschutz-8216 |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE]
>
>Dies hat nur Einfluss auf Zellen in Zeilen, die „AAID = 77“ und eine DEL-DEVICE-Beschriftung enthalten.

| user=Mary <br> expandIDs=false | user=Mary <br> expandIDs=false | user=Mary <br> expandIDs=false | user=Mary <br> expandIDs=false | user=Mary <br> expandIDs=false |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Datenschutz-0523 | 77 | Datenschutz-1866 | Datenschutz-3681 | X |
| Datenschutz-0523 | 88 | Datenschutz-2178 | Datenschutz-1975 | Y |
| Datenschutz-0523 | 99 | Datenschutz-9045 | Datenschutz-2864 | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE]
>
>Dies hat nur Einfluss auf Zellen in Zeilen, die „user = Mary“ und eine DEL-PERSON-Beschriftung enthalten. In der Praxis würde es sich zudem bei der Variablen mit dem A_ID-Wert wahrscheinlich um ein Prop- oder eVar-Objekt handeln, und der zugehörige Ersatzwert wäre wahrscheinlich eine Zeichenfolge, die mit „Privacy-“ gefolgt von einer zufälligen Nummer (GUID) beginnt, statt dass der numerische Wert durch einen anderen, zufälligen numerischen Wert ersetzt wird.

| user=Mary <br> expandIDs=true | user=Mary <br> expandIDs=true | user=Mary <br> expandIDs=true | user=Mary <br> expandIDs=true | user=Mary <br> expandIDs=true |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Datenschutz-5782 | 09 | Datenschutz-0859 | Datenschutz-8183 | Datenschutz-9152 |
| Datenschutz-5782 | 16 | Datenschutz-6104 | Datenschutz-2911 | Datenschutz-6821 |
| Datenschutz-5782 | 83 | Datenschutz-2714 | Datenschutz-0219 | Datenschutz-4395 |
| John | 09 | D | Datenschutz-8454 | Datenschutz-8216 |
| John | 16 | E | Datenschutz-2911 | Datenschutz-2930 |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

Beachten Sie Folgendes:

* Zellen in Zeilen, die `user=Mary` und die Beschriftung `DEL-DEVICE` oder `DEL-PERSON` enthalten, sind ebenso betroffen wie Zellen mit der Beschriftung `DEL-DEVICE` in Zeilen mit einer beliebigen Besucher-ID, die in einer Zeile mit dem Wert `user=Mary` auftritt.
* `MyEvar2` in der vierten und fünften Zeile wird aktualisiert, weil diese Zeilen dieselben Besucher-ID-Werte wie die in der ersten und zweiten Zeile enthalten. Demzufolge werden sie bei der ID-Erweiterung für Löschvorgänge auf Geräteebene einbezogen.
* Die Werte für `MyEvar2` in den Zeilen zwei und fünf stimmen vor und nach dem Löschvorgang überein. Sie stimmen jedoch nach dem Löschvorgang nicht mehr mit dem Wert N in der letzten Zeile überein, da diese Zeile im Rahmen der Löschanfrage nicht aktualisiert wurde.
* `MyEvar3` verhält sich mit ID-Erweiterung anders als ohne, da ohne ID-Erweiterung keine `ID-DEVICES` übereingestimmt haben. Jetzt stimmt `AAID` in den ersten fünf Zeilen überein.
