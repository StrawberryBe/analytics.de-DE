---
description: Mit Filtern können Sie den Bericht eingrenzen und Einzelelemente, die mit einem Filter übereinstimmen, ein- oder ausschließen.
title: Filtern von Berichtsdaten
uuid: b6dcaaf7-61f0-4793-870d-e1d156575d5a
feature: Grundlagen zu Reports & Analysen
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 99%

---


# Berichtsdaten filtern {#concept_09DC5B986A644738B12204DAC76A90E1}

Mit Filtern können Sie den Bericht eingrenzen und Einzelelemente, die mit einem Filter übereinstimmen, ein- oder ausschließen.

## Einfacher Filter {#section_5C4DE873F8D5484BB77F38A4AEB57B4A}

![](assets/filter.png)

Der einfache Filter wird in den meisten Berichten angezeigt, damit Sie spezielle Einzelelemente einfach finden können. Bei einfachen Filtern werden keine Sonderzeichen verwendet, sodass `-, ", ', +` und andere Sonderzeichen dem literalen Wert im Bericht entsprechen. Sie können Einzelelemente, die mehrere Begriffe enthalten, mit einem Leerzeichen suchen.

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

Mit erweiterten Filtern können Sie den Umfang Ihrer Suche anhand einer Sammlung aus Filtern kontrollieren. Sie können festlegen, dass alle Filter oder beliebige Filter abgeglichen werden.

![](assets/advanced_filter.png)

**Enthält**

Gibt ein Ergebnis zurück, wenn der Begriff an irgendeiner Stelle im Einzelelement gefunden wird. Dieser Filter funktioniert genauso wie der einfache Filter.

>[!NOTE]
>
> Leerzeichen können nicht in Filtern verwendet werden, da sie als Trennzeichen bei Suchvorgängen verwendet werden.

**Enthält nicht**

Gibt ein Ergebnis zurück, wenn der Begriff an keiner Stelle im Einzelelement gefunden wird. Mit „Enthält nicht“ können Sie „Nicht angegeben“, „Keine“, „Keyword nicht verfügbar“ und andere [spezielle Werte](https://docs.adobe.com/content/help/de-DE/analytics/technotes/unspecified.html) aus Berichten filtern.

Enthält nicht: `none`

Mit dem Filter „Erweitert (Sonderzeichen)“ können Sie noch genauer filtern:

* Erweitert (Sonderzeichen): `-^none$`
* Erweitert (Sonderzeichen): `-"keyword unavailable"`

Beispiel: Das folgende Einzelelement wird vom Kriterium „Enthält nicht“ gefiltert, aber nicht vom Kriterium „Erweitert (Sonderzeichen)“:

```
help:Rename the None classification key
```

**Enthält eins von**

Gibt ein Ergebnis zurück, wenn beliebige durch Leerzeichen getrennte Begriffe im Einzelelement gefunden werden. Der folgende Filter zeigt alle Seiten an, die „Männer“ oder „Verkauf“ enthalten:

Enthält eins von: `mens sale`

Gibt die folgenden Seiten zurück:

```
Womens
Mens
Mens:Desk & TravelJewelry & Accessories:Accessories:Hats:Mens
Sale & Values
```

**Gleich**

Gibt ein Ergebnis zurück, wenn das ganze Einzelelement, einschließlich Leerzeichen und anderer Zeichen, mit der angegebenen Phrase übereinstimmt.

Gleich: `mens:desk & travel`

`Mens:Desk & Travel`

**Beginnt mit**

Gibt ein Ergebnis zurück, wenn das Einzelelement, einschließlich Leerzeichen und anderer Zeichen, mit der angegebenen Phrase beginnt.

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

Gibt ein Ergebnis zurück, wenn das Einzelelement, einschließlich Leerzeichen und anderer Zeichen, mit dem angegebenen Ausdruck endet.

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

Mit dem erweiterten Filter können Sie Platzhalter- und andere komplexe Suchvorgänge durchführen.

| Erweitert (Sonderzeichen) | Beschreibung |
|--- |--- |
| `" "` | Übereinstimmung mit genauem Wortlaut. |
| `*` | Platzhalter, Greedy-Abgleich. <br>Beispielsweise entspricht `r*p` „Registration Signup“. |
| `^` | Beginnt mit. <br>Verwenden Sie kein Leerzeichen zwischen dem Sonderzeichen und dem Suchausdruck. |
| `$` | Endet mit. <br>Verwenden Sie kein Leerzeichen zwischen dem Sonderzeichen und dem Suchausdruck. |
| `-` | Nicht. <br>Verwenden Sie kein Leerzeichen zwischen dem Sonderzeichen und dem Suchausdruck. |
| `|` | Oder<br>Hinweis: Sie müssen ein Leerzeichen auf jeder Seite des Senkrechtstriches (`" | "`) einfügen. |

## Berichtsspezifische Filter erstellen {#task_DEBB0632411D4CA8AA0B3BA267A5B35F}

In diesen Schritten wird beschrieben, wie Filter für Berichte erstellt werden.

<!-- 

t_reports_filter_specific.xml

 -->

Bestimmte Berichte enthalten einen Filter, der speziell an diesen angepasst ist. Der [!UICONTROL Bericht „Kaufkonversionstrichter“] kann z. B. nach Webseiten gefiltert werden. In einem [!UICONTROL Geosegmentation-Bericht] können Sie nach geografischen Regionen filtern. Weitere Berichte enthalten andere, jeweils spezifische Filter.

Wenn Sie auf diese Filter zugreifen, werden Berichtsmetriken für die in der Liste angegebenen Elemente angezeigt.

**So erstellen Sie berichtsspezifische Filter**

1. Erstellen Sie einen Bericht, wie zum Beispiel einen [!UICONTROL Kaufbericht] (**[!UICONTROL Site-Metriken]** > **[!UICONTROL Kauf]** > **[!UICONTROL Einkaufs-Konversionstrichter]**).
1. Klicken Sie im Berichtkopf auf den Link **[!UICONTROL Filter]**.
1. Klicken Sie auf der Seite [!UICONTROL Filterauswahl] auf **[!UICONTROL Einen Filter einsetzen]** und wählen Sie anschließend einen Filtertyp aus.
1. Geben Sie zur Suche nach einem Element eine Zeichenfolge in das **[!UICONTROL Suchfeld]** ein.
1. Klicken Sie auf **[!UICONTROL OK]**.

## Korrelationsfilter hinzufügen {#task_065042E384DA4BF3864C58AF2B88D6E2}

In diesen Schritten wird beschrieben, wie Sie einen Korrelationsfilter hinzufügen.

<!-- 

t_reports_correlation_filter.xml

 -->

Bestimmten Berichten können Sie benutzerspezifische Korrelationsfilter hinzufügen. Wenn Sie beispielsweise den [!UICONTROL Bericht „Seiten“] für eine Report Suite anzeigen, der mit einer Frauen-Seite korrelierte Site-Bereiche enthält, können Sie einen Filter für einen Bericht einrichten, der die bevorzugten Seiten innerhalb des Site-Bereichs „Frauen“ anzeigt.

Sie können die in einem Korrelationsbericht angezeigten Daten anhand einer beliebigen verfügbaren Korrelation filtern. Das hier dargestellte Beispiel zeigt, wie Sie einen Korrelationsfilter für Suchmaschinen hinzufügen.

**So fügen Sie einen Korrelationsfilter hinzu**

1. Führen Sie einen Bericht aus, der Korrelationen unterstützt. (Siehe [Ausführen eines Detailberichts](/help/analyze/reports-analytics/reports-customize/breakdowns.md#task_F685624830E64C829C8BE6435A107F69).)
1. Klicken Sie in dem Berichtkopf auf den Link **[!UICONTROL „Korrelationsfilter“]**.
1. Wählen Sie unter [!UICONTROL „Filterregelerstellung“] eine Kategorie, die Sie mit einem Element korrelieren möchten.
1. Klicken Sie auf **[!UICONTROL OK]**.
