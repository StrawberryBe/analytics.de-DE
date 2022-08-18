---
title: Erstellen oder Bearbeiten eines Daten-Feeds
description: Erfahren Sie, wie Sie einen Daten-Feed erstellen oder bearbeiten.
feature: Data Feeds
exl-id: 36c8a40e-6137-4836-9d4b-bebf17b932bc
source-git-commit: 60335be9a60b467969f5e1796ce465a7d453951f
workflow-type: tm+mt
source-wordcount: '1518'
ht-degree: 56%

---

# Erstellen oder Bearbeiten eines Daten-Feeds

Durch das Erstellen eines Daten-Feeds weiß Adobe, wohin Rohdatendateien gesendet werden sollen und was Sie in die einzelnen Dateien aufnehmen möchten. Auf dieser Seite werden die einzelnen Einstellungen aufgelistet, die Sie beim Erstellen eines Daten-Feeds anpassen können.

Das Vorliegen grundlegender Kenntnisse zu Daten-Feeds ist empfehlenswert, bevor Sie diese Seite lesen. Beachten Sie die Informationen unter [Daten-Feed-Übersicht](data-feed-overview.md), um sicherzustellen, dass Sie die Anforderungen zum Erstellen eines Daten-Feeds erfüllen.

## Feed-Informationsfelder

* **Name**: Der Name des Daten-Feeds. Muss innerhalb der ausgewählten Report Suite eindeutig sein. Er kann bis zu 255 Zeichen enthalten.
* **Report Suite:** Die Report Suite, auf der der Daten-Feed basiert. Wenn mehrere Daten-Feeds für dieselbe Report Suite erstellt werden, müssen sie unterschiedliche Spaltendefinitionen haben. Nur Quell-Report Suites unterstützen Daten-Feeds. Virtual Report Suites werden nicht unterstützt.
* **E-Mail nach Abschluss**: Die E-Mail-Adresse, die benachrichtigt werden soll, wenn die Verarbeitung eines Feeds abgeschlossen ist. Die E-Mail-Adresse muss korrekt formatiert sein.
* **Feed-Intervall**: Stündliche Feeds enthalten Daten aus einer Stunde. Tägliche Feeds enthalten Daten eines ganzen Tages, von Mitternacht bis Mitternacht in der Zeitzone der Report Suite.
* **Verarbeitung verzögern**: Warten Sie einen bestimmten Zeitraum, bevor Sie eine Daten-Feed-Datei verarbeiten. Eine Verzögerung kann nützlich sein, um mobilen Implementierungen die Möglichkeit zu geben, dass Offlinegeräte online gehen und Daten senden können. Sie kann auch verwendet werden, um die serverseitigen Prozesse Ihrer Organisation bei der Verwaltung zuvor verarbeiteter Dateien zu berücksichtigen. In den meisten Fällen ist keine Verzögerung erforderlich. Ein Feed kann um bis zu 120 Minuten verzögert werden.
* **Start- und Enddaten**: Das Startdatum gibt das erste Datum an, an dem Sie einen Daten-Feed erstellen möchten. Legen Sie dieses Datum in der Vergangenheit fest, um sofort mit der Verarbeitung von Daten-Feeds für historische Daten zu beginnen. Feeds werden bis zum Enddatum verarbeitet. Start- und Enddatum basieren auf der Zeitzone der Report Suite.
* **Kontinuierlicher Feed**: Mit diesem Kontrollkästchen wird das Enddatum entfernt, sodass ein Feed unbegrenzt ausgeführt werden kann. Wenn ein Feed die Verarbeitung historischer Daten abschließt, wartet er, bis die Datenerfassung für die jeweilige Stunde bzw. dem jeweiligen Tag abgeschlossen ist. Sobald die aktuelle Stunde oder der aktuelle Tag abgeschlossen ist, beginnt die Verarbeitung nach der angegebenen Verzögerung.

## Zielfeld

Die unter den Zielfeldern verfügbaren Felder hängen vom Zieltyp ab.

### Google Cloud Platform

GCP-Speicher-Buckets als sicheres Ziel aufrufen

**Felder**
* *Typ:* Zieltyp der Google Cloud-Plattform
* *Projekt-ID:* GCP-Projekt-ID, an der der Speicherbehälter vorhanden ist
* *Speichername:* Behälternamen ohne Punkte sind auf 3-63 Zeichen begrenzt. Namen, die Punkte enthalten, können bis zu 222 Zeichen enthalten, jede Komponente mit Punkt-Trennzeichen darf jedoch nicht länger als 63 Zeichen sein.
* *Pfad (optional):* &amp; *Report Suite-ID an Pfad anhängen:* Speicherort der abzurufenden oder zu speichernden Ressourcen

![GCP-Info](assets/dest-gcp.png)

**Prozess zur Erstellung von Dienstkonten**

Der Benutzer muss ein Dienstkonto für das Google Cloud Platform-Ziel erstellen.

Pro Analytics-Organisation ist nur ein GCP-Dienstkonto zulässig. Nachdem das Dienstkonto für den Datenfeed erstellt wurde, werden alle zusätzlichen Datenfeeds innerhalb der Organisation vorab mit dem Dienstkonto ausgefüllt.

![GCP-Dienstkontoinformationen](assets/service-account.png)


### Amazon S3

Amazon S3-Behälterspeicher, auf den über die IAM-Rolle innerhalb einer vertrauenswürdigen Entität zugegriffen wird.

**Felder**

* *Typ:* Zieltyp des Amazon S3
* *Bucket:* S3-Behältername
* *Vertrauenswürdige Entitäts-ARN:* AWS IAM Entity ARN `arn:aws:iam::<12 digit account number>:user/<username>`
* *Rolle ARN:* AWS IAM Role ARN `arn:aws:iam::<12 digit account number>:role/<role name>`
* *Pfad (optional):* &amp; *Report Suite-ID an Pfad anhängen:* Speicherort der abzurufenden oder zu speichernden Ressourcen
* *Region angeben (optional):* Dropdown-Liste aller verfügbaren AWS-Regionen, einschließlich KN-Regionen

![Amazon S3-Info](assets/dest-s3-secure.png)


**Erstellen und Auswählen einer vertrauenswürdigen Entität**

Der Benutzer kann aus allen im Dropdown-Menü aufgeführten Optionen eine vertrauenswürdige Entität auswählen oder eine neue erstellen und abrufen, indem er auf die `Create Entity` Schaltfläche.

Nach dem Klicken auf die `Create Entity` -Schaltfläche, wird der Benutzer zu einem Authentifizierungsprozess umgeleitet. Nachdem sich der Benutzer authentifiziert hat, wird die vertrauenswürdige Entität erstellt und den Optionen im Dropdown-Menü hinzugefügt.

Das Dropdown-Menü listet alle vertrauenswürdigen Entitäten auf, die von diesem Benutzer in der Organisation erstellt wurden.

![Entitätsinformationen](assets/entity-creation.png)

Sie können Feeds direkt über die veraltete Methode an Amazon S3-Behälter senden. Weitere Informationen finden Sie unter [Benennungsanforderungen für Amazon S3-Behälter](https://docs.aws.amazon.com/de_de/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in der Amazon S3-Dokumenation.

**Felder - veraltet**

* *Typ:* Zieltyp der veralteten S3-Methode
* *Bucket:* Amazon S3-Bucket-Name
* *Pfad (optional):* &amp; *Report Suite-ID an Pfad anhängen:* Speicherort der abzurufenden oder zu speichernden Ressourcen
* *Zugriffsschlüssel:* Zugriffsschlüssel-ID des AWS-Benutzers
* *Geheimer Schlüssel:* Geheimer Schlüssel für AWS-Benutzer
* *Geheimen Schlüssel bestätigen:* Geheimschlüssel des AWS-Benutzers erneut eingeben

![S3-Info](assets/dest-s3-dpr.png)

Der Benutzer, den Sie zum Hochladen von Daten-Feeds angeben, muss über die folgenden [Berechtigungen](https://docs.aws.amazon.com/de_de/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html) verfügen:

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

[!DNL Analytics] fügt für jeden Upload in einen Amazon S3-Bucket den Bucket-Eigentümer zur BucketOwnerFullControl-ACL hinzu, unabhängig davon, ob der Bucket eine Richtlinie enthält, die dies erfordert. Weitere Informationen finden Sie unter [Was ist die BucketOwnerFullControl-Einstellung für Amazon S3-Daten-Feeds?](df-faq.md#BucketOwnerFullControl).

**Unterstützte AWS-Regionen**:
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
* cn-north-1
* cn-northwest-1


### Azure Blob

Azure Blob-sicheres Ziel mit rollenbasierter Zugriffssteuerung (RBAC) oder Shared Access Signature (SAS). Bei Auswahl der Zugriffskontrolle wird der Inhalt des Bedienfelds aktualisiert, um die entsprechenden Felder widerzuspiegeln.

**Felder - RBAC**
* *Typ:* Zieltyp von Azure Blob
* *Zugriffskontrolle:* Option zur Verwendung von RBAC oder SAS
* *Active Directory-Mandanten-ID:* Organisations-ID des Azure-Kontos
* *Anwendungs-ID:* Anwendungs-ID von Active Directory Adapter
* *Client Secret:* Azure Client Secret
* *Name des Speicherkontos:* Name des Kontos, das Datenobjekte enthält
* *Container Name:* Container, der zu einem bestimmten Speicherkonto gehört.
* *Pfad (optional):* &amp; *Report Suite-ID an Pfad anhängen:* Speicherort der abzurufenden oder zu speichernden Ressourcen

![Azure RBAC-Info](assets/dest-azure-rbac.png)

**Felder - SAS**
* *Typ:* Zieltyp von Azure Blob
* *Zugriffskontrolle:* Option zur Verwendung von RBAC oder SAS
* *Active Directory-Mandanten-ID:* ID der Azure Active Directory-Instanz
* *Anwendungs-ID:* Anwendungs-ID von Active Directory Adapter
* *Client Secret:* Azure Client Secret
* *Key Vault URI:* Speicherort des Azure Key Vault
* *Key Vault Secret Name:* Geheimer Name für den Zugriff auf sicheres Key Vault
* *Pfad (optional):* &amp; *Report Suite-ID an Pfad anhängen:* Speicherort der abzurufenden oder zu speichernden Ressourcen

![Azure SAS-Info](assets/dest-azure-sas.png)

**Felder - veraltet**
* *Typ:* Zieltyp von Azure Blob
* *Container:* Name des Azure-Containers
* *Pfad (optional):* &amp; *Report Suite-ID an Pfad anhängen:* Speicherort der abzurufenden oder zu speichernden Ressourcen
* *Konto:* Azure-Konto-Geheimnis
* *Key Vault URI:* Speicherort des Azure Key Vault
* *Key Vault Secret Name:* Geheimer Name für den Zugriff auf sicheres Key Vault

Sie müssen Ihren eigenen Prozess implementieren, um Speicherplatz auf dem Feed-Ziel zu verwalten. Adobe löscht keine Daten vom Server.
Weitere Informationen finden Sie unter [Erstellen eines Speicherkontos](https://docs.microsoft.com/de-de/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in der Dokumentation zu Microsoft Azure.

![Azure - veraltete Informationen](assets/dest-azure-dpr.png)

>[!NOTE]
>
>Sie müssen Ihren eigenen Prozess implementieren, um Speicherplatz auf dem Feed-Ziel zu verwalten. Adobe löscht keine Daten vom Server.

### FTP - veraltet

**Felder**
* *Typ:* Zieltyp des FTP
* *Host:* Endpunkt für den Zugriff auf den Host
* *Pfad (optional):* &amp; *Report Suite-ID an Pfad anhängen:* Speicherort der abzurufenden oder zu speichernden Ressourcen
* *Benutzername:* Benutzername für Host
* *Kennwort:* Kennwort für Host
* *Kennwort bestätigen:* Kennwort für Host erneut eingeben und überprüfen

![FTP-Info](assets/dest-ftp-dpr.png)

### SFTP - Nicht mehr verwendet

SFTP-Unterstützung für Daten-Feeds ist verfügbar. Erfordert einen SFTP-Host und Benutzernamen. Außerdem muss die Ziel-Site einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Feeds herunterladen.

**Felder**
* *Typ:* Zieltyp von SFTP
* *Host:* Endpunkt für den Zugriff auf den Host
* *Pfad (optional):* &amp; *Report Suite-ID an Pfad anhängen:* Speicherort der abzurufenden oder zu speichernden Ressourcen
* *RSA Public Key:* oder *DSA Public Key:* Öffentlicher Schlüssel für den Zugriff auf den Host

![SFTP-Info](assets/dest-sftp-dpr.png)

## Datenspaltendefinitionen

Es sind alle Spalten verfügbar, unabhängig davon, ob sie über Daten verfügen. Ein Daten-Feed muss mindestens eine Spalte enthalten.

* **Escapezeichen entfernen**: Beim Erfassen von Daten können einige Zeichen (z. B. Zeilenumbrüche) Probleme verursachen. Aktivieren Sie dieses Kontrollkästchen, wenn diese Zeichen aus Feed-Dateien entfernt werden sollen.
* **Komprimierungsformat**: Die verwendete Art der Komprimierung. Gzip gibt Dateien im `.tar.gz`-Format aus. Zip gibt Dateien im `.zip`-Format aus.
* **Verpackungstyp**: Eine einzelne Datei gibt die `hit_data.tsv`-Datei in einer einzigen, potenziell riesigen Datei aus. Mehrere Dateien paginieren Ihre Daten in 2-GB-Blöcke (unkomprimiert). Wenn mehrere Dateien ausgewählt sind und die nicht komprimierten Daten für das Berichtsfenster weniger als 2 GB betragen, wird eine Datei gesendet. Adobe empfiehlt die Verwendung mehrerer Dateien für die meisten Daten-Feeds.
* **Manifest**: Gibt an, ob Adobe eine [Manifestdatei](c-df-contents/datafeeds-contents.md#feed-manifest) an das Ziel senden soll, wenn für ein Feed-Intervall keine Daten erfasst wurden. Wenn Sie diese Option auswählen, erhalten Sie eine Manifestdatei ähnlich der folgenden, falls keine Daten erfasst werden:

```text
   Datafeed-Manifest-Version: 1.0
    Lookup-Files: 0
    Data-Files: 0
    Total-Records: 0
```

* **Spaltenvorlagen**: Adobe empfiehlt, beim Erstellen vieler Daten-Feeds eine Spaltenvorlage zu erstellen. Bei Auswahl einer Spaltenvorlage werden automatisch die angegebenen Spalten in der Vorlage eingefügt. Adobe stellt standardmäßig auch mehrere Vorlagen bereit.
* **Verfügbare Spalten**: Alle in Adobe Analytics verfügbaren Datenspalten. Klicken Sie auf [!UICONTROL Alle hinzufügen], um alle Spalten in einen Daten-Feed einzubeziehen.
* **Einbezogene Spalten**: Die Spalten, die in einen Daten-Feed aufgenommen werden sollen. Klicken Sie auf [!UICONTROL Alle entfernen], um alle Spalten aus einem Daten-Feed zu entfernen.
* **CSV herunterladen**: Lädt eine CSV-Datei herunter, die alle einbezogenen Spalten enthält.
