---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anfrage erstellen.
title: Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage
feature: Data Warehouse
exl-id: 3c7faea3-4d90-4274-88f3-e9337c94155f
source-git-commit: 4e4b5e1c362778223be01f78b173a698c53f9b32
workflow-type: tm+mt
source-wordcount: '2430'
ht-degree: 99%

---

# Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Im Folgenden wird beschrieben, wie Sie ein Berichtsziel für die Anfrage konfigurieren.

Informationen zum Erstellen einer Anfrage sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

>[!NOTE]
>
>Beachten Sie bei der Konfiguration eines Berichtsziels Folgendes:
>
>* Es wird empfohlen, ein Cloud-Konto oder eine E-Mail-Adresse für Ihr Berichtsziel zu verwenden. Alte FTP- und SFTP-Konten sind verfügbar, werden jedoch nicht empfohlen.
>
>* Alle Cloud-Konten, die Sie zuvor für [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder zum [Importieren von Adobe Analytics-Klassifizierungsdaten](/help/components/locations/locations-manager.md) konfiguriert haben, sind für die Verwendung für Data Warehouse verfügbar. Es können jedoch keine Speicherorte verwendet werden, die für den Import von Klassifizierungsdaten konfiguriert sind.
>
>* Cloud-Konten sind mit Ihrem Adobe Analytics-Benutzerkonto verknüpft. Andere Benutzende können die von Ihnen konfigurierten Cloud-Konten nicht verwenden oder anzeigen.
>

Konfigurieren des Ziels, an das die Data Warehouse-Berichte gesendet werden:

1. Beginnen Sie, falls noch nicht geschehen, mit der Erstellung einer Anforderung in Adobe Analytics, indem Sie **[!UICONTROL Instrumente]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**].

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite „Neue Data Warehouse-Anfrage“ die Registerkarte [!UICONTROL **Berichtsziel**] aus.

   ![Registerkarte „Berichtsziel“](assets/dw-report-destination.png)

1. (Bedingt) Wenn ein Konto (und ein Ziel in diesem Konto) bereits konfiguriert wurde und Sie es als Berichtsziel verwenden möchten:

   1. (Optional) Wenn Sie Systemadmin sind, ist die Option [!UICONTROL **Alle Ziele anzeigen**] verfügbar. Aktivieren Sie diese Option, um Zugriff auf alle Konten und Speicherorte zu erhalten, die von Benutzenden in der Organisation erstellt wurden.

   1. Wählen Sie das Konto aus dem Dropdown-Menü [!UICONTROL **Konto auswählen**] aus.

      Alle Cloud-Konten, die Sie zum [Importieren von Adobe Analytics-Klassifizierungsdaten](/help/components/locations/locations-manager.md) von einem Cloud-Ziel konfiguriert haben, werden hier angezeigt und können verwendet werden. Es können jedoch keine Speicherorte verwendet werden, die für den Import von Klassifizierungsdaten konfiguriert sind. Fügen Sie stattdessen ein neues Ziel wie unten beschrieben hinzu.

   1. Wählen Sie das mit dem Konto verknüpfte Ziel aus dem Dropdown-Menü [!UICONTROL **Ziel auswählen**] aus. <!-- Is this correct? -->

1. (Bedingt) Wenn Sie noch kein Konto konfiguriert haben:

   1. Wählen Sie [!UICONTROL **Konto hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Kontotyp**] | Wählen Sie Ihren Cloud-Kontotyp aus. Es wird empfohlen, für jeden Kontotyp ein einziges Konto mit mehreren Speicherorten nach Bedarf innerhalb dieses Kontos zu führen. <p>Nach Auswahl eines Kontotyps werden die für diesen Kontotyp spezifischen Felder angezeigt. </p> |
      | [!UICONTROL **Kontoname**] | Geben Sie einen Namen für das Konto an. Dieser Name wird beim Erstellen eines Speicherorts angezeigt. <!-- true? --> |
      | [!UICONTROL **Kontobeschreibung**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. |

      Erweitern Sie für Konfigurationsanweisungen den folgenden Abschnitt, der dem ausgewählten [!UICONTROL **Kontotyp**] entspricht.

      Verwenden Sie beim Konfigurieren eines Berichtsziels einen der folgenden Kontotypen. Erweitern Sie den Kontotyp, um Konfigurationsanweisungen anzuzeigen. (Zusätzliche [alte Ziele](#legacy-destinations) sind ebenfalls verfügbar, werden jedoch nicht empfohlen.)

      +++Amazon S3

      Geben Sie die folgenden Informationen an, um ein Amazon S3-Rollen-ARN-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Rollen-ARN**] | Sie müssen einen Rollen-ARN (Amazon Resource Name) bereitstellen, den Adobe verwenden kann, um Zugriff auf das Amazon S3-Konto zu erhalten. Erstellen Sie hierfür eine IAM-Berechtigungsrichtlinie für das Quellkonto, hängen Sie die Richtlinie an eine Benutzerin oder einen Benutzer an und erstellen Sie dann eine Rolle für das Zielkonto. Spezifische Informationen finden Sie in [dieser AWS-Dokumentation](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/).<p>Informationen zum Einrichten der Berechtigung für den Bucket finden Sie im Artikel [Wie kann ich kontoübergreifenden Zugriff auf Objekte in Amazon S3-Buckets gewähren?](https://repost.aws/knowledge-center/cross-account-access-s3) im Amazon-Wissenszentrum |
      | [!UICONTROL **Benutzer-ARN**] | Der Benutzer-ARN (Amazon Resource Name) wird von Adobe bereitgestellt. Sie müssen diese Benutzerin oder diesen Benutzer an die von Ihnen erstellte Richtlinie anhängen. |

      {style="table-layout:auto"}

+++

      +++Google Cloud Platform

      Geben Sie die folgenden Informationen an, um ein Google Cloud Platform-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Projekt-ID**] | Ihre Google Cloud-Projekt-ID. Siehe [Dokumentation zu Google Cloud zum Abrufen einer Projekt-ID](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

      {style="table-layout:auto"}

+++

      +++Azure SAS

      Geben Sie die folgenden Informationen an, um ein Azure SAS-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Anwendungs-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Mandanten-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Key Vault-URI**] | <p>Der Pfad zum SAS-Token im Azure Key Vault.  Um Azure SAS zu konfigurieren, müssen Sie ein SAS-Token mithilfe des Azure Key Vault als Geheimnis speichern. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/de-de/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nachdem die Key Vault-URI erstellt wurde:<ul><li>Fügen Sie im Key Vault eine Zugriffsrichtlinie hinzu, um der von Ihnen erstellten Azure-Anwendung Berechtigungen zu erteilen.</li><li>Stellen Sie sicher, dass der Anwendungs-ID die `Key Vault Certificate User` integrierte Rolle für den Zugriff auf den URI des Key Vault zugewiesen wurde.</br><p>Weitere Informationen finden Sie unter [Integrierte Azure-Rollen](https://learn.microsoft.com/de-de/azure/role-based-access-control/built-in-roles).</p></li></ul><p>Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation für die Zuweisung einer Key Vault-Zugriffsrichtlinie](https://learn.microsoft.com/de-de/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
      | [!UICONTROL **Key Vault-Geheimnisname**] | Der Geheimnisname, den Sie beim Hinzufügen des Geheimnisses zum Azure Key Vault erstellt haben. In Microsoft Azure befinden sich diese Informationen im von Ihnen erstellten Key Vault auf den **Key Vault**-Einstellungsseiten. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/de-de/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
      | [!UICONTROL **Geheimnis**] | Kopieren Sie das Geheimnis aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Zertifikate und Geheimnisse** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Geben Sie die folgenden Informationen an, um ein Azure RBAC-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Anwendungs-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Mandanten-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Geheimnis**] | Kopieren Sie das Geheimnis aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Zertifikate und Geheimnisse** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

+++

      +++E-Mail

      Geben Sie die folgenden Informationen an, um ein E-Mail-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Empfangende**] | Es können E-Mail-Benachrichtigungen an bestimmte Benutzende gesendet werden, wenn der Bericht gesendet wird. Geben Sie eine einzelne E-Mail-Adresse oder eine durch Kommata getrennte Liste von E-Mail-Adressen an. <!-- How does this differ from the Notification email tab? --> |

   1. Wählen Sie [!UICONTROL **Speicherort hinzufügen**] aus und geben Sie dann die folgenden Informationen an:
|Feld | Funktion |
|---------|----------|
| [!UICONTROL **Name**] | Der Name des Speicherorts.  |
| [!UICONTROL **Beschreibung**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. |
| [!UICONTROL **Speicherortkonto**] | Wählen Sie das Speicherortkonto aus, das Sie in [Konto hinzufügen](#add-an-account) erstellt haben. |

   1. Geben Sie im Abschnitt [!UICONTROL **Speicherorteigenschaften**] spezifische Informationen zum Kontotyp Ihres Speicherortkontos an.

      Erweitern Sie für Konfigurationsanweisungen den folgenden Abschnitt, der dem [!UICONTROL **Kontotyp**] entspricht, den Sie zuvor ausgewählt haben.

      +++Amazon S3

      Geben Sie die folgenden Informationen an, um einen Amazon S3-Speicherort zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Bucket-Name**] | Der Bucket in Ihrem Amazon S3-Konto, an den Adobe Analytics-Daten gesendet werden sollen. <p>Stellen Sie sicher, dass der von Adobe bereitgestellte Benutzer-ARN über die `S3:PutObject`-Berechtigung verfügt, um Dateien in diesen Bucket hochzuladen. Diese Berechtigung ermöglicht es dem Benutzer-ARN, ursprüngliche Dateien hochzuladen und Dateien für nachfolgende Uploads zu überschreiben.</p> |
      | [!UICONTROL **Schlüssel-Präfix**] | Der Ordner im Bucket, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. (Beispiel: Ordnername/) |

      {style="table-layout:auto"}

+++

      +++Google Cloud Platform

      Geben Sie die folgenden Informationen an, um einen Google Cloud Platform-Speicherort zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Bucket-Name**] | Der Bucket in Ihrem GCP-Konto, an den Adobe Analytics-Daten gesendet werden sollen. <p>Stellen Sie sicher, dass Sie dem von Adobe bereitgestellten Prinzipal eine der folgenden Berechtigungen erteilt haben:<ul><li>`roles/storage.objectCreator`: Verwenden Sie diese Berechtigung, wenn Sie den Prinzipal so einschränken möchten, dass nur Dateien in Ihrem GCP-Konto erstellt werden. </br>**Wichtig:** Wenn Sie diese Berechtigung mit geplanten Berichten einsetzen, müssen Sie für jeden neuen geplanten Export einen eindeutigen Dateinamen verwenden. Andernfalls schlägt die Berichterstellung fehl, da der Prinzipal nicht berechtigt ist, vorhandene Dateien zu überschreiben.</li><li>`roles/storage.objectUser`: Verwenden Sie diese Berechtigung, wenn der Prinzipal berechtigt sein soll, Dateien in Ihrem GCP-Konto anzuzeigen, aufzulisten, zu aktualisieren und zu löschen.</br>Mit dieser Berechtigung kann der Prinzipal vorhandene Dateien bei nachfolgenden Uploads überschreiben, ohne dass für jeden neuen geplanten Export automatisch eindeutige Dateinamen generiert werden müssen.</li></ul><p>Informationen zum Gewähren von Berechtigungen finden Sie in der Google Cloud-Dokumentation unter [Hauptkonto zu einer Richtlinie auf Bucket-Ebene hinzufügen](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add).</p> |
      | [!UICONTROL **Schlüsselpräfix**] | Der Ordner im Bucket, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. (Beispiel: Ordnername/) |

      {style="table-layout:auto"}

+++

      +++Azure SAS

      Geben Sie die folgenden Informationen an, um einen Azure SAS-Speicherort zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Container-Name**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. |
      | [!UICONTROL **Schlüsselpräfix**] | Der Ordner im Container, in dem Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/`<p>Stellen Sie sicher, dass der SAS-Token-Speicher, den Sie bei der Konfiguration des Azure SAS-Kontos im Feld „Key Vault-Geheimnisname“ angegeben haben, über die `Write`-Berechtigung verfügt. Dadurch kann das SAS-Token Dateien in Ihrem Azure-Container erstellen. <p>Wenn Sie möchten, dass das SAS-Token auch Dateien überschreibt, stellen Sie sicher, dass der SAS-Token-Speicher die `Delete`-Berechtigung besitzt.</p><p>Weitere Informationen finden Sie in der Azure Blob Storage-Dokumentation unter [Blob Storage-Ressourcen](https://learn.microsoft.com/de-de/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources).</p> |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Geben Sie die folgenden Informationen an, um einen Azure RBAC-Speicherort zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Container-Name**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie Berechtigungen zum Hochladen von Dateien in die Azure-Anwendung erteilen, die Sie zuvor erstellt haben. |
      | [!UICONTROL **Schlüsselpräfix**] | Der Ordner im Container, in dem Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/`<p>Stellen Sie sicher, dass die Anwendungs-ID, die Sie beim Konfigurieren des Azure RBAC-Kontos angegeben haben, der Rolle `Storage Blob Data Contributor` zugeteilt wurde, damit der Zugriff auf den Container (Ordner) möglich ist.</p> <p>Weitere Informationen finden Sie unter [Integrierte Azure-Rollen](https://learn.microsoft.com/de-de/azure/role-based-access-control/built-in-roles).</p> |
      | [!UICONTROL **Kontoname**] | Das Azure-Speicherkonto. |

      {style="table-layout:auto"}

+++

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der Registerkarte [!UICONTROL **Berichtsoptionen**] fort. Weitere Informationen finden Sie unter [Konfigurieren von Berichtsoptionen für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-report-options.md).

## Veraltete Ziele

>[!IMPORTANT]
>
>Die in diesem Abschnitt beschriebenen Ziele sind veraltet und werden nicht empfohlen. Verwenden Sie stattdessen eines der folgenden Ziele beim Erstellen eines Data Warehouse-Ziels: Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS oder E-Mail. Weitere Informationen zu den einzelnen empfohlenen Zielen finden Sie in den Informationen oben.

Die folgenden Informationen enthalten Konfigurationsinformationen für die einzelnen veralteten Ziele:

### FTP

Data Warehouse-Daten können für einen von Adobe oder auf Kundenseite gehosteten FTP-Speicherort bereitgestellt werden. Erfordert einen FTP-Host, einen Benutzernamen und ein Kennwort. Verwenden Sie das Pfadfeld, um Feed-Dateien in einem Ordner zu platzieren. Ordner müssen bereits vorhanden sein; Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist.

Verwenden Sie beim Ausfüllen der verfügbaren Felder die folgenden Informationen:

#### Kontofelder

* [!UICONTROL **Kontoname**]: Der Name des FTP-Kontos.

* [!UICONTROL **Kontobeschreibung**]: Eine Beschreibung des FTP-Kontos.

* [!UICONTROL **Host-Name**]: Geben Sie die gewünschte FTP-Ziel-URL ein. Zum Beispiel `ftp.company.com`.

  >[!NOTE]
  >
  >  Schließen Sie `ftp://` am Anfang der URL nicht mit ein.

* [!UICONTROL **Benutzername**]: Geben Sie den Benutzernamen ein, um sich bei der FTP-Site anzumelden.

* [!UICONTROL **Kennwort und Kennwort bestätigen**]: Geben Sie das Kennwort ein, um sich bei der FTP-Site anzumelden.

#### Speicherortfelder

* [!UICONTROL **Speicherortname**]: Der Name des Speicherorts im FTP-Konto, an den Dateien gesendet werden sollen.

* [!UICONTROL **Speicherortbeschreibung**]: Eine Beschreibung des Speicherorts im FTP-Konto.

* [!UICONTROL **Verzeichnispfad**]: Der Pfad zum Speicherort im FTP-Konto.

### SFTP

SFTP-Unterstützung für Data Warehouse ist verfügbar. Erfordert einen SFTP-Host und Benutzernamen. Außerdem muss die Ziel-Site einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Data Warehouse-Ziels herunterladen.

Verwenden Sie beim Ausfüllen der verfügbaren Felder die folgenden Informationen:

#### Kontofelder

* [!UICONTROL **Kontoname**]: Der Name des FTP-Kontos.

* [!UICONTROL **Kontobeschreibung**]: Eine Beschreibung des FTP-Kontos.

* [!UICONTROL **Host-Name**]: Geben Sie die gewünschte SFTP-Ziel-URL ein. Zum Beispiel `sftp.company.com`.

  >[!NOTE]
  >
  >  Schließen Sie `sftp://` am Anfang der URL nicht mit ein.

* [!UICONTROL **Benutzername**]: Geben Sie den Benutzernamen ein, um sich bei der SFTP-Site anzumelden.

* [!UICONTROL **Beim Hochladen temporäre Dateierweiterung verwenden**]: Wenn diese Option aktiviert ist, wird die Dateierweiterung `.part` während des Upload-Prozesses verwendet. Lassen Sie diese Option aktiviert, sofern der SFTP-Server die Änderung von Dateinamen nach Abschluss des Uploads zulässt.

* [!UICONTROL **Öffentliche Schlüssel**]: Laden Sie den entsprechenden öffentlichen Schlüssel herunter, wenn Sie das Data Warehouse-Ziel erstellen.

#### Speicherortfelder

* [!UICONTROL **Speicherortname**]: Der Name des Speicherorts im SFTP-Konto, an den Dateien gesendet werden sollen.

* [!UICONTROL **Speicherortbeschreibung**]: Eine Beschreibung des Speicherorts im SFTP-Konto.

* [!UICONTROL **Verzeichnispfad**]: Der Pfad zum Speicherort im SFTP-Konto.

Weitere Informationen zur SFTP-Konfiguration finden Sie unter [Senden von Data Warehouse-Anfragen an SFTP-Server](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md).

### S3

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

### Azure Blob

Data Warehouse unterstützt Azure Blob-Ziele. Erfordert einen Container, ein Konto und einen Schlüssel. Amazon verschlüsselt die Daten automatisch während der Ruhezeit. Wenn Sie die Daten herunterladen, werden sie automatisch entschlüsselt. Weitere Informationen finden Sie unter [Erstellen eines Speicherkontos](https://docs.microsoft.com/de-de/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in der Dokumentation zu Microsoft Azure.

>[!NOTE]
>
>Sie müssen Ihren eigenen Prozess implementieren, um Speicherplatz auf dem Data Warehouse-Ziel zu verwalten. Adobe löscht keine Daten vom Server.
