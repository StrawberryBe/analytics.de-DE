---
description: Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.
keywords: ftp;sftp
title: Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen
feature: FTP Export
exl-id: 727d4f7a-d7d1-40cf-bdcd-c783ca47f51c
source-git-commit: 62132284ca70f3bdb1a8896e4548b8b63a5c03c8
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 64%

---

# Verbindung zu einem FTP-Konto mit SFTP herstellen

So richten Sie eine sichere Übertragung mit FTP ein:

1. (Bedingt) Wenn Sie eine sichere Übertragung mit Adobe FTP-Servern einrichten möchten:

   1. Von Adobe gehostetes FTP-Konto anfordern (max. 50 MB)

   1. Öffentlichen/privaten RSA-Schlüssel erstellen.

      * Führen Sie in der Linux-Umgebung Folgendes aus:

        ```
        ssh-keygen -t rsa
        ```

      * Verwenden Sie in einer Windows-Umgebung puttyGen.

1. (Bedingt) Wenn Sie eine sichere Übertragung mit Ihrem eigenen FTP-Speicherort einrichten möchten, müssen Sie über einen SFTP-Host, einen Benutzernamen und die Ziel-Site verfügen, die einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Feeds herunterladen.

1. Datei mit dem Namen [!DNL authorized_keys] (ohne Erweiterung) erstellen.

1. Den Inhalt des öffentlichen Schlüssels in die Datei [!DNL authorized_keys] kopieren.

1. Die Datei [!DNL authorized_keys] in ein FTP-Konto hochladen:

   * Mit dem Adobe FTP-Konto verbinden.
   * Das Verzeichnis [!DNL .ssh] erstellen (sofern es noch nicht vorhanden ist).
   * Die Datei [!DNL authorized_keys] in das Verzeichnis [!DNL .ssh] hochladen.

1. Die Verbindung testen, indem Sie sich per SFTP bei dem FTP-Konto anmelden.

Weitere Informationen finden Sie unter [Verbindung zu Adobe über SFTP ohne Kennwort herstellen](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md).
