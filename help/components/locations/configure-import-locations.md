---
description: Konfigurieren Sie das Cloud-Importkonto und den Speicherort, an den Classification-Daten hochgeladen werden können.
keywords: Analysis Workspace
title: Konfigurieren von Cloud-Importspeicherorten
feature: Classifications
source-git-commit: 4efb0623d734419c376ca5f2bf2bbd94097ee4e4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 8%

---

# Konfigurieren von Cloud-Importspeicherorten

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

Bevor Sie Adobe Analytics-Classification-Daten aus einem Cloud-Ziel importieren können, müssen Sie das Konto und den Speicherort in diesem Konto hinzufügen und konfigurieren, in dem die Classification-Daten erfasst werden sollen.

Dieser Prozess besteht aus dem Hinzufügen und Konfigurieren des Kontos (z. B. Amazon S3 Role ARN, Google Cloud Platform usw.) und des Speicherorts innerhalb des Kontos (z. B. eines Ordners innerhalb des Kontos).

So konfigurieren Sie einen Cloud-Importspeicherort:

1. Sie müssen ein Konto hinzufügen, bevor Sie einen Ort hinzufügen können. Fügen Sie, falls noch nicht geschehen, ein Konto wie unter [Konfigurieren von Cloud-Importkonten](/help/components/locations/configure-import-accounts.md).
1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] > [!UICONTROL **Standorte**].
1. Im [!UICONTROL Standorte] Seite, wählen Sie die [!UICONTROL **Standorte**] Registerkarte.
1. Auswählen [!UICONTROL **Ort hinzufügen**]. <!-- add screenshot? -->

   Das Dialogfeld Standort wird angezeigt.
1. Geben Sie die folgenden Informationen an: |Feld | Funktion | |—|—| | [!UICONTROL **Name**] | Der Name des Standorts.  | | [!UICONTROL **Beschreibung**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. | | [!UICONTROL **Standortkonto**] | Wählen Sie das Standortkonto aus, das Sie in erstellt haben. [Konto hinzufügen](#add-an-account). |

1. Im [!UICONTROL **Standorteigenschaften**] -Abschnitt Informationen zum Kontotyp Ihres Standortkontos angeben.

   Erweitern Sie für Konfigurationsanweisungen den folgenden Abschnitt, der dem Kontotyp entspricht, den Sie in der Variablen [!UICONTROL **Standortkonten**] -Feld.

   +++Amazon S3 Role ARN

   Geben Sie die folgenden Informationen an, um einen Amazon S3 Role ARN-Speicherort zu konfigurieren:

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Behältername**] | Der Behälter in Ihrem Amazon S3-Konto, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass die von Adobe bereitgestellte Benutzer-ARN Zugriff auf das Hochladen von Dateien in diesen Behälter hat. |
   | [!UICONTROL **Schlüssel-Präfix**] | Der Ordner im Behälter, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: folder_name/ |

   {style="table-layout:auto"}

+++

   +++Google Cloud Platform

   Geben Sie die folgenden Informationen an, um einen Google Cloud Platform-Speicherort zu konfigurieren:

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Behältername**] | Der Behälter in Ihrem GCP-Konto, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie dem von Adobe bereitgestellten Prinzipal Berechtigungen zum Hochladen von Dateien in diesen Bucket erteilt haben. |
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