---
description: Die Verbindung ohne Kennwort zu FTP-Konten ist nur über eine SFTP-Verbindung und eine alternative Authentifizierungsmethode möglich. Hierzu sind zwei Dateien erforderlich (eine im FTP-Konto und die andere auf Ihrem Computer), die eine Kombination aus öffentlichem und privatem Schlüssel bilden.
keywords: ftp; sftp
seo-description: Die Verbindung ohne Kennwort zu FTP-Konten ist nur über eine SFTP-Verbindung und eine alternative Authentifizierungsmethode möglich. Hierzu sind zwei Dateien erforderlich (eine im FTP-Konto und die andere auf Ihrem Computer), die eine Kombination aus öffentlichem und privatem Schlüssel bilden.
seo-title: Verbindung mit Adobe über SFTP ohne Kennwort
solution: Analytics
title: Verbindung mit Adobe über SFTP ohne Kennwort
uuid: 88728309-50 d 2-450 b-b 0 e 6-7 dcdf 61 b 5 dbc
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Verbindung mit Adobe über SFTP ohne Kennwort

Die Verbindung ohne Kennwort zu FTP-Konten ist nur über eine SFTP-Verbindung und eine alternative Authentifizierungsmethode möglich. Hierzu sind zwei Dateien erforderlich (eine im FTP-Konto und die andere auf Ihrem Computer), die eine Kombination aus öffentlichem und privatem Schlüssel bilden.

Dies ist nicht weniger sicher als eine Authentifizierung über ein Kennwort. Es handelt sich um eine andere Form der Authentifizierung, bei der der Benutzer nicht jedes Mal ein Kennwort eingeben muss. Bei korrekter Anwendung kann sich ein bestimmter Computer mithilfe dieser Dateien ohne Angabe eines Kennworts anmelden. Dieses Verfahren muss für jeden Computer einzeln eingerichtet werden. Für alle anderen Verbindungen, die keine Schlüsseldateien verwenden, muss weiterhin ein Kennwort angegeben werden.

Einige Kunden benötigen ein SFTP (Secure File Transfer Protocol) für die Übertragung vertraulicher Daten. Eine SFTP-Verbindung ist sicherer als eine normale FTP-Verbindung, da sie eine verschlüsselte Datenkommunikation zulässt. Standardmäßig sind alle Adobe FTP-Konten SFTP bereit. Eine SFTP-Verbindung kann mit einem gültigen Benutzernamen und Kennwort geöffnet werden, indem ein SFTP-Client verwendet wird, der eine Verbindung zu Port 22 herstellt (normale FTP-Verbindungen, die nicht sicher sind, Port 21).

Wenn Sie SFTP verwenden, können unter bestimmten Bedingungen private Schlüssel verwendet werden, um ohne Kennwort eine Verbindung zu dem Konto herzustellen. Bei diesem Verfahren verwendet Ihr Computer für die Authentifizierung anstelle der üblichen Kennwortauthentifizierung Schlüsseldateien. Dies bedeutet, dass nur der Computer, auf dem sich der private Schlüssel befindet, ohne Kennwort eine Verbindung herstellen kann. Alle anderen Computer/Benutzer müssen weiterhin eine Kennwortauthentifizierung verwenden (sofern nicht auch auf diesen Computern private Schlüssel eingerichtet sind).

**Einrichten und Verwenden von privaten Schlüsseln für eine Authentifizierung ohne Kennwort**

1. FTP-Konto erstellen (Adobe)

   Ein Adobe-Support-Mitarbeiter kann ein FTP-Konto erstellen, falls noch keines vorhanden ist. Wenden Sie sich an Ihren Adobe-Kundenbetreuer oder an die Adobe-Kundenunterstützung, um ein Konto zu erhalten.
1. Öffentlichen/privaten Schlüssel erstellen (Kunde)

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

1. Öffentlichen Schlüssel in das FTP-Konto hochladen (Kunde)

   Laden Sie den öffentlichen Schlüssel hoch und testen Sie ihn. Connect to the Adobe FTP account and create a [!DNL .ssh] directory, if it does not already exist. Upload the [!DNL authorized_keys] file to this [!DNL .ssh] directory. Hierzu gibt es verschiedene Möglichkeiten (Befehlszeile, grafischer FTP-Client usw.). Alles was Sie benötigen, ist die Berechtigung, ein Verzeichnis zu erstellen und eine Datei hochzuladen.

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

