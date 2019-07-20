---
description: Sie können Analytics nutzen, um FTP-basierte Data Sources zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in die Experience Cloud zu importieren.
keywords: ftp; sftp
seo-description: Sie können Analytics nutzen, um FTP-basierte Data Sources zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in die Experience Cloud zu importieren.
seo-title: Data Sources
solution: Analytics
title: Data Sources
uuid: 41 ba 2 de 7-d 33 d -4394-b 7 d 8-04 a 116 f 45419
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Data Sources

Sie können Analytics nutzen, um FTP-basierte Data Sources zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in die Experience Cloud zu importieren.

Nach der Erstellung der Data Sources-Instanz stellt das Tool einen FTP-Speicherort bereit, den Sie zum Hochladen von Data Sources-Dateien verwenden können. Data Sources erkennt und verarbeitet die Dateien nach dem Hochladen automatisch. Nach der Verarbeitung der Dateien stehen die Daten für Analytics-Berichte zur Verfügung.

Auf dem Register [!UICONTROL Erstellen] können Sie im Data Sources Manager eine neue Data Sources-Instanz für die ausgewählte Report Suite konfigurieren. Der [!UICONTROL Data Sources-Assistent] führt Sie durch den Erstellungsvorgang einer Data Sources-Vorlage und legt einen FTP-Speicherort zum Hochladen der Daten an.

Suchen Sie im Fenster [!UICONTROL Data Sources verwalten] nach Ihrer Datenquelle und wählen Sie den Link zu den FTP-Informationen aus. Ihre FTP-Anmeldedaten werden im Fenster [!UICONTROL Eine Datenquelle aktivieren] im Abschnitt [!UICONTROL Hochladen/FTP-Info] angezeigt.

Informationen zu FTP-Beschränkungen und zur Datenaufbewahrung finden Sie unter [FTP-Beschränkungen und Datenaufbewahrung](../../../export/ftp-and-sftp/ftp-limits.md#concept_8CAA1D8F27B3411AB902520AD6C9A70E)

## Informationen zur FIN-Datei für Uploads für Classifications und Data Sources {#section_1484719F8A134EAE91212DBD8F15174F}

When you upload a classifications or [!UICONTROL Data Source] file ( [!DNL .tab] or [!DNL .txt]) the upload also requires that you upload an empty file with the exact same name as the data file being imported, but with a [!DNL .fin] extension. This [!DNL .fin] file is a finish file. Sie dient dazu, dem System mitzuteilen, dass die Datendatei vollständig in das FTP-Konto hochgeladen wurde. The [!DNL .fin] file lets Adobe recognize that you are done with your import. Nachdem Sie diese Datei übermittelt haben, entfernt Adobe beide Dateien aus dem FTP-Konto und startet den Importprozess.
Datei importieren: [!DNL Classifications.tab]

Finish File: [!DNL Classifications.fin]

If you upload your Data Sources or SAINT file without an accompanying [!DNL .fin] file, Adobe does not add it to the queue for processing. The file remains on the FTP, and is not applied to your data in the [!UICONTROL Experience Cloud]. Sie werden hierüber nur dann benachrichtigt, wenn Sie Ihre E-Mail-Adresse als [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] der Berichterstellung angegeben haben. Wenn hier keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.

If you do upload your file with a [!DNL .fin] file, but there is an error in the file, it is submitted for processing, but the error causes the processing to cease and the file to be sent to an error folder. In diesem Fall wird eine Benachrichtigung an die im Feld [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] angegebene E-Mail-Adresse gesendet. Wenn keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.
