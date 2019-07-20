---
description: SFTP ist ein sicheres Protokoll für die Übertragung von Daten, mit dem sichergestellt wird, dass niemand Ihre Daten sehen kann, aber Sie. Adobe Engineering Services kann ein SFTP-Konto einrichten, um Ihre Daten sicher zu halten.
keywords: ftp; sftp
seo-description: SFTP ist ein sicheres Protokoll für die Übertragung von Daten, mit dem sichergestellt wird, dass niemand Ihre Daten sehen kann, aber Sie. Adobe Engineering Services kann ein SFTP-Konto einrichten, um Ihre Daten sicher zu halten.
seo-title: Secure File Transfer Protocol - Übersicht
solution: Analytics
title: Secure File Transfer Protocol - Übersicht
uuid: 7 dd 1 a 867-e 828-4 c 7 b-bf 11-75 a 81 d 4 c 149 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Secure File Transfer Protocol - Übersicht

SFTP ist ein sicheres Protokoll für die Übertragung von Daten, mit dem sichergestellt wird, dass niemand Ihre Daten sehen kann, aber Sie. Adobe Engineering Services kann ein SFTP-Konto einrichten, um Ihre Daten sicher zu halten.

## Push-Auslieferung {#section_A47831BB1DCA490BB57F0940617AA506}

Hierbei übertragen die Server von Adobe die Datei per Push auf Ihre Server. Faktisch wird sie an Ihren Endpunkt geliefert.

[Data Warehouse](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md#concept_904ADB7B4FE04DCCB90EFDB6D0DB1076) - und [Analytics-Datenfeed](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html) können Daten über SFTP senden.

The following Analytics tools **cannot** push data via SFTP:

* Reports &amp; Analytics
* Ad Hoc Analysis
* ReportBuilder

## Pull-Auslieferung {#section_FA29FAEF02FE40B8B32452146A036F48}

Hierbei wird die Datei über normales FTP an einen der Server von Adobe gesendet. Wenn Sie die Datei auf Ihrem Server benötigen, müssen Sie sie vom Server des Adobe-Servers per SFTP auf den FTP-Server von Adobe ziehen. Hierzu sind drei Methoden verfügbar:

* [Verbindung mit Adobe über SFTP ohne Kennwort](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md#concept_962A381F42A4472AA366A08CCC962846)
* [Verbindung zu einem Adobe FTP-Konto mit SFTP](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md#concept_01176600188441C6AFB28F5E264D89F8)
* Sie können beliebige Berichte per Push an FTP-artige Adobe Data Feeds/Reports und Analysen/Ad Hoc usw. übertragen und dann abrufen. Diese Berichte können von Adobe nicht auf dem von Ihnen eingerichteten SFTP-Server bereitgestellt werden.

