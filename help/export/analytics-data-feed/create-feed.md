---
title: Datenfeed erstellen oder bearbeiten
description: Erfahren Sie, wie Sie einen Datenfeed erstellen oder bearbeiten.
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Datenfeed erstellen oder bearbeiten

Durch das Erstellen eines Datenfeeds kann Adobe wissen, wo Rohdatendateien gesendet werden und was Sie in die einzelnen Dateien aufnehmen möchten. Auf dieser Seite werden die einzelnen Einstellungen aufgelistet, die Sie beim Erstellen eines Datenfeeds anpassen können.

Grundlegende Kenntnisse zu Datenfeeds werden vor dem Lesen dieser Seite empfohlen. Siehe Übersicht über [Datenfeeds](data-feed-overview.md) , um sicherzustellen, dass Sie die Anforderungen zum Erstellen eines Datenfeeds erfüllen.

## Feed-Informationsfelder

* **Name**: Der Name des Datenfeeds. Muss innerhalb der ausgewählten Report Suite eindeutig sein und kann bis zu 255 Zeichen lang sein.
* **** Report Suite: Die Report Suite, auf der der Datenfeed basiert. Wenn mehrere Datenfeeds für dieselbe Report Suite erstellt werden, müssen sie unterschiedliche Spaltendefinitionen haben. Nur Quell-Report Suites unterstützen Datenfeeds. Virtual Report Suites werden nicht unterstützt.
* **E-Mail nach Abschluss**: Die E-Mail-Adresse, die benachrichtigt werden soll, wenn ein Feed die Verarbeitung abgeschlossen hat. Die E-Mail-Adresse muss korrekt formatiert sein.
* **Feed-Intervall**: Stündliche Feeds enthalten Daten aus einer Stunde. Tägliche Feeds enthalten Daten zum vollen Tageswert.
* **Verarbeitung** verzögern: Warten Sie einen bestimmten Zeitraum, bevor Sie eine Data Feed-Datei verarbeiten. Eine Verzögerung kann nützlich sein, um mobilen Implementierungen die Möglichkeit zu geben, dass Offlinegeräte online gehen und Daten senden können. Es kann auch verwendet werden, um die serverseitigen Prozesse Ihres Unternehmens bei der Verwaltung zuvor verarbeiteter Dateien zu berücksichtigen. In den meisten Fällen ist keine Verzögerung erforderlich. Ein Feed kann um bis zu 120 Minuten verzögert werden.
* **Start- und Enddaten**: Das Startdatum gibt das erste Datum an, an dem Sie einen Datenfeed erstellen möchten. Legen Sie dieses Datum in der Vergangenheit fest, um sofort mit der Verarbeitung von Datenfeeds für historische Daten zu beginnen. Feeds werden bis zum Enddatum verarbeitet.
* **Kontinuierlicher Feed**: Mit diesem Kontrollkästchen wird das Enddatum entfernt, sodass ein Feed unbegrenzt ausgeführt werden kann. Wenn ein Feed die Verarbeitung historischer Daten beendet, wartet ein Feed, bis die Datenerfassung für eine bestimmte Stunde oder einen bestimmten Tag abgeschlossen ist. Sobald die aktuelle Stunde oder der aktuelle Tag abgeschlossen ist, beginnt die Verarbeitung nach der angegebenen Verzögerung.

## Zielfelder

Die unter den Zielfeldern verfügbaren Felder hängen vom Zieltyp ab.

### FTP

Datenfeed-Daten können für einen von Adobe oder vom Kunden gehosteten FTP-Speicherort bereitgestellt werden. Erfordert einen FTP-Host, Benutzernamen und ein Kennwort. Verwenden Sie das Pfadfeld, um Feed-Dateien in einem Ordner zu platzieren. Ordner müssen bereits vorhanden sein; Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist.

![FTP-Info](assets/dest-ftp.jpg)

### SFTP

SFTP-Unterstützung für Data Feeds ist verfügbar. Erfordert einen SFTP-Host, Benutzernamen und die Ziel-Site, um einen gültigen öffentlichen RSA- oder DSA-Schlüssel zu enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Feeds herunterladen.

![SFTP-Info](assets/dest-sftp.jpg)

### S3

Sie können Feeds direkt an Amazon S3-Behälter senden. Erfordert einen Behälternamen, eine Zugriffsschlüssel-ID und einen geheimen Schlüssel. Weitere Informationen finden Sie unter [Amazon S3-Behälterbenennungsanforderungen](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in den Amazon S3-Dokumenten.

![S3-Info](assets/dest-s3.jpg)

Die folgenden 11 standardmäßigen AWS-Regionen werden unterstützt (gegebenenfalls unter Verwendung des entsprechenden Signaturalgorithmus):

* us-east-1
* us-west-1
* us-west-2
* ap-south-1
* ap-northeast-2
* ap-southeast-1
* ap-southeast-2
* ap-northeast-1
* eu-central-1
* eu-west-1
* sa-east-1

> [!NOTE] Die cn-north-1-Region wird nicht unterstützt.

### Azure Blob

Datenfeeds unterstützen Blumenziele. Erfordert einen Container, ein Konto und einen Schlüssel. Amazon verschlüsselt die Daten automatisch während der Ruhezeit. Wenn Sie die Daten herunterladen, werden sie automatisch entschlüsselt. Weitere Informationen finden Sie unter [Erstellen eines Speicherkontos](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in den Microsoft Azurblase-Dokumenten.

![Azurinfo](assets/azure.png)

> [!NOTE] Sie müssen einen eigenen Prozess implementieren, um Speicherplatz auf dem Feed-Ziel zu verwalten. Adobe löscht keine Daten vom Server.

## Datenspaltendefinitionen

Es sind alle Spalten verfügbar, unabhängig davon, ob sie über Daten verfügen. Ein Datenfeed muss mindestens eine Spalte enthalten.

* **Entfernen Sie Escapezeichen**: Beim Erfassen von Daten können einige Zeichen (z. B. Zeilenumbrüche) Probleme verursachen. Aktivieren Sie dieses Kontrollkästchen, wenn diese Zeichen aus Feed-Dateien entfernt werden sollen.
* **Komprimierungsformat**: Die verwendete Komprimierung. Gzip gibt Dateien im `.tar.gz` Format aus. Zip gibt Dateien im `.zip` Format aus.
* **Verpackungstyp**: Eine einzelne Datei gibt die `hit_data.tsv` Datei in einer einzigen, potenziell umfangreichen Datei aus. Mehrere Dateien paginieren Ihre Daten in 2-GB-Blöcke (unkomprimiert). Wenn mehrere Dateien ausgewählt sind und die nicht komprimierten Daten für das Berichtsfenster weniger als 2 GB betragen, wird eine Datei gesendet. Adobe empfiehlt die Verwendung mehrerer Dateien für die meisten Datenfeeds.
* **Spaltenvorlagen**: Adobe empfiehlt, beim Erstellen vieler Datenfeeds eine Spaltenvorlage zu erstellen. Bei Auswahl einer Spaltenvorlage werden automatisch die angegebenen Spalten in der Vorlage eingefügt. Adobe stellt standardmäßig auch mehrere Vorlagen bereit.
* **Verfügbare Spalten**: Alle in Adobe Analytics verfügbaren Datenspalten. Klicken Sie auf Alle [!UICONTROL hinzufügen] , um alle Spalten in einen Datenfeed einzuschließen.
* **Spalten** einschließen: Die Spalten, die in einen Datenfeed aufgenommen werden sollen. Klicken Sie auf Alle [!UICONTROL entfernen] , um alle Spalten aus einem Datenfeed zu entfernen.
* **CSV** herunterladen: Lädt eine CSV-Datei herunter, die alle enthaltenen Spalten enthält.
