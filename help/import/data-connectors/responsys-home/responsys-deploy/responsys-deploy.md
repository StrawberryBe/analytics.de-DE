---
description: 'null'
title: Bereitstellen der Integration
uuid: 5abf6d49-b05b-4e0f-8d9b-bb02d8f1c84a
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 100%

---


# Bereitstellen der Integration {#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert:

## Abschließen des Adobe-Integrationsassistenten {#completing-the-adobe-integration-wizard}

Schritte zum Abschließen des Integrationsassistenten auf der Data Connectors-Oberfläche.

1. Navigieren Sie in der Adobe Experience Cloud zum Bereich „Data Connectors“ (früher Genesis).
1. Starten Sie den Responsys-Integrationsassistenten.
1. Wählen Sie die gewünschte Report Suite aus. Geben Sie dann einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:

   | Element | Beschreibung |
   |---|---|
   | E-Mail  Adresse | Die E-Mail-Adresse des Hauptkontakts. |
   | Beschreibung | (Optional) Beschreibung für die Einrichtung dieser Integration |
   | Konto-ID | Wenden Sie sich dazu unter support@responsys.com an das Responsys-Supportteam |

1. Konfigurieren Sie die folgenden **[!UICONTROL Variablenzuordnungselemente]**:

   | Element | Beschreibung |
   |---|---|
   | Nachrichten-ID | Wählen Sie eine eVar, um Nachrichten-IDs in Echtzeit zu erfassen. |
   | Empfänger-ID | Wählen Sie eine eVar, um Empfänger-IDs in Echtzeit zu erfassen. |
   | Rücksendungen insgesamt | Wählen Sie ein numerisches Ereignis aus, um tägliche Absprünge von Responsys zu erhalten. |
   | E-Mail gesendet | Wählen Sie ein numerisches Ereignis aus, um tägliche Sendungen von Responsys zu erhalten. |
   | Angeklickt | Wählen Sie ein numerisches Ereignis aus, um die tägliche Gesamtzahl der Klicks von Responsys zu erhalten. |
   | Geöffnet | Wählen Sie ein numerisches Ereignis aus, um die tägliche Gesamtzahl der geöffneten Elemente von Responsys zu erhalten. |
   | Abo storniert | Wählen Sie ein numerisches Ereignis aus, um die täglichen gekündigten Abonnements von Responsys zu erhalten. |
   | Lieferung | Wählen Sie ein numerisches Ereignis aus, um die täglichen Lieferungen von Responsys zu erhalten. |

1. Aktivieren Sie den Datenzugriff und konfigurieren Sie die Datenerfassung.
   1. Benennen Sie Klassifizierungen nach Bedarf um.
   1. **[!UICONTROL Partnersegmente]** sind Remarketing-Standardsegmente, die in Ihrer Integration enthalten sind.
   1. Aktivieren Sie unter **[!UICONTROL Zugriffsanforderungen]** das Kontrollkästchen, damit Produktinformationen in täglichen Remarketing-Segmenten nach Responsys exportiert werden können.
   1. Konfigurieren Sie, ob Sie IDs durch manuelles Aktualisieren Ihres Analytics-Erfassungscodes oder durch Verwendung der automatisierten Lösung erfassen werden. Wenn Sie **[!UICONTROL Automatisierte Lösung]** auswählen, müssen Sie die Parameter angeben, die in E-Mail-Links zur Übergabe von IDs verwendet werden.
1. Überprüfen Sie alle Konfigurationselemente. Klicken Sie dann auf **[!UICONTROL Jetzt aktivieren]**.

## Konfigurieren im Responsys-System {#configuring-within-the-responsys-system}

Zur Aktivierung der Integration wenden Sie sich an den Responsys-Support.

Nach Abschluss des Integrationsassistenten müssen Sie die Integration in Responsys aktivieren.

Wenden Sie sich hierzu unter support@responsys.com an das Supportteam von Responsys.
