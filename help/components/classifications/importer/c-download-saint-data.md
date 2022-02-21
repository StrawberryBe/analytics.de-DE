---
description: (Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.
title: Klassifizierungsvorlage
feature: Classifications
exl-id: e299509a-0c4f-4ba8-9e91-96356c386054
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 100%

---

# Klassifizierungsvorlage

(Optional) Vor dem Importieren von Klassifizierungen in Marketing-Berichte können Sie eine Vorlage herunterladen, um eine Klassifizierungsdatendatei zu erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.

## Klassifizierungsvorlage {#concept_0F06847AD8D042F5BA818AE3C37E2417}

(Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

| Element | Beschreibung |
| --- | ---|
| Report Suite auswählen | Wählen Sie die Report Suite aus, die in der Vorlage genutzt werden soll. Report Suite und Datensatz müssen übereinstimmen. |
| Datensatz, der klassifiziert werden soll | Wählen Sie den Typ der Daten für die Datendatei aus. Das Menü enthält alle Berichte aus Ihren Report Suites, die für Classifications konfiguriert sind. |
| Export von Numerisch 2 | **Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |
| Codierung | Wählen Sie die Zeichencodierung für die Datendatei aus. Standardmäßig wird das Kodierungsformat UTF-8 verwendet.<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |
| Download | Lädt die Vorlagendatei herunter. |

Die Vorlage beinhaltet die aktuell definierten Classifications (Spaltenüberschriften) eines spezifischen Datensatzes ohne die jeder Classification zugeordneten Daten.

>[!NOTE]
>
>Die Vorlagenmethode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

Weitere Informationen zur Datendateistruktur finden Sie unter [Informationen zu Klassifizierungsdatendateien](/help/components/classifications/importer/c-saint-data-files.md).

## Herunterladen einer Classification-Datenvorlage (optional) {#task_8DFCF309B6FD43ABB1D6FEE9AFAEC596}

Die Vorlage liefert das Dateiformat, das für Classifications genutzt werden muss.

>[!NOTE]
>
>Die Vorlagenmethode beschränkt Ihre heruntergeladenen Daten auf eine einzige Report Suite.

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Legen Sie unter der Registerkarte **[!UICONTROL Vorlage herunterladen]** die Konfiguration für die [-Datenvorlage fest](/help/components/classifications/importer/c-download-saint-data.md).
1. Klicken Sie auf **[!UICONTROL Herunterladen]**.
1. Speichern Sie die Vorlagendatei auf Ihrem lokalen System.

   Die Vorlagendatei ist eine tabulatorgetrennte Datendatei (Dateierweiterung [!DNL .tab]), die von den meisten Tabellenkalkulationsprogrammen unterstützt wird.
