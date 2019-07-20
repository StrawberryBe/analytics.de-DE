---
description: In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.
seo-description: In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.
seo-title: FTP-Import
solution: Analytics
subtopic: Classifications
title: FTP-Import
topic: Admin Tools
uuid: a 914970 d-ba 02-4111-9 dcf -06448 f 71 b 9 f 3
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# FTP-Import

In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.

## FTP import {#concept_2F965BE873254546A61FB755F25299FD}

In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.

**[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.

Beachten Sie bitte die folgenden Empfehlungswerte:

* Viele kleine Dateien werden langsamer verarbeitet als wenige große. Dies hängt mit der Warteschlangenlänge und der erforderlichen Priorisierung für kleine Aufgaben zusammen.
* Teilen Sie die Dateien in 50-MB-Pakete auf. Dies ist nicht erforderlich, wird aber für eine verbesserte Fortschrittssichtbarkeit am Prozessende empfohlen. Treten bei der Aufgabenverarbeitung Fehler auf, wird die Aufgabe neu gestartet. Bei großen Dateien muss in diesem Fall viel Aufwand investiert werden.

Bei der anfänglichen Einrichtung wird die Classification-Datenbank mit einer großen Menge an Originaldaten gefüllt oder die Classifications werden neu strukturiert; es werden also nicht nur einige wenige Reihen neu klassifiziert oder hinzugefügt.

Adobe empfiehlt, nach einem ersten Upload in eine Report Suite (für eine gegebene Variable oder einen Bericht) in den darauffolgenden Importen nur neue und aktualisierte Zeilen zu importieren. Zeilen, die nicht geändert werden, sollten bei zukünftigen Uploads ausgeklammert werden.

Jeder neue Schlüsselwert, den Sie hochladen, zählt als eindeutige Classification der entsprechenden Variable für den Monat.

Wenn Sie die Zahl eindeutiger Classifications für den Monat überschritten haben, werden Ihnen für die über dem Grenzwert liegenden Classifications in den Berichten nicht die zugehörigen Classification-Daten angezeigt. Sie können sich diese Classifications entweder in Data Warehouse oder der Ad-hoc-Analyse anzeigen lassen.

>[!NOTE]
>
>Die erforderliche Verarbeitungszeit für eine Classification-Datendatei hängt von der Dateigröße und der aktuellen Anzahl der Dateien ab, die bereits von den Adobe-Servern verarbeitet werden. Die Verarbeitung von Datendateien nimmt in der Regel nicht mehr als 72 Stunden in Anspruch.

Erstellen Sie vor dem Hochladen von Daten via FTP ein FTP-Konto. Weitere Informationen finden Sie unter [Erstellen Sie ein FTP-Konto](../../../components/c-classifications2/c-classifications-importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF).

## Importieren von Classifications über FTP {#task_132C36830B69418B8C929E39838EF01D}

<!-- 

t_upload_a_saint_data_file_via_ftp.xml

 -->

In diesen Schritten wird beschrieben, wie Sie Classifications mithilfe eines FTP-Kontos in Adobe Analytics importieren.

Weitere Informationen zum Erstellen eines FTP-Kontos finden Sie unter [Erstellen Sie ein FTP-Konto](../../../components/c-classifications2/c-classifications-importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF).

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Click **[!UICONTROL Import File]**, then click **[!UICONTROL FTP Import]**.
1. Next to the FTP account that you want to use, click **[!UICONTROL View]**.
1. Verwenden Sie die FTP-Zugriffsinformationen (Host, Benutzername, Kennwort), um mit einem FTP-Client Ihrer Wahl auf den FTP-Server zuzugreifen.
1. Upload the data file ( [!DNL .tab] or [!DNL .txt]) to the FTP server.
1. Laden Sie nach dem Hochladen der Datendatei eine FIN-Datei hoch, die anzeigt, dass die Datei zur Verarbeitung bereit ist.

   The FIN file is an empty file that has the same name as your data file, with a [!DNL .fin] filename extension. For example, if your data file is [!DNL classdata1.tab], the FIN filename is [!DNL classdata1.fin].

Adobe ruft in regelmäßigen Abständen die hochgeladenen Datendateien mit zugewiesener FIN-Datei ab. Diese werden dann von Adobe in die Report Suites und Datensätze importiert, die bei der Konfiguration des FTP-Kontos angegeben wurden.

## Erstellen Sie ein FTP-Konto {#task_C019268E6C934C7C95F4326F42A22CCF}

Erstellen Sie vor dem Hochladen von Daten via FTP ein FTP-Konto. &gt;

<!-- 

t_create_an_ftp_account.xml

 -->

Weitere Details zu Adobe FTP-Servern finden Sie unter [FTP und sFTP](https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/).

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Click **[!UICONTROL Import File]**, then click **[!UICONTROL FTP Import]**.
1. Klicken Sie auf der Registerkarte **Datei importieren** auf **[!UICONTROL Neu hinzufügen]**.
1. Geben Sie die Details zum FTP-Konto an:

   | Element | Beschreibung |
   |---|---|
   | Name | Der Name des FTP-Kontos. |
   | Datensatz, der klassifiziert werden soll | Wählen Sie in der Dropdown-Liste den zu klassifizierenden Datensatz (Marketing-Berichtsvariable) aus. |
   | Report Suites auswählen | Wählen Sie die Report Suites aus, in denen Sie den ausgewählten Datensatz klassifizieren möchten. Zur Auswahl mehrerer Report Suites müssen die Classifications für jede ausgewählte Report Suite identisch sein. |
   | Daten bei Konflikten überschreiben | Mit dieser Option werden doppelte Daten überschrieben. Diese Option ist hilfreich, wenn Sie bestehende Classifications aktualisieren. Wenn Sie zusätzliche Classifications hinzufügen, wird diese Option nicht empfohlen. |
   | Nach Abschluss des Imports | Mit dieser Option wird der aktualisierte Datensatz automatisch auf dasselbe FTP-Konto hochgeladen, sobald der Importvorgang abgeschlossen ist. |
   | Benachrichtigungsempfänger | Geben Sie die E-Mail-Adresse an, an die Benachrichtigungen zu diesem FTP-Konto gesendet werden sollen. |
   | Genehmigung | (Erforderlich) Berechtigt Adobe zum automatischen Importieren aller an das neue FTP-Konto gesendeten Datendateien. |

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Nach dem Erstellen können Sie FTP-Konten bearbeiten oder löschen, indem Sie auf den entsprechenden Link neben dem gewünschten FTP-Konto klicken.
