---
title: Einstellungen für Klassifizierungssätze
description: Erstellen oder bearbeiten Sie einen Classification-Satz.
source-git-commit: c9465ea0524225494aa5067d00ca5e7aba4bca92
workflow-type: tm+mt
source-wordcount: '286'
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
