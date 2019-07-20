---
description: Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.
keywords: ftp; sftp
seo-description: Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.
seo-title: Verbindung zu einem Adobe FTP-Konto mit SFTP
solution: Analytics
title: Verbindung zu einem Adobe FTP-Konto mit SFTP
uuid: 4 faf 27 b 8-7276-4 c 68-87 cb -35802 b 809 e 27
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Verbindung zu einem Adobe FTP-Konto mit SFTP

Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.

1. Von Adobe gehostetes FTP-Konto anfordern (max. 50 MB)
1. Öffentlichen/privaten RSA-Schlüssel erstellen Befehl für Linux:

   ```
   ssh-keygen -t rsa
   ```

   Benutzen Sie in einer Windows-Umgebung puttyGen, um die Schlüssel zu erstellen.

1. Create a file named [!DNL authorized_keys] (no extension).
1. Copy the contents of the Public key into [!DNL authorized_keys].
1. [!DNL authorized_keys] Auf ein FTP-Konto hochladen:

   * Mit dem Adobe FTP-Konto verbinden.
   * Create a [!DNL .ssh] directory (if it does not already exist).
   * Upload the [!DNL authorized_keys] file to the [!DNL .ssh] directory.

1. Testen Sie die Verbindung, indem Sie sich mit SFTP beim FTP-Konto anmelden.

For more detailed information, see [How to Connect to Adobe via sFTP Without a Password_...](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md#concept_962A381F42A4472AA366A08CCC962846).
