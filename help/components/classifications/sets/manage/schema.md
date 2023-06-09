---
title: Klassifizierungsset-Schema
description: Anzeigen und Bearbeiten des Schemas für einen einzelnen Classification-Satz.
source-git-commit: d0e3b28590b24d630a192ee857a7d84c115dc8c1
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 46%

---

# Schema

Zeigen Sie die derzeit konfigurierten Classification-Dimensionen für diesen Classification-Satz an.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > Klicken Sie auf den Namen des gewünschten Klassifizierungssatzes > **[!UICONTROL Schema]**

Folgende Schaltflächen sind verfügbar:

<!--* **[!UICONTROL Add]**: Adds an empty row so that you can add a classification dimension to the schema.-->
* **[!UICONTROL Hochladen]**: Manuelles Hochladen von Klassifizierungsdaten für eine oder mehrere Klassifizierungsdimensionen. `JSON`, `CSV`, `TSV`und `TAB` -Dateien unterstützt. Beim Hochladen einer gültigen Datei wird eine Tabellenvorschau der zu klassifizierenden Daten angezeigt.
   * **[!UICONTROL Dateikodierung]**: Wählen Sie mithilfe dieser Dropdown-Liste die richtige Dateikodierung aus. Zu den gültigen Optionen gehören [!UICONTROL UTF-8] und [!UICONTROL Latin1].
   * **[!UICONTROL Listentrennzeichen]**: Wählen Sie das richtige Listentrennzeichen aus. Wenn Sie eine heruntergeladene Datei oder eine Vorlagendatei verwenden, stellen Sie sicher, dass das [!UICONTROL Listentrennzeichen] hier mit dem [!UICONTROL Listentrennzeichen] übereinstimmt, das beim Herunterladen der Datei verwendet wurde.
   * **[!UICONTROL Anwenden]**: Speichern Sie die hochgeladenen Classification-Daten in den Classification-Satz.

  ![Classification-Set-Upload](../../assets/classification-set-upload.png)

* **[!UICONTROL Herunterladen]**: Laden Sie Schlüsselwerte und ihre Classification-Spalten herunter.
   * **[!UICONTROL Zeilen]**: Die maximale Anzahl von Zeilen, die in die herunterzuladene Datei aufgenommen werden sollen.
   * **[!UICONTROL Zeilen herunterladen, die eingingen zwischen]**: Eine Datumsauswahl im Kalender, mit der Sie Schlüsselwerte nach dem Zeitpunkt filtern können, zu dem sie in Berichten angezeigt werden. Wenn in diesem Datumsbereich kein Schlüsselwert erfasst wurde, erscheint er nicht in der heruntergeladenen Datei.
   * **[!UICONTROL Zurückgegebene Daten]**: Eine Dropdown-Liste, mit der Sie in der heruntergeladenen Datei enthaltene Schlüsselwerte anhand der zugehörigen Classification-Daten filtern können.
      * **[!UICONTROL Alle klassifizierten Werte]**: Umfasst Zeilen, in denen in mindestens einer Spalte Klassifizierungsdaten enthalten sind.
      * **[!UICONTROL Alle nicht klassifizierten Werte]**: Umfasst Zeilen, in denen in mindestens einer Spalte Klassifizierungsdaten fehlen.
   * **[!UICONTROL Dateiformat]**: Eine Dropdown-Liste, die das Dateiformat der Download-Datei bestimmt. Die Optionen umfassen [!UICONTROL JSON], [!UICONTROL Kommagetrennte Werte] und [!UICONTROL Tabulatorgetrennte Werte für Excel].
   * **[!UICONTROL Dateikodierung]**: Eine Dropdown-Liste, die die Dateikodierung bestimmt. Die Optionen umfassen [!UICONTROL UTF-8] und [!UICONTROL Latin1]. UTF-8 wird empfohlen.

  ![Herunterladen von Klassifizierungssätzen](../../assets/classification-set-download.png)

* **[!UICONTROL Vorlage]**: Herunterladen einer Vorlagendatei. Diese Datei ähnelt der Datei, die mit der Schaltfläche [!UICONTROL Herunterladen] erhalten wird, mit der Ausnahme, dass sie keine Klassifizierungsdaten oder Schlüsselwerte enthält.
   * **[!UICONTROL Dateiformat]**: Eine Dropdown-Liste, die das Dateiformat der Vorlagendatei bestimmt. Die Optionen umfassen [!UICONTROL Kommagetrennte Werte] und [!UICONTROL Tabulatorgetrennte Werte für Excel].
   * **[!UICONTROL Dateikodierung]**: Eine Dropdown-Liste, die die Dateikodierung bestimmt. Die Optionen umfassen [!UICONTROL UTF-8] und [!UICONTROL Latin1]. UTF-8 wird empfohlen.
   * **[!UICONTROL Trennzeichen auflisten]**: Eine Dropdown-Liste, die das Listentrennzeichen bestimmt, das Classification-Spalten für jede Zeile trennt.

  ![Classification-Set-Vorlage](../../assets/classification-set-template.png)

* **[!UICONTROL Auftragsverlauf]**: Ein Verknüpfungslink, über den Sie zum [Job Manager](../job-manager.md), die Aufträge nur für diesen Classification-Satz anzeigt.
* **[!UICONTROL Automatisieren]**: Daten werden automatisch von externen Speicherorten erfasst.
   * **[!UICONTROL Standortkonto]**: Eine Dropdown-Liste mit vorhandenen Standortkonten, die Ihre Organisation konfiguriert hat. Es steht eine Schaltfläche zum Erstellen eines Standortkontos zur Verfügung.
   * **[!UICONTROL Standort]**: Eine Dropdown-Liste, die die vorhandenen Orte anzeigt, die Ihre Organisation konfiguriert hat. Es steht eine Schaltfläche zum Erstellen eines Standorts zur Verfügung.
   * **[!UICONTROL Trennzeichen]**: Das Spaltentrennzeichen für hochgeladene Dateien. Optionen umfassen [!UICONTROL Komma], [!UICONTROL Semikolon], [!UICONTROL Doppelpunkt], [!UICONTROL Vertikaler Balken], [!UICONTROL Leerzeichen], [!UICONTROL Vorwärtsschrägstrich], [!UICONTROL Abwärtsschrägstrich], [!UICONTROL Dash]oder [!UICONTROL Unterstrich].
   * **[!UICONTROL Kodierung]**: Eine Dropdown-Liste, die die Dateikodierung bestimmt. Die Optionen umfassen [!UICONTROL UTF-8] und [!UICONTROL Latin1]. UTF-8 wird empfohlen.
