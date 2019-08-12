---
description: 'null '
seo-description: 'null '
seo-title: Beschriftungsbeispiel
title: Beschriftungsbeispiel
uuid: a 9 a 5 b 937-dbde -4 f 0 f-a 171-005 ef 4 c 79 df 9
translation-type: tm+mt
source-git-commit: edafa9ca8dc34bd1f3af8c56b4f23c4a983aa677

---


# Beschriftungsbeispiel

## Treffer-Beispieldaten

Angenommen, es liegen die folgenden Trefferdaten vor:

* Die erste Zeile enthält die Beschriftungen für die einzelnen Variablen.
* Die zweite Zeile entspricht dem Namen der Variable. Wenn sie eine ID-Beschriftung aufweist, enthält sie den zugewiesenen Namespace in Klammern.
* Die Trefferdaten beginnen in der dritten Reihe.

| Bezeichnungen | I2<br>ID-PERSONDEL<br>-PERSONACC<br>-PERSONAL | I 2<br>ID-DEVICEDEL<br>-DEVICEACC<br>-ALL | I 2<br>DEL-PERSONACC<br>-PEOPLE | I 2<br>DEL-DEVICEDEL<br>-PERSONACC<br>-ALL | I 2<br>ID-DEVICEDEL<br>-DEVICEACC<br>-ALL |
|---|---|---|---|---|---|
| **Variablenname**<br>**(Namespace)** | **Myprop 1**<br>**(Benutzer)** | **Besucher-ID**<br>**(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3**<br>**(xyz)** |
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

| API-Werte | API-Werte | Zurückgegebener Dateityp | Data in <br>Summary Access File | Data in <br>Summary Access File | Data in <br>Summary Access File | Data in <br>Summary Access File | Data in <br>Summary Access File |
|--- |--- |--- |---|---|---|---|---|
| **Namensraum/ID** | **expandIDs** |  | **MyProp1** | **Visitor ID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| AAID=77 | false | Gerät | Variable nicht vorhanden | 77 | Variable nicht vorhanden | M, P | X, W |
| AAID=77 | true | Gerät | Variable nicht vorhanden | 77 | Variable nicht vorhanden | M, P | X, W |
| user=Mary | false | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true | Gerät | nicht vorhanden | 77, 88 | nicht vorhanden | N, P | U, W |
| user=Mary AAID=66 | true | Person | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary AAID=66 | true | Gerät | nicht vorhanden | 66, 77, 88 | nicht vorhanden | N, P | U, W, Z |
| xyz=X | false | Gerät | nicht vorhanden | 55, 77 | nicht vorhanden | M, R | X |
| xyz=X | true | Gerät | nicht vorhanden | 55, 77 | nicht vorhanden | M, P, R | W, X |

Beachten Sie, dass die Einstellung für „expandIDs“ keinen Einfluss auf die Ausgabe hat, wenn eine Cookie-ID verwendet wird.

## Beispiel einer Löschanfrage

Wenn für eine Löschanfrage die API-Werte in der ersten Zeile der Tabelle verwendet werden, wird die Treffertabelle aktualisiert und sieht dann folgendermaßen aus:

| AAID=77 expandIDs value<br>does not matter | AAID=77 expandIDs value<br>does not matter | AAID=77 expandIDs value<br>does not matter | AAID=77 expandIDs value<br>does not matter | AAID=77 expandIDs value<br>does not matter |
|---|---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Mary | 42 | A | GDPR-7398 | GDPR-9152 |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 42 | D | GDPR-1866 | GDPR-8216 |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE] Nur Zellen in Zeilen mit AAID = 77 und einer DEL-DEVICE-Beschriftung sind betroffen.

| user = maryexpandids<br>= false | user = maryexpandids<br>= false | user = maryexpandids<br>= false | user = maryexpandids<br>= false | user = maryexpandids<br>= false |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| GDPR-0523 | 77 | GDPR-1866 | GDPR-3681 | X |
| GDPR-0523 | 88 | GDPR-2178 | GDPR-1975 | Y |
| GDPR-0523 | 99 | GDPR-9045 | GDPR-2864 | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE] Nur Zellen in Zeilen, die Benutzer = Mary und eine DEL-Personenbeschriftung enthalten, sind betroffen. In der Praxis würde es sich zudem bei der Variablen mit dem A_ID-Wert wahrscheinlich um ein Prop- oder eVar-Objekt handeln, und der zugehörige Ersatzwert wäre wahrscheinlich eine Zeichenfolge, die mit „DSGVO“ gefolgt von einer zufälligen Nummer (GUID) beginnt, statt dass der numerische Wert durch einen anderen, zufälligen numerischen Wert ersetzt wird.

| user=Mary<br>expandIDs=true | user = maryexpandids<br>= true | user = maryexpandids<br>= true | user = maryexpandids<br>= true | user = maryexpandids<br>= true |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| GDPR-5782 | 09 | GDPR-0859 | GDPR-8183 | GDPR-9152 |
| GDPR-5782 | 16 | GDPR-6104 | GDPR-2911 | GDPR-6821 |
| GDPR-5782 | 83 | GDPR-2714 | GDPR-0219 | GDPR-4395 |
| John | 09 | D | GDPR-8454 | GDPR-8216 |
| John | 16 | E | GDPR-2911 | GDPR-2930 |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

Beachten Sie Folgendes:

* Cells on rows containing `user=Mary` and a `DEL-DEVICE` or `DEL-PERSON` label are impacted, as well as cells with a `DEL-DEVICE` label on rows containing any Visitor ID that occurred on a row containing `user=Mary`.
* `MyEvar2`“ in der vierten und fünften Zeile wird aktualisiert, weil diese Zeilen dieselben Besucher-ID-Werte wie die in der ersten und zweiten Zeile enthalten. Demzufolge werden sie bei der ID-Erweiterung für Löschvorgänge auf Geräteebene einbezogen.
* The values of `MyEvar2` in rows two and five match both before and after the delete, but after the delete no longer matches the value N that occurs in the last row, because that row was not updated as part of the delete request.
* `MyEvar3` verhält sich mit ID-Erweiterung anders als ohne, da ohne ID-Erweiterung keine übereingestimmt haben. `ID-DEVICES` Now `AAID` matches on the first five rows.
