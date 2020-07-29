---
description: Beispiele, die den Import von Nummerisch 2 Klassifizierungen veranschaulichen.
subtopic: Classifications
title: Beispiele
topic: Admin tools
uuid: 0553d07f-87c1-4372-90ce-7118a6393a01
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 100%

---


# Beispiele

Beispiele, die den Import von Nummerisch-2-Classifications veranschaulichen.

<!-- 

c_example_1__rate.xml

 -->

In diesem Fall haben Sie die Classification im Manager für [!UICONTROL Konversion-Classifications] erstellt und möchten die Januar-Werte importieren:

| Schlüssel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product 1 | Text1 | `Cost1_jan_var` |  | `.2` |
| Product 2 | Text2 | `Cost2_jan_var` |  | `.3` |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 – 2010/01/31 | Umsatz | Umsatz |
| 2010/01/01 – 2010/01/31 | Umsatz | Umsatz |

Im Januar hatte Produkt 1 Kosten in Höhe von 20 % seines Umsatzes (zu sehen unter `~MyCost^~value~`), bei Produkt 2 lagen die Kosten bei 30 % des Umsatzes. Da Sie eine neue Zeile importieren, ist `~MyCost^~id~` leer.

## Ergebnis {#section_E0569289C9B34C479C7D2CD9ECBF866E}

Hier sehen Sie eine Beispielausgabe des Berichts:

Zeitraum: Jan. 2010

Bericht: Produkte

| Produkte | Umsatz | MyCost |
|---|---|---|
| Product 1 | 10.000,23 $ | 2000,05 $ |
| Product 2 | 9000,04 $ | 2700,01 $ |

<!-- 

c_example_2__rate.xml

 -->

| Schlüssel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product 1 | Text1 | `Cost1_jan_var` | 1 | .2 |
| Product 2 | Text2 | `Cost2_jan_var` | 2 | .3 |
| Product 1 | Text1 | `Cost1_feb_var` |  | .15 |
| Product 2 | Text2 | `Cost2_feb_var` |  | .25 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 – 2010/01/31 | Umsatz | Umsatz |
| 2010/01/01 – 2010/01/31 | Umsatz | Umsatz |
| 2010/02/01 – 2010/02/28 | Umsatz | Umsatz |
| 2010/02/01 – 2010/02/28 | Umsatz | Umsatz |

Im Februar sind die Kosten des Benutzers für Produkt 1 um 15 % des Umsatzes gefallen, bei Produkt 2 sanken die Kosten um 25 % des Umsatzes.

## Ergebnis {#section_23DF5353AC1B478C88647F222703352C}

Hier sehen Sie eine Beispielausgabe des Berichts:

Zeitraum: Jan. 2010

Bericht: Produkte

| Produkte | Umsatz | MyCost |
|---|---|---|
| Product 1 | 10.000,23 $ | 2000,05 $ |
| Product 2 | 9000,04 $ | 2700,01 $ |

Zeitraum: Feb 2010

Bericht: Produkte

| Produkte | Umsatz | MyCost |
|---|---|---|
| Product 1 | 15.500,75 $ | 2325,11 $ |
| Product 2 | 12.300,52 $ | 3075,13 $ |

Zeitraum: 1. Jan 2010 – 28. Feb 2010

Bericht: Produkte

| Produkte | Umsatz | MyCost |
|---|---|---|
| Product 1 | 25.500,98 $ | 4325,16 $ |
| Product 2 | 21.300,56 $ | 5775,14 $ |

<!-- 

c_example_3__fixed.xml

 -->

Daher würden Sie die folgenden Daten importieren:

| Schlüssel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product 1 | Text1 | `Cost1_mar_fixed` |  | 3000,00 |
| Product 2 | Text2 | `Cost2_jan_fixed` |  | 2000,00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 – 2010/03/31 | fest | Keine |
| 2010/03/01 – 2010/03/31 | fest | Keine |

## Ergebnis {#section_674B57ADB8284B878F9E670038C31464}

Hier sehen Sie eine Beispielausgabe des Berichts:

Zeitraum: März 2010

Bericht: Produkte

| Produkte | Umsatz | MyCost |
|---|---|---|
| Product 1 | 11.023,75 $ | 3000,00$ |
| Product 2 | 8000,12 $ | 2000.00 $ |

<!-- 

c_example_4__(advanced)_multiple_row_per_time_period.xml

 -->

In diesem Beispiel fügen Sie für den Januar Lieferkosten in Höhe von 500 USD zu Produkt1 hinzu, für den Februar in Höhe von 600 USD.

| Schlüssel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product 1 | Text1 | `Cost1_jan_var` | 1 | .2 |
| Product 1 | Text1 | `Cost2_jan_fixed` |  | 500 |
| Product 1 | Text1 | `Cost1_feb_var` | 2 | .15 |
| Product 1 | Text1 | `Cost2_feb_fixed` |  | 600 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 – 2010/01/31 | Umsatz | Umsatz |
| 2010/01/01 – 2010/01/31 | fest | Keine |
| 2010/02/01–2010/01/31 | Umsatz | Umsatz |
| 2010/02/01–2010/01/31 | fest | Keine |

Die zuvor importierten Zeilen weisen eine ID auf, die anzeigt, dass es keine neuen Kosten sind.

## Ergebnis {#section_2096084176614B9AA60F97D5853CB9EA}

Hier sehen Sie eine Beispielausgabe des Berichts:

Zeitraum: Jan. 2010

Bericht: Produkte

| Produkte | Umsatz | MyCost |
|---|---|---|
| Product 1 | 10.000,23 $ | 2500,05 $ |

>[!NOTE]
>
>Diese Funktion sollte nur von fortgeschrittenen Benutzern zur Ermittlung von Näherungswerten genutzt werden. Die Ergebnisinformationen sollten nicht als exakte Werte gesehen werden.

<!-- 

c_example_5__identical_rate_hinge.xml

 -->

Dieses Beispiel wird im Folgenden illustriert:

| Schlüssel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product 1 | Text1 | `Cost1_mar_var` |  | 1 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 – 2010/03/31 | order | order |

## Ergebnis {#section_39E24ECCC3B34C9AADC25572662750E5}

Hier sehen Sie eine Beispielausgabe des Berichts:

Zeitraum: März 2010

Bericht: Produkte nach Seite

| Produkte nach Seite | Bestellungen | MyCost |
|---|---|---|
| Product 1 | 1000 | 1000.00 $ |
| „Homepage“ | 600 | 600 $ |
| Warenkorb | 400 | 400$ |

<!-- 

c_example_5__fixed_no_hinge.xml

 -->

| Schlüssel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product 1 | Text1 | `Cost1_mar_fixed` |  | 3000,00 |
| Product 2 | Text2 | `Cost2_mar_fixed` |  | 2000,00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 – 2010/03/31 | fest | Keine |
| 2010/03/01 – 2010/03/31 | fest | Keine |

## Ergebnis {#section_7F5F5970077D4E14A5DC91495E23540D}

Hier sehen Sie eine Beispielausgabe des Berichts:

Zeitraum: März 2010

Bericht: Produkte nach Seite

| Produkte nach Seite | Bestellungen | MyCost |
|---|---|---|
| Product 1 | 1000 | 3000,00$ |
| „Homepage“ | 600 | 0 |
| Warenkorb | 400 | 0 |

<!-- 

c_example_7__fixed_hinge.xml

 -->

In diesem Fall würden Sie die folgenden Daten eingeben:

| Schlüssel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product 1 | Text1 | `Cost1_mar_fixed` |  | 3000,00 |
| Product 2 | Text2 | `Cost2_mar_fixed` |  | 2000,00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 – 2010/03/31 | fest | Umsatz |
| 2010/03/01 – 2010/03/31 | fest | Umsatz |

## Ergebnis {#section_5953BB6FD0CE4EF69D1D60B8B1203431}

Hier sehen Sie eine Beispielausgabe des Berichts:

Zeitraum: März 2010

Bericht: Produkte nach Seite

| Produkte nach Seite | Bestellungen | MyCost |
|---|---|---|
| Product 1 | 1000 | 3000,00$ |
| „Homepage“ | 600 | 1800,00$ |
| Warenkorb | 400 | 1200,00$ |

<!-- 

c_example_7_continued__different_rate_hinge.xml

 -->

In diesem Fall geben Sie die folgenden Daten ein:

| Schlüssel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product 1 | Text1 | Cost1_mar_fixed |  | 3 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 – 2010/03/31 | order | Umsatz |

## Ergebnis {#section_6E2604D9A3B0455585EFF0F80FF54127}

Hier sehen Sie eine Beispielausgabe des Berichts:

Zeitraum: März 2010

Bericht: Produkte nach Seite

| Produkte nach Seite | Bestellungen | MyCost |
|---|---|---|
| Product 1 | 1000 | 3000,00$ |
| „Homepage“ | 600 | 1.000,00$ |
| Warenkorb | 400 | 2.000,00$ |

