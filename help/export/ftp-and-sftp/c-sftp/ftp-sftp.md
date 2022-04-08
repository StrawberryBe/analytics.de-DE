---
description: SFTP ist ein sicheres Protokoll für die Übertragung von Daten, mit dem sichergestellt wird, dass außer Ihnen niemand Ihre Daten sehen kann. Für Adobe Engineering Services kann ein SFTP-Konto eingerichtet werden, in dem Ihre Daten sicher sind.
keywords: ftp;sftp
title: Secure File Transfer Protocol – Übersicht
feature: FTP Export
exl-id: ea0448f9-1685-4a8f-b2f9-49d315c6ab71
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: ht
source-wordcount: '235'
ht-degree: 100%

---

# Secure File Transfer Protocol – Übersicht

SFTP ist ein sicheres Protokoll für die Übertragung von Daten, mit dem sichergestellt wird, dass außer Ihnen niemand Ihre Daten sehen kann. Für Adobe Engineering Services kann ein SFTP-Konto eingerichtet werden, in dem Ihre Daten sicher sind.

## Push-Auslieferung {#section_A47831BB1DCA490BB57F0940617AA506}

Hierbei übertragen die Server von Adobe die Datei per Push auf Ihre Server. Faktisch wird sie an Ihren Endpunkt geliefert.

[Data Warehouse](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) - und [Analytics-Daten-Feed](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=de) können Daten per SFTP übertragen.

Folgende Analytics-Werkzeuge können **keine** Daten per Push über SFTP zustellen:

* Reports &amp; Analytics
* Ad Hoc Analysis
* Report Builder

## Pull-Auslieferung {#section_FA29FAEF02FE40B8B32452146A036F48}

Hierbei wird die Datei über normales FTP an einen der Server von Adobe gesendet. Wenn Sie die Datei auf Ihrem Server haben möchten, müssen Sie sie über Ihren Server per SFTP vom Adobe FTP-Server abrufen. Hierzu sind drei Methoden verfügbar:

* [Verbindung zu Adobe über SFTP ohne Kennwort herstellen.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* Sie können beliebige Berichte per Push an FTP-basierte Adobe Daten-Feeds/Reports &amp; Analytics/Ad Hoc usw. übertragen und dann abrufen. Adobe kann diese Berichte nicht an den von Ihnen eingerichteten SFTP-Server ausliefern.
