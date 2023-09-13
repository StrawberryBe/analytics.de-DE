---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anforderung erstellen.
title: Berichtsziel für eine Data Warehouse-Anforderung konfigurieren
feature: Data Warehouse
source-git-commit: 5ed0c4b8cb4b1a50cf25df1459faecadcc19ea29
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 16%

---

# Berichtsziel für eine Data Warehouse-Anforderung konfigurieren

>[!AVAILABILITY]
>
>Einige der in diesem Artikel beschriebenen Data Warehouse-Funktionen (und andere Data Warehouse-Artikel in diesem Abschnitt) sind nur in der Phase der eingeschränkten Testphase der Veröffentlichung verfügbar und sind möglicherweise noch nicht in Ihrer Umgebung verfügbar.
>
>Informationen darüber, welche Funktionen noch nicht für alle Kunden verfügbar sind, sowie Informationen über die Veröffentlichungszeitleiste dieser Funktionen finden Sie in der [Versionshinweise](/help/release-notes/latest.md).
>
>Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Im Folgenden wird beschrieben, wie Sie ein Berichtsziel für die Anfrage konfigurieren.

Informationen zum Erstellen einer Anforderung sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

>[!NOTE]
>
>Beachten Sie beim Konfigurieren eines Berichtsziels Folgendes:
>
>* Es wird empfohlen, ein Cloud-Konto oder eine E-Mail für Ihr Berichtsziel zu verwenden. Ältere FTP- und SFTP-Konten sind verfügbar, werden jedoch nicht empfohlen.
>
>* Cloud-Konten sind Ihrem Adobe Analytics-Benutzerkonto zugeordnet. Andere Benutzer können die von Ihnen konfigurierten Cloud-Konten nicht verwenden oder anzeigen.
>
>* Alle Cloud-Konten, die Sie zuvor erstellt haben [für Daten-Feeds konfiguriert](/help/export/analytics-data-feed/create-feed.md) sind für Data Warehouse verfügbar.
>
>* Cloud-Konten, die für [Importieren von Adobe Analytics-Classification-Daten](/help/components/locations/locations-manager.md) von einem Cloud-Ziel aus können bei der Konfiguration eines Berichtsziels verwendet werden. Es können jedoch keine Speicherorte verwendet werden, die für den Import von Classification-Daten konfiguriert sind.

So konfigurieren Sie das Ziel, an das Data Warehouse-Berichte gesendet werden:

1. Erstellen einer Anforderung in Adobe Analytics durch Auswahl von **[!UICONTROL Instrumente]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**].

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite Neue Data Warehouse-Anforderung die [!UICONTROL **Berichtsziel**] Registerkarte.

   ![Berichtsziel-Tab](assets/dw-report-destination.png)

1. (Bedingt) Wenn Sie zuvor ein Konto (und ein Ziel für dieses Konto) konfiguriert haben, das Sie als Berichtsziel verwenden möchten:

   1. Wählen Sie das Konto aus der [!UICONTROL **Konto auswählen**] Dropdown-Menü.

      Alle Cloud-Konten, für die Sie konfiguriert haben [Importieren von Adobe Analytics-Classification-Daten](/help/components/locations/locations-manager.md) von einem Cloud-Ziel aus angezeigt werden und verwendet werden können. Es können jedoch keine Speicherorte verwendet werden, die für den Import von Classification-Daten konfiguriert sind. Fügen Sie stattdessen ein neues Ziel wie unten beschrieben hinzu.

   1. Wählen Sie das mit dem Konto verknüpfte Ziel aus dem [!UICONTROL **Ziel auswählen**] Dropdown-Menü. <!-- Is this correct? -->

1. (Bedingt) Wenn Sie noch kein Konto konfiguriert haben:

   1. Auswählen [!UICONTROL **Konto hinzufügen**] und geben Sie dann die folgenden Informationen an:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Kontotyp**] | Wählen Sie Ihren Cloud-Kontotyp aus. Es wird empfohlen, für jeden Kontotyp ein einziges Konto mit mehreren Positionen innerhalb dieses Kontos zu haben. <p>Nach Auswahl eines Kontotyps werden die für diesen Kontotyp spezifischen Felder angezeigt. </p> |
      | [!UICONTROL **Kontoname**] | Geben Sie einen Namen für das Konto an. Dieser Name wird beim Erstellen eines Standorts angezeigt. <!-- true? --> |
      | [!UICONTROL **Kontobeschreibung**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. |

      Erweitern Sie für Konfigurationsanweisungen den folgenden Abschnitt, der dem [!UICONTROL **Kontotyp**] die Sie ausgewählt haben.

      Verwenden Sie einen der folgenden Kontotypen beim Konfigurieren eines Berichtsziels. Erweitern Sie für Konfigurationsanweisungen den Kontotyp. (zusätzlich [Legacy-Ziele](#legacy-destinations) sind ebenfalls verfügbar, werden jedoch nicht empfohlen.)

      +++Amazon S3

      Geben Sie die folgenden Informationen an, um ein Amazon S3 Role ARN-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Rollen-ARN**] | Sie müssen einen Role ARN (Amazon Resource Name) bereitstellen, den Adobe verwenden kann, um Zugriff auf das Amazon S3-Konto zu erhalten. Dazu erstellen Sie eine IAM-Berechtigungsrichtlinie für das Quellkonto, hängen die Richtlinie an einen Benutzer an und erstellen dann eine Rolle für das Zielkonto. Weitere Informationen finden Sie unter [Diese AWS-Dokumentation](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
      | [!UICONTROL **Benutzer-ARN**] | Die Benutzer-ARN (Amazon Resource Name) wird von Adobe bereitgestellt. Sie müssen diesen Benutzer an die von Ihnen erstellte Richtlinie anhängen. |

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
      | [!UICONTROL **Anwendungs-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen im **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft-Identitätsplattform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Mandanten-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen im **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft-Identitätsplattform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Key Vault-URI**] | <p>Der Pfad zum SAS-Token im Azure Key Vault.  Um Azure SAS zu konfigurieren, müssen Sie ein SAS-Token mithilfe des Azure Key Vault als Geheimnis speichern. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nachdem der Schlüssel-Vault-URI erstellt wurde, fügen Sie im Key Vault eine Zugriffsrichtlinie hinzu, um der von Ihnen erstellten Azure-Anwendung Berechtigungen zu erteilen. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zur Zuweisung einer Key Vault-Zugriffsrichtlinie](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
      | [!UICONTROL **Key Vault-Geheimnisname**] | Der geheime Name, den Sie beim Hinzufügen des Geheimnisses zum Azure Key Vault erstellt haben. In Microsoft Azure befinden sich diese Informationen im von Ihnen erstellten Key Vault im **Key Vault** Einstellungsseiten. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
      | [!UICONTROL **Geheimnis**] | Kopieren Sie das Geheimnis aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen im **Zertifikate &amp; Geheimnisse** in Ihrer Anwendung. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft-Identitätsplattform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Geben Sie die folgenden Informationen an, um ein Azure RBAC-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Anwendungs-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen im **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft-Identitätsplattform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Mandanten-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen im **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft-Identitätsplattform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Geheimnis**] | Kopieren Sie das Geheimnis aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen im **Zertifikate &amp; Geheimnisse** in Ihrer Anwendung. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft-Identitätsplattform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

+++

      +++E-Mail

      Geben Sie die folgenden Informationen an, um ein E-Mail-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Empfänger**] | Es können E-Mail-Benachrichtigungen an bestimmte Benutzerinnen und Benutzer gesendet werden, wenn der Bericht gesendet wird. Geben Sie eine einzelne E-Mail-Adresse oder eine durch Kommata getrennte Liste von E-Mail-Adressen an. <!-- How does this differ from the Notification email tab? --> |

   1. Auswählen [!UICONTROL **Ort hinzufügen**] und geben Sie dann die folgenden Informationen an: |Feld | Funktion | |—|—| | [!UICONTROL **Name**] | Der Name des Standorts.  | | [!UICONTROL **Beschreibung**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. | | [!UICONTROL **Standortkonto**] | Wählen Sie das Standortkonto aus, das Sie in [Konto hinzufügen](#add-an-account). |

   1. Im [!UICONTROL **Standorteigenschaften**] Informationen zum Kontotyp Ihres Standortkontos angeben.

      Erweitern Sie für Konfigurationsanweisungen den folgenden Abschnitt, der dem [!UICONTROL **Kontotyp**] die Sie zuvor ausgewählt haben.

      +++Amazon S3

      Geben Sie die folgenden Informationen an, um einen Amazon S3-Speicherort zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Behältername**] | Der Behälter in Ihrem Amazon S3-Konto, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass die von Adobe bereitgestellte Benutzer-ARN Zugriff auf das Hochladen von Dateien in diesen Bucket hat. |
      | [!UICONTROL **Schlüssel-Präfix**] | Der Ordner im Behälter, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: folder_name/ |

      {style="table-layout:auto"}

+++

      +++Google Cloud Platform

      Geben Sie die folgenden Informationen an, um einen Google Cloud Platform-Speicherort zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Behältername**] | Der Behälter in Ihrem GCP-Konto, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie dem von Adobe bereitgestellten Prinzipal die Berechtigung zum Hochladen von Dateien in diesen Bucket erteilt haben. Informationen zum Gewähren von Berechtigungen finden Sie unter [Einen Prinzipal zu einer Richtlinie auf Behälterebene hinzufügen](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in der Dokumentation zu Google Cloud. |
      | [!UICONTROL **Schlüssel-Präfix**] | Der Ordner im Behälter, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: folder_name/ |

      {style="table-layout:auto"}

+++

      +++Azure SAS

      Geben Sie die folgenden Informationen an, um einen Azure SAS-Speicherort zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Container-Name**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. |
      | [!UICONTROL **Schlüssel-Präfix**] | Der Ordner im Container, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Zum Beispiel, `folder_name/` |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Geben Sie die folgenden Informationen an, um einen Azure RBAC-Speicherort zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Container-Name**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie Berechtigungen zum Hochladen von Dateien in die Azure-Anwendung erteilen, die Sie zuvor erstellt haben. |
      | [!UICONTROL **Schlüssel-Präfix**] | Der Ordner im Container, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Zum Beispiel, `folder_name/` |
      | [!UICONTROL **Kontoname**] | Das Azure-Speicherkonto. |

      {style="table-layout:auto"}

+++

   1. Wählen Sie [!UICONTROL **Speichern**] aus.

      Sie können jetzt Daten in das Konto und den Speicherort importieren, die Sie konfiguriert haben.

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der [!UICONTROL **Berichtsoptionen**] Registerkarte. Weitere Informationen finden Sie unter [Berichtsoptionen für eine Data Warehouse-Anforderung konfigurieren](/help/export/data-warehouse/create-request/dw-request-report-options.md).

## Veraltete Ziele

>[!IMPORTANT]
>
>Die in diesem Abschnitt beschriebenen Ziele sind veraltet und werden nicht empfohlen. Verwenden Sie stattdessen eines der folgenden Ziele beim Erstellen eines Data Warehouse-Ziels: Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS oder E-Mail. Weitere Informationen zu den einzelnen empfohlenen Zielen finden Sie in den Informationen oben.

Die folgenden Informationen enthalten Konfigurationsinformationen für die einzelnen alten Ziele:

### FTP

Data Warehouse-Daten können an einen Adobe- oder kundengehosteten FTP-Speicherort bereitgestellt werden. Erfordert einen FTP-Host, einen Benutzernamen und ein Kennwort. Verwenden Sie das Pfadfeld, um Feed-Dateien in einem Ordner zu platzieren. Ordner müssen bereits vorhanden sein; Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist.

Verwenden Sie beim Ausfüllen der verfügbaren Felder die folgenden Informationen:

* [!UICONTROL **Host**]: Geben Sie die gewünschte FTP-Ziel-URL ein. Zum Beispiel `ftp://ftp.omniture.com`.
* [!UICONTROL **Pfad**]: Kann leer gelassen werden
* [!UICONTROL **Benutzername**]: Geben Sie den Benutzernamen ein, um sich bei der FTP-Site anzumelden.
* [!UICONTROL **Kennwort und Kennwort bestätigen**]: Geben Sie das Kennwort ein, um sich bei der FTP-Site anzumelden.

### SFTP

SFTP-Unterstützung für Data Warehouse ist verfügbar. Erfordert einen SFTP-Host und Benutzernamen. Außerdem muss die Ziel-Site einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Data Warehouse-Ziels herunterladen.

### S3

Sie können Warehouse-Daten direkt an Amazon S3-Behälter senden. Dieser Zieltyp erfordert einen Behälternamen, eine Zugriffsschlüssel-ID und einen geheimen Schlüssel. Weitere Informationen finden Sie unter [Benennungsanforderungen für Amazon S3-Behälter](https://docs.aws.amazon.com/de_de/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in der Amazon S3-Dokumenation.

Der Benutzer, den Sie zum Hochladen von Data Warehouse-Daten angeben, muss über Folgendes verfügen: [Berechtigungen](https://docs.aws.amazon.com/de_de/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html):

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