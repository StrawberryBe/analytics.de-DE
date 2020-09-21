---
description: Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.
keywords: ftp;sftp
title: Data Warehouse-Anforderungen an SFTP-Server senden
uuid: 393634a1-0643-4d63-bb6e-fb80f1ba76c1
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '412'
ht-degree: 100%

---


# Data Warehouse-Anforderungen an SFTP-Server senden

Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.

Folgende Aufgaben müssen abgeschlossen sein:

Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server, wenn folgende Voraussetzungen erfüllt sind:

* Im Feld „Host“ ist als Protokoll [!DNL sftp://] angegeben (z. B. [!DNL sftp://ftp.example.com]) und beim Anfordern von Data Warehouse-Berichten wird AUSSCHLIESSLICH Port 22 verwendet.

   Sie können auch die Option [!DNL sftp+norename://] wie unten beschrieben verwenden.

* Die Datei [!DNL authorized_keys] von Adobe befindet sich im Verzeichnis [!DNL .ssh] innerhalb des Stammverzeichnisses des Benutzers, der sich anmeldet

* Das Ziel darf nicht [!DNL ftp.omniture.com] sein. Das SFTP-Protokoll wird zwischen den internen Servern von Adobe nicht unterstützt.
* Das Ziel unterstützt eine Ein-Faktor-Authentifizierung (PKI). Falls eine Zwei-Faktor-Authentifizierung erforderlich ist, schlägt die Bereitstellung des Berichts fehl. Stellen Sie sicher, dass der Server nicht so konfiguriert ist, dass er versucht, eine Zwei-Faktor-Authentifizierung durchzuführen. Für Adobe Analytics ist es erforderlich, dass ausschließlich der Schlüssel für die Anmeldung verwendet wird.
* Adobe unterstützt eine SSHv2-Verschlüsselung und führt ein Fallback auf SSHv1 aus (nur RSA-Schlüssel).

So senden Sie eine [!DNL Data Warehouse]-Anforderung erfolgreich über SFTP:

1. Besorgen Sie sich die Datei [!DNL authorized_keys]. Dazu muss sich ein unterstützter Benutzer Ihrer Organisation an die Kundenunterstützung wendet.
1. Nachdem Sie die Datei erhalten haben, melden Sie sich bei der FTP-Site mit den Anmeldedaten an, die für die [!DNL Data Warehouse]-Anforderung verwendet werden.
1. Navigieren Sie im Stammverzeichnis zu dem Ordner [!DNL .ssh] (erstellen Sie diesen, falls er nicht vorhanden ist) und legen Sie dort die Datei [!DNL authorized_keys] ab.

1. Wechseln Sie zum [!DNL Data Warehouse]-Anforderungs-Manager. Konfigurieren Sie die Anforderung und klicken Sie auf **[!UICONTROL Erweiterte Bereitstellungsoptionen]**.

1. Klicken Sie im Popup-Fenster auf **[!UICONTROL FTP]** und geben Sie die FTP-Site (mit dem Protokoll [!DNL sftp://], z. B. [!DNL sftp://ftp.omniture.com]) über Port 22 an.

   Die Angabe des Protokolls [!DNL sftp://] ist nur zulässig, wenn SFTP verwendet wird. Für normale FTP-Anforderungen sollte kein Protokollpräfix angegeben werden (z. B. [!DNL ftp.omniture.com] anstatt [!DNL ftp://ftp.omniture.com]).

1. Geben Sie im Feld „Ordner“ den Namen des Ordners ein, in dem Sie die Datei ablegen möchten. Es muss ein Ordner eingegeben werden.
1. Geben Sie den Benutzernamen und das Kennwort aus Schritt 2 ein.
1. Klicken Sie auf **[!UICONTROL Senden]**.

Der SFTP-Befehl PUT platziert eine temporäre Datei mit der Erweiterung „.part“ im angegebenen Verzeichnis. Sobald das Hochladen abgeschlossen ist, wird die Dateierweiterung in die endgültige Erweiterung geändert, und die Datei kann verwendet werden.

Alternativ kann auch [!DNL sftp+norename://] anstelle von [!DNL sftp://] angegeben werden, um die Datei direkt mit dem endgültigen Namen hochzuladen, ohne dass beim Hochladen ein temporärer Dateiname mit dem Bestandteil [!DNL .part] angegeben wird. Dieser Ansatz ist von Vorteil, wenn der SFTP-Server die Dateiumbenennung während des Uploads automatisch durchführt und die Datei vor Abschluss des Uploads nicht verarbeitet wird.
