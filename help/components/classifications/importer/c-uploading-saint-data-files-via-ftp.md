---
description: In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.
subtopic: Classifications
title: FTP-Import
topic: Admin tools
uuid: a914970d-ba02-4111-9dcf-06448f71b9f3
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 96%

---


# FTP-Import

In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.

## FTP-Import {#concept_2F965BE873254546A61FB755F25299FD}

In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**

Beachten Sie bitte die folgenden Empfehlungswerte:

* Viele kleine Dateien werden langsamer verarbeitet als wenige große. Dies hängt mit der Warteschlangenlänge und der erforderlichen Priorisierung für kleine Aufgaben zusammen.
* Teilen Sie die Dateien in 50-MB-Pakete auf. Dies ist nicht erforderlich, wird aber für eine verbesserte Fortschrittssichtbarkeit am Prozessende empfohlen. Treten bei der Aufgabenverarbeitung Fehler auf, wird die Aufgabe neu gestartet. Bei großen Dateien muss in diesem Fall viel Aufwand investiert werden.

Bei der anfänglichen Einrichtung wird die Classification-Datenbank mit einer großen Menge an Originaldaten gefüllt oder die Classifications werden neu strukturiert; es werden also nicht nur einige wenige Reihen neu klassifiziert oder hinzugefügt.

Adobe empfiehlt, nach einem ersten Upload in eine Report Suite (für eine gegebene Variable oder einen Bericht) in den darauffolgenden Importen nur neue und aktualisierte Zeilen zu importieren. Zeilen, die nicht geändert werden, sollten bei zukünftigen Uploads ausgeklammert werden.

Jeder neue Schlüsselwert, den Sie hochladen, zählt als eindeutige Classification der entsprechenden Variable für den Monat.

Wenn Sie die Zahl eindeutiger Classifications für den Monat überschritten haben, werden Ihnen für die über dem Grenzwert liegenden Classifications in den Berichten nicht die zugehörigen Classification-Daten angezeigt. Sie können sich diese Classifications entweder in Data Warehouse oder der Ad-hoc-Analyse anzeigen lassen.

>[!NOTE]
>
>Die erforderliche Verarbeitungszeit für eine Klassifizierungsdatendatei hängt von der Dateigröße und der aktuellen Anzahl der Dateien ab, die zu dem Zeitpunkt auf den Adobe-Servern verarbeitet werden. Die Verarbeitung von Datendateien nimmt in der Regel nicht mehr als 72 Stunden in Anspruch.

Erstellen Sie vor dem Hochladen von Daten via FTP ein FTP-Konto. Weitere Informationen finden Sie unter [Erstellen eines FTP-Kontos](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF).

## Importieren von Classifications über FTP {#task_132C36830B69418B8C929E39838EF01D}

<!-- 

t_upload_a_saint_data_file_via_ftp.xml

 -->

In diesen Schritten wird beschrieben, wie Sie Classifications mithilfe eines FTP-Kontos in Adobe Analytics importieren.

Weitere Informationen zum Erstellen eines FTP-Kontos finden Sie unter [Erstellen Sie ein FTP-Konto](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF).

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]** und dann auf **[!UICONTROL FTP-Import]**.
1. Klicken Sie neben dem FTP-Konto, das Sie verwenden möchten, auf **[!UICONTROL Ansicht]**.
1. Verwenden Sie die FTP-Zugriffsinformationen (Host, Benutzername, Kennwort), um mit einem FTP-Client Ihrer Wahl auf den FTP-Server zuzugreifen.
1. Laden Sie die Datendatei ([!DNL .tab] oder [!DNL .txt]) auf den FTP-Server hoch.
1. Laden Sie nach dem Hochladen der Datendatei eine FIN-Datei hoch, die anzeigt, dass die Datei zur Verarbeitung bereit ist.

   Die FIN-Datei ist eine leere Datei mit demselben Namen wie Ihre Datendatei, nur mit der Dateierweiterung [!DNL .fin]. Wenn Ihre Datendatei also [!DNL classdata1.tab] heißt, lautet der Name der FIN-Datei [!DNL classdata1.fin].

Adobe ruft in regelmäßigen Abständen die hochgeladenen Datendateien mit zugewiesener FIN-Datei ab. Diese werden dann von Adobe in die Report Suites und Datensätze importiert, die bei der Konfiguration des FTP-Kontos angegeben wurden.

## Erstellen Sie ein FTP-Konto {#task_C019268E6C934C7C95F4326F42A22CCF}

Erstellen Sie vor dem Hochladen von Daten via FTP ein FTP-Konto. >

<!-- 

t_create_an_ftp_account.xml

 -->

Weitere Details zu Adobe FTP-Servern finden Sie unter [FTP und sFTP](https://docs.adobe.com/content/help/de-DE/analytics/export/ftp-and-sftp/ftp-overview.html).

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]** und dann auf **[!UICONTROL FTP-Import]**.
1. Klicken Sie auf der Registerkarte **[!UICONTROL Datei importieren]** auf **[!UICONTROL Neu hinzufügen]**.
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

>[!NOTE]
>
>Benachrichtigungen werden nicht gesendet, wenn bei einem Import keine Änderungen an einer Klassifizierung vorgenommen werden. Eine E-Mail wird nur gesendet, wenn sie erfolgreich ist und Änderungen an einer Classification zur Folge hat.
