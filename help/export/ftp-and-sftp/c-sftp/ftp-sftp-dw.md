---
description: Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.
keywords: ftp;sftp
title: Data Warehouse-Anforderungen an SFTP-Server senden
uuid: 393634a1-0643-4d63-bb6e-fb80f1ba76c1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Data Warehouse-Anforderungen an SFTP-Server senden

Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.

Folgende Aufgaben müssen abgeschlossen sein:

Adobe unterstützt den Export von Data Warehouse-Anfragen an SFTP-Server, sofern folgende Voraussetzungen erfüllt sind:

* [!DNL sftp://] -Protokoll im Hostfeld angegeben ist (z. B. [!DNL sftp://ftp.example.com]), und beim Anfordern eines Data Warehouse-Berichts wird NUR Port 22 verwendet.

   Sie können die [!DNL sftp+norename://] Option auch wie unten beschrieben verwenden.

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

Alternatively, [!DNL sftp+norename://] can be specified instead of [!DNL sftp://] to upload the file directly with the final name, without a temporary [!DNL .part] file name during upload. Dieser Ansatz ist geeignet, wenn der SFTP-Server beim Hochladen automatisch Dateiumbenennungen verarbeitet und die Datei vor dem Hochladen nicht verarbeitet wird.
