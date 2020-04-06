---
description: In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.
subtopic: Classifications
title: FTP-Import
topic: Admin tools
uuid: a914970d-ba02-4111-9dcf-06448f71b9f3
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# FTP-Import

In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.

## FTP-Import {#concept_2F965BE873254546A61FB755F25299FD}

In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

Die folgenden empfohlenen Grenzwerte sind wichtig:

* Viele kleine Dateien werden langsamer verarbeitet als einige große Dateien. Dies ist auf die Warteschlange und Priorisierung zurückzuführen, die für die kleineren Aufträge erforderlich sind.
* Bitte brechen Sie große Dateien in 50-MB-Pakete auf. Dies ist nicht erforderlich, wird aber empfohlen, da es eine bessere Sichtbarkeit des Fortschritts am Back-End ermöglicht. Wenn außerdem während der Verarbeitung Ihres Auftrags Fehler auftreten, wird der Auftrag neu gestartet. große Dateien führen in diesem Szenario zu einer großen Menge an Arbeit.

Beim ersten Setup wird die Classification-Datenbank mit einem großen Satz Originaldaten gefüllt oder die Classifications werden neu strukturiert, anstatt nur wenige Zeilen neu zu klassifizieren oder Zeilen hinzuzufügen.

Nach einem ersten Upload in eine Report Suite (für eine bestimmte Variable oder einen Bericht) empfiehlt Adobe, bei nachfolgenden Importen nur neue und aktualisierte Zeilen hochzuladen. Zeilen, die nicht geändert werden, sollten bei zukünftigen Uploads weggelassen werden.

Jeder neue Schlüsselwert, den Sie hochladen, zählt mit Ihren individuellen Werten für diese Variable für den Monat.

Wenn Sie Ihre individuellen Werte für den Monat überschritten haben, werden Ihnen die entsprechenden Classification-Daten für die über dem Grenzwert liegenden Classifications in Berichte nicht angezeigt. Sie können diese Klassifizierungen entweder in Data Warehouse oder in Ad-hoc-Analysen anzeigen.

>[!NOTE] Die erforderliche Verarbeitungszeit für eine Klassifizierungsdatendatei hängt von der Dateigröße und der aktuellen Anzahl der Dateien ab, die zu dem Zeitpunkt auf den Adobe-Servern verarbeitet werden. Die Verarbeitung von Datendateien dauert in der Regel nicht länger als 72 Stunden.

Erstellen Sie vor dem Hochladen von Daten via FTP ein FTP-Konto. Weitere Informationen finden Sie unter [Erstellen eines FTP-Kontos](/help/components/c-classifications2/c-classifications-importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF).

## Importieren von Classifications über FTP {#task_132C36830B69418B8C929E39838EF01D}

<!-- 

t_upload_a_saint_data_file_via_ftp.xml

 -->

In diesen Schritten wird beschrieben, wie Sie Classifications mithilfe eines FTP-Kontos in Adobe Analytics importieren.

Weitere Informationen zum Erstellen eines FTP-Kontos finden Sie unter  [Erstellen Sie ein FTP-Konto](/help/components/c-classifications2/c-classifications-importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF).

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Import File]** und dann auf **[!UICONTROL FTP Import]**.
1. Next to the FTP account that you want to use, click **[!UICONTROL View]**.
1. Verwenden Sie die FTP-Zugriffsinformationen (Host, Benutzername, Kennwort), um mit einem FTP-Client Ihrer Wahl auf den FTP-Server zuzugreifen.
1. Laden Sie die Datendatei ([!DNL .tab] oder [!DNL .txt]) auf den FTP-Server hoch.
1. Laden Sie nach dem Hochladen der Datendatei eine FIN-Datei hoch, die anzeigt, dass die Datei zur Verarbeitung bereit ist.

   Die FIN-Datei ist eine leere Datei mit demselben Namen wie Ihre Datendatei, nur mit der Dateierweiterung [!DNL .fin]. Wenn Ihre Datendatei also [!DNL classdata1.tab] heißt, lautet der Name der FIN-Datei [!DNL classdata1.fin].

Adobe ruft in regelmäßigen Abständen hochgeladene Datendateien mit zugewiesener FIN-Datei ab. Adobe importiert sie in die Report Suites und Datensätze, die in der Konfiguration des FTP-Kontos angegeben sind.

## Erstellen Sie ein FTP-Konto {#task_C019268E6C934C7C95F4326F42A22CCF}

Erstellen Sie vor dem Hochladen von Daten via FTP ein FTP-Konto. >

<!-- 

t_create_an_ftp_account.xml

 -->

Weitere Details zu Adobe FTP-Servern finden Sie unter [FTP und sFTP](https://marketing.adobe.com/resources/help/de_DE/whitepapers/ftp/).

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Import File]** und dann auf **[!UICONTROL FTP Import]**.
1. Klicken Sie auf der **[!UICONTROL Import File]** Registerkarte auf **[!UICONTROL Add New]**.
1. Geben Sie die Details zum FTP-Konto an:

   | Element | Beschreibung |
   |---|---|
   | Name | Der Name des FTP-Kontos. |
   | Zu klassifizierender Datensatz | Wählen Sie in der Dropdown-Liste den Datensatz (Marketing-Berichtsvariable) aus, den Sie klassifizieren möchten. |
   | Report Suites auswählen | Wählen Sie die Report Suites aus, in denen Sie den ausgewählten Datensatz klassifizieren möchten. Zur Auswahl mehrerer Report Suites müssen die Classifications für jede der ausgewählten Report Suites identisch sein. |
   | Daten bei Konflikten überschreiben | Wählen Sie diese Option, um Duplikat-Daten zu überschreiben. Diese Option ist nützlich, wenn Sie vorhandene Classifications aktualisieren. Wenn Sie zusätzliche Classifications hinzufügen, wird diese Option nicht empfohlen. |
   | Nach Abschluss des Imports | Wählen Sie diese Option, um den aktualisierten Datensatz automatisch in dasselbe FTP-Konto zu exportieren, sobald der Import abgeschlossen ist. Geben Sie die E-Mail-Adresse an, an die Benachrichtigungen über dieses FTP-Konto gesendet werden sollen. |
   | Benachrichtigungsempfänger | Geben Sie die E-Mail-Adresse an, an die Benachrichtigungen über dieses FTP-Konto gesendet werden sollen. |
   | Autorisieren | (Erforderlich) Autorisiert Adobe zum automatischen Importieren aller an das neue FTP-Konto gesendeten Datendateien. |

1. Klicken Sie auf **[!UICONTROL Save]**.

Nach dem Erstellen können Sie FTP-Konten bearbeiten oder löschen, indem Sie auf den entsprechenden Link neben dem gewünschten FTP-Konto klicken.
