---
description: SFTP ist ein sicheres Protokoll zur Datenübertragung, das sicherstellt, dass niemand Ihre Daten sehen kann, außer Sie. Adobe Engineering Services kann ein SFTP-Konto einrichten, um Ihre Daten sicher zu speichern.
keywords: ftp;sftp
title: Secure File Transfer Protocol – Übersicht
uuid: 7dd1a867-e828-4c7b-bf11-75a81d4c149c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Secure File Transfer Protocol – Übersicht

SFTP ist ein sicheres Protokoll zur Datenübertragung, das sicherstellt, dass niemand Ihre Daten sehen kann, außer Sie. Adobe Engineering Services kann ein SFTP-Konto einrichten, um Ihre Daten sicher zu speichern.

## Push-Auslieferung {#section_A47831BB1DCA490BB57F0940617AA506}

Hierbei übertragen die Server von Adobe die Datei per Push auf Ihre Server. Faktisch wird sie an Ihren Endpunkt geliefert.

[Data Warehouse](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) - und [Analytics-Data Feed](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html) können Daten per SFTP übertragen.

The following Analytics tools **cannot** push data via SFTP:

* Reports &amp; Analytics
* Ad Hoc Analysis
* ReportBuilder

## Pull-Auslieferung {#section_FA29FAEF02FE40B8B32452146A036F48}

Hierbei wird die Datei über normales FTP an einen der Server von Adobe gesendet. Wenn Sie die Datei auf Ihrem Server haben möchten, müssen Sie sie mithilfe von SFTP vom Server zum Adobe FTP-Server abrufen. Hierzu sind drei Methoden verfügbar:

* [Verbindung zu Adobe über SFTP ohne Kennwort herstellen.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [Stellen Sie eine Verbindung zu einem Adobe FTP-Konto mit SFTP her.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* Sie können beliebige Berichte per Push an FTP-artige Adobe Data Feeds/Reports und Analysen/Ad Hoc usw. übertragen und dann abrufen. Adobe kann diese Berichte nicht an den von Ihnen eingerichteten SFTP-Server übermitteln.

