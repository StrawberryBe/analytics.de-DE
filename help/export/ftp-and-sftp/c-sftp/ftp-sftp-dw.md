---
description: Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.
keywords: ftp; sftp
seo-description: Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.
seo-title: Senden von Data Warehouse-Anfragen an SFTP-Server
solution: Analytics
title: Senden von Data Warehouse-Anfragen an SFTP-Server
uuid: 393634 a 1-064-4 d 63-bb 6 e-fb 80 f 1 ba 76 c 1
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Senden von Data Warehouse-Anfragen an SFTP-Server

Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.

Folgende Aufgaben müssen abgeschlossen sein:

Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server, sofern die folgenden Voraussetzungen erfüllt sind:

* [!DNL sftp://] im Host-Feld angegeben ist (z. [!DNL sftp://ftp.example.com]B.) und der Anschluss 22 wird beim Anfordern eines Data Warehouse-Berichts verwendet.

   You can also use the [!DNL sftp+norename://] option, as described below.

* Adobe's [!DNL authorized_keys] file is in the [!DNL .ssh] directory within the root directory of the user you log in with

* Das Ziel darf nicht [!DNL ftp.omniture.com] sein. Das sFTP-Protokoll wird zwischen den internen Servern von Adobe nicht unterstützt.
* Das Ziel unterstützt eine Ein-Faktor-Authentifizierung (PKI). Falls eine Zwei-Faktor-Authentifizierung erforderlich ist, schlägt die Bereitstellung des Berichts fehl. Stellen Sie sicher, dass der Server nicht so konfiguriert ist, dass er versucht, eine Zwei-Faktor-Authentifizierung durchzuführen. Für Adobe Analytics ist es erforderlich, dass ausschließlich der Schlüssel für die Anmeldung verwendet wird.
* Adobe unterstützt eine SSHv2-Verschlüsselung und führt ein Fallback auf SSHv1 aus (nur RSA-Schlüssel).

To successfully send a [!DNL Data Warehouse] request via SFTP:

1. Besorgen Sie sich die Datei [!DNL authorized_keys], indem sich ein unterstützter Benutzer Ihrer Organisation an die Kundenunterstützung wendet.
1. Nachdem Sie die Datei erhalten haben, melden Sie sich bei der FTP-Site mit den Anmeldedaten an, die für die [!DNL Data Warehouse]-Anforderung verwendet werden.
1. In the root directory, navigate to the folder named [!DNL .ssh] (if one does not exist, create one) and place the [!DNL authorized_keys] file there.

1. Go to the [!DNL Data Warehouse] request manager. Konfigurieren Sie die Anforderung und klicken Sie auf **[!UICONTROL Erweiterte Bereitstellungsoptionen]**.

1. In the pop-up window, click **[!UICONTROL FTP]**, then specify the ftp site (including the [!DNL sftp://] protocol, such as [!DNL sftp://ftp.omniture.com]) via port 22.

   Including the [!DNL sftp://] protocol is only permitted when using SFTP. Regular FTP requests should omit the protocol prefix (such as, [!DNL ftp.omniture.com] instead of [!DNL ftp://ftp.omniture.com]).

1. Geben Sie im Feld „Ordner“ den Namen des Ordners ein, in dem Sie die Datei ablegen möchten. Es muss ein Ordner eingegeben werden.
1. Geben Sie den Benutzernamen und das Kennwort aus Schritt 2 ein.
1. Klicken Sie auf **[!UICONTROL Senden]**.

Der sFTP-Befehl PUT platziert eine temporäre Datei mit der Erweiterung „.part“ im angegebenen Verzeichnis. Sobald das Hochladen abgeschlossen ist, wird die Dateierweiterung in die endgültige Erweiterung geändert, und die Datei kann verwendet werden.

Alternatively, [!DNL sftp+norename://] can be specified instead of [!DNL sftp://] to upload the file directly with the final name, without a temporary [!DNL .part] file name during upload. Dieser Ansatz eignet sich, wenn der SFTP-Server die Datei beim Hochladen automatisch umgeht, und es besteht keine Möglichkeit, dass die Datei verarbeitet wird, bevor der Upload abgeschlossen ist.
