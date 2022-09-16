---
description: Die FTP-Option für Klassifizierungen (SAINT) bietet mehr Flexibilität beim Hochladen großer Klassifizierungs-Datensätze. So können u. a. auch Daten in mehrere Report Suites und Datensätze mit mehr als 50.000 Zeilen hochgeladen werden.
keywords: ftp;sftp
title: Classifications
feature: FTP Export
exl-id: fc783328-a70b-4af3-b3d3-c59ab79d6b8f
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 100%

---

# Klassifizierungen

Die FTP-Option für Classifications bietet mehr Flexibilität beim Hochladen großer Classification-Datensätze. So können u. a. auch Daten in mehrere Report Suites und Datensätze mit mehr als 50.000 Zeilen hochgeladen werden.

Unter [Classifications](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html?lang=de) finden Sie Schritte für das Herunterladen von Classification-Daten über FTP und das Hochladen von Datendateien über FTP (einschließlich der für das Erstellen eines FTP-Kontos erforderlichen Schritte).

Wie lange das System für das Importieren dieser Dateien benötigt, hängt von verschiedenen Faktoren ab. Wenn eine hochgeladene Datei länger als drei Tage auf dem FTP-Server vorhanden ist, wenden Sie sich an einen unterstützten Benutzer Ihrer Organisation, damit er Kontakt mit der Adobe-Kundenunterstützung aufnimmt.

Bei einem erfolgreichen Import erscheinen die entsprechenden Änderungen sofort in einem Export, während die Datenänderungen in Analytics bei einem Browser-Import bis zu 4 Stunden und bei einem FTP-Import bis zu 24 Stunden später erscheinen können.

Informationen zu FTP-Beschränkungen und zur Datenaufbewahrung finden Sie unter [FTP-Beschränkungen und Datenaufbewahrung](/help/export/ftp-and-sftp/ftp-limits.md).

## Informationen zur `.fin`-Datei für Uploads von Klassifizierungen und Datenquellen {#section_1484719F8A134EAE91212DBD8F15174F}

Beim Hochladen einer Klassifizierungs- oder einer Datenquelldatei (`.tab` oder `.txt`) müssen Sie auch eine leere Datei mit exakt demselben Namen wie die importierte Datei, jedoch mit der Dateierweiterung .`.fin`, hochladen. Diese `.fin`-Datei ist eine Finish-Datei. Sie dient dazu, dem System mitzuteilen, dass die Datendatei vollständig in das FTP-Konto hochgeladen wurde. Über die `.fin`-Datei erkennt Adobe, dass Sie mit Ihrem Import fertig sind.

Nachdem Sie sowohl die Quelldatei als auch die `.fin`-Datei übermittelt haben, müssen Sie sich unbedingt von der FTP-Site abmelden. Adobe Analytics verwendet Abmeldeereignisse nämlich als Trigger dafür, dass Dateien zur Verarbeitung bereit sind. Nach Abschluss des Imports entfernt Adobe beide Dateien aus dem FTP-Verzeichnis.

Finish-Datei: [!DNL Classifications.fin]

Wenn Sie Ihre Datenquell- oder Klassifizierungs-Datei ohne zugehörige `.fin`-Datei hochladen, fügt Adobe Ihre Datei nicht zur Verarbeitungswarteschlange hinzu. Die Datei bleibt im FTP-Konto und wird nicht auf Ihre Daten in [!UICONTROL Experience Cloud] angewendet. Sie werden hierüber nur dann benachrichtigt, wenn Sie Ihre E-Mail-Adresse als [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] von Analytics angegeben haben. Wenn hier keine E-Mail-Adresse angegeben ist, wird keine Benachrichtigung gesendet.

Wenn Sie Ihre Datei zusammen mit einer `.fin`-Datei hochgeladen haben, die Datei jedoch fehlerhaft ist, wird sie zur Verarbeitung gesendet. Der Fehler sorgt dann dafür, dass die Verarbeitung abgebrochen und die Datei an einen Fehlerordner gesendet wird. In diesem Fall wird eine Benachrichtigung an die im Feld [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] angegebene E-Mail-Adresse gesendet. Wenn keine E-Mail-Adresse angegeben wurde, wird keine Benachrichtigung gesendet.
