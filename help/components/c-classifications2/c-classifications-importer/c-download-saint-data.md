---
description: (Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.
subtopic: Classifications
title: Klassifizierungsvorlage
topic: Admin tools
uuid: 4edd411b-164c-4b4d-a872-b57a3163ca72
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '366'
ht-degree: 100%

---


# Klassifizierungsvorlage

(Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.

## Klassifizierungsvorlage {#concept_0F06847AD8D042F5BA818AE3C37E2417}

(Optional) Vor dem Importieren von Classifications in Marketingberichte können Sie eine Vorlage herunterladen, mit der Sie eine Classification-Datendatei erstellen. Die Datendatei verwendet Ihre gewünschten Classifications als Spaltenüberschriften und organisiert dann den Berichtdatensatz unter den entsprechenden Classification-Überschriften.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**

| Element | Beschreibung |
|---|---|
| Report Suite auswählen | Wählen Sie die Report Suite aus, die in der Vorlage genutzt werden soll. Report Suite und Datensatz müssen übereinstimmen. |
| Datensatz, der klassifiziert werden soll | Wählen Sie den Typ der Daten für die Datendatei aus. Das Menü enthält alle Berichte aus Ihren Report Suites, die für Classifications konfiguriert sind. |
| Nummerisch exportieren 2 | Mit dem Importeur können Sie Nummerisch-2-Classifications in das System importieren. Nummerisch-2-Classifications sind für Variablen sinnvoll, die sich im Laufe der Zeit für verschiedene Artikel bzw. Einheiten ändern, z. B. Kosten und Budgetwerte im [!UICONTROL Marketingkanal] bericht. Unter [„Numerisch 2“-Klassifizierungen](/help/components/c-classifications2/c-numeric-2/c-numeric-2-classifications.md) finden Sie Informationen zum Hochladen von Daten mithilfe von „Numerisch 2“-Klassifizierungen. |
| Kodierung | Wählen Sie die Zeichenkodierung für die Datendatei aus. Standardmäßig wird das Kodierungsformat UTF-8 verwendet. |
| Download | Lädt die Vorlagendatei herunter. |

Die Vorlage beinhaltet die aktuell definierten Classifications (Spaltenüberschriften) eines spezifischen Datensatzes ohne die jeder Classification zugeordneten Daten.

>[!NOTE]
>
>Die Vorlagenmethode beschränkt Ihre heruntergeladenen Klassifizierungsdaten auf eine einzige Report Suite.

Weitere Informationen zur Datendateistruktur finden Sie unter [Informationen zu Klassifizierungsdatendateien](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md).

## Herunterladen einer Classification-Datenvorlage (optional) {#task_8DFCF309B6FD43ABB1D6FEE9AFAEC596}

Die Vorlage liefert das Dateiformat, das für Classifications genutzt werden muss.

>[!NOTE]
>
>Die Vorlagenmethode beschränkt Ihre heruntergeladenen Daten auf eine einzige Report Suite.

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Legen Sie unter der Registerkarte **[!UICONTROL Vorlage herunterladen]** die Konfiguration für die [-Datenvorlage fest](/help/components/c-classifications2/c-classifications-importer/c-download-saint-data.md).
1. Klicken Sie auf **[!UICONTROL Herunterladen]**.
1. Speichern Sie die Vorlagendatei auf Ihrem lokalen System.

   Die Vorlagendatei ist eine tabulatorgetrennte Datendatei (Dateierweiterung [!DNL .tab]), die von den meisten Tabellenkalkulationsprogrammen unterstützt wird.

