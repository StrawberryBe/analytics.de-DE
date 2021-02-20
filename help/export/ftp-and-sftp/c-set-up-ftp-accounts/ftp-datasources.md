---
description: Sie können Analytics nutzen, um FTP-basierte Data Sources zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in die Experience Cloud zu importieren.
keywords: ftp;sftp
title: Data Sources
uuid: 41ba2de7-d33d-4394-b7d8-04a116f45419
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 99%

---


# Datenquellen

Sie können Analytics nutzen, um FTP-basierte Data Sources zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in die Experience Cloud zu importieren.

Nach der Erstellung der Data Sources-Instanz stellt das Tool einen FTP-Speicherort bereit, den Sie zum Hochladen von Data Sources-Dateien verwenden können. Data Sources erkennt und verarbeitet die Dateien nach dem Hochladen automatisch. Nach der Verarbeitung der Dateien stehen die Daten für Analytics-Berichte zur Verfügung.

Auf dem Register [!UICONTROL Erstellen] können Sie im Data Sources Manager eine neue Data Sources-Instanz für die ausgewählte Report Suite konfigurieren. Der [!UICONTROL Data Sources-Assistent] führt Sie durch den Erstellungsvorgang einer Data Sources-Vorlage und legt einen FTP-Speicherort zum Hochladen der Daten an.

Suchen Sie im Fenster [!UICONTROL Data Sources verwalten] nach Ihrer Datenquelle und wählen Sie den Link zu den FTP-Informationen aus. Ihre FTP-Anmeldedaten werden im Fenster [!UICONTROL Eine Datenquelle aktivieren] im Abschnitt [!UICONTROL Hochladen/FTP-Info] angezeigt.

Informationen zu FTP-Beschränkungen und zur Datenaufbewahrung finden Sie unter [FTP-Beschränkungen und Datenaufbewahrung](/help/export/ftp-and-sftp/ftp-limits.md).

## Informationen zur FIN-Datei für Uploads für Classifications und Data Sources {#section_1484719F8A134EAE91212DBD8F15174F}

Beim Hochladen einer Classification oder einer [!UICONTROL Datenquell]-Datei ([!DNL .tab] oder [!DNL .txt]) muss eine leere Datei mit exakt demselben Namen wie der der importierten Datei, jedoch mit der Dateierweiterung [!DNL .fin], hochgeladen werden. Diese [!DNL .fin]-Datei ist eine Finish-Datei. Sie dient dazu, dem System mitzuteilen, dass die Datendatei vollständig in das FTP-Konto hochgeladen wurde. Über die [!DNL .fin]-Datei erkennt Adobe, dass Sie mit Ihrem Import fertig sind. Nachdem Sie diese Datei übermittelt haben, entfernt Adobe beide Dateien aus dem FTP-Konto und startet den Importprozess.
Importdatei: [!DNL Classifications.tab]

Finish-Datei: [!DNL Classifications.fin]

Wenn Sie Ihre Data-Sources- oder SAINT-Datei ohne zugehörige [!DNL .fin]-Datei hochladen, fügt Adobe Ihre Datei nicht zur Verarbeitungswarteschlange hinzu. Die Datei bleibt im FTP-Konto und wird nicht auf Ihre Daten in der [!UICONTROL Experience Cloud] angewendet. Sie werden hierüber nur dann benachrichtigt, wenn Sie Ihre E-Mail-Adresse als [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] der Berichterstellung angegeben haben. Wenn hier keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.

Wenn Sie Ihre Datei zusammen mit einer [!DNL .fin]-Datei hochgeladen haben, die Datei jedoch fehlerhaft ist, wird sie zur Verarbeitung gesendet. Der Fehler sorgt dann dafür, dass die Verarbeitung abgebrochen und die Datei an einen Fehlerordner gesendet wird. In diesem Fall wird eine Benachrichtigung an die im Feld [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] angegebene E-Mail-Adresse gesendet. Wenn keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.
