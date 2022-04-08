---
description: Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.
keywords: ftp;sftp
title: Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen
feature: FTP Export
exl-id: 727d4f7a-d7d1-40cf-bdcd-c783ca47f51c
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: ht
source-wordcount: '134'
ht-degree: 100%

---

# Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen

Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.

1. Von Adobe gehostetes FTP-Konto anfordern (max. 50 MB)
1. Öffentlichen/privaten RSA-Schlüssel erstellen. Befehl für Linux:

   ```
   ssh-keygen -t rsa
   ```

   Benutzen Sie in einer Windows-Umgebung puttyGen, um die Schlüssel zu erstellen.

1. Datei mit dem Namen [!DNL authorized_keys] (ohne Erweiterung) erstellen.
1. Den Inhalt des öffentlichen Schlüssels in die Datei [!DNL authorized_keys] kopieren.
1. Die Datei [!DNL authorized_keys] in ein FTP-Konto hochladen:

   * Mit dem Adobe FTP-Konto verbinden.
   * Das Verzeichnis [!DNL .ssh] erstellen (sofern es noch nicht vorhanden ist).
   * Die Datei [!DNL authorized_keys] in das Verzeichnis [!DNL .ssh] hochladen.

1. Die Verbindung testen, indem Sie sich per SFTP bei dem FTP-Konto anmelden.

Weitere Informationen finden Sie unter [Verbindung zu Adobe über SFTP ohne Kennwort herstellen](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md).
