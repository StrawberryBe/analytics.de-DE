---
title: Aktualisierung der SFTP-Dienste - Häufig gestellte Fragen
description: Häufig gestellte Fragen zum geplanten Upgrade der SFTP-Dienste im Mai 2022.
source-git-commit: eb9bdcbd99d45afc913c5ade37e8fb5c62a3a456
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 2%

---


# Aktualisierung der SFTP-Dienste - Häufig gestellte Fragen

on **2. Mai 2022**, aktualisiert Adobe Analytics sein Secure File Transfer Protocol [SFTP] Dienste zur Verbesserung der Sicherheit für Dateiübertragungen. Mit dieser Änderung werden einige SFTP-Client-Konfigurationen nicht mehr unterstützt. Wir werden auch einige Verbindungsoptionen hinzufügen, die verfügbar sind von **1. März 2022**. Dies wirkt sich nur auf Daten aus, die über SFTP an Adobe Analytics gesendet oder aus abgerufen werden. Das FTP-Protokoll ist davon nicht betroffen. Um Dienstunterbrechungen zu vermeiden, stellen Sie bitte sicher, dass Ihre SFTP-Clients (Code, Tools, Dienste) den unten beschriebenen Änderungen entsprechen.

## Wie kann ich feststellen, welche Algorithmen, Verbindungstypen und Protokolle derzeit von meinem Unternehmen verwendet werden?

Die FTP-/SFTP-Software, die Sie verwenden, sollte angeben, welche spezifischen Einstellungen in den Verbindungen verwendet werden, die Sie für den Datenaustausch mit Adobe Analytics konfiguriert haben. Diese Software sollte auch eine Dokumentation zu den verschiedenen verfügbaren Optionen für Verbindungen enthalten. Die Optionen, die nach dieser Aktualisierung unterstützt werden, werden in der Branche weithin unterstützt und akzeptiert.

## Welche Adobe Analytics-Funktionen verwenden SFTP für die Datenerfassung?

Die folgenden Funktionen bieten eine Option zum Hochladen von Daten in Adobe Analytics mithilfe von SFTP.

* [Klassifizierungen](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-saint.html)

* [Data Feeds](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datafeeds.html)

* [Datenquellen](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datasources.html)

* [Von Data Warehouse bereitgestellte Berichte](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-dw-reports.html)

* Darüber hinaus werden einige benutzerdefinierte Implementierungen durch erstellt. [Engineering Services](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-eng-services.html) kann SFTP verwenden, um Daten mit Adobe auszutauschen.

## Welche spezifischen Änderungen werden in dieser Aktualisierung enthalten sein?

Nachstehend finden Sie eine detaillierte Liste, welche Verbindungen und Algorithmen entfernt werden und welche unterstützt werden:

* SFTP-Protokoll mac-Algorithmen:

   * Wir werden Folgendes nicht mehr unterstützen: hmac-md5, hmac-md5-96, hmac-ripemd160, hmacripemd160@openssh.com, hmac-sha1, hmac-sha1-96, hmac-sha1-etm@openssh.com, umac-64-etm@openssh.com, umac-64@openssh.com

   * Wir werden nur Folgendes unterstützen: hmac-sha2-512-etm@openssh.com, hmac-sha2-256-etm@openssh.com, umac-128-etm@openssh.com, hmac-sha2-512, hmacsha2-256, umac-128@openssh.com

* SFTP-Protokollskriptalgorithmus:

   * Wir werden Folgendes nicht mehr unterstützen: 3des-cbc, aes128-cbc, aes128-gcm@openssh.com, aes192-cbc, aes256-cbc, aes256-gcm@openssh.com, arcfour, arcfour128, arcfour256, blowfish-cbc, cast128-cbc, rijndael-cbc@lysator.liu.se

   * Wir werden nur Folgendes unterstützen: aes128-ctr, aes192-ctr, aes256-ctr

* Vom SFTP-Protokoll unterstützte Verbindungen:

   * Die Verwendung von SCP- und Rsync-Befehlen oder Verbindungen über das SFTP-Protokoll wird nicht mehr unterstützt

   * Wir unterstützen nur reine SFTP-Protokollverbindungen

* Unterstützte FTP-/SFTP-Clients/Protokolle:

   * FTP: vsftpd-Version 3.0.2-25 oder höher

   * SFTP: openssh Version 7.4p1-21 oder höher