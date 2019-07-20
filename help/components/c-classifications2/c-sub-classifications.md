---
description: Adobe Analytics unterstützt sowohl einstufige als auch mehrstufige Classifications-Modelle. Mit einer Classification-Hierarchie können Sie eine Classification auf eine Classification anwenden.
seo-description: Adobe Analytics unterstützt sowohl einstufige als auch mehrstufige Classifications-Modelle. Mit einer Classification-Hierarchie können Sie eine Classification auf eine Classification anwenden.
seo-title: Unter-Classifications
solution: Analytics
subtopic: Classifications
title: Unter-Classifications
topic: Admin Tools
uuid: 48 bd 7 fc 1-54 a 1-40 ef-bc 55-395338522 f 2 d
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Unter-Classifications

Adobe Analytics unterstützt sowohl einstufige als auch mehrstufige Classifications-Modelle. Mit einer Classification-Hierarchie können Sie eine Classification auf eine Classification anwenden.

>[!NOTE]
>
>Unter-Classifications sind die Möglichkeit, Klassifizierungen für Classifications zu erstellen. Das ist allerdings nicht dasselbe wie eine zum Erstellen von [!UICONTROL Hierarchie]berichten verwendete [!UICONTROL Classification-Hierarchie]. For more information about Classification hierarchies, see [Classification Hierarchies](classification-hierarchies.md).

<!-- 

<p>Removed sub-classifications in rule builder. Preserve subclass files in project for future reference. </p>

 -->

<!-- 

c_single-level_classifications.xml

 -->

Beispiel:

![](assets/single-level-popup-C.png)

Jede Classification in diesem Modell ist unabhängig und entspricht einem neuen Unterbericht für die ausgewählte Berichterstellungsvariable. Darüber hinaus stellt jede Classification eine Datenspalte in der Datendatei dar, wobei der Classification-Name als Spaltenüberschrift dient. Beispiel:

| SCHLÜSSEL | EIGENSCHAFT 1 | EIGENSCHAFT 2 |
|---|---|---|
| 123 | ABC | A12B |
| 456 | DEF | C3D4 |

Weitere Informationen über die Datendatei finden Sie unter [Classification-Datendateien](../../components/c-classifications2/c-classifications-importer/c-saint-data-files.md#concept_EBA7669C546040BE8162ADACA3548735).

<!-- 

c_multiple-level_classifications.xml

 -->

Mehrstufige Classifications bestehen aus über- und untergeordneten Classifications. Beispiel:

![](assets/Multi-Level-Class-popup.png)

**Übergeordnete Classifications:** Als übergeordnete Classification zählt jede Classification, der eine andere Classification untergeordnet ist. Eine Classification kann gleichzeitig über- und untergeordnet sein. Die übergeordneten Classifications der obersten Ebene entsprechen einer einstufigen Classification (siehe [Einstufige Classifications](../../components/c-classifications2/c-sub-classifications.md#concept_6B909B54221F4A9BAEA8E30594F06C49)).

**Untergeordnete Classifications:** Als untergeordnete Classification gilt jede Classification, der eine andere Classification anstelle der Variablen übergeordnet ist. Untergeordnete Classifications enthalten zusätzliche Informationen über ihre übergeordnete Classification. Beispielsweise könnte einer [!UICONTROL Kampagnen]-Classification eine Kampagnenverantwortlichen-Classification untergeordnet sein. [!UICONTROL Nummerische] Classifications fungieren auch als Metriken in Classification-Berichten.

Jede Classification, ob über- oder untergeordnet, stellt eine Datenspalte in der Datendatei dar. Die Spaltenüberschrift für eine untergeordnete Classification nutzt das folgende Namensformat.

`<parent_name>^<child_name>`

For more information about the data file format, see [Classification Data Files](../../components/c-classifications2/c-classifications-importer/c-saint-data-files.md#concept_EBA7669C546040BE8162ADACA3548735).

Beispiel:

| SCHLÜSSEL | EIGENSCHAFT 1 | Property 1 &amp; amp; Hat; Eigenschaft 1-1 | Property 1 &amp; amp; Hat; Eigenschaft 1-2 | Eigenschaft 2 |
|---|---|---|---|---|
| 123 | ABC | Grün | Klein | A12B |
| 456 | DEF | Rot | Groß | C3D4 |

Obwohl die Dateivorlage für eine mehrstufige Classification komplexer ist, liegt der Vorteil mehrstufiger Classifications darin, dass einzelne Stufen als einzelne Dateien hochgeladen werden können. Dieser Ansatz sorgt für eine Minimierung der Datenmenge, die regelmäßig hochgeladen werden muss (täglich, wöchentlich usw.), indem Daten in Classification-Stufen gruppiert werden, die sich mit der Zeit ändern, im Gegensatz zu solchen, die das nicht tun.

>[!NOTE]
>
>If the [!UICONTROL Key] column in a data file is blank, Adobe automatically generates unique keys for each data row. Um beim Hochladen einer Datendatei mit Classification-Daten der zweiten oder einer höheren Stufe mögliche Dateibeschädigungen zu vermeiden, fügen Sie in jeder Zeile der [!UICONTROL Schlüssel]spalte ein Sternchen (*) ein.

Weitere Informationen zur Fehlerbehebung finden Sie unter [Häufige Probleme beim Hochladen von Classifications](https://marketing.adobe.com/resources/help/en_US/home/index.html#kb-common-saint-upload-issues).

<!-- 

c_classifications_example.xml

 -->

![](assets/sample-product-classifications.png)

>[!NOTE]
Produktklassifizierungsdaten sind auf Datenattribute beschränkt, die direkt mit dem Produkt zusammenhängen. Die Daten sind nicht darauf beschränkt, wie die Produkte kategorisiert sind oder auf der Website zum Verkauf angeboten werden. Datenelemente wie Verkaufskategorien, Website-Browserknoten oder Verkaufselemente sind keine Produkt-Classification-Daten. Diese Elemente werden stattdessen in Berichtskonversionsvariablen erfasst.

Beim Hochladen von Datendateien für diese Produkt-Classification können Sie die Classification-Daten wahlweise als einzelne Datei oder in mehreren Dateien hochladen (siehe unten). Durch das Aufteilen des Farbcodes in Datei 1 und des Farbnamens in Datei 2 müssen die Farbnamensdaten (die möglicherweise nur ein paar Zeilen umfassen) nur aktualisiert werden, wenn neue Farbcodes erstellt werden. Dadurch wird der Farbname entfernt (CODE &amp; amp; Hat; Farbfeld) aus der häufiger aktualisierten Datei 1 und verringert Dateigröße und Komplexität beim Generieren der Datendatei.

## Produkt-Classification – Einzeldatei {#section_E8C5E031869C449F9B636F5EB3BFEC17}

| SCHLÜSSEL | PRODUKTNAME | PRODUKTDETAILS | GESCHLECHT | GRÖSSE | CODE | CODE &amp; amp; Hat; COLOR |
|---|---|---|---|---|---|---|
| 410390013 | Polo-SS | Herren-Poloshirt – Kurzarm (M,01) | Mo | Mo | 01 | Stein |
| 410390014 | Polo-SS | Herren-Poloshirt – Kurzarm (L,03) | Mo | L | 03 | Heather |
| 410390015 | Polo-LS | Damen-Poloshirt – Langarm (S,23) | Fr | S | 23 | Aqua |

## Produkt-Classification – Mehrere Dateien (Datei 1) {#section_A99F7D0F145540069BA4EEC0597FF13F}

| SCHLÜSSEL | PRODUKTNAME | PRODUKTDETAILS | GESCHLECHT | GRÖSSE | CODE |
|---|---|---|---|---|---|
| 410390013 | Polo-SS | Herren-Poloshirt – Kurzarm (M,01) | Mo | Mo | 01 |
| 410390014 | Polo-SS | Herren-Poloshirt – Kurzarm (L,03) | Mo | L | 03 |
| 410390015 | Polo-LS | Damen-Poloshirt – Langarm (S,23) | Fr | S | 23 |

## Produkt-Classification – Mehrere Dateien (Datei 2) {#section_19ED95C33B174A9687E81714568D56A3}

| SCHLÜSSEL | CODE | CODE &amp; amp; Hat; COLOR |
|---|---|---|
| * | 01 | Stein |
| * | 03 | Heather |
| * | 23 | Aqua |
