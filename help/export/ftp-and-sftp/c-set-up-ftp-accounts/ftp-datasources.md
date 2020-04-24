---
description: Sie können Analytics nutzen, um FTP-basierte Data Sources zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in die Experience Cloud zu importieren.
keywords: ftp;sftp
title: Data Sources
uuid: 41ba2de7-d33d-4394-b7d8-04a116f45419
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Data Sources

Sie können Analytics nutzen, um FTP-basierte Data Sources zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in die Experience Cloud zu importieren.

Nach der Erstellung der Data Sources-Instanz stellt das Tool einen FTP-Speicherort bereit, den Sie zum Hochladen von Data Sources-Dateien verwenden können. Data Sources erkennt und verarbeitet die Dateien nach dem Hochladen automatisch. Nach der Verarbeitung der Dateien stehen die Daten für Analytics-Berichte zur Verfügung.

The [!UICONTROL Create] tab in the Data Sources Manager lets you configure a new Data Sources instance for the selected report suite. The [!UICONTROL Data Sources Wizard] guides you through the process of creating a Data Sources template, and creates an FTP location for uploading data.

In the [!UICONTROL Manage Data Sources] window, find your data source and select the FTP Info link. Ihre FTP-Anmeldeinformationen werden im [!UICONTROL Activate a Data Source] Fenster im [!UICONTROL Upload/FTP Information] Abschnitt angezeigt.

Informationen zu FTP-Beschränkungen und zur Datenaufbewahrung finden Sie unter [FTP-Beschränkungen und Datenaufbewahrung](/help/export/ftp-and-sftp/ftp-limits.md).

## Informationen zur FIN-Datei für Uploads für Classifications und Data Sources {#section_1484719F8A134EAE91212DBD8F15174F}

When you upload a classifications or [!UICONTROL Data Source] file ( [!DNL .tab] or [!DNL .txt]) the upload also requires that you upload an empty file with the exact same name as the data file being imported, but with a [!DNL .fin] extension. Diese [!DNL .fin]-Datei ist eine Finish-Datei. Sie dient dazu, dem System mitzuteilen, dass die Datendatei vollständig in das FTP-Konto hochgeladen wurde. Über die [!DNL .fin]-Datei erkennt Adobe, dass Sie mit Ihrem Import fertig sind. Nachdem Sie diese Datei übermittelt haben, entfernt Adobe beide Dateien aus dem FTP-Konto und startet den Importprozess.
Importdatei: [!DNL Classifications.tab]

Finish-Datei: [!DNL Classifications.fin]

Wenn Sie Ihre Data-Sources- oder SAINT-Datei ohne zugehörige [!DNL .fin]-Datei hochladen, fügt Adobe Ihre Datei nicht zur Verarbeitungswarteschlange hinzu. Die Datei bleibt im FTP-Konto und wird nicht auf Ihre Daten in der [!UICONTROL Experience Cloud] angewendet. You are notified of this only if you have entered your email address as the [!UICONTROL Notification Recipient] in the [!UICONTROL Create FTP Account] window of reporting. Wenn hier keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.

Wenn Sie Ihre Datei zusammen mit einer [!DNL .fin]-Datei hochgeladen haben, die Datei jedoch fehlerhaft ist, wird sie zur Verarbeitung gesendet. Der Fehler sorgt dann dafür, dass die Verarbeitung abgebrochen und die Datei an einen Fehlerordner gesendet wird. If this occurs, a notification is sent to the email address listed in the [!UICONTROL Notification Recipient] field in the [!UICONTROL Create FTP Account] window. Wenn keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.
