---
description: 'null '
seo-description: 'null '
seo-title: Beschriftungsbeispiel
title: Beschriftungsbeispiel
uuid: a 9 a 5 b 937-dbde -4 f 0 f-a 171-005 ef 4 c 79 df 9
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Beschriftungsbeispiel

## Treffer-Beispieldaten {#section_94DE6BC0026F46D7AD7061C5625C8D52}

Angenommen, es liegen die folgenden Trefferdaten vor:

* Die erste Zeile enthält die Beschriftungen für die einzelnen Variablen.
* Die zweite Zeile entspricht dem Namen der Variable. Wenn sie eine ID-Beschriftung aufweist, enthält sie den zugewiesenen Namespace in Klammern.
* Die Trefferdaten beginnen in der dritten Reihe.

<!-- Meike, I converted html tables for fix elusive validation error. Bob -->

| Bezeichnungen | I2<br>ID-PERSONDEL<br>-PERSONACC<br>-PERSONAL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|:---:|:---:|:---:|:---:|:---:|:---:|
| Variable Name<br>(Namespace) | MyProp1<br>(user) | Visitor ID<br>(AAID) | MyEvar1 | MyEvar2 | MyEvar3<br>(xyz) |
| Trefferdaten | Mary | 77 | A | M | X |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | Z |


## Beispiel einer Zugriffsanfrage {#section_BDA817FD2415420DAAC835825484BA9D}

Wenn Sieh eine Zugriffsanfrage senden, enthält die Zusammenfassungsdatei die in der Tabelle unten angegebenen Werte. Eine Anfrage kann nur eine Gerätedatei, eine Personendatei oder je eine von beiden zurückgeben. Zwei Zusammenfassungsdateien werden nur dann zurückgegeben, wenn eine Personen-ID verwendet wird und wenn die Option „expandIDs“ auf „true“ festgelegt ist.

| API-Werte | Zurückgegebener Dateityp | Daten in der Zusammenfassungsdatei für den Zugriff |
|--- |--- |--- |
| Namensraum/ID | expandIDs |  | MyProp1 | Visitor ID | MyEvar1 | MyEvar2 | MyEvar3 |
| AAID=77 | false | Gerät | Variable nicht vorhanden | 77 | Variable nicht vorhanden | M, P | X, W |
| AAID=77 | true | Gerät | 77 | M, P | X, W |
| user=Mary | false | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| Gerät | nicht vorhanden | 77, 88 | nicht vorhanden | N, P | U, W |
| user=Mary AAID=66 | true | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| Gerät | nicht vorhanden | 66, 77, 88 | nicht vorhanden | N, P | U, W, Z |
| xyz=X | false | Gerät | nicht vorhanden | 55, 77 | nicht vorhanden | M, R | X |
| xyz=X | true | Gerät | nicht vorhanden | 55, 77 | nicht vorhanden | M, P, R | W, X |

Beachten Sie, dass die Einstellung für „expandIDs“ keinen Einfluss auf die Ausgabe hat, wenn eine Cookie-ID verwendet wird.

## Beispiel einer Löschanfrage {#section_6C75F70F5D574BE7AA540981E8B7EA26}

Wenn für eine Löschanfrage die API-Werte in der ersten Zeile der Tabelle verwendet werden, wird die Treffertabelle aktualisiert und sieht dann folgendermaßen aus:

| AAID = 77 expandids-Wert ist nicht wichtig |
|--- |
| MyProp1 | AAID | MyEvar1 | MyEvar2 | MyEvar3 |
| Mary | 42 | A | GDPR-7398 | GDPR-9152 |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 42 | D | GDPR-1866 | GDPR-8216 |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE]
>
>Nur Zellen in Zeilen mit AAID = 77 und einer DEL-DEVICE-Beschriftung sind betroffen.

| user = Mary expandids = false |
|--- |
| MyProp1 | AAID | MyEvar1 | MyEvar2 | MyEvar3 |
| GDPR-0523 | 77 | GDPR-1866 | GDPR-3681 | X |
| GDPR-0523 | 88 | GDPR-2178 | GDPR-1975 | Y |
| GDPR-0523 | 99 | GDPR-9045 | GDPR-2864 | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE]
>
>Nur Zellen in Zeilen, die Benutzer = Mary und eine DEL-Personenbeschriftung enthalten, sind betroffen. In der Praxis würde es sich zudem bei der Variablen mit dem A_ID-Wert wahrscheinlich um ein Prop- oder eVar-Objekt handeln, und der zugehörige Ersatzwert wäre wahrscheinlich eine Zeichenfolge, die mit „DSGVO“ gefolgt von einer zufälligen Nummer (GUID) beginnt, statt dass der numerische Wert durch einen anderen, zufälligen numerischen Wert ersetzt wird.

| user=Mary expandIDs=true |
|--- |
| MyProp1 | AAID | MyEvar1 | MyEvar2 | MyEvar3 |
| GDPR-5782 | 09 | GDPR-0859 | GDPR-8183 | GDPR-9152 |
| GDPR-5782 | 16 | GDPR-6104 | GDPR-2911 | GDPR-6821 |
| GDPR-5782 | 83 | GDPR-2714 | GDPR-0219 | GDPR-4395 |
| John | 09 | D | GDPR-8454 | GDPR-8216 |
| John | 16 | E | GDPR-2911 | GDPR-2930 |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

Beachten Sie Folgendes:

* Zellen in Zeilen, die „user=Mary“ und eine DEL-DEVICE- oder DEL-PERSON-Beschriftung enthalten, sind ebenso betroffen wie Zellen mit einer DEL-DEVICE-Beschriftung in Zeilen mit einer beliebigen Besucher-ID, die in einer Zeile mit dem Wert „user=Mary“ auftritt.
* „MyEvar2“ in der vierten und fünften Zeile wird aktualisiert, weil diese Zeilen dieselben Besucher-ID-Werte wie die in der ersten und zweiten Zeile enthalten. Demzufolge werden sie bei der ID-Erweiterung für Löschvorgänge auf Geräteebene einbezogen.
* Die Werte für „MyEvar2“ in den Zeilen zwei und fünf stimmen vor und nach dem Löschvorgang überein. Sie stimmen jedoch nach dem Löschvorgang nicht mehr mit dem Wert N in der letzten Zeile überein, da diese Zeile im Rahmen der Löschanfrage nicht aktualisiert wurde.
* MyEvar3 verhält sich mit ID-Erweiterung anders als ohne, da ohne ID-Erweiterung keine ID-DEVICES übereingestimmt haben. Jetzt stimmt „AAID “ in den ersten fünf Zeilen überein.
