---
description: Diese Schritte beschreiben, wie Sie eine Datenquellen-Datei hochladen.
seo-description: Diese Schritte beschreiben, wie Sie eine Datenquellen-Datei hochladen.
seo-title: Hochladen einer Datenquellen-Datei
solution: Analytics
subtopic: Datenquellen
title: Hochladen einer Datenquellen-Datei
topic: Entwickler und Implementierung
uuid: 5 a 9 dde 91-1297-47 e 5-9393-611 b 40413 c 17
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Hochladen einer Datenquellen-Datei

Diese Schritte beschreiben, wie Sie eine Datenquellen-Datei hochladen.

Nachdem Sie eine Data Sources-Datendatei vorbereitet haben, geben Sie sie zur Verarbeitung an Data Sources weiter. Adobe unterhält mehrere Data Sources-FTP-Server, auf die Sie Data Sources-Dateien hochladen können. Beachten Sie Folgendes über die Data Sources-FTP-Server:

* Wählen Sie auf der Registerkarte [!UICONTROL „Data Sources-Manager“] neben dem Datenquelleneintrag die Option „FTP-Info“ aus, um den FTP-Host sowie Anmelde- und Kennwortinformationen für das FTP-Konto der Datenquelle anzuzeigen. Jeder mit Zugriff auf diese Informationen kann Daten in Ihre Report Suite hochladen.
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

