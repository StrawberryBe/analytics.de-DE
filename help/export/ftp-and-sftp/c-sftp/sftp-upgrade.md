---
title: Aktualisierung der SFTP-Services – Häufig gestellte Fragen
description: Häufig gestellte Fragen zur geplanten Aktualisierung der SFTP-Services im Mai 2022.
feature: FTP Export
exl-id: e271b545-0769-4a69-9d7f-dc46bc654737
source-git-commit: dd1b2d358e6074fc393e6e5999c4286549a1b82d
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 92%

---

# Aktualisierung der SFTP-Services – Häufig gestellte Fragen

Am **15. Mai 2022** werden in Adobe Analytics die [SFTP]-Service (Secure File Transfer Protocol) zur Verbesserung der Sicherheit für Dateiübertragungen aktualisiert. Mit dieser Änderung werden einige SFTP-Client-Konfigurationen nicht mehr unterstützt. Wir werden auch einige Verbindungsoptionen hinzufügen, die am **1. März 2022** verfügbar sein werden. Dies wirkt sich nur auf Daten aus, die über SFTP an Adobe Analytics gesendet oder von dort aus abgerufen werden. Das FTP-Protokoll ist davon nicht betroffen. Um Service-Unterbrechungen zu vermeiden, stellen Sie sicher, dass Ihre SFTP-Clients (Code, Tools, Services) den unten beschriebenen Änderungen entsprechen.

## Wie kann ich feststellen, welche Algorithmen, Verbindungstypen und Protokolle derzeit von meiner Organisation verwendet werden?

Die FTP-/SFTP-Software, die Sie verwenden, sollte angeben, welche spezifischen Einstellungen in den Verbindungen verwendet werden, die Sie für den Datenaustausch mit Adobe Analytics konfiguriert haben. Diese Software sollte auch eine Dokumentation zu den verschiedenen verfügbaren Optionen für Verbindungen enthalten. Die Optionen, die nach dieser Aktualisierung unterstützt werden, werden in der Branche weithin unterstützt und akzeptiert.

Die Verbindungsoptionen, die entfernt werden, werden im Allgemeinen als veraltet betrachtet und in der aktuellen Software nicht verwendet. Wenn Sie Ihre FTP/SFTP-Software in den letzten drei Jahren aktualisiert haben, verfügen Sie vermutlich bereits über eine konforme Verbindung.

## Welche Adobe Analytics-Funktionen verwenden SFTP für die Datenaufnahme?

Die folgenden Funktionen bieten eine Option zum Hochladen von Daten in Adobe Analytics mithilfe von SFTP.

* [Klassifizierungen](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-saint.html?lang=de)

* [Daten-Feeds](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datafeeds.html?lang=de)

* [Datenquellen](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datasources.html?lang=de)

* [Von Data Warehouse bereitgestellte Berichte](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-dw-reports.html?lang=de)

* Darüber hinaus können einige benutzerdefinierte Implementierungen, die durch [Engineering Services](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-eng-services.html?lang=de) erstellt wurden, SFTP zum Datenaustausch mit Adobe verwenden.

## Welche spezifischen Änderungen werden in dieser Aktualisierung enthalten sein?

Nachstehend finden Sie eine detaillierte Liste, welche Verbindungen und Algorithmen entfernt werden und welche unterstützt werden:

* SFTP-Protokoll mac-Algorithmen:

   * Wir werden die folgenden nicht mehr unterstützen: hmac-md5, hmac-md5-96, hmac-ripemd160, hmacripemd160@openssh.com, hmac-sha1, hmac-sha1-96, hmac-sha1-etm@openssh.com, umac-64-etm@openssh.com, umac-64@openssh.com

   * Wir werden nur die folgenden unterstützen: hmac-sha2-512-etm@openssh.com, hmac-sha2-256-etm@openssh.com, umac-128-etm@openssh.com, hmac-sha2-512, hmacsha2-256, umac-128@openssh.com

* Algorithmus zur Verschlüsselung des SFTP-Protokolls:

   * Wir werden die folgenden nicht mehr unterstützen: 3des-cbc, aes128-cbc, aes128-gcm@openssh.com, aes192-cbc, aes256-cbc, aes256-gcm@openssh.com, arcfour, arcfour128, arcfour256, blowfish-cbc, cast128-cbc, rijndael-cbc@lysator.liu.se

   * Wir werden nur die folgenden unterstützen: aes128-ctr, aes192-ctr, aes256-ctr

* Vom SFTP-Protokoll unterstützte Verbindungen:

   * Die Verwendung von SCP- und Rsync-Befehlen oder Verbindungen über das SFTP-Protokoll wird nicht mehr unterstützt

   * Wir unterstützen nur reine SFTP-Protokollverbindungen

* Unterstützte FTP-/SFTP-Clients/-Protokolle:

   * FTP: vsftpd Version 3.0.2-25 oder höher

   * SFTP: openssh Version 7.4p1-21 oder höher
