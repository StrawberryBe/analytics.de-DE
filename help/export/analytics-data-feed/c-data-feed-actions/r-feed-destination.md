---
description: Im Abschnitt „Feed-Ziel“ wird die Verteilung des Feeds definiert.
keywords: Datenfeed; Feed; destination; sftp; s 3; ftp; Einstellungen
seo-description: Im Abschnitt „Feed-Ziel“ wird die Verteilung des Feeds definiert.
seo-title: Feed-Ziel
solution: Analytics
title: Feed-Ziel
uuid: 4 a 59 e 8 de-e 7 a 6-4 f 7 a-bf 42-db 7 d 59 e 61 b 4 c
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Feed-Ziel

Im Abschnitt „Feed-Ziel“ wird die Verteilung des Feeds definiert.

Es gibt vier Verteilungskanäle:

* FTP
* SFTP
* Amazon S3
* Azure Blob

## FTP {#section_D2B521C49BDE4F91A1999FE222CF306F}

Datenfeed-Daten können für einen von Adobe oder vom Kunden gehosteten FTP-Speicherort bereitgestellt werden.

Wenn Sie auswählen, dass die Daten auf Ihren FTP-Server hochgeladen werden sollen, müssen Sie Adobe den entsprechenden Benutzernamen sowie das Kennwort und den Upload-Pfad zur Verfügung stellen. Sie müssen Ihren eigenen Vorgang zur Verwaltung des Speicherplatzes auf dem Server implementieren, da Adobe keine Daten auf dem Server löscht.

![](assets/dest-ftp.jpg)

## SFTP {#section_8D9215E441474D2BBC56228C2BC926E5}

Datenfeed-Daten können für einen von Adobe oder vom Kunden gehosteten sFTP-Speicherort bereitgestellt werden.

Wenn Sie den Upload von Daten auf Ihren FTP-Server auswählen, müssen Sie Adobe den entsprechenden Benutzernamen und den Upload-Pfad zur Verfügung stellen.

<!-- 

Adobe Customer Care will provide you with a Public key. Verify in recording.

 -->

Sie müssen Ihren eigenen Vorgang zur Verwaltung des Speicherplatzes auf dem Server implementieren, da Adobe keine Daten auf dem Server löscht.

![](assets/dest-sftp.jpg)

## Amazon S3 {#section_4191CD7B8D3F419EB850B286B542C14A}

Sie können Ihre Dateien in einen Amazon S3-Behälter hochladen. Die Daten werden bei der Speicherung automatisch (auf den Amazon-Servern) verschlüsselt. Wenn Sie die Daten herunterladen, werden sie automatisch entschlüsselt.

Wenn Sie sich für einen Upload von Daten über Amazon S3 entscheiden, müssen Sie einen Behälternamen, eine Zugriffsschlüssel-ID, einen geheimen Schlüssel und einen Ordnernamen bereitstellen.

![](assets/dest-s3.jpg)

Daten-Feeds kommunizieren mit den folgenden 11 Standard-AWS-Regionen (gegebenenfalls unter Verwendung des entsprechenden Signaturalgorithmus)

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

Peking, AWS-Region China (cn-north-1), wird zurzeit nicht unterstützt.

## Azure Blob {#section_1E9F1D0E7EAB4189A5D748FCA57D63D1}

Sie können Daten in einen Azure Blob-Speicher hochladen.

![](assets/azure.png)

## Felder {#section_AD54B41BC7C945DC85F5FB8FCD4A4792}

In der folgenden Tabelle werden alle Optionen für sämtliche Verteilungskanäle aufgeführt. Die verfügbaren Optionen sind vom ausgewählten Verteilungskanal abhängig.

<table id="table_F743C620C82349D9943A13B99EA312BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feld </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Zugriffsschlüssel </p> </td> 
   <td colname="col2"> <p>Geben Sie den Amazon S3-Zugriffsschlüssel ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Behälter </p> </td> 
   <td colname="col2"> <p>Geben Sie den Speicherort des Amazon S3-Behälters ein. </p> <p>Dieser Wert muss mit dem entsprechenden S3-Behälterformat übereinstimmen. (See <a href="https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html" format="html" scope="external"> https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html</a>.) </p> <p> <p>Hinweis: Einzelheiten zu den Amazon S3-Einstellungen finden Sie unter <a href="../../../export/analytics-data-feed/feed-troubleshooting.md#section_6797EBBB7E6D44D4B00C7AEDF4C2EE1D" format="dita" scope="local">BucketOwnerFullControl-Einstellung für Amazon S3-Datenfeeds</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Behälter </p> </td> 
   <td colname="col2"> <p>Geben Sie den Namen des Azure Blob-Behälters ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Host </p> </td> 
   <td colname="col2"> <p>Geben Sie das FTP- oder SFTP-Hostverzeichnis an. </p> <p>Dieser Wert muss dem korrekten FTP/SFTP-Format entsprechen, <code>ftp.domain.com/subdomain</code> oder <code>sftp.domain.com/subdomain</code>. </p> <p> Die Standardports 21 und 22 für FTP und sFTP sind erforderlich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passwort </p> <p>Passwort bestätigen </p> </td> 
   <td colname="col2"> <p>Geben Sie das FTP-Kennwort ein. Zur Bestätigung neu eingeben </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pfad </p> </td> 
   <td colname="col2"> <p>Wählen Sie den Pfad zum Host oder Behälter aus. Dieser Pfad muss bereits vor der Feed-Erstellung vorhanden sein. </p> <p> <p>Hinweis: Einzelheiten zu den Amazon S3-Einstellungen finden Sie unter <a href="../../../export/analytics-data-feed/feed-troubleshooting.md#section_6797EBBB7E6D44D4B00C7AEDF4C2EE1D" format="dita" scope="local">BucketOwnerFullControl-Einstellung für Amazon S3-Datenfeeds</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Konto </p> </td> 
   <td colname="col2"> <p> Geben Sie das Konto des Azure-Speichers ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Öffentlicher Schlüssel </p> </td> 
   <td colname="col2"> <p>Stellen Sie den öffentlichen SFTP-Schlüssel bereit. </p> <p>Sie müssen den öffentlichen Schlüssel herunterladen, um das SFTP Repository einrichten zu können. </p> <p> <p>Hinweis: Zum Erstellen des Feeds muss der öffentliche Schlüssel nicht heruntergeladen werden. </p> </p> <p>Sie können einen öffentlichen Schlüssel verwenden, den Sie bereits beim Erstellen eines vorherigen Feeds heruntergeladen haben. </p> <p>Weitere Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/ftp_sftp_dw.html" format="html" scope="external">https://marketing.adobe.com/resources/help/de_DE/whitepapers/ftp/ftp_sftp_dw.html</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Schlüssel </p> <p>Schlüssel bestätigen </p> </td> 
   <td colname="col2"> <p> Geben Sie Ihren Zugriffsschlüssel für den Speicher ein. Erneut eingeben und bestätigen. </p> <p> <p>Hinweis: Unter <a href="https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account#view-and-copy-storage-access-keys" format="https" scope="external">https://docs.microsoft.com/de-de/azure/storage/common/storage-create-storage-account#view-and-copy-storage-access-keys</a> erfahren Sie, wie Sie auf Zugangsschlüssel zugreifen können. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geheimer Schlüssel </p> <p>Geheimen Schlüssel bestätigen </p> </td> 
   <td colname="col2"> <p>Geben Sie den geheimen Amazon S3-Schlüssel ein. Geben Sie ihn zur Bestätigung erneut ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Typ </p> </td> 
   <td colname="col2"> <p>Wählen Sie den Zieltyp aus. </p> <p> 
     <ul id="ul_B893EEDA73A34DE0AEB8570BE9027F21"> 
      <li id="li_325546FCEB404C50AA6829573CCA340B">FTP (Standard) </li> 
      <li id="li_6A2C03115903484797485D073A610607">AmazonS3 </li> 
      <li id="li_C24540F6FCD24702B7693A515CEBE977">SFTP </li> 
      <li id="li_8E03CA78E7FE427C9F6F8B112BC76266">Azure Blob </li> 
     </ul> </p> <p>Nach Auswahl des Zieltyps ändert sich die Feldliste und spiegelt die verfügbaren Optionen für das ausgewählte Ziel wider. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzername </p> </td> 
   <td colname="col2"> <p>Geben Sie den FTP-Benutzernamen ein. </p> </td> 
  </tr> 
 </tbody> 
</table>

