---
description: In diesen Schritten wird beschrieben, wie Sie Classification-Daten löschen oder entfernen.
seo-description: In diesen Schritten wird beschrieben, wie Sie Klassifizierungsdaten löschen oder entfernen.
seo-title: Löschen von Classification-Daten
solution: Analytics
subtopic: Classifications
title: Löschen von Classification-Daten
topic: Admin Tools
uuid: 5b1b0ac7-ee52-4fd8-b98e-25283595cf0c
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Löschen von Classification-Daten

In diesen Schritten wird beschrieben, wie Sie Classification-Daten löschen oder entfernen.

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Click **[!UICONTROL Browser Export]**.
1. Wählen Sie die Report Suite und den Datensatz aus, aus denen Classification-Daten entfernt werden sollen.
1. Adjust any optional settings to filter specific data you're looking for, then click **[!UICONTROL Export File]**.
1. Once the file has been downloaded, open the file and replace any classification values you wish to delete with [!DNL ~empty~].

   Alternatively, use [!DNL ~deletekey~]. Mit diesem Befehl wird die Classification für den betreffenden Schlüssel so behandelt, als wäre sie nie erfolgt. Der Schlüssel und alle Spaltendaten werden aus den Suchtabellen entfernt.

   **Caveat**: Sie benötigen nur eine Spalte, die [!DNL ~deletekey~]enthält. The [!DNL ~empty~] command works at the cell level (key and column combination), so you need [!DNL ~empty~] in the classification column you want to remove. However, [!DNL ~deletekey~] works at the row level (the key and all associated metadata), so it only needs to appear in one of the columns in the row. Mit diesem Befehl werden alle Metadaten aus der Zeile gelöscht. Adobe interpretiert dies so, als wäre der Schlüssel nie klassifiziert worden, und zeigt ihn in der Kategorie [Keine](../../../components/c-classifications2/c-classifications-importer/nonclassified-keys.md#concept_233E51DDF3084FF7B7EA89381C73C5FF) an.

1. Speichern Sie die Datei, und laden Sie sie danach über die Registerkarte [!UICONTROL Datei importieren] hoch.

   After you upload the file, the system recognizes [!DNL ~empty~] as a command to delete that classification value.

   **Eigenschaften dieses Befehls**

* [!DNL ~leer~] muss Kleinbuchstaben ohne Leerzeichen sein. Die folgenden Eingaben sind ungültig:

   * [!DNL ~EMPTY~]
   * [!DNL ~ empty ~]
   * [!DNL ~Empty~]

* Werte in der Schlüsselspalte können nicht gelöscht werden. Diese Daten werden direkt an die Berichterstellung übergeben und sind dauerhaft.
* Wenn Sie einen Classification-Wert entfernen, der Unter-Classifications enthält, werden diese ebenfalls entfernt. Classifications können nicht ohne Schlüsselwert bestehen, und die übergeordnete Classification ist der Schlüsselwert für eine Unter-Classification.
* Sie können die Unter-Classificationsdaten entfernen, wobei die übergeordnete Classification intakt bleibt.

