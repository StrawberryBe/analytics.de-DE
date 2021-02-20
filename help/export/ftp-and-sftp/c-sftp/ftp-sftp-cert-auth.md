---
description: Eine Verbindung zu FTP-Konten kann nur dann ohne Kennwort hergestellt werden, wenn sowohl eine SFTP-Verbindung als auch ein alternatives Authentifizierungsverfahren genutzt werden. Hierzu sind zwei Dateien erforderlich (eine im FTP-Konto und die andere auf Ihrem Computer), die eine Kombination aus öffentlichem und privatem Schlüssel bilden.
keywords: ftp;sftp
title: Verbindung zu Adobe über SFTP ohne Kennwort herstellen
uuid: 88728309-50d2-450b-b0e6-7dcdf61b5dbc
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 99%

---


# Verbindung zu Adobe über SFTP ohne Kennwort herstellen

Eine Verbindung zu FTP-Konten kann nur dann ohne Kennwort hergestellt werden, wenn sowohl eine SFTP-Verbindung als auch ein alternatives Authentifizierungsverfahren genutzt werden. Hierzu sind zwei Dateien erforderlich (eine im FTP-Konto und die andere auf Ihrem Computer), die eine Kombination aus öffentlichem und privatem Schlüssel bilden.

Dies ist nicht weniger sicher als eine Authentifizierung über ein Kennwort. Es handelt sich um eine andere Form der Authentifizierung, bei der der Benutzer nicht jedes Mal ein Kennwort eingeben muss. Bei korrekter Anwendung kann sich ein bestimmter Computer mithilfe dieser Dateien ohne Angabe eines Kennworts anmelden. Dieses Verfahren muss für jeden Computer einzeln eingerichtet werden. Für alle anderen Verbindungen, die keine Schlüsseldateien verwenden, muss weiterhin ein Kennwort angegeben werden.

Manche Clients benötigen SFTP (Secure File Transfer Protocol), um sensible Daten zu übertragen. Eine SFTP-Verbindung ist sicherer als eine normale FTP-Verbindung, da die Datenkommunikation verschlüsselt erfolgen kann. Alle Adobe FTP-Konten sind standardmäßig SFTP-fähig. Eine SFTP-Verbindung kann mit einem gültigen Benutzernamen und einem Kennwort über einen SFTP-Client hergestellt werden, der eine Verbindung über Port 22 herstellt (normale FTP-Verbindungen, die nicht sicher sind, nutzen Port 21).

Bei Verwendung von SFTP ist es unter bestimmten Bedingungen möglich, private Schlüssel zu verwenden, um ohne Kennwort eine Verbindung zu einem Konto herzustellen. Bei diesem Verfahren verwendet Ihr Computer für die Authentifizierung anstelle der üblichen Kennwortauthentifizierung Schlüsseldateien. Dies bedeutet, dass nur der Computer, auf dem sich der private Schlüssel befindet, ohne Kennwort eine Verbindung herstellen kann. Alle anderen Computer/Benutzer müssen weiterhin eine Kennwortauthentifizierung verwenden (sofern nicht auch auf diesen Computern private Schlüssel eingerichtet sind).

**Einrichten und Verwenden von privaten Schlüsseln für eine Authentifizierung ohne Kennwort**

1. FTP-Konto erstellen (Adobe).

   Ein Adobe-Support-Mitarbeiter kann ein FTP-Konto erstellen, falls noch keines vorhanden ist. Wenden Sie sich an Ihren Adobe-Kundenbetreuer oder an die Adobe-Kundenunterstützung, um ein Konto zu erhalten.
1. Öffentlichen/privaten Schlüssel erstellen (Kunde).

   Erstellen Sie eine Kombination aus öffentlichem und privatem Schlüssel. Der private Schlüssel ist eine Datei, die sich auf Ihrem Computer/Server befindet. Der öffentliche Schlüssel muss in das Adobe-Konto hochgeladen werden. Wenn dies der Fall ist, können Sie eine Verbindung ohne Kennwortauthentifizierung herstellen. Die öffentliche Schlüsseldatei bei Adobe passt zu der privaten Schlüsseldatei auf Ihrem Computer/Server und wird auf diese Weise authentifiziert.

   Wenden Sie sich für das Erstellen dieser Dateien an Ihren internen Netzwerksupport, der einen für Ihre Umgebung passenden Schlüsselsatz erstellen kann. Es gibt eine Vielzahl von Werkzeugen und Anwendungen, mit denen diese beiden Dateien erstellt werden können.

   Unten sehen Sie ein Beispiel für den Ablauf in einer UNIX-Shell-Umgebung. Dies ist nur ein Beispiel, das beim Übermitteln der Anforderungen an Ihr Team oder Ihre interne Netzwerkgruppe als Referenz dienen kann.

   ```
   // Linux/Unix (bash shell)
   
   // First make sure the ".ssh" directory exists
   
   $ mkdir ~/.ssh
   
   $ cd ~/.ssh
   
   // Now actually generate the key pair
   
   // Usually we will want to create an empty passphrase (just hit "Enter" for both password prompts)
   
   $ ssh-keygen -q -t dsa
   
   Enter file in which to save the key (/home/user/.ssh/id_dsa):
   
   Enter passphrase (empty for no passphrase): ...
   
   Enter same passphrase again: ...
   
   // Rename or copy the public key file to "authorized_keys"
   
   // This "authorized_keys" file is the one that we will upload to the Adobe FTP server in step 3
   
   $ cp id_dsa.pub authorized_keys 
   ```

1. Öffentlichen Schlüssel in das FTP-Konto hochladen (Kunde).

   Laden Sie den öffentlichen Schlüssel hoch und testen Sie ihn. Stellen Sie eine Verbindung zum Adobe FTP-Konto her und erstellen Sie das Verzeichnis [!DNL .ssh], sofern es noch nicht vorhanden ist. Laden Sie die Datei [!DNL authorized_keys] in das Verzeichnis [!DNL .ssh] hoch. Hierzu gibt es verschiedene Möglichkeiten (Befehlszeile, grafischer FTP-Client usw.). Alles was Sie benötigen, ist die Berechtigung, ein Verzeichnis zu erstellen und eine Datei hochzuladen.

   Auch hier sehen Sie ein Beispiel dafür innerhalb einer UNIX-Shell.

   ```
   $ ftp ftp.Adobe.com
   
   OR (depending on hostname provided by Adobe)
   
   $ ftp ftp2.Adobe.com
   
   // Enter username and password for account as prompted
   
   ftp> mkdir .ssh
   
   ftp> cd .ssh
   
   ftp> put authorized_keys
   
   ftp> exit
   
   // Now test the connection by logging in to the server using "sftp" command:
   
   $ sftp username@ftp.omniture.com
   
   OR (depending on hostname provided by Adobe)
   
   $ sftp username@ftp2.omniture.com
   
   // You should immediately receive an sftp prompt without having to enter the password:
   
   sftp>
   ```

