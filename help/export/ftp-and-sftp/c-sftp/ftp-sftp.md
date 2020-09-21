---
description: SFTP ist ein sicheres Protokoll für die Übertragung von Daten, mit dem sichergestellt wird, dass außer Ihnen niemand Ihre Daten sehen kann. Für Adobe Engineering Services kann ein SFTP-Konto eingerichtet werden, in dem Ihre Daten sicher sind.
keywords: ftp;sftp
title: Secure File Transfer Protocol – Übersicht
uuid: 7dd1a867-e828-4c7b-bf11-75a81d4c149c
translation-type: ht
source-git-commit: 322e2e87ab532d5e8a864dc06613a9b275c71df5
workflow-type: ht
source-wordcount: '235'
ht-degree: 100%

---


# Secure File Transfer Protocol – Übersicht

SFTP ist ein sicheres Protokoll für die Übertragung von Daten, mit dem sichergestellt wird, dass außer Ihnen niemand Ihre Daten sehen kann. Für Adobe Engineering Services kann ein SFTP-Konto eingerichtet werden, in dem Ihre Daten sicher sind.

## Push-Auslieferung {#section_A47831BB1DCA490BB57F0940617AA506}

Hierbei übertragen die Server von Adobe die Datei per Push auf Ihre Server. Faktisch wird sie an Ihren Endpunkt geliefert.

[Data Warehouse](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) - und [Analytics-Daten-Feed](https://docs.adobe.com/content/help/de-DE/analytics/export/analytics-data-feed/data-feed-overview.html) können Daten per SFTP übertragen.

Folgende Analytics-Werkzeuge können **keine** Daten per Push über SFTP zustellen:

* Reports &amp; Analytics
* Ad Hoc Analysis
* Report Builder

## Pull-Auslieferung {#section_FA29FAEF02FE40B8B32452146A036F48}

Hierbei wird die Datei über normales FTP an einen der Server von Adobe gesendet. Wenn Sie die Datei auf Ihrem Server haben möchten, müssen Sie sie über Ihren Server per SFTP vom Adobe FTP-Server abrufen. Hierzu sind drei Methoden verfügbar:

* [Verbindung zu Adobe über SFTP ohne Kennwort herstellen.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* Sie können beliebige Berichte per Push an FTP-basierte Adobe Daten-Feeds/Reports &amp; Analytics/Ad Hoc usw. übertragen und dann abrufen. Adobe kann diese Berichte nicht an den von Ihnen eingerichteten SFTP-Server ausliefern.

