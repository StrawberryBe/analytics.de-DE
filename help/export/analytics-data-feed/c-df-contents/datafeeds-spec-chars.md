---
description: In diesem Abschnitt erhalten Sie Informationen zu Sonderzeichen, die im Datenfeed verwendet werden.
keywords: Datenfeed; job; Sonderzeichen; hit_ data; Variablen mit mehreren Werten; events_ list; products_ list; mvvars
seo-description: In diesem Abschnitt erhalten Sie Informationen zu Sonderzeichen, die im Datenfeed verwendet werden.
seo-title: Sonderzeichen
solution: Analytics
subtopic: Datenfeeds
title: Sonderzeichen
topic: Reports and Analytics
uuid: 5 efe 019 b -39 e 6-4226-a 936-88202 a 02 f 5 e 6
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Sonderzeichen

In diesem Abschnitt erhalten Sie Informationen zu Sonderzeichen, die im Datenfeed verwendet werden.

* [Sonderzeichen in der Datei „hit_data“](../../../export/analytics-data-feed/c-df-contents/datafeeds-spec-chars.md#section_9759C7A6AE684EB5B4A154FB6A26B39E)
* [Sonderzeichen in Variablen mit mehreren Werten (events_list, products_list, mvvars)](../../../export/analytics-data-feed/c-df-contents/datafeeds-spec-chars.md#section_056F8D540FFC4F24A001DC74331C2AAC)
* [Beispielarbeitsablauf](../../../export/analytics-data-feed/c-df-contents/datafeeds-spec-chars.md#section_97F8C2925A35433DA2E7E8BE60037E37)

## Sonderzeichen in der Datei „hit_data“ {#section_9759C7A6AE684EB5B4A154FB6A26B39E}

Die folgenden Zeichen haben in der Datei „hit_data“ eine besondere Bedeutung:

| Zeichen | Beschreibung | Beschreibung |
|--- |--- |--- |
| \t (Tabstoppzeichen) | Spaltenende | Markiert das Ende des Datenfelds. |
| \n (Zeilenumbruchzeichen) | Ende der Zeile | Markiert das Ende einer Datenzeile. |
| \  (umgekehrter Schrägstrich) | Escape-Zeichen | Kommentiert die Zeichen „Tabstopp“, „Zeilenumbruch“ und „umgekehrter Schrägstrich“ aus, wenn das Zeichen Teil des Werts war, der bei der Datenerfassung gesendet wurde. |

Wenn einem dieser Sonderzeichen ein umgekehrter Schrägstrich vorangestellt ist, repräsentiert es das tatsächliche (literale) Zeichen.

| Zeichen | Beschreibung | Beschreibung |
|--- |--- |--- |
| \\t | Tab | Tabstoppzeichen in Textform. Dieses Zeichen war Teil des Werts, der bei der Datenerfassung gesendet wurde. |
| \\n | Umbruch | Umbruch in Textform. Dieses Zeichen war Teil des Werts, der bei der Datenerfassung gesendet wurde. |
| \\ | Umgekehrter Schrägstrich | Umgekehrter Schrägstrich in Textform. Dieses Zeichen war Teil des Werts, der bei der Datenerfassung gesendet wurde. |

## Sonderzeichen in Variablen mit mehreren Werten (events_list, products_list, mvvars) {#section_056F8D540FFC4F24A001DC74331C2AAC}

Die folgenden Zeichen haben in Variablen mit mehreren Werten eine besondere Bedeutung:

<table id="table_FDA13DE05A784ED4972C2955BD2642C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Zeichen </th> 
   <th colname="col02" class="entry"> Beschreibung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <code> , </code> (Kommazeichen) </td> 
   <td colname="col02"> Ende des Werts </td> 
   <td colname="col2"> <p>Trennt Produktzeichenfolgen, Ereignis-IDs oder andere Werte in Variablen mit mehreren Werten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> ; </code> (Semikolon-Zeichen) </td> 
   <td colname="col02"> Ende des untergeordneten Werts in einem einzelnen Produktwert </td> 
   <td colname="col2"> <p>Trennt Werte, die mit einem einzelnen Produkt in der <code>product_list</code> verknüpft sind . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> = </code> (Gleichheitszeichen) </td> 
   <td colname="col02"> Wertzuweisung </td> 
   <td colname="col2"> <p>Weist einem Ereignis in <code>event_list</code> einen Wert zu . </p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn einem dieser Sonderzeichen ein Caret vorangestellt ist, repräsentiert es das tatsächliche (literale) Zeichen.

| Zeichen | Beschreibung | Beschreibung |
|--- |--- |--- |
| ^, | Komma | Komma in Textform. Dieses Zeichen war Teil des Werts, der bei der Datenerfassung gesendet wurde. |
| ^; | Semikolon | Semikolon in Textform. Dieses Zeichen war Teil des Werts, der bei der Datenerfassung gesendet wurde. |
| ^= | Gleichheitszeichen | Gleichheitszeichen in Textform. Dieses Zeichen war Teil des Werts, der bei der Datenerfassung gesendet wurde. |
| ^^ | Caret | Caret in Textform. Dieses Zeichen war Teil des Werts, der bei der Datenerfassung gesendet wurde. |

## Beispielarbeitsablauf {#section_97F8C2925A35433DA2E7E8BE60037E37}

Wenn einige Spalten in Ihrem Datenfeed vom Benutzer übermittelte Daten enthalten, sollte Sie eine Überprüfung auf Sonderzeichen ausführen, bevor Sie die Daten mithilfe von `split`, `readLine` usw. nach Spalten oder Zeilen aufteilen.

Betrachten wir die folgenden Daten:

| Browserbreite | Browserhöhe | eVar1 | prop1 |
|---|---|---|---|
| 1680 | 1050 | search\nstring | en |
| 800 | 600 | search\tstring | en |

Beim Export werden die Zeichen für Zeilenumbruch und Tabstopp in den eVar1-Werten mit Escape-Zeichen versehen. Der Datenfeed für diese Zeilen wird wie folgt angezeigt:

```
1680\t1050\tsearch\\nstring\ten\n 
800\t600\tsearch\\tstring\ten\n
```

Calling `readLine()` on the first row returns the following partial string:

```
800\t600\tsearch\
```

Calling `split("\t")` on the second row returns the following string array:

```
800 
600 
search\ 
string 
en
```

Um dies zu vermeiden, wird die Verwendung folgender Vorgehensweise empfohlen:

1. Beginnen Sie am Anfang der Datei und lesen Sie, bis Sie auf ein Tabstopp-, Umbruch-, Caret-Zeichen oder einen umgekehrten Schrägstrich treffen.
1. Führen Sie – je nach aufgetretenem Sonderzeichen – eine entsprechende Aktion aus:

   * Tabstopp – Fügen Sie die Zeichenfolge bis dahin in eine Datenspeicherzelle ein und setzen Sie den Vorgang fort.
   * Umbruch – Schließen Sie die Datenspeicherzeile ab.
   * Umgekehrter Schrägstrich – Lesen Sie das nächste Zeichen, fügen Sie die entsprechende Zeichenfolge in Textform ein und setzen Sie den Vorgang fort.
   * Caret – Lesen Sie das nächste Zeichen, fügen Sie die entsprechende Zeichenfolge in Textform ein und setzen Sie den Vorgang fort.

