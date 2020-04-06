---
description: Classification-Regeln suchen regelmäßig nach nicht klassifizierten Begriffen. Wenn eine Regelübereinstimmung gefunden wird, fügen die Regeln die Begriffe automatisch zu Ihren Classification-Datentabellen hinzu. Sie können auch Classification-Regeln verwenden, um vorhandene Schlüssel zu überschreiben.
subtopic: Classifications
title: Klassifizierungsregeln
topic: Admin tools
uuid: 08685919-216d-448b-b886-3adf5ff5405e
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Klassifizierungsregeln

Classification-Regeln suchen regelmäßig nach nicht klassifizierten Begriffen. Wenn eine Regelübereinstimmung gefunden wird, fügen die Regeln die Begriffe automatisch zu Ihren Classification-Datentabellen hinzu. Sie können auch Classification-Regeln verwenden, um vorhandene Schlüssel zu überschreiben.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

Mit dem Rule Builder können Sie einen *`classification rule set`* erstellen, der eine Liste von *`classification rules`* ist. Eine Regel entspricht den von Ihnen angegebenen Kriterien und führt dann eine Aktion durch.

Classification-Regeln eignen sich für:

* **E-Mail** - und **Display-Anzeigen**: Erstellen Sie Classification-Regeln, um individuelle Display-Anzeigengruppen zu gruppieren, sodass Sie die Leistung der Display-Kampagnen im Vergleich zu E-Mail-Kampagnen verdienen können.

* **Rückverfolgungscodes**: Erstellen Sie Classification-Regeln, um aus Zeichenfolgen in Trackingcodes abgeleitete Schlüsselwerte zu kategorisieren und sie bestimmten von Ihnen definierten Kriterien zuzuordnen.
* **Suchbegriffe**: Mithilfe von  [regulären Ausdrücken](/help/components/c-classifications2/crb/classification-quickstart-rules.md) und Platzhaltern vereinfachen Sie die Classification der Suchbegriffe. Wenn ein Suchbegriff beispielsweise *`baseball`* enthält, können Sie eine *`Sports League`*-Klassifizierung auf *`MLB`* festlegen.

Der Trackingcode für eine E-Mail-Kampagnen-ID lautet beispielsweise:

`em:Summer:2013:Sale`.

Sie können drei Regeln in einem Regelsatz festlegen, die die Teile der Zeichenfolge ermitteln, und dann die Werte klassifizieren:

| Regeltyp auswählen | Übereinstimmungskriterien eingeben | Classification auswählen | Hierzu |
|---|---|---|---|
| Beginnt mit | em: | Kanal | E-Mail |
| Endet in | Verkauf | Typ | Verkauf |
| Enthält | 2013 | Jahr | 2013 |

## Verarbeitung der Regeln {#how-rules-are-processed}

Wichtige Informationen zur Verarbeitung von Classification-Regeln.

<!-- 

about_classification_rules.xml

 -->

* [Wichtige Informationen zu Regeln](/help/components/c-classifications2/crb/classification-rule-builder.md)
* [Wann werden Schlüssel nicht in Regeln klassifiziert?](/help/components/c-classifications2/crb/classification-rule-builder.md)
* [Informationen zur Regelpriorität](/help/components/c-classifications2/crb/classification-quickstart-rules.md)

>[!NOTE] Nummerisch-2-Klassifizierungen werden [!UICONTROL Rule Builder] nicht unterstützt.

## Wichtige Informationen zu Regeln

* Legen Sie [Gruppenberechtigungen](https://marketing.adobe.com/resources/help/de_DE/reference/groups.html) für Classifications in fest [!UICONTROL Admin Tools].

* **Reguläre Ausdrücke**: Hilfe finden Sie unter [Reguläre Ausdrücke in Klassifizierungsregeln](/help/components/c-classifications2/crb/classification-quickstart-rules.md).

* **Report Suites**: Sie können erst dann eine Classification auswählen, wenn mindestens eine Report Suite ausgewählt ist. Sie können die Report Suite erst dann anwenden, wenn Sie den Regelsatz erstellt und eine Variable zugewiesen haben.

   Wenn Sie den Regelsatz testen, verwenden Sie Schlüssel (die zu klassifizierende Variable) aus dem Bericht, um zu sehen, wie sie von dem Regelsatz beeinflusst werden. (The [key](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md) is the variable being classified, or the first column in the classification upload table.)

* **Regelpriorität**: Wenn ein Schlüssel mit mehreren Regeln übereinstimmt, die dieselbe Classification festlegen (in der [!UICONTROL Set Classification] Spalte), wird die letzte mit der Classification übereinstimmende Regel verwendet. See [About Rule Priority](/help/components/c-classifications2/crb/classification-quickstart-rules.md).

* **Begrenzungen der Anzahl der Regeln**: Für die Anzahl der Regeln, die Sie erstellen können, gibt es keine festgelegte Beschränkung. Eine große Anzahl von Regeln kann sich jedoch auf die Browserleistung auswirken.
* **Verarbeitung**: Regeln werden in kurzen Abständen verarbeitet, je nach dem Umfang des klassifizierungsbezogenen Traffics.

   Aktive Regeln werden alle vier Stunden verarbeitet, wobei Classification-Daten in der Regel einen Monat zurückgehen. Die Regeln suchen automatisch nach neuen Werten und laden die Klassifizierungen mit dem Importeur hoch.

* **Überschreiben von vorhandenen Classifications:** Siehe [In welchen Fällen werden Schlüssel nicht durch Regeln klassifiziert?](/help/components/c-classifications2/crb/classification-quickstart-rules.md) Bei Bedarf können Sie vorhandene Klassifizierungen mithilfe des Imports löschen oder entfernen.

## Wann werden Schlüssel nicht in Regeln klassifiziert?

Wenn Sie Regeln aktivieren, können Sie vorhandene Classifications überschreiben. In den folgenden Situationen wird ein  [Schlüssel](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md) (eine Variable) nicht durch eine Classification-Regel klassifiziert, wenn Folgendes gilt:

* Der Schlüssel wurde bereits klassifiziert, und Sie haben nicht die Option [Überschreiben von Classifications für](/help/components/c-classifications2/crb/classification-rule-definitions.md) ausgewählt.

   Sie können Classifications überschreiben, wenn Sie  eine Regel [hinzufügen und aktivieren](/help/components/c-classifications2/crb/classification-quickstart-rules.md), und wenn Sie eine Data Connectors-Integration aktivieren. (Bei Data Connectors werden Regeln von Partnern im Dev Center erstellt und im [!UICONTROL Classification Rule Builder]angezeigt.)

* Ein klassifizierter Schlüssel wurde nicht in den Daten nach Ablauf eines Zeitraums angezeigt, der beim Überschreiben eines Schlüssels angegeben wurde, auch nicht, nachdem Sie die Option &quot;Klassifizierungen [überschreiben&quot;aktiviert haben](/help/components/c-classifications2/crb/classification-rule-definitions.md).
* Der Schlüssel wird nicht klassifiziert, und nach Beginn des Zeitrahmens (vor etwa einem Monat) wurde der Schlüssel auch nicht in [!DNL Adobe Analytics] übergeben.

   >[!NOTE]
   >
   >In Berichten gelten Klassifizierungen für jeden beliebigen angegebenen Zeitrahmen, sofern ein Schlüssel existiert. Der Datumsbereich eines Berichts wirkt sich nicht auf die Berichterstellung aus.

![](assets/overwrite_keys.png)

## Reguläre Ausdrücke in Classification-Regeln {#regex-in-classification-rules}

Verwenden Sie reguläre Ausdruck, um konsistent formatierte Zeichenfolgenwerte mit einer Classification abzugleichen. Sie können beispielsweise eine Classification aus bestimmten Zeichen in einem Trackingcode erstellen. Sie können bestimmte Zeichen, Wörter oder Zeichenmuster abgleichen.

<!-- 

regex_classification_rules.xml

 -->

* [Regulärer Ausdruck – Beispiel für Trackingcode](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_2EF7951398EB4C2F8E52CEFAB4032669)
* [Regulärer Ausdruck – Klassifizieren eines bestimmten Zeichens](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_5D300C03FA484BADACBFCA983E738ACF)
* [Reguläre Ausdrücke – Abgleichen von Trackingcodes unterschiedlicher Länge](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_E86F5BF5C2F44ABC8FFCE3EA67EE3BB2)
* [Reguläre Ausdrücke – Beispiel für „enthält nicht“ ](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_FCA88A612A4E4B099458E3EF7B60B59C)
* [Reguläre Ausdrücke – Referenztabelle](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_0211DCB1760042099CCD3ED7A665D716)

>[!NOTE] Reguläre Ausdrücke eignen sich als Best Practice für Trackingcodes, in denen Trennzeichen verwendet werden; dies gehört zu den bewährten Verfahren.

## Regulärer Ausdruck – Beispiel für Trackingcode {#section_2EF7951398EB4C2F8E52CEFAB4032669}

>[!NOTE] Wenn der Trackingcode URL-kodiert ist, wird er **nicht** durch den Rule Builder klassifiziert.

In diesem Beispiel wird angenommen, dass die folgende Kampagnen-ID klassifiziert werden soll:

[!UICONTROL Sample Key]: `em:JuneSale:20130601`

Die folgenden Teile des Trackingcodes sind zu klassifizieren:

* `em` = email
* `JuneSale` = Kampagnenname
* `20130601` = date

[!UICONTROL Regular Expression]: `^(.+)\:(.+)\:(.+)$`

Korreliert der reguläre Ausdruck mit der Kampagnen-ID:

![](assets/regex.png)

[!UICONTROL Match Groups]: Zeigt, wie der reguläre Ausdruck den Zeichen der Kampagnen-ID entspricht, sodass Sie eine Position in der Kampagnen-ID klassifizieren können.

![](assets/regex_tracking_code.png)

In diesem Beispiel gilt die Regel, dass sich das Kampagnendatum `20140601` in der dritten Gruppe `(.+)` befindet, identifiziert durch `$3`.

**[!UICONTROL Rule Builder]**

In the [!UICONTROL Rule Builder], configure the rule as follows:

| Regeltyp auswählen | Übereinstimmungskriterien eingeben | Classification auswählen | Hierzu |
|---|---|---|---|
| Regulärer Ausdruck | &amp;Hat;(.+)\:(.+)\:(.+)$ | Kampagne | 3$ |

**Syntax**

| Regulärer Ausdruck | Zeichenfolge oder Übereinstimmungsergebnis | Entsprechende Übereinstimmungsgruppen |
|--- |--- |--- |
| `^(.+)\:(.+)\:(.+)$` | em:JuneSale:20130601 | `$0`: em:JuniAusverkauf:20130601  `$1`: em  `$2`: JuniAusverkauf`$3`: 20130601 |
| Aufbauen der Syntax | `^` = Beginn einer Zeile () = gruppiert Zeichen und ermöglicht das Extrahieren von übereinstimmenden Zeichen in den Klammern.  `(.+)` = erfasst ein ( . ) Zeichen und ( + ) beliebige mehr \ = Beginn einer Zeichenfolge.  `$` = gibt an, dass das vorhergehende Zeichen (oder die vorhergehende Zeichengruppe) das letzte Element in der Zeile ist. |

Weitere Informationen zur Bedeutung der Zeichen in einem regulären Ausdruck finden Sie unter [Reguläre Ausdrücke – Referenztabelle](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_0211DCB1760042099CCD3ED7A665D716).

## Regulärer Ausdruck – Klassifizieren eines bestimmten Zeichens  {#section_5D300C03FA484BADACBFCA983E738ACF}

Eine Möglichkeit, einen regulären Ausdruck zu verwenden, besteht darin, ein bestimmtes Zeichen in einer Zeichenfolge zu klassifizieren. Beispiel: Der folgende Trackingcode enthält zwei wichtige Zeichen:

[!UICONTROL Sample Key]: `4s3234`

* `4` = Markenname
* `s` = Suchmaschine, z. B. Google

![](assets/regex_char_position.png)

**[!UICONTROL Rule Builder]**

In the [!UICONTROL Rule Builder], configure the rule as follows:

| Regeltyp auswählen | Übereinstimmungskriterien eingeben | Classification auswählen | Hierzu |
|--- |--- |--- |--- |
| Regulärer Ausdruck | `^.(s).*$` | Marke und Suchmaschine | `$0` (Erfasst die ersten beiden Zeichen für den Markennamen und die Suchmaschine.) |
| Regulärer Ausdruck | `^.(s).*$` | Suchmaschine | `$1` (Erfasst das zweite Zeichen für Google.) |

## Reguläre Ausdrücke – Abgleichen von Trackingcodes unterschiedlicher Länge {#section_E86F5BF5C2F44ABC8FFCE3EA67EE3BB2}

Dieses Beispiel zeigt, wie Sie bestimmte Zeichen zwischen Doppelpunkt-Trennzeichen identifizieren, wenn Sie Rückverfolgungscodes unterschiedlicher Länge haben. Adobe empfiehlt die Verwendung eines regulären Ausdrucks für jeden Rückverfolgungscode.

Beispielschlüssel:

* `a:b`
* `a:b:c`
* `a:b:c:d`

**Syntax**

![](assets/regex_b.png)

![](assets/regex_varying_length.png)

**[!UICONTROL Rule Builder]**

In the [!UICONTROL Rule Builder], configure the rule as follows:

| Regeltyp auswählen | Übereinstimmungskriterien eingeben | Classification auswählen | Hierzu |
|--- |--- |--- |--- |
| Regulärer Ausdruck: Für Übereinstimmungszeichenfolge a:b | `^([^\:]+)\:([^\:]+)$` | a | `$1` |
| Regulärer Ausdruck: Für Übereinstimmungszeichenfolge a:b | `^([^\:]+)\:([^\:]+)$` | b | `$2` |
| Regulärer Ausdruck: Für Übereinstimmungszeichenfolge a:b: c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | a | `$1` |
| Regulärer Ausdruck: Für Übereinstimmungszeichenfolge a:b: c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | b | `$2` |
| Regulärer Ausdruck: Für Übereinstimmungszeichenfolge a:b: c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | c | `$3` |
| Regulärer Ausdruck  Für Übereinstimmungszeichenfolge a:b:c:d | `^([^\:]+)\:([^\:]+)\:([^\:]+)\:([^\:])$` | d | `$4` |

## Reguläre Ausdrücke – Beispiel für „enthält nicht“ {#section_FCA88A612A4E4B099458E3EF7B60B59C}

Dieses Beispiel zeigt einen regulären Ausdruck, mit dem alle Zeichenfolgen abgeglichen werden, die bestimmte Zeichen nicht enthalten (in diesem Fall `13`).

Regulärer Ausdruck:

`^(?!.*13.*).*$`

Testzeichenfolgen:

```
a:b:
a:b:1313
c:d:xoxo
c:d:yoyo
```

Übereinstimmungsergebnisse:

```
a:b:
c:d:xoxo
c:d:yoyo
```

In diesem Ergebnis zeigt `a:b:1313` keine Übereinstimmung an.

## Reguläre Ausdrücke – Referenztabelle {#section_0211DCB1760042099CCD3ED7A665D716}

| Ausdruck | Beschreibung |
|---|---|
| `(?ms)` | Hierdurch wird der gesamte reguläre Ausdruck mit einer mehrzeiligen Eingabe abgeglichen, wodurch die Variable aktiviert wird. Platzhalter für alle Zeilenumbruchzeichen |
| (`?i`) | Bei regulären Ausdrücken muss die Groß-/Kleinschreibung nun nicht mehr berücksichtigt werden |
| [`abc`] | Beliebiges einzelnes Zeichen aus: a, b oder c |
| [`^abc`] | Beliebiges einzelnes Zeichen, außer: a, b oder c |
| [`a-z`] | Beliebiges einzelnes Zeichen im Bereich a-z |
| [`a-zA-Z`] | Beliebiges einzelnes Zeichen im Bereich a-z oder A-Z |
| `^` | Zeilenanfang (Übereinstimmung mit dem Zeilenanfang) |
| `$` | Übereinstimmung mit dem Zeilenende (oder vor dem Umbruch am Ende) |
| `\A` | Beginn der Zeichenfolge |
| `\z` | Ende der Zeichenfolge |
| `.` | Übereinstimmung mit einem beliebigen Zeichen (außer Umbruch) |
| `\s` | Beliebiges Whitespace-Zeichen |
| `\S` | Beliebiges Zeichen, außer Whitespace-Zeichen |
| `\d` | Beliebige Ziffer |
| `\D` | Beliebiges Zeichen, außer Ziffern |
| `\w` | Beliebiges Zeichen, das in Wörtern zulässig ist (Buchstabe, Ziffer, Unterstrich) |
| `\W` | Beliebiges Zeichen, das nicht in Wörtern zulässig ist |
| `\b` | Beliebige Wortgrenze |
| `(...)` | Alles erfassen zwischen |
| `(a|b)` | a oder b |
| `a?` | Null oder eins von a |
| `a*` | Null oder mehr von a |
| `a+` | Ein oder mehr von a |
| `a{3}` | Genau 3 von a |
| `a{3,}` | 3 oder mehr von a |
| `a{3,6}` | Zwischen 3 und 6 von a |

https://rubular.com/ ist eine gute Ressource, mit der Sie die Gültigkeit regulärer Ausdrücke testen können.

## Informationen zur Regelpriorität

If a key is matched to multiple rules, and it sets the same classification column shown in the [!UICONTROL Set Classification] column, the last rule is used. Daher sollten Sie möglicherweise den wichtigsten letzten Platz im Regelsatz einstufen.

<!-- 

rule_priority.xml

 -->

Wenn Sie mehrere Regeln erstellen, die nicht dieselbe Classification verwenden, spielt die Verarbeitungsreihenfolge keine Rolle.

Wie folgt ein Beispiel für eine Suchbegriffregel, die Suchtypen für einen Sportler klassifiziert:

| Regelnummer | Regeltyp | Übereinstimmung | Classification auswählen | Hierzu |
|---|---|---|---|---|
| 1 | Enthält | Cowboys | Suchtyp | Team |
| 2 | Enthält | Fantasie | Suchtyp | Fantasie |
| 3 | Enthält | Romo | Suchtyp | Player |

Wenn ein Benutzer nach  *`Cowboys fantasy Tony Romo`* sucht, ist der Begriff *`Player`* klassifiziert, weil dieser Begriff mit der letzten in der Spalte „Klassifizierung auswählen“ angegebenen Klassifizierung übereinstimmt.

Angenommen, Sie richten zwei Regeln in einem Satz für die folgenden Suchbegriffe ein:

| Regelnummer | Regeltyp | Übereinstimmung | Classification auswählen | Hierzu |
|---|---|---|---|---|
| 1 | Enthält | Cowboys | Stadt | Dallas |
| 2 | Enthält | Broncos | Stadt | Denver |

Ein Benutzer sucht nach  *`Cowboys vs. Broncos`*. Wenn der Regel-Builder einen Konflikt bei der Regelübereinstimmung feststellt, gilt für diese Suche die Classification für die zweite Regel (Denver).

## Hinzufügen einer Klassifizierungsregel zu einem Regelsatz {#add-classification-to-rule-set}

<!-- 

t_classification_rule.xml

 -->

In diesen Schritten wird beschrieben, wie Sie eine Classification-Regel hinzufügen oder bearbeiten.

Hinzufügen Regeln durch Zuordnen einer Bedingung zu einer Classification und Festlegen der Aktion.

>[!NOTE]
>
>Im Rahmen dieses Verfahrens müssen Sie die Regeln auf eine oder mehrere Report Suites anwenden. Es wird empfohlen, zwischen 500 und 1000 Regeln in einen Regelsatz aufzunehmen. Es gibt allerdings keine Begrenzungen. Wenn Sie mehr als 100 Regeln nutzen, vereinfachen Sie den Regelsatz ggf. mithilfe von  [Unter-Classifications](/help/components/c-classifications2/c-sub-classifications.md).

1. [Erstellen Sie einen Klassifizierungsregelsatz](/help/components/c-classifications2/crb/classification-rule-set.md).
1. On the rule set page, click **[!UICONTROL Add Rule]**.

   ![](assets/add_rule.png)

1. Next to **[!UICONTROL Report Suites]**, click **[!UICONTROL Add Suites]** to specify one or more report suites to assign to this rule set.

   Die **[!UICONTROL Select Report Suites]** Seite wird angezeigt.

   >[!NOTE]
   Report Suites werden *`only`* auf dieser Seite angezeigt, wenn die folgenden Bedingungen erfüllt sind:        >

   * Mindestens eine Classification ist für die Variable in [!UICONTROL Admin Tools] für die Report Suites definiert.
   (Eine Erläuterung zu dieser Voraussetzung finden Sie unter *`Variable`* in den [Klassifizierungsregelsätzen](/help/components/c-classifications2/crb/classification-rule-set.md).)

   * You selected the report suite on the **[!UICONTROL Available Report Suites]** page, which displays after you click [Add Rule Set](/help/components/c-classifications2/crb/classification-rule-set.md) to create the rule set.


1. Festlegen, ob vorhandene Werte überschrieben werden sollen:

   | **Regeln überschreiben alle vorhandenen Werte.** | (Standardeinstellung) Vorhandene Classification-Schlüssel werden immer überschrieben, einschließlich Classifications, die über den Importeur (SAINT) hochgeladen wurden. |
   |---|---|
   | **Regeln überschreiben nur nicht festgelegte Werte.** | Nur leere (nicht festgelegte) Zellen ausfüllen. Vorhandene Classifications werden nicht geändert. |

1. [Definieren Sie die Regel(n)](/help/components/c-classifications2/crb/classification-rule-definitions.md#section_4A5BF384EEEE4994B6DC888339833529).

   ![Schritt Ergebnis](assets/classification_rules_page.png)

   Beispiele zum Erstellen von Regeln finden Sie unter [Classifications Rule Builder](/help/components/c-classifications2/crb/classification-rule-builder.md) und [Reguläre Ausdrücke in Klassifizierungsregeln](/help/components/c-classifications2/crb/classification-quickstart-rules.md).

   >[!NOTE]
   >
   >Wenn ein Schlüssel mit mehreren Regeln übereinstimmt, die dieselbe Klassifizierung festlegen (in der Spalte „Klassifizierung auswählen“), wird die jeweils letzte mit der Klassifizierung übereinstimmende Regel verwendet. Weitere Informationen zum Sortieren der Regeln finden Sie unter **Informationen zur Regelpriorität**.

1. [Testen Sie den Regelsatz](/help/components/c-classifications2/crb/classification-quickstart-rules.md).
1. After testing, click **[!UICONTROL Active]** to validate and activate the rule.

   Beim Aktivieren einer Regel wird die Datei automatisch erstellt und hochgeladen.

   Felddefinitionen: Vollständige Definitionen der Optionen auf dieser Seite finden Sie unter [Classification Rule Builder](/help/components/c-classifications2/crb/classification-rule-definitions.md).

## Testen eines Klassifizierungsregelsatzes

<!-- 

t_classifications_test_rule.xml

 -->

Schritte, die beschreiben, wie Sie eine Classification-Regel oder einen Classification-Regelsatz testen. Beim Ausführen eines Tests werden alle Regeln in einem Satz überprüft.

1. [Erstellen Sie einen Klassifizierungsregelsatz](/help/components/c-classifications2/crb/classification-rule-set.md).
1. On the [!UICONTROL Classification Rule Builder], click the rule set name.
1. Stellen Sie sicher, dass der Regelsatz einer Report Suite zugeordnet ist.
1. On the rule editor, click **[!UICONTROL Test Rule Set]**.

   ![Schritt Ergebnis](assets/classification_test_rule_set.png)

1. Type or paste test keys in the [!UICONTROL Sample Keys] field.

   Beispielschlüssel umfassen:

   * Rückverfolgungscodes
   * Suchbegriffe oder -ausdrücke
   See [Regular Expressions in Classification Rules](/help/components/c-classifications2/crb/classification-quickstart-rules.md) for information about testing regular expressions.
1. Klicken Sie auf **[!UICONTROL Run Test]**.

   Rules that match are displayed in the [!UICONTROL Results] table.
1. (Optional) Click **[!UICONTROL Activate]** to activate the rule, and to overwrite existing classifications.

   Weitere Informationen zum Überschreiben vorhandener Klassifizierungen mithilfe von Regeln finden Sie hier.

## Validieren und Aktivieren von Klassifizierungsregeln

<!-- 

t_validate_rules.xml

 -->

In diesen Schritten wird beschrieben, wie Sie Classification-Regeln validieren und aktivieren.

1. [Erstellen Sie einen Klassifizierungsregelsatz](/help/components/c-classifications2/crb/classification-rule-set.md) und [fügen Sie dem Satz dann Klassifizierungsregeln](/help/components/c-classifications2/crb/classification-quickstart-rules.md) hinzu.
1. On the rule editor, click **[!UICONTROL Activate]**.

   ![](assets/overwrite_keys.png)

1. (Optional) Um Classifications zu überschreiben, aktivieren Sie **[!UICONTROL Overwrite classifications for]***`<selection>`*.

   Mit dieser Option können Sie vorhandene Classifications für die betroffenen Schlüssel überschreiben.

   Eine Definition dieser Option finden Sie auf der Seite &quot; [Regeln&quot;](/help/components/c-classifications2/crb/classification-rule-definitions.md#section_4A5BF384EEEE4994B6DC888339833529) .
