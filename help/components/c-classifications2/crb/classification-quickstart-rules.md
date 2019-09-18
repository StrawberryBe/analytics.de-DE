---
description: Classification-Regeln suchen nach nicht klassifizierten Begriffen. Wird eine Regelübereinstimmung gefunden, so fügen die Regeln die Begriffe automatisch den Classification-Datentabellen hinzu. Mit Classification-Regeln können Sie außerdem vorhandene Schlüssel überschreiben.
seo-description: Classification-Regeln suchen nach nicht klassifizierten Begriffen. Wird eine Regelübereinstimmung gefunden, so fügen die Regeln die Begriffe automatisch den Classification-Datentabellen hinzu. Mit Classification-Regeln können Sie außerdem vorhandene Schlüssel überschreiben.
seo-title: Klassifizierungsregeln
solution: Analytics
subtopic: Classifications
title: Klassifizierungsregeln
topic: Admin Tools
uuid: 08685919-216d-448b-b886-3adf5ff5405e
translation-type: tm+mt
source-git-commit: 646d6e01d0f0201c78117ee9bf9ff64fda9a026a

---


# Klassifizierungsregeln

Classification-Regeln suchen nach nicht klassifizierten Begriffen. Wird eine Regelübereinstimmung gefunden, so fügen die Regeln die Begriffe automatisch den Classification-Datentabellen hinzu. Mit Classification-Regeln können Sie außerdem vorhandene Schlüssel überschreiben.

## Klassifizierungsregeln {#concept_CF2F64BD96454FBFAA84638FC7DEA263}

Classification-Regeln suchen nach nicht klassifizierten Begriffen. Wird eine Regelübereinstimmung gefunden, so fügen die Regeln die Begriffe automatisch den Classification-Datentabellen hinzu. Mit Classification-Regeln können Sie außerdem vorhandene Schlüssel überschreiben.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Rule Builder]**

Mit dem Regel-Builder können Sie eine Liste *`classification rule set`* erstellen, die eine Liste von *`classification rules`*. Eine Regel überprüft, ob eine Übereinstimmung mit den angegebenen Kriterien vorliegt, und führt dann eine Aktion durch.

Classification-Regeln eignen sich für Folgendes:

* **E-Mail-** und **Display-Anzeigen:** Erstellen Sie Classification-Regeln, die die einzelnen Display-Anzeigekampagnen gruppieren, so dass ersichtlich wird, wie die Display-Kampagnen im Vergleich zu den E-Mail-Kampagnen abschneiden.

* **Trackingcodes:** Erstellen Sie Classification-Regeln, die die aus den Zeichenfolgen in den Trackingcodes abgeleiteten Schlüsselwerte kategorisieren und dann prüfen, ob diese Schlüsselwerte mit den angegebenen Kriterien übereinstimmen.
* **Suchbegriffe:** Mithilfe von [regulären Ausdrücken](../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_8A63F9BCF9484963962E14E6286D312D) und Platzhaltern vereinfachen Sie die Classification der Suchbegriffe. Wenn ein Suchbegriff beispielsweise enthält *`baseball`*, können Sie eine *`Sports League`* Klassifizierung auf *`MLB`*.

Der Trackingcode für eine E-Mail-Kampagnen-ID lautet beispielsweise:

`em:Summer:2013:Sale`.

Sie können drei Regeln in einem Regelsatz festlegen, die die Teile der Zeichenfolge ermitteln, und dann die Werte klassifizieren:

| Regeltyp auswählen | Übereinstimmungskriterien eingeben | Classification auswählen | Hierzu |
|---|---|---|---|
| Beginnt mit | em: | Kanal | E-Mail |
| Endet in | Ausverkauf | Typ | Ausverkauf |
| „Enthält“ | 2013 | Jahr | 2013 |

## Verarbeitung der Regeln {#concept_A67A23F523844D37898583C632DB9D25}

Wichtige Informationen zu den Verfahren, wie Classification-Regeln verarbeitet werden.

<!-- 

about_classification_rules.xml

 -->

* [Wichtige Informationen zu Regeln](/help/components/c-classifications2/crb/classification-rule-builder.md)
* [In welchen Fällen werden Schlüssel nicht durch Regeln klassifiziert?](/help/components/c-classifications2/crb/classification-rule-builder.md)
* [Informationen zur Regelpriorität](../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_93527FEB3C9B48FB96FB7DF857E5F980)

>[!NOTE]
>
>The [!UICONTROL Rule Builder] does not support Numeric 2 classifications.

## Wichtige Informationen zu Regeln {#section_0BD46702FBEC4D98A4DD2EA0BD428046}

* Specify [group permissions](https://marketing.adobe.com/resources/help/en_US/reference/?f=groups) for classifications in [!UICONTROL Admin Tools].

* **Reguläre Ausdrücke**: Hilfe finden Sie unter [Reguläre Ausdrücke in Classification-Regeln](../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_8A63F9BCF9484963962E14E6286D312D).

* **Report Suites:** Sie können erst dann eine Classification auswählen, wenn Sie mindestens eine Report Suite ausgewählt haben. Die Report Suite kann erst dann angewendet werden, wenn Sie den Regelsatz erstellt und eine Variable zugewiesen haben.

   Beim Testen des Regelsatzes verwenden Sie Schlüssel (die zu klassifizierende Variable) aus dem Bericht, um zu prüfen, wie sich der Regelsatz auf diese Schlüssel auswirkt. (Der [Schlüssel](../../../components/c-classifications2/c-classifications-importer/c-saint-data-files.md#concept_0B77B3079B5C414F9956058688990443) ist die zu klassifizierende Variable oder die erste Spalte in der Classification-Upload-Tabelle.)

* **Regelpriorität:** Wenn ein Schlüssel mit mehreren Regeln übereinstimmt, die dieselbe Classification festlegen (in der Spalte [!UICONTROL Classification auswählen]), wird die jeweils letzte mit der Classification übereinstimmende Regel verwendet. Siehe [Informationen zur Regelpriorität](../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_93527FEB3C9B48FB96FB7DF857E5F980).

* **Beschränkungen hinsichtlich der Regelanzahl:** Für die Anzahl der erstellbaren Regeln gelten keine Einschränkungen. Eine große Regelanzahl kann jedoch die Browserleistung beeinträchtigen.
* **Verarbeitung**: Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.

   Aktive Regeln werden alle vier Stunden verarbeitet, wobei die zu untersuchenden Classification-Daten in der Regel einen Monat zurückgehen. Die Regeln suchen automatisch nach neuen Werten und laden die Classification mit dem Importeur hoch.

* **Überschreiben von vorhandenen Classifications:** Siehe [In welchen Fällen werden Schlüssel nicht durch Regeln klassifiziert?](../../../components/c-classifications2/crb/classification-quickstart-rules.md#section_4481E88CA28246B6B19EA16E2D83A3A8) Bei Bedarf können Sie vorhandene Klassifizierungen mit dem Importeur löschen oder entfernen.

## In welchen Fällen werden Schlüssel nicht durch Regeln klassifiziert? {#section_4481E88CA28246B6B19EA16E2D83A3A8}

Beim Aktivieren von Regeln können Sie vorhandene Classifications überschreiben. In den folgenden Situationen wird ein [Schlüssel](../../../components/c-classifications2/c-classifications-importer/c-saint-data-files.md#concept_0B77B3079B5C414F9956058688990443) (eine Variable) nicht durch eine Classification-Regel klassifiziert, wenn Folgendes gilt:

* Der Schlüssel wurde bereits klassifiziert, und Sie haben nicht die Option [Überschreiben von Classifications für](../../../components/c-classifications2/crb/classification-rule-definitions.md#overwrite_classifications) ausgewählt.

   Sie können Classifications überschreiben, wenn Sie [](../../../components/c-classifications2/crb/classification-quickstart-rules.md#task_86F216DFD2534FA181E64ABDF306782B) eine Regel hinzufügen und aktivieren, und wenn Sie eine Data Connectors-Integration aktivieren. (Regeln für Data Connectors werden von Partnern im Entwicklungszentrum erstellt und im [!UICONTROL Classification Rule Builder] angezeigt.)

* Ein klassifizierter Schlüssel wird beim Überschreiben nach Ablauf eines bestimmten Zeitrahmens auch dann nicht in den Daten sichtbar, wenn Sie die Option [Überschreiben von Classifications für](../../../components/c-classifications2/crb/classification-rule-definitions.md#overwrite_classifications) aktiviert haben.
* Der Schlüssel wird nicht klassifiziert, und nach Beginn des Zeitrahmens (vor etwa einem Monat) wurde der Schlüssel auch nicht in [!DNL Adobe Analytics] übergeben.

   >[!NOTE]
   >
   >In Berichten gelten Classifications für jeden angegebenen Zeitraum, sobald ein Schlüssel vorhanden ist. Der Datumsbereich eines Berichts wirkt sich nicht auf die Berichterstellung aus.

![](assets/overwrite_keys.png)

## Reguläre Ausdrücke in Classification-Regeln {#concept_8A63F9BCF9484963962E14E6286D312D}

Mithilfe von regulären Ausdrücken gleichen Sie konsistent formatierte Zeichenfolgenwerte mit einer Classification ab. So können Sie beispielsweise eine Classification anhand bestimmter Zeichen in einem Trackingcode erstellen. Sie können bestimmte Zeichen, Wörter oder Zeichenmuster abgleichen.

<!-- 

regex_classification_rules.xml

 -->

* [Regulärer Ausdruck – Beispiel für Trackingcode](../../../components/c-classifications2/crb/classification-quickstart-rules.md#section_2EF7951398EB4C2F8E52CEFAB4032669)
* [Regulärer Ausdruck – Klassifizieren eines bestimmten Zeichens](../../../components/c-classifications2/crb/classification-quickstart-rules.md#section_5D300C03FA484BADACBFCA983E738ACF)
* [Reguläre Ausdrücke – Abgleichen von Trackingcodes unterschiedlicher Länge](../../../components/c-classifications2/crb/classification-quickstart-rules.md#section_E86F5BF5C2F44ABC8FFCE3EA67EE3BB2)
* [Reguläre Ausdrücke – Beispiel für „enthält nicht“](../../../components/c-classifications2/crb/classification-quickstart-rules.md#section_FCA88A612A4E4B099458E3EF7B60B59C)
* [Reguläre Ausdrücke – Referenztabelle](../../../components/c-classifications2/crb/classification-quickstart-rules.md#section_0211DCB1760042099CCD3ED7A665D716)

>[!NOTE]
>
>Reguläre Ausdrücke eignen sich am besten für Rückverfolgungscodes, die Trennzeichen verwenden.

## Regulärer Ausdruck – Beispiel für Trackingcode {#section_2EF7951398EB4C2F8E52CEFAB4032669}

>[!NOTE]
>
>If the tracking code is URL encoded, it will **not** be classified by the Rules Builder.

In diesem Beispiel wird angenommen, dass die folgende Kampagnen-ID klassifiziert werden soll:

[!UICONTROL Sample Key]: `em:JuneSale:20130601`

Die folgenden Teile des Trackingcodes sind zu klassifizieren:

* `em` = email
* `JuneSale` = Kampagnenname
* `20130601` = date

[!UICONTROL Regular Expression]: `^(.+)\:(.+)\:(.+)$`

Zusammenhang zwischen dem regulären Ausdruck und der Kampagnen-ID:

![](assets/regex.png)

[!UICONTROL Übereinstimmungsgruppen:] Zeigt, wie der reguläre Ausdruck den Zeichen der Kampagnen-ID entspricht, so dass Sie eine Position in der Kampagnen-ID klassifizieren können.

![](assets/regex_tracking_code.png)

This example tells the rule that the campaign date `20140601` is at the third group `(.+)`, identified by `$3`.

**[!UICONTROL Regel-Builder]**

Konfigurieren Sie die Regel im [!UICONTROL Regel-Builder] wie folgt:

| Regeltyp auswählen | Übereinstimmungskriterien eingeben | Classification auswählen | Hierzu |
|---|---|---|---|
| Regulärer Ausdruck | &amp;Hat;(.+)\:(.+)\:(.+)$ | Kampagnendatum | $3 |

**Syntax**

| Regulärer Ausdruck | Zeichenfolge oder Übereinstimmungsergebnis | Zugehörige Übereinstimmungsgruppen |
|--- |--- |--- |
| `^(.+)\:(.+)\:(.+)$` | em:JuneSale:20130601 | `$0`: em:JuniAusverkauf:20130601 `$1`: em `$2`: JuniAusverkauf `$3`: 20130601 |
| Aufbauen der Syntax | `^` = beginnt die Zeile () = Gruppen-Zeichen und ermöglicht das Extrahieren übereinstimmender Zeichen in den Klammern.  `(.+)` = erfasst ein ( . ) und ( + ) beliebiger \ = Beginn einer Zeichenfolge.  `$` = gibt an, dass das vorhergehende Zeichen (oder die vorhergehende Zeichengruppe) das letzte Element in der Zeile ist. |

Weitere Informationen zur Bedeutung der Zeichen in einem regulären Ausdruck finden Sie unter [Reguläre Ausdrücke – Referenztabelle](../../../components/c-classifications2/crb/classification-quickstart-rules.md#section_0211DCB1760042099CCD3ED7A665D716).

## Regulärer Ausdruck – Klassifizieren eines bestimmten Zeichens {#section_5D300C03FA484BADACBFCA983E738ACF}

Mit einem regulären Ausdruck können Sie beispielsweise ein bestimmes Zeichen in einer Zeichenfolge klassifizieren. Angenommen, der folgende Trackingcode enthält zwei wichtige Zeichen:

[!UICONTROL Sample Key]: `4s3234`

* `4` = Markenname
* `s` = Suchmaschine, z. B. Google

![](assets/regex_char_position.png)

**[!UICONTROL Regel-Builder]**

Konfigurieren Sie die Regel im [!UICONTROL Regel-Builder] wie folgt:

| Regeltyp auswählen | Übereinstimmungskriterien eingeben | Classification auswählen | Hierzu |
|--- |--- |--- |--- |
| Regulärer Ausdruck | `^.(s).*$` | Marke und Suchmaschine | `$0` (Erfasst die ersten beiden Zeichen für den Markennamen und die Suchmaschine.) |
| Regulärer Ausdruck | `^.(s).*$` | Suchmaschine | `$1` (Erfasst das zweite Zeichen für Google.) |

## Reguläre Ausdrücke – Abgleichen von Trackingcodes unterschiedlicher Länge {#section_E86F5BF5C2F44ABC8FFCE3EA67EE3BB2}

Dieses Beispiel zeigt, wie Sie bestimmte Zeichen zwischen Doppelpunkten als Trennzeichen erkennen, wenn Sie Trackingcodes mit unterschiedlicher Länge nutzen. Adobe empfiehlt die Verwendung von je einem regulären Ausdruck pro Trackingcode.

Beispielschlüssel:

* `a:b`
* `a:b:c`
* `a:b:c:d`

**Syntax**

![](assets/regex_b.png)

![](assets/regex_varying_length.png)

**[!UICONTROL Regel-Builder]**

Konfigurieren Sie die Regel im [!UICONTROL Regel-Builder] wie folgt:

| Regeltyp auswählen | Übereinstimmungskriterien eingeben | Classification auswählen | Hierzu |
|--- |--- |--- |--- |
| Regulärer Ausdruck für Übereinstimmungszeichenfolge a:b | `^([^\:]+)\:([^\:]+)$` | a | `$1` |
| Regulärer Ausdruck für Übereinstimmungszeichenfolge a:b | `^([^\:]+)\:([^\:]+)$` | b | `$2` |
| Regulärer Ausdruck für Übereinstimmungszeichenfolge a:b:c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | a | `$1` |
| Regulärer Ausdruck für Übereinstimmungszeichenfolge a:b:c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | b | `$2` |
| Regulärer Ausdruck für Übereinstimmungszeichenfolge a:b:c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | c | `$3` |
| Regulärer Ausdruck für Übereinstimmungszeichenfolge a:b:c:d | `^([^\:]+)\:([^\:]+)\:([^\:]+)\:([^\:])$` | d | `$4` |

## Reguläre Ausdrücke – Beispiel für „enthält nicht“{#section_FCA88A612A4E4B099458E3EF7B60B59C}

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

In this result, `a:b:1313` does not indicate a match.

## Reguläre Ausdrücke – Referenztabelle {#section_0211DCB1760042099CCD3ED7A665D716}

| Ausdruck  | Beschreibung |
|---|---|
| `(?ms)` | Der gesamte reguläre Ausdruck wird mit einer mehrzeiligen Eingabe abgeglichen, sodass das . -Platzhalterzeichen mit allen Zeilenumbruchzeichen abgeglichen wird |
| (`?i`) | Bei regulären Ausdrücken muss nun nicht mehr auf Groß- und Kleinschreibung geachtet werden |
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

Eine gute Ressource zum Testen der Gültigkeit regulärer Ausdrücke ist https://rubular.com/.

## Informationen zur Regelpriorität {#concept_93527FEB3C9B48FB96FB7DF857E5F980}

Wenn ein Schlüssel mit mehreren Regeln übereinstimmt, die dieselbe Classification-Spalte festlegen (wie in der Spalte [!UICONTROL „Classification auswählen“] angegeben), wird die jeweils letzte Regel verwendet. Weisen Sie daher der wichtigsten Regel die letzte Stelle im Regelsatz zu.

<!-- 

rule_priority.xml

 -->

Wenn Sie mehrere Regeln erstellen, die nicht dieselbe Classification nutzen, ist die Verarbeitungsreihenfolge nicht von Bedeutung.

Im folgenden Beispiel für eine Suchbegriffregel werden Suchtypen für Sportler klassifiziert:

| Regelnummer | Regeltyp | Übereinstimmung | Classification auswählen | Hierzu |
|---|---|---|---|---|
| 1 | „Enthält“ | Cowboys | Suchtyp | Team |
| 2 | „Enthält“ | Fantasy | Suchtyp | Fantasy |
| 3 | „Enthält“ | Romo | Suchtyp | Spieler |

Wenn ein Benutzer nach *`Cowboys fantasy Tony Romo`*, the term *`Player`* is classified, because it matches the last given classification shown in the Set Classification column.

Ein weiteres Beispiel. Angenommen, Sie legen zwei Regeln in einem Regelsatz für die folgenden Suchbegriffe fest:

| Regelnummer | Regeltyp | Übereinstimmung | Classification auswählen | Hierzu |
|---|---|---|---|---|
| 1 | „Enthält“ | Cowboys | Stadt | Dallas |
| 2 | „Enthält“ | Broncos | Stadt | Denver |

Ein Benutzer sucht nach *`Cowboys vs. Broncos`*. Wenn der Regel-Builder einen Konflikt bei der Regelübereinstimmung feststellt, gilt für diese Suche die Classification für die zweite Regel (Denver).

## Add a Classification Rule to a Rule Set {#task_86F216DFD2534FA181E64ABDF306782B}

<!-- 

t_classification_rule.xml

 -->

In diesen Schritten wird beschrieben, wie Sie Classification-Regeln hinzufügen oder bearbeiten.

Zum Hinzufügen einer Regel ordnen Sie eine Bedingung einer Classification zu, und legen Sie die gewünschte Aktion fest.

>[!NOTE]
>
>Bei diesem Verfahren müssen Sie die Regeln auf eine oder mehrere Report Suites anwenden. Es wird empfohlen, zwischen 500 und 1000 Regeln in einen Regelsatz aufzunehmen. Es gibt allerdings keine Begrenzungen. Wenn Sie mehr als 100 Regeln nutzen, vereinfachen Sie den Regelsatz ggf. mithilfe von [Unter-Classifications](../../../components/c-classifications2/c-sub-classifications.md#concept_19EE5513A7DC43C38CC396E96F306CFE).

1. [Erstellen Sie einen Classification-Regelsatz](../../../components/c-classifications2/crb/classification-rule-set.md#task_86F216DFD2534FA181E64ABDF306782B) .
1. On the rule set page, click **[!UICONTROL Add Rule]**.

   ![](assets/add_rule.png)

1. Next to **[!UICONTROL Report Suites]**, click **[!UICONTROL Add Suites]** to specify one or more report suites to assign to this rule set.

   Die Seite **[!UICONTROL Report Suites auswählen]wird angezeigt.**

   >[!NOTE]
   Report Suites werden auf dieser Seite angezeigt, *`only`* wenn die folgenden Bedingungen erfüllt sind:        &gt;

   * Mindestens eine Classification ist für die Variable in [!UICONTROL Admin Tools] für die Report Suites definiert.
   (Eine Erläuterung zu dieser Voraussetzung finden Sie *`Variable`* in den [Classification-Regelsätzen](../../../components/c-classifications2/crb/classification-rule-set.md#concept_CD3D510F5070486584F3BB535AE41524) .)

   * Sie haben die Report Suite auf der Seite **[!UICONTROL Verfügbare Report Suites]** ausgewählt, die angezeigt wird, wenn Sie auf Regelsatz [hinzufügen klicken, um den Regelsatz zu erstellen](/help/components/c-classifications2/crb/classification-rule-set.md) .


1. Festlegen, ob vorhandene Werte überschrieben werden sollen:

   | **Regeln überschreiben alle vorhandenen Werte.** | (Standardeinstellung) Vorhandene Classification-Schlüssel werden immer überschrieben, einschließlich Classifications, die über das Importtool (SAINT) hochgeladen wurden. |
   |---|---|
   | **Regeln überschreiben nur nicht festgelegte Werte.** | Es werden nur leere (nicht festgelegte) Zellen ausgefüllt. Vorhandene Classifications werden nicht geändert. |

1. [Definieren Sie die Regel(n)](../../../components/c-classifications2/crb/classification-rule-definitions.md#section_4A5BF384EEEE4994B6DC888339833529). 

   ![Schritt Ergebnis](assets/classification_rules_page.png)

   Beispiele zum Erstellen von Regeln finden Sie unter Classifications Rule Builder[ und ](/help/components/c-classifications2/crb/classification-rule-builder.md)Reguläre Ausdrücke in Classification-Regeln[](../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_8A63F9BCF9484963962E14E6286D312D).

   >[!NOTE]
   >
   >Wenn ein Schlüssel mit mehreren Regeln übereinstimmt, die dieselbe Classification festlegen (in der Spalte Classification festlegen), wird die letzte Regel verwendet, die mit der Classification übereinstimmt. See **About Rule Priority** above for more information about sorting rules.

1. [Testen Sie den Regelsatz](../../../components/c-classifications2/crb/classification-quickstart-rules.md#task_618A1E7CC8664E728F312250E8367158).
1. After testing, click **[!UICONTROL Active]** to validate and activate the rule.

   Beim Aktivieren einer Regel wird die Datei automatisch erstellt und hochgeladen.

   Field definitions: See [Classification Rule Builder](../../../components/c-classifications2/crb/classification-rule-definitions.md#concept_6CAEFB1CA4564E2CA5808097C11EF468) for complete definitions of interface options on this page.

## Test a Classification Rule Set {#task_618A1E7CC8664E728F312250E8367158}

<!-- 

t_classifications_test_rule.xml

 -->

In diesen Schritten wird beschrieben, wie Sie eine Classification-Regel oder einen Classification-Regelsatz testen. Im Rahmen des Tests werden alle Regeln innerhalb eines Satzes übeprüft.

1. [Erstellen Sie einen Classification-Regelsatz](../../../components/c-classifications2/crb/classification-rule-set.md#task_86F216DFD2534FA181E64ABDF306782B) .
1. Klicken Sie im [!UICONTROL Classification Rule Builder] auf den Namen des Regelsatzes.
1. Stellen Sie sicher, dass der Regelsatz einer Report Suite zugeordnet ist.
1. On the rule editor, click **[!UICONTROL Test Rule Set]**.

   ![Schritt Ergebnis](assets/classification_test_rule_set.png)

1. Geben oder fügen Sie Testschlüssel in das Feld [!UICONTROL Beispielschlüssel] ein.

   Beispielschlüssel umfassen Folgendes:

   * Trackingcodes
   * Keywords oder Suchausdrücke
   Siehe [Reguläre Ausdrücke in Classification-Regeln](../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_8A63F9BCF9484963962E14E6286D312D), um Informationen zum Testen von regulären Ausdrücken zu erhalten.
1. Click **[!UICONTROL Run Test]**.

   Passende Regeln werden in der [!UICONTROL Ergebnistabelle] angezeigt.
1. (Optional) Click **[!UICONTROL Activate]** to activate the rule, and to overwrite existing classifications.

   Weitere Informationen zum Überschreiben vorhandener Classifications mithilfe von Regeln finden Sie unter .

## Validate and Activate Classification Rules {#task_2B4FA41F1EE64F4AAC6170C5EFC066AC}

<!-- 

t_validate_rules.xml

 -->

In diesen Schritten wird beschrieben, wie Sie Classification-Regeln validieren und aktivieren.

1. [Erstellen Sie einen Classification-Regelsatz](../../../components/c-classifications2/crb/classification-rule-set.md#task_86F216DFD2534FA181E64ABDF306782B) und [fügen Sie dem Satz dann Classification-Regeln](../../../components/c-classifications2/crb/classification-quickstart-rules.md#task_86F216DFD2534FA181E64ABDF306782B) hinzu.
1. On the rule editor, click **[!UICONTROL Activate]**.

   ![](assets/overwrite_keys.png)

1. (Optional) To overwrite classifications, enable **[!UICONTROL Overwrite classifications for]** *`<selection>`*.

   Mit dieser Option können Sie bestehende Classifications für die betroffenen Schlüssel überschreiben.

   Eine Definition dieser Option finden Sie auf der [Seite „Regeln“](../../../components/c-classifications2/crb/classification-rule-definitions.md#section_4A5BF384EEEE4994B6DC888339833529).
