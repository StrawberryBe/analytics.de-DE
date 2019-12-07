---
description: Die FTP-Option für Classifications (SAINT) bietet mehr Flexibilität beim Hochladen großer Classification-Datensätze. So können u. a. auch Daten in mehrere Report Suites und Datensätze mit mehr als 50.000 Zeilen hochgeladen werden.
keywords: ftp;sftp
title: Klassifizierungen
uuid: 35936c98-b785-43eb-89f4-ab42a10db256
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Klassifizierungen

Die FTP-Option für Classifications bietet mehr Flexibilität beim Hochladen großer Classification-Datensätze, einschließlich der Möglichkeit, Daten in mehrere Report Suites hochzuladen und Datensätze mit mehr als 50.000 Zeilen hochzuladen.

Unter [Classifications](https://marketing.adobe.com/resources/help/en_US/reference/c_working_with_saint.html) finden Sie Schritte für das Herunterladen von Classification-Daten über FTP und das Hochladen von Datendateien über FTP (einschließlich der für das Erstellen eines FTP-Kontos erforderlichen Schritte).

Wie lange das System für das Importieren dieser Dateien benötigt, hängt von verschiedenen Faktoren ab. Wenn eine hochgeladene Datei nach 6 Stunden immer noch auf dem FTP-Server vorhanden ist, wenden Sie sich an einen unterstützten Benutzer Ihrer Organisation, damit er Kontakt mit der Adobe-Kundenunterstützung aufnimmt.

Bei einem erfolgreichen Import erscheinen die entsprechenden Änderungen sofort in einem Export, während die Datenänderungen in Analytics bei einem Browserimport bis zu 4 Stunden und bei einem FTP-Import bis zu 24 Stunden später erscheinen können.

Informationen zu FTP-Beschränkungen und zur Datenaufbewahrung finden Sie unter [FTP-Beschränkungen und Datenaufbewahrung](/help/export/ftp-and-sftp/ftp-limits.md)

## Informationen zur FIN-Datei für Uploads für Classifications und Data Sources {#section_1484719F8A134EAE91212DBD8F15174F}

When you upload a classification or [!UICONTROL Data Source] file ( [!DNL .tab]or [!DNL .txt]) the upload also requires that you upload an empty file with the exact same name as the data file being imported, but with a [!DNL .fin] extension. This [!DNL .fin] file is a finish file. Sie dient dazu, dem System mitzuteilen, dass die Datendatei vollständig in das FTP-Konto hochgeladen wurde. The [!DNL .fin] file lets Adobe recognize that you are done with your import. Nachdem Sie diese Datei übermittelt haben, entfernt Adobe beide Dateien aus dem FTP-Konto und startet den Importprozess.
Datei importieren: [!DNL Classifications.tab]

Datei beenden: [!DNL Classifications.fin]

If you upload your Data Sources or classification file without an accompanying [!DNL .fin] file, Adobe does not add it to the queue for processing. The file remains on the FTP, and is not applied to your data in the [!UICONTROL Experience Cloud]. Sie werden hierüber nur dann benachrichtigt, wenn Sie Ihre E-Mail-Adresse als [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] von Analytics angegeben haben. Wenn hier keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.

If you do upload your file with a [!DNL .fin] file, but there is an error in the file, it is submitted for processing, but the error causes the processing to cease and the file to be sent to an error folder. In diesem Fall wird eine Benachrichtigung an die im Feld [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] angegebene E-Mail-Adresse gesendet. Wenn keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.
