---
description: Adobe Analytics unterstützt sowohl einstufige als auch mehrstufige Klassifizierungsmodelle. Mit einer Classification-Hierarchie können Sie eine Classification auf eine Classification anwenden.
subtopic: Classifications
title: Informationen über Unterklassifizierungen
topic: Admin tools
uuid: 48bd7fc1-54a1-40ef-bc55-395338522f2d
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Informationen über Unterklassifizierungen

Adobe Analytics unterstützt sowohl einstufige als auch mehrstufige Klassifizierungsmodelle. Mit einer Classification-Hierarchie können Sie eine Classification auf eine Classification anwenden.

>[!NOTE] Unterklassifizierungen bezeichnen die Möglichkeit, Klassifizierungen weiter zu klassifizieren. However, this is not the same as a [!UICONTROL Classification Hierarchy] used to create [!UICONTROL Hierarchy] reports. Weitere Informationen zu Klassifizierungshierarchien finden Sie unter [Klassifizierungshierarchien](classification-hierarchies.md).

Beispiel:

![](assets/single-level-popup-C.png)

Jede Klassifizierung in diesem Berichte ist unabhängig und entspricht einem neuen Unterbericht für die ausgewählte Variable. Darüber hinaus stellt jede Klassifizierung eine Datenspalte in der Datendatei dar, wobei der Klassifizierungsname als Spaltenüberschrift dient. Beispiel:

| SCHLÜSSEL | EIGENSCHAFT 1 | EIGENSCHAFT 2 |
|---|---|---|
| 123 | ABC | A12B |
| 456 | DEF | C3D4 |

Weitere Informationen über die Datendatei finden Sie unter  [Klassifizierungsdatendateien](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md).

Mehrstufige Classifications bestehen aus über- und untergeordneten Classifications. Beispiel:

![](assets/Multi-Level-Class-popup.png)

**Übergeordnete Classifications:** Als übergeordnete Classification zählt jede Classification, der eine andere Classification untergeordnet ist. Eine Classification kann gleichzeitig über- und untergeordnet sein. Die übergeordneten Classifications der obersten Ebene entsprechen einer einstufigen Classification (siehe  [Einstufige Classifications](/help/components/c-classifications2/c-sub-classifications.md)).

**Untergeordnete Classifications:** Als untergeordnete Classification gilt jede Classification, der eine andere Classification anstelle der Variablen übergeordnet ist. Untergeordnete Classifications bieten zusätzliche Informationen über ihre übergeordnete Classification. Eine [!UICONTROL Campaigns] Classification könnte beispielsweise eine untergeordnete Classification der Kampagne Inhaber haben. [!UICONTROL Numeric] Klassifizierungen fungieren auch als Metriken in Klassifizierungsberichten.

Jede Classification, ob über- oder untergeordnet, stellt eine Datenspalte in der Datendatei dar. Die Spaltenüberschrift für eine untergeordnete Classification mit dem folgenden Benennungsformat:

`<parent_name>^<child_name>`

Weitere Informationen zum Datendateiformat finden Sie unter [Klassifizierungsdatendateien](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md).

Beispiel:

| SCHLÜSSEL | EIGENSCHAFT 1 | Eigenschaft 1&amp;Hat;Eigenschaft1-1 | Eigenschaft 1&amp;Hat;Eigenschaft1-2 | Eigenschaft 2 |
|---|---|---|---|---|
| 123 | ABC | Grün | Klein | A12B |
| 456 | DEF | Rot | Groß | C3D4 |

Obwohl die Dateivorlage für eine mehrstufige Klassifizierung komplexer ist, haben mehrstufige Klassifizierungen den Vorteil, dass separate Ebenen als separate Dateien hochgeladen werden können. Dieser Ansatz kann verwendet werden, um die Menge der Daten zu minimieren, die regelmäßig hochgeladen werden müssen (täglich, wöchentlich usw.), indem Daten in Klassifizierungsstufen gruppiert werden, die sich im Laufe der Zeit ändern, im Gegensatz zu solchen, die dies nicht tun.

>[!NOTE] Wenn die [!UICONTROL Key] Spalte in einer Datendatei leer ist, generiert Adobe automatisch eindeutige Schlüssel für jede Datenzeile. To avoid possible file corruption when uploading a data file with second-level or higher-level classification data, populate each row of the [!UICONTROL Key] column with an asterisk (*).

Weitere Informationen zur Fehlerbehebung finden Sie unter [Häufige Probleme beim Hochladen von Classifications](https://marketing.adobe.com/resources/help/de_DE/home/index.html#kb-common-saint-upload-issues).

## Beispiele

![](assets/sample-product-classifications.png)

>[!NOTE] Die Produktklassifizierungsdaten sind auf Datenattribute beschränkt, die sich direkt auf das Produkt beziehen. Die Daten beschränken sich nicht darauf, wie die Produkte auf der Website kategorisiert oder verkauft werden. Datenelemente wie Verkaufs-Kategorien, Site-Browse-Knoten oder Sonderangebotsartikel sind keine Produktklassifizierungsdaten. Stattdessen werden diese Elemente in Berichtskonversionsvariablen erfasst.

Beim Hochladen von Datendateien für diese Produktklassifizierung können Sie die Klassifizierungsdaten als einzelne Datei oder als mehrere Dateien hochladen (siehe unten). Durch Trennung des Farbcodes in Datei 1 und des Farbnamens in Datei 2 müssen die Farbnamensdaten (die möglicherweise nur einige Zeilen umfassen) nur aktualisiert werden, wenn neue Farbcodes erstellt werden. Dies schließt das Farbnamenfeld (CODE&amp;Hat;FARBE) aus der häufiger aktualisierten Datei 1 aus und verringert damit Dateigröße und Komplexität beim Generieren der Datendatei.

### Produkt-Classification – Einzeldatei {#section_E8C5E031869C449F9B636F5EB3BFEC17}

| SCHLÜSSEL | PRODUKTNAME | PRODUKTDETAILS | GESCHLECHT | GRÖSSE | CODE | CODE&amp;Hat;FARBE |
|---|---|---|---|---|---|---|
| 410390013 | Polo-SS | Herren Poloshirt, Kurzarm (M,01) | Mo | Mo | 01 | Stein |
| 410390014 | Polo-SS | Herren Poloshirt, Kurzarm (L,03) | Mo | L | 03 | Heather |
| 410390015 | Polo-LS | Damen Poloshirt, Langarm (S,23) | Fr | S | 23 | Aqua |

### Produkt-Classification – Mehrere Dateien (Datei 1)  {#section_A99F7D0F145540069BA4EEC0597FF13F}

| SCHLÜSSEL | PRODUKTNAME | PRODUKTDETAILS | GESCHLECHT | GRÖSSE | CODE |
|---|---|---|---|---|---|
| 410390013 | Polo-SS | Herren Poloshirt, Kurzarm (M,01) | Mo | Mo | 01 |
| 410390014 | Polo-SS | Herren Poloshirt, Kurzarm (L,03) | Mo | L | 03 |
| 410390015 | Polo-LS | Damen Poloshirt, Langarm (S,23) | Fr | S | 23 |

### Produkt-Classification – Mehrere Dateien (Datei 2)  {#section_19ED95C33B174A9687E81714568D56A3}

| SCHLÜSSEL | CODE | CODE&amp;Hat;FARBE |
|---|---|---|
| * | 01 | Stein |
| * | 03 | Heather |
| * | 23 | Aqua |
