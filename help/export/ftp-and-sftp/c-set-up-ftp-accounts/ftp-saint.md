---
description: Die FTP-Option für Classifications (SAINT) bietet mehr Flexibilität beim Hochladen großer Classification-Datensätze. So können u. a. auch Daten in mehrere Report Suites und Datensätze mit mehr als 50.000 Zeilen hochgeladen werden.
keywords: ftp;sftp
title: Classifications
uuid: 35936c98-b785-43eb-89f4-ab42a10db256
translation-type: tm+mt
source-git-commit: 7a70a5185b768dbc09deca5c8989693501af0cca
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 68%

---


# Klassifizierungen

Die FTP-Option für Classifications bietet mehr Flexibilität beim Hochladen großer Classification-Datensätze. So können u. a. auch Daten in mehrere Report Suites und Datensätze mit mehr als 50.000 Zeilen hochgeladen werden.

Unter [Classifications](https://docs.adobe.com/content/help/de-DE/analytics/components/classifications/classifications-importer/c-working-with-saint.html) finden Sie Schritte für das Herunterladen von Classification-Daten über FTP und das Hochladen von Datendateien über FTP (einschließlich der für das Erstellen eines FTP-Kontos erforderlichen Schritte).

Wie lange das System für das Importieren dieser Dateien benötigt, hängt von verschiedenen Faktoren ab. Wenn eine hochgeladene Datei mehr als drei Tage auf dem FTP-Server vorhanden ist, wenden Sie sich an die unterstützten Benutzer Ihres Unternehmens, um sich an die Kundenunterstützung der Adobe zu wenden.

Bei einem erfolgreichen Import erscheinen die entsprechenden Änderungen sofort in einem Export, während die Datenänderungen in Analytics bei einem Browserimport bis zu 4 Stunden und bei einem FTP-Import bis zu 24 Stunden später erscheinen können.

Informationen zu FTP-Beschränkungen und zur Datenaufbewahrung finden Sie unter [FTP-Beschränkungen und Datenaufbewahrung](/help/export/ftp-and-sftp/ftp-limits.md).

## Informationen zur Datei `.fin` für Classifications- und Data Sources-Uploads {#section_1484719F8A134EAE91212DBD8F15174F}

Wenn Sie eine Classification- oder Datenquelle-Datei (`.tab` oder `.txt`) hochladen, müssen Sie beim Hochladen auch eine leere Datei hochladen, die genau denselben Namen hat wie die importierte Datendatei, jedoch mit der Erweiterung .`.fin`. Diese `.fin`-Datei ist eine Finish-Datei. Sie dient dazu, dem System mitzuteilen, dass die Datendatei vollständig in das FTP-Konto hochgeladen wurde. Über die `.fin`-Datei erkennt Adobe, dass Sie mit Ihrem Import fertig sind.

Nachdem Sie sowohl die Quelldatei als auch die `.fin`-Datei gesendet haben, müssen Sie sich unbedingt von der FTP-Site abmelden. Der Grund dafür ist, dass Adobe Analytics Abmeldedateien als Trigger verwendet, der zur Verarbeitung bereit ist. Nach Abschluss des Imports entfernt Adobe beide Dateien aus dem FTP-Speicherort.

Finish-Datei: [!DNL Classifications.fin]

Wenn Sie Ihre Data Sources- oder Classification-Datei ohne zugehörige `.fin`-Datei hochladen, fügt die Adobe sie nicht zur Verarbeitung in die Warteschlange ein. Die Datei bleibt im FTP-Konto und wird nicht auf Ihre Daten in [!UICONTROL Experience Cloud] angewendet. Sie werden hierüber nur dann benachrichtigt, wenn Sie Ihre E-Mail-Adresse als [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] von Analytics angegeben haben. Wenn hier keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.

Wenn Sie Ihre Datei zusammen mit einer `.fin`-Datei hochgeladen haben, die Datei jedoch fehlerhaft ist, wird sie zur Verarbeitung gesendet. Der Fehler sorgt dann dafür, dass die Verarbeitung abgebrochen und die Datei an einen Fehlerordner gesendet wird. In diesem Fall wird eine Benachrichtigung an die im Feld [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] angegebene E-Mail-Adresse gesendet. Wenn keine E-Mail-Adresse eingegeben wurde, wird keine Benachrichtigung gesendet.
