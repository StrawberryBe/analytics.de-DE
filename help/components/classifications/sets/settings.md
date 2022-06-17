---
title: Einstellungen für Klassifizierungssätze
description: Erstellen oder bearbeiten Sie einen Classification-Satz.
exl-id: abf00508-5dde-4669-bf94-5eb4754888cc
source-git-commit: c849f216f8dda83070fc3f8d8b1c25fba4d2786a
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# Einstellungen für Klassifizierungssätze

Konfigurieren Sie einen Classification-Satz, laden Sie Daten hoch oder laden Sie Daten herunter.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > Klicken Sie auf den Namen des gewünschten Klassifizierungssatzes

Beim Bearbeiten eines Classification-Sets stehen zwei Registerkarten zur Verfügung. **[!UICONTROL Schema]** und **[!UICONTROL Einstellungen]**.

## Einstellungen 

Die folgenden Felder sind im [!UICONTROL Einstellungen] und kann bearbeitet werden:

* **[!UICONTROL Name]**: Der Name des Klassifizierungssatzes.
* **[!UICONTROL Beschreibung]**: Die Beschreibung für den Classification-Satz.
* **[!UICONTROL Name des Inhabers]**: Der Name des Eigentümers.
* **[!UICONTROL E-Mail-Inhaber]**: Die E-Mail-Adresse des Eigentümers.
* **[!UICONTROL Über Probleme informieren]**: Eine kommagetrennte Liste von E-Mail-Adressen, die über Probleme mit diesem Klassifizierungssatz benachrichtigt werden.
* **[!UICONTROL Tags]**: Fügen Sie den ausgewählten Classification-Sets ein oder mehrere Tags hinzu, um Classification-Sets zu organisieren oder zu gruppieren, damit sie in Zukunft leichter zu finden sind.

Zusätzliche Felder stehen zu Informationszwecken zur Verfügung und können nicht bearbeitet werden:

* **[!UICONTROL Typ]**: Der Classification-Typ zwischen [!UICONTROL Primär] und [!UICONTROL Suche]. Normalerweise werden Primäre Classifications verwendet.
* **[!UICONTROL Abonnements]**: Die Report Suite und Variable, für die der Classification-Satz gilt. Derzeit wird nur eine Report Suite für einen bestimmten Classification-Satz unterstützt. Unterstützung für mehrere Report Suites ist geplant.

## Schema

Zeigen Sie die derzeit konfigurierten Klassifizierungsdimensionen für dieses Abonnement an. Die folgenden Schaltflächen sind verfügbar:

* **[!UICONTROL Hochladen]**: Manuelles Hochladen von Classification-Daten für eine oder mehrere Classification-Dimensionen. JSON-, CSV-, TSV- und TAB-Dateien werden unterstützt. Beim Hochladen einer gültigen Datei wird eine Tabellenvorschau der zu klassifizierenden Daten angezeigt.
   * **[!UICONTROL Dateikodierung]**: Wählen Sie die richtige Dateikodierung mithilfe dieses Dropdown-Menüs aus. Zu den gültigen Optionen gehören [!UICONTROL UTF-8] und [!UICONTROL Latin1].
   * **[!UICONTROL Trennzeichen auflisten]**: Wählen Sie das richtige Listentrennzeichen aus. Wenn Sie eine heruntergeladene Datei oder Vorlagendatei verwenden, stellen Sie sicher, dass die Variable [!UICONTROL Trennzeichen auflisten] hier stimmt mit der [!UICONTROL Trennzeichen auflisten] wenn die Datei heruntergeladen wurde.
   * **[!UICONTROL Anwenden]**: Speichern Sie die hochgeladenen Classification-Daten in den Classification-Satz.

   ![Classification-Set-Upload](../assets/classification-set-upload.png)

* **[!UICONTROL Download]**: Laden Sie Schlüsselwerte und ihre Classification-Spalten herunter.
   * **[!UICONTROL Zeilen]**: Die maximale Anzahl von Zeilen, die in die Download-Datei aufgenommen werden sollen.
   * **[!UICONTROL Zeilen herunterladen, die zwischen]**: Eine Datumsauswahl im Kalender , mit der Sie Schlüsselwerte nach dem Zeitpunkt filtern können, zu dem sie in Berichten angezeigt werden. Wenn in diesem Datumsbereich kein Schlüsselwert erfasst wurde, wird er nicht in der heruntergeladenen Datei angezeigt.
   * **[!UICONTROL Zurückgegebene Daten]**: Ein Dropdown-Menü, mit dem Sie die in der heruntergeladenen Datei enthaltenen Schlüsselwerte anhand der zugehörigen Classification-Daten filtern können.
      * **[!UICONTROL Alle klassifizierten Werte]**: Umfasst Zeilen, in denen Classification-Daten in mindestens einer Spalte enthalten sind.
      * **[!UICONTROL Alle nicht klassifizierten Werte]**: Umfasst Zeilen, in denen Classification-Daten in mindestens einer Spalte fehlen.
   * **[!UICONTROL Dateiformat]**: Dropdown-Liste, das das Dateiformat der Download-Datei bestimmt. Optionen umfassen [!UICONTROL JSON], [!UICONTROL Kommagetrennte Werte]und [!UICONTROL Excel-Tabulatorgetrennte Werte].
   * **[!UICONTROL Dateikodierung]**: Dropdown, das die Dateikodierung bestimmt. Optionen umfassen [!UICONTROL UTF-8] und [!UICONTROL Latin1]. UTF-8 wird empfohlen.
   * **[!UICONTROL Trennzeichen auflisten]**: Dropdown-Liste, das das Listentrennzeichen bestimmt, das Classification-Spalten in jeder Zeile trennt.

   ![Herunterladen von Klassifizierungssets](../assets/classification-set-download.png)

* **[!UICONTROL Vorlage]**: Laden Sie eine Vorlagendatei herunter. Diese Datei ähnelt der [!UICONTROL Download] -Schaltfläche, mit der Ausnahme, dass sie keine Classification-Daten oder Schlüsselwerte enthält.
   * **[!UICONTROL Dateiformat]**: Dropdown-Liste, das das Dateiformat der Vorlagendatei bestimmt. Optionen umfassen [!UICONTROL Kommagetrennte Werte]und [!UICONTROL Excel-Tabulatorgetrennte Werte].
   * **[!UICONTROL Dateikodierung]**: Dropdown, das die Dateikodierung bestimmt. Optionen umfassen [!UICONTROL UTF-8] und [!UICONTROL Latin1]. UTF-8 wird empfohlen.
   * **[!UICONTROL Trennzeichen auflisten]**: Dropdown-Liste, das das Listentrennzeichen bestimmt, das Classification-Spalten in jeder Zeile trennt.
* **[!UICONTROL Auftragsverlauf]**: Ein Verknüpfungslink, über den Sie zum [Job Manager](job-manager.md), die Aufträge nur für diesen Classification-Satz anzeigt.

   ![Classification-Set-Vorlage](../assets/classification-set-template.png)
