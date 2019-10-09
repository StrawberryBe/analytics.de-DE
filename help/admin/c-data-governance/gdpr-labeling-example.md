---
description: 'null'
seo-description: 'null'
seo-title: Beschriftungsbeispiel
title: Beschriftungsbeispiel
uuid: a9a5b937-dbde-4f0f-a171-005ef4c79df9
translation-type: tm+mt
source-git-commit: d2134271c4586d629c8b25f60c746902ba13683b

---


# Beschriftungsbeispiel

## Treffer-Beispieldaten

Angenommen, es liegen die folgenden Trefferdaten vor:

* Die erste Zeile enthält die Beschriftungen für die einzelnen Variablen.
* Die zweite Zeile entspricht dem Namen der Variable. Wenn sie eine ID-Beschriftung aufweist, enthält sie den zugewiesenen Namespace in Klammern.
* Die Trefferdaten beginnen in der dritten Reihe.

| Bezeichnungen | I2<br>ID-<br>PERSONDEL-<br>PERSONACC-PERSON | I2<br>ID-<br>DEVICEDEL-<br>DEVICEACC-ALL | I2<br>DEL-<br>PERSONACC-PERSON | I2<br>DEL-<br>DEVICEDEL-<br>PERSONACC-ALL | I2<br>ID-<br>DEVICEDEL-<br>DEVICEACC-ALL |
|---|---|---|---|---|---|
| **Variablenname**<br>**(Namespace)** | **MyProp1**<br>**(Benutzer)** | **Besucher-ID**<br>**(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3**<br>**(xyz)** |
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
| Mary | 42 | A | Privacy-7398 | Privacy-9152 |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 42 | D | Privacy-1866 | Privacy-8216 |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE] Nur Zellen in Zeilen mit AAID = 77 und einer DEL-GERÄTEbeschriftung sind betroffen.

| user=<br>MarytenderIDs=false | user=<br>MarytenderIDs=false | user=<br>MarytenderIDs=false | user=<br>MarytenderIDs=false | user=<br>MarytenderIDs=false |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Privacy-0523 | 77 | Privacy-1866 | Privacy-3681 | X |
| Privacy-0523 | 88 | Privacy-2178 | Privacy-1975 | Y |
| Privacy-0523 | 99 | Privacy-9045 | Privacy-2864 | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE] Nur Zellen in Zeilen, die die Beschriftung "user=Mary"und "DEL-PERSON"enthalten, sind betroffen. In der Praxis wäre die Variable, die A_ID enthält, wahrscheinlich eine Eigenschaftsvariable oder eVar, und ihr Ersetzungswert wäre eine Zeichenfolge, die mit "Privacy" beginnt, gefolgt von einer Zufallszahl (GUID), anstatt den numerischen Wert durch einen anderen, zufälligen numerischen Wert zu ersetzen.

| user=<br>MarytenderIDs=true | user=<br>MarytenderIDs=true | user=<br>MarytenderIDs=true | user=<br>MarytenderIDs=true | user=<br>MarytenderIDs=true |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Privacy-5782 | 09 | Privacy-0859 | Privacy-8183 | Privacy-9152 |
| Privacy-5782 | 16 | Privacy-6104 | Privacy-2911 | Privacy-6821 |
| Privacy-5782 | 83 | Privacy-2714 | Privacy-0219 | Privacy-4395 |
| John | 09 | D | Privacy-8454 | Privacy-8216 |
| John | 16 | E | Privacy-2911 | Privacy-2930 |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

Beachten Sie Folgendes:

* Cells on rows containing `user=Mary` and a `DEL-DEVICE` or `DEL-PERSON` label are impacted, as well as cells with a `DEL-DEVICE` label on rows containing any Visitor ID that occurred on a row containing `user=Mary`.
* `MyEvar2`“ in der vierten und fünften Zeile wird aktualisiert, weil diese Zeilen dieselben Besucher-ID-Werte wie die in der ersten und zweiten Zeile enthalten. Demzufolge werden sie bei der ID-Erweiterung für Löschvorgänge auf Geräteebene einbezogen.
* The values of `MyEvar2` in rows two and five match both before and after the delete, but after the delete no longer matches the value N that occurs in the last row, because that row was not updated as part of the delete request.
* `MyEvar3` verhält sich mit ID-Erweiterung anders als ohne, da ohne ID-Erweiterung keine übereingestimmt haben. `ID-DEVICES` Now `AAID` matches on the first five rows.
