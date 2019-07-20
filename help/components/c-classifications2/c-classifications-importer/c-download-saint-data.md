---
description: (Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.
seo-description: (Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.
seo-title: Classification-Vorlage
solution: Analytics
subtopic: Classifications
title: Classification-Vorlage
topic: Admin Tools
uuid: 4 edd 411 b -164 c -4 b 4 d-a 872-b 57 a 3163 ca 72
translation-type: tm+mt
source-git-commit: 1986561a83f22619b627d754376f7e936902a737

---


# Classification-Vorlage

(Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.

## Classification template {#concept_0F06847AD8D042F5BA818AE3C37E2417}

(Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.

**[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.

| Element | Beschreibung |
|---|---|
| Report Suite auswählen | Wählen Sie die Report Suite aus, die in der Vorlage genutzt werden soll. Report Suite und Datensatz müssen übereinstimmen. |
| Datensatz, der klassifiziert werden soll | Wählen Sie den Typ der Daten für die Datendatei aus. Das Menü enthält alle Berichte aus Ihren Report Suites, die für Classifications konfiguriert sind. |
| Nummerisch exportieren 2 | Mit dem Importeur können Sie Nummerisch-2-Classifications in das System importieren. Nummerisch-2-Classifications sind für Variablen sinnvoll, die sich im Laufe der Zeit für verschiedene Artikel bzw. Einheiten ändern, z. B. Kosten und Budgetwerte im [!UICONTROL Marketingkanal]bericht. Unter [Numerisch-2-Classifications](../../../components/c-classifications2/c-numeric-2/c-numeric-2-classifications.md#concept_71024B7B91DF4E909076062AB1380D8B) für Informationen zum Hochladen von Daten mit Numerisch-2-Classifications. |
| Kodierung | Wählen Sie die Zeichenkodierung für die Datendatei aus. Standardmäßig wird das Kodierungsformat UTF-8 verwendet. |
| Download | Lädt die Vorlagendatei herunter. |

Die Vorlage beinhaltet die aktuell definierten Classifications (Spaltenüberschriften) eines spezifischen Datensatzes ohne die jeder Classification zugeordneten Daten.

>[!NOTE]
>
>Die Vorlagenmethode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

For more information about the data file structure, see [About Classification Data Files](../../../components/c-classifications2/c-classifications-importer/c-saint-data-files.md#concept_EBA7669C546040BE8162ADACA3548735).

## Herunterladen einer Classification-Datenvorlage (optional) {#task_8DFCF309B6FD43ABB1D6FEE9AFAEC596}

Die Vorlage liefert das Dateiformat, das für Classifications genutzt werden muss.

>[!NOTE]
>
>Die Vorlagenmethode beschränkt Ihre Daten auf eine einzige Report Suite.

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Legen Sie unter der Registerkarte **Vorlage herunterladen** die Konfiguration für die [-Datenvorlage fest](../../../components/c-classifications2/c-classifications-importer/c-download-saint-data.md#concept_0F06847AD8D042F5BA818AE3C37E2417).
1. Klicken Sie auf **[!UICONTROL Herunterladen]**.
1. Speichern Sie die Vorlagendatei auf Ihrem lokalen System.

   The template file is a tab-delimited data file ( [!DNL .tab] filename extension) that most spreadsheet applications support.

