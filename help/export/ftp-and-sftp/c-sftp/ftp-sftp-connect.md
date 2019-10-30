---
description: Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.
keywords: ftp;sftp
seo-description: Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.
seo-title: Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen
solution: Analytics
title: Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen
uuid: 4faf27b8-7276-4c68-87cb-35802b809e27
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen

Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.

1. Von Adobe gehostetes FTP-Konto anfordern (max. 50 MB)
1. Öffentlichen/privaten RSA-Schlüssel erstellen Befehl für Linux:

   ```
   ssh-keygen -t rsa
   ```

   Benutzen Sie in einer Windows-Umgebung puttyGen, um die Schlüssel zu erstellen.

1. Create a file named [!DNL authorized_keys] (no extension).
1. Copy the contents of the Public key into [!DNL authorized_keys].
1. Upload [!DNL authorized_keys] to an FTP account:

   * Mit dem Adobe FTP-Konto verbinden.
   * Create a [!DNL .ssh] directory (if it does not already exist).
   * Upload the [!DNL authorized_keys] file to the [!DNL .ssh] directory.

1. Testen Sie die Verbindung, indem Sie sich mit SFTP beim FTP-Konto anmelden.

[Weitere Informationen finden Sie unter ](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md#concept_962A381F42A4472AA366A08CCC962846)Verbindung mit Adobe über sFTP ohne Kennwort herstellen_....
