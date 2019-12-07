---
description: Diese Schritte beschreiben, wie Sie eine Datenquellen-Datei hochladen.
subtopic: Data sources
title: Datenquellen-Datei hochladen
topic: Developer and implementation
uuid: 5a9dde91-1297-47e5-9393-611b40413c17
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Datenquellen-Datei hochladen

Diese Schritte beschreiben, wie Sie eine Datenquellen-Datei hochladen.

Nachdem Sie eine Data Sources-Datendatei vorbereitet haben, geben Sie sie zur Verarbeitung an Data Sources weiter. Adobe unterhält mehrere Data Sources-FTP-Server, auf die Sie Data Sources-Dateien hochladen können. Beachten Sie Folgendes über die Data Sources-FTP-Server:

* Select FTP Info next to the Data Source entry in the [!UICONTROL Data Sources Manage] tab to see the FTP Host, Login, and Password information for the data source's FTP account. Jeder mit Zugriff auf diese Informationen kann Daten in Ihre Report Suite hochladen.
* Aus Sicherheitsgründen werden FTP-Konten nach 30 Tagen Inaktivität geschlossen.
* FTP-Konten sind Datenquellen-spezifisch. Sie können nicht ein FTP-Konto zum Hochladen von Data Sources-Dateien in mehrere Datenquellen verwenden.

**So laden Sie eine Datenquellen-Datei hoch**

1. Verwenden Sie einen FTP-Client, um die Daten an Ihre Data Sources-FTP-Site zu senden.

   (Verfügbar im Data Sources-Manager unter dem Link „FTP-Info“).

1. Upload a [!DNL .fin] file to notify Adobe that the Data Sources file upload is complete.

   The [!DNL .fin] file must have the exact same name as the Data Sources file, except for the file extension. Adobe does not queue the Data Sources file for processing until you upload the [!DNL .fin] file.

   Laden Sie die Datei erst hoch, wenn alle Data Sources-Dateien vollständig hochgeladen wurden. Anderenfalls könnte Data Sources versuchen, eine unvollständige Datei zu verarbeiten.
1. Achten Sie darauf, ob bei der Verarbeitung der Data Sources-Datei Meldungen ausgegeben werden.

   Im Data Sources-Manager werden Fehler angezeigt, die u. U. während der Dateiverarbeitung auftreten.

