---
description: Mit Filtern können Sie den Bericht eingrenzen und Einzelelemente, die mit einem Filter übereinstimmen, ein- oder ausschließen.
title: Filtern von Berichtsdaten
topic: Reports and analytics
uuid: b6dcaaf7-61f0-4793-870d-e1d156575d5a
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Berichtsdaten filtern {#concept_09DC5B986A644738B12204DAC76A90E1}

Mit Filtern können Sie den Bericht eingrenzen und Einzelelemente, die mit einem Filter übereinstimmen, ein- oder ausschließen.

## Einfacher Filter  {#section_5C4DE873F8D5484BB77F38A4AEB57B4A}

![](assets/filter.png)

Der einfache Filter wird in den meisten Berichten angezeigt, damit Sie spezielle Einzelelemente einfach finden können. Bei einfachen Filtern werden keine Sonderzeichen verwendet, sodass `-, ", ', +` und andere Sonderzeichen dem literalen Wert im Bericht entsprechen. Sie können Zeilenelemente, die mehrere Begriffe enthalten, mit einem Leerzeichen suchen.

Beispiel:

```
help search
```

Gibt die folgenden Seiten zurück:

```
help:Search
help:Paid Search Detection
help:Configure paid search detection
help:Search Keywords Report
help:Internal Search Term
```

## Erweiterte Filter {#section_E016626C084640E8A066B2FDA5B932BF}

Mit erweiterten Filtern können Sie den Umfang Ihrer Suche mithilfe einer Sammlung von Filtern steuern. Sie können festlegen, dass alle Filter oder Filter übereinstimmen.

![](assets/advanced_filter.png)

**Enthält**

Sucht nach Begriffen, die an einer beliebigen Stelle im Zeileneintrag gefunden werden. Dies funktioniert genauso wie der einfache Filter.

>[!NOTE] Leerzeichen können nicht in Filtern verwendet werden, da sie als Trennzeichen bei Suchvorgängen verwendet werden.

**Enthält nicht**

Sucht, wenn der Begriff an keiner Stelle im Zeileneintrag gefunden wird. Mit „Enthält nicht“ können Sie „Nicht angegeben“, „Keine“, „Keyword nicht verfügbar“ und andere [spezielle Werte](https://marketing.adobe.com/resources/help/de_DE/reference/none-unspecified-unknown-other.html) aus Berichten filtern.

Enthält nicht: `none`

Für einen genaueren Filter können Sie den Filter &quot;Erweitert (Sonderzeichen)&quot;verwenden:

* Erweitert (Sonderzeichen): `-^none$`
* Erweitert (Sonderzeichen): `-"keyword unavailable"`

Beispielsweise wird der folgende Zeileneintrag nach dem Kriterium &quot;Enthält nicht&quot;gefiltert, jedoch nicht nach dem Kriterium &quot;Erweitert (Sonderzeichen)&quot;:

```
help:Rename the None classification key
```

**Enthält eins von**

Sucht nach Begriffen, die durch Leerzeichen voneinander getrennt sind, im Zeileneintrag. Der folgende Filter zeigt alle Seiten an, die &quot;Männer&quot;oder &quot;Verkauf&quot;enthalten:

Enthält eins von: `mens sale`

Gibt die folgenden Seiten zurück:

```
Womens
Mens
Mens:Desk & TravelJewelry & Accessories:Accessories:Hats:Mens
Sale & Values
```

**Gleich**

Sucht nach Übereinstimmung des gesamten Zeileneintrags, einschließlich Leerzeichen und anderer Zeichen, mit der angegebenen Wortgruppe.

Gleich: `mens:desk & travel`

`Mens:Desk & Travel`

**Beginnt mit**

Sucht nach Beginn mit der angegebenen Wortgruppe, wenn das Zeilenelement einschließlich Leerzeichen und anderer Zeichen übereinstimmt.

Beginnt mit: `mens`

Gibt die folgenden Seiten zurück:

```
Mens
Mens:Desk & Travel
Mens:Apparel
Mens Perfume Spray
Mens Hemp/Bamboo Flip Flops
```

**Endet in**

Gibt ein Ergebnis zurück, wenn das Zeilenelement, einschließlich Leerzeichen und anderer Zeichen, mit der angegebenen Wortgruppe endet.

Endet in: `jean`

Gibt die folgenden Seiten zurück:

```
Bell Bottom Jean
Velvet Dream Skinny Leg Jean
Dark Slimmer Jean
Bling Belt High Waist Jean
Ocean Blue Jean
```

## Erweitert (Sonderzeichen) {#section_83DA3B6C23EB4C119DB6D74062DB501D}

Mit &quot;Erweitert&quot;können Sie Platzhalter und andere komplexe Suchen durchführen.

| Erweitert (Sonderzeichen) | Beschreibung |
|--- |--- |
| `" "` | Übereinstimmung mit genauem Wortlaut. |
| `*` | Platzhalter, Greedy-Abgleich. <br>Beispielsweise entspricht `r*p` „Registration Signup“. |
| `^` | Beginnt mit. <br>Verwenden Sie kein Leerzeichen zwischen dem Sonderzeichen und dem Suchausdruck. |
| `$` | Endet mit. <br>Verwenden Sie kein Leerzeichen zwischen dem Sonderzeichen und dem Suchausdruck. |
| `-` | Nicht. <br>Verwenden Sie kein Leerzeichen zwischen dem Sonderzeichen und dem Suchausdruck. |
| `|` | Oder<br>Hinweis: Sie müssen ein Leerzeichen auf jeder Seite des Senkrechtstriches (`" | "`) einfügen. |

## Berichtsspezifische Filter erstellen {#task_DEBB0632411D4CA8AA0B3BA267A5B35F}

Schritte, die beschreiben, wie Filter für Berichte erstellt werden.

<!-- 

t_reports_filter_specific.xml

 -->

Bestimmte Berichte enthalten einen Filter, der für diesen Bericht spezifisch ist. Beispielsweise [!UICONTROL Purchase Conversion Funnel Report] können Sie mit einer nach Webseiten filtern. Mit einer [!UICONTROL Geosegmentation Report] können Sie nach geografischer Region filtern. Zusätzliche Berichte haben andere Filter, die spezifisch für diese Berichte sind.

Wenn Sie auf diese Filter zugreifen, werden Berichtsmetriken zu den in der Liste angegebenen Elementen angezeigt.

**So erstellen Sie berichtsspezifische Filter**

1. Erstellen Sie einen Bericht, z. B. [!UICONTROL Purchase Report] ( **[!UICONTROL Site Metrics]** > **[!UICONTROL Purchases]** > **[!UICONTROL Purchase Conversion Funnel]**).
1. Klicken Sie im Berichtkopf auf den Link **[!UICONTROL Filter]**.
1. Klicken Sie auf der [!UICONTROL Filter Selector] Seite auf **[!UICONTROL Apply a Filter]** und wählen Sie dann einen Filtertyp aus.
1. To search for an item, type a character string in the **[!UICONTROL Search]** field.
1. Klicken Sie auf **[!UICONTROL OK]**.

## Korrelationsfilter hinzufügen {#task_065042E384DA4BF3864C58AF2B88D6E2}

In diesen Schritten wird beschrieben, wie Sie einen Korrelationsfilter hinzufügen.

<!-- 

t_reports_correlation_filter.xml

 -->

Bestimmte Berichte ermöglichen Ihnen das Hinzufügen benutzerdefinierter Korrelationsvariablen-Filter. Wenn Sie beispielsweise die [!UICONTROL Pages Report] für eine Report Suite anzeigen, für die Sitebereiche mit einer Frauenseite korreliert sind, können Sie eine Filterregel erstellen, die einen Bericht generiert, der die bevorzugten Seiten zeigt, wenn Site-Abschnitte = Frauen.

Sie können die in einem Korrelationsbericht angezeigten Daten mit einer beliebigen verfügbaren Korrelation filtern. Das Beispiel hier zeigt, wie Sie einen Korrelationsfilter für Suchmaschinen hinzufügen.

**So fügen Sie einen Korrelationsfilter hinzu**

1. Führen Sie einen Bericht aus, der Korrelationen unterstützt. (Siehe [Ausführen eines Unterteilungsberichts](/help/analyze/reports-analytics/reports-customize/breakdowns.md#task_F685624830E64C829C8BE6435A107F69).)
1. Klicken Sie im Berichtkopf auf den Link **[!UICONTROL Correlation Filter]**.
1. Wählen Sie unter [!UICONTROL Filter Rule Creator]eine Kategorie aus, die mit einem Element korreliert werden soll.
1. Klicken Sie auf **[!UICONTROL OK.]**
