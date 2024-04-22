---
description: Konfigurieren Sie das Cloud-Importkonto und den Speicherort, an den Classification-Daten hochgeladen werden können.
keywords: Analysis Workspace
title: Konfigurieren von Cloud-Import- und -Exportspeicherorten
feature: Classifications
exl-id: 55179868-6228-44ff-835c-f4a7b38e929b
source-git-commit: 5bf6ed9b71a87d79fec960b6618667238019ac7f
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 31%

---

# Konfigurieren von Cloud-Import- und -Exportspeicherorten

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

Sie können ein Cloud-Konto (und einen Speicherort auf diesem Konto) konfigurieren. Ein einzelner Ort kann für einen der folgenden Zwecke verwendet werden (ein einzelner Ort kann nicht mehreren Zwecken zugeordnet werden, z. B. Daten-Feeds und Data Warehouse oder Data Warehouse- und Classification-Sets):

* Exportieren von Dateien mithilfe von [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md)
* Exportieren von Berichten mithilfe von [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Importieren von Schemata mit [Klassifizierungssätze](/help/components/classifications/sets/overview.md)

Sie müssen Adobe Analytics mit den für den Zugriff auf Ihr Cloud-Konto erforderlichen Informationen konfigurieren. Dieser Prozess besteht aus dem Hinzufügen und Konfigurieren des Kontos (z. B. Amazon S3 Role ARN, Google Cloud Platform usw.), wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md)und dann den Speicherort innerhalb dieses Kontos hinzufügen und konfigurieren (wie in diesem Artikel beschrieben).

## Erstellen oder Bearbeiten eines Cloud-Exportspeicherorts beginnen

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] > [!UICONTROL **Standorte**].
1. Im [!UICONTROL Standorte] Seite, wählen Sie die [!UICONTROL **Standorte**] Registerkarte.
1. Um einen neuen Speicherort zu erstellen, wählen Sie [!UICONTROL **Ort hinzufügen**]. (Wenn Sie noch kein Konto hinzugefügt haben, fügen Sie eines wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md).

   Oder

   Um einen vorhandenen Speicherort zu bearbeiten, wählen Sie das Menü mit 3 Punkten im [!UICONTROL **Ortsname**] Spalte für den Speicherort, den Sie bearbeiten möchten, und wählen Sie [!UICONTROL **Bearbeiten**].
Das Dialogfeld Standort wird angezeigt.

1. Geben Sie die folgenden Informationen an: |Feld | Funktion | |—|—| | [!UICONTROL **Name**] | Der Name des Standorts.  |
| [!UICONTROL **Beschreibung**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. | | [!UICONTROL **Verwenden Sie**] | Wählen Sie aus, ob Sie diesen Standort mit [!UICONTROL **Daten-Feeds**], [!UICONTROL **Data Warehouse**] oder [!UICONTROL **Klassifizierungssätze**]. <p>Beachten Sie bei der Auswahl Folgendes:</p><ul><li>Ein einzelner Ort kann nicht für mehrere Zwecke verwendet werden. Beispielsweise kann ein Speicherort, der für Daten-Feeds verwendet wird, nicht auch für Data Warehouse- oder Classification-Sets verwendet werden.</li><li>Um Dateikonflikte innerhalb eines Standorts zu vermeiden, ändern Sie nicht den Wert der [!UICONTROL **Verwenden Sie**] -Feld, nachdem der Speicherort verwendet wurde.</li></ul> | | [!UICONTROL **Standortkonto**] | Wählen Sie das Standortkonto aus, in dem Sie diesen Ort erstellen möchten. Informationen zum Erstellen eines Kontos finden Sie unter [Konto hinzufügen](#add-an-account). |

1. Geben Sie im Abschnitt [!UICONTROL **Speicherorteigenschaften**] spezifische Informationen zum Kontotyp Ihres Speicherortkontos an.

   Fahren Sie mit dem folgenden Abschnitt fort, der dem Kontotyp entspricht, den Sie in der [!UICONTROL **Standortkonten**] -Feld. (Es sind auch zusätzliche veraltete Kontotypen verfügbar, jedoch nicht empfohlen.)



### Amazon S3 Role ARN

Geben Sie die folgenden Informationen an, um einen Amazon S3 Role ARN-Speicherort zu konfigurieren:

1. [Erstellen oder Bearbeiten eines Cloud-Exportspeicherorts beginnen](#begin-creating-or-editing-a-cloud-export-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Bucket-Name**] | Der Bucket in Ihrem Amazon S3-Konto, an den Adobe Analytics-Daten gesendet werden sollen. <p>Stellen Sie sicher, dass die von Adobe bereitgestellte Benutzer-ARN über die `S3:PutObject` -Berechtigung, um Dateien in diesen Bucket hochzuladen. </p><p>Behälternamen müssen bestimmten Benennungsregeln entsprechen. Sie müssen beispielsweise zwischen 3 und 63 Zeichen lang sein, dürfen nur aus Kleinbuchstaben, Zahlen, Punkten (.) und Bindestrichen (-) bestehen und müssen mit einem Buchstaben oder einer Zahl beginnen und enden. [Eine vollständige Liste der Benennungsregeln finden Sie in der Dokumentation zu AWS .](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
   | [!UICONTROL **Schlüssel-Präfix**] | Der Ordner im Bucket, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. (Beispiel: Ordnername/) |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das oder aus dem von Ihnen konfigurierten Konto und Speicherort importieren oder exportieren. Verwenden Sie zum Exportieren von Daten [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Verwenden Sie zum Importieren von Daten [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

   Importierte Daten werden nach dem Import nicht mehr aus dem Cloud-Ziel gelöscht.

   >[!NOTE]
   >
   >   Wenn Sie zuvor [FTP zum Importieren von Classifications](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) nach Adobe Analytics, müssen Sie eine FIN-Datei hochladen. Diese FIN-Datei ist beim Import aus Cloud-Konten nicht erforderlich.


### Google Cloud Platform

Geben Sie die folgenden Informationen an, um einen Google Cloud Platform-Speicherort zu konfigurieren:

1. [Erstellen oder Bearbeiten eines Cloud-Exportspeicherorts beginnen](#begin-creating-or-editing-a-cloud-export-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Bucket-Name**] | Der Behälter in Ihrem GCP-Konto, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie dem von Adobe bereitgestellten Prinzipal die Berechtigung zum Hochladen von Dateien in diesen Bucket erteilt haben. |
   | [!UICONTROL **Schlüssel-Präfix**] | Der Ordner im Bucket, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. (Beispiel: Ordnername/) |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das oder aus dem von Ihnen konfigurierten Konto und Speicherort importieren oder exportieren. Verwenden Sie zum Exportieren von Daten [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Verwenden Sie zum Importieren von Daten [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

   Importierte Daten werden nach dem Import nicht mehr aus dem Cloud-Ziel gelöscht.

   >[!NOTE]
   >
   >   Wenn Sie zuvor [FTP zum Importieren von Classifications](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) nach Adobe Analytics, müssen Sie eine FIN-Datei hochladen. Diese FIN-Datei ist beim Import aus Cloud-Konten nicht erforderlich.


### Azure SAS

Geben Sie die folgenden Informationen an, um einen Azure SAS-Speicherort zu konfigurieren:

1. [Erstellen oder Bearbeiten eines Cloud-Exportspeicherorts beginnen](#begin-creating-or-editing-a-cloud-export-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Container-Name**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. |
   | [!UICONTROL **Schlüsselpräfix**] | Der Ordner im Container, in dem Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/` |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das oder aus dem von Ihnen konfigurierten Konto und Speicherort importieren oder exportieren. Verwenden Sie zum Exportieren von Daten [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Verwenden Sie zum Importieren von Daten [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

   Importierte Daten werden nach dem Import nicht mehr aus dem Cloud-Ziel gelöscht.

   >[!NOTE]
   >
   >   Wenn Sie zuvor [FTP zum Importieren von Classifications](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) nach Adobe Analytics, müssen Sie eine FIN-Datei hochladen. Diese FIN-Datei ist beim Import aus Cloud-Konten nicht erforderlich.


### Azure RBAC

Geben Sie die folgenden Informationen an, um einen Azure RBAC-Speicherort zu konfigurieren:

1. [Erstellen oder Bearbeiten eines Cloud-Exportspeicherorts beginnen](#begin-creating-or-editing-a-cloud-export-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Container-Name**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie Berechtigungen zum Hochladen von Dateien in die Azure-Anwendung erteilen, die Sie zuvor erstellt haben. |
   | [!UICONTROL **Schlüsselpräfix**] | Der Ordner im Container, in dem Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/` |
   | [!UICONTROL **Kontoname**] | Das Azure-Speicherkonto. |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das oder aus dem von Ihnen konfigurierten Konto und Speicherort importieren oder exportieren. Verwenden Sie zum Exportieren von Daten [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Verwenden Sie zum Importieren von Daten [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

   Importierte Daten werden nach dem Import nicht mehr aus dem Cloud-Ziel gelöscht.

   >[!NOTE]
   >
   >   Wenn Sie zuvor [FTP zum Importieren von Classifications](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) nach Adobe Analytics, müssen Sie eine FIN-Datei hochladen. Diese FIN-Datei ist beim Import aus Cloud-Konten nicht erforderlich.

### Alte Kontotypen

Diese veralteten Kontotypen sind nur verfügbar, wenn Daten mit [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) und [Data Warehouse](/help/export/data-warehouse/create-request/t-dw-create-request.md). Diese Optionen stehen beim Datenimport mit [Klassifizierungssätze](/help/components/classifications/sets/manage/schema.md).

+++FTP

Daten-Feed-Daten können an einen Adobe- oder kundengehosteten FTP-Speicherort bereitgestellt werden. Ordner angeben Verwenden Sie das Pfadfeld, um Feed-Dateien in einem Ordner zu platzieren.

| Feld | Funktion |
|---------|----------|
| [!UICONTROL **Verzeichnispfad**] | Geben Sie den Pfad zum Verzeichnis auf dem FTP-Server ein. Ordner müssen bereits vorhanden sein. Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist. </br>Beispiel: `/folder_name/folder_name`. |

{style="table-layout:auto"}

+++

+++SFTP

Daten-Feed-Daten können an einen Adobe- oder kundengehosteten SFTP-Speicherort bereitgestellt werden. Die Ziel-Site muss einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Feeds herunterladen.

| Feld | Funktion |
|---------|----------|
| [!UICONTROL **Verzeichnispfad**] | Geben Sie den Pfad zum Verzeichnis auf dem FTP-Server ein. Ordner müssen bereits vorhanden sein. Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist. </br>Beispiel: `/folder_name/folder_name`. |

{style="table-layout:auto"}

+++

++ + S3

Sie können Warehouse-Daten direkt an Amazon S3-Buckets senden. Dieser Zieltyp erfordert einen Behälternamen, eine Zugriffsschlüssel-ID und einen geheimen Schlüssel. Weitere Informationen finden Sie unter [Benennungsanforderungen für Amazon S3-Behälter](https://docs.aws.amazon.com/de_de/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in der Amazon S3-Dokumentation.

Die Benutzerin oder der Benutzer, die bzw. den Sie zum Hochladen von Data Warehouse-Daten angeben, muss über die folgenden [Berechtigungen](https://docs.aws.amazon.com/de_de/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html) verfügen:

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

Die folgenden 16 standardmäßigen AWS-Regionen werden unterstützt (gegebenenfalls unter Verwendung des entsprechenden Signaturalgorithmus):

* us-east-2
* us-east-1
* us-west-1
* us-west-2
* ap-south-1
* ap-northeast-2
* ap-southeast-1
* ap-southeast-2
* ap-northeast-1
* ca-central-1
* eu-central-1
* eu-west-1
* eu-west-2
* eu-west-3
* eu-north-1
* sa-east-1

>[!NOTE]
>
>Die Region „cn-north-1“ wird nicht unterstützt.

+++

+++Azure Blob

Data Warehouse unterstützt Azure Blob-Ziele. Erfordert einen Container, ein Konto und einen Schlüssel. Amazon verschlüsselt die Daten automatisch während der Ruhezeit. Wenn Sie die Daten herunterladen, werden sie automatisch entschlüsselt. Weitere Informationen finden Sie unter [Erstellen eines Speicherkontos](https://docs.microsoft.com/de-de/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in der Dokumentation zu Microsoft Azure.

>[!NOTE]
>
>Sie müssen Ihren eigenen Prozess implementieren, um Speicherplatz auf dem Data Warehouse-Ziel zu verwalten. Adobe löscht keine Daten vom Server.

+++


