---
description: Diese Schritte beschreiben, wie Sie eine Datenquellen-Datei hochladen.
subtopic: Data sources
title: Data Sources-Datei hochladen
topic: Developer and implementation
uuid: 5a9dde91-1297-47e5-9393-611b40413c17
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '266'
ht-degree: 100%

---


# Data Sources-Datei hochladen

Diese Schritte beschreiben, wie Sie eine Datenquellen-Datei hochladen.

Nachdem Sie eine Data Sources-Datendatei vorbereitet haben, geben Sie sie zur Verarbeitung an Data Sources weiter. Adobe unterhält mehrere Data Sources-FTP-Server, auf die Sie Data Sources-Dateien hochladen können. Beachten Sie Folgendes über die Data Sources-FTP-Server:

* Wählen Sie auf der Registerkarte [!UICONTROL Data Sources-Manager] neben dem Datenquelleneintrag die Option „FTP-Info“ aus, um den FTP-Host sowie Anmelde- und Kennwortinformationen für das FTP-Konto der Datenquelle anzuzeigen. Jeder mit Zugriff auf diese Informationen kann Daten in Ihre Report Suite hochladen.
* Aus Sicherheitsgründen werden FTP-Konten nach 30 Tagen Inaktivität geschlossen.
* FTP-Konten sind Datenquellen-spezifisch. Sie können nicht ein FTP-Konto zum Hochladen von Data Sources-Dateien in mehrere Datenquellen verwenden.

**So laden Sie eine Datenquellen-Datei hoch**

1. Verwenden Sie einen FTP-Client, um die Daten an Ihre Data Sources-FTP-Site zu senden.

   (Verfügbar im Data Sources-Manager unter dem Link „FTP-Info“).

1. Laden Sie eine [!DNL .fin]-Datei hoch, um Adobe darüber zu informieren, dass der Data Sources-Datei-Upload abgeschlossen ist.

   Die [!DNL .fin]-Datei muss genau den gleichen Namen aufweisen wie die Data Sources-Datei, mit Ausnahme der Dateierweiterung. Adobe stellt die Data Sources-Datei nicht für die Verarbeitung in eine Warteschlange, bis Sie die [!DNL .fin]-Datei hochgeladen haben.

   Laden Sie die Datei erst hoch, wenn alle Data Sources-Dateien vollständig hochgeladen wurden. Anderenfalls könnte Data Sources versuchen, eine unvollständige Datei zu verarbeiten.
1. Achten Sie darauf, ob bei der Verarbeitung der Data Sources-Datei Meldungen ausgegeben werden.

   Im Data Sources-Manager werden Fehler angezeigt, die u. U. während der Dateiverarbeitung auftreten.

