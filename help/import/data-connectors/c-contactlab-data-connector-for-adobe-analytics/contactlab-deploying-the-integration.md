---
description: Stellen Sie die ContactLab-Integration für die Verwendung in Adobe Analytics bereit.
title: Bereitstellen der Integration
uuid: df3f24c9-d2e3-489e-b97e-e1af0d5dd1fa
translation-type: tm+mt
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 97%

---


# Bereitstellen der Integration {#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert:

## Abschließen des Adobe-Integrationsassistenten {#completing-the-adobe-integration-wizard}

Schritte zum Abschließen des Integrationsassistenten auf der Data Connectors-Oberfläche.

1. Navigieren Sie in der Adobe Experience Cloud zum Bereich „Data Connectors“ (früher Genesis).
1. Starten Sie den ContactLab-Integrationsassistenten.
1. Wählen Sie die gewünschte Report Suite aus. Geben Sie dann einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:

   | Element | Beschreibung |
   |---|---|
   | E-Mail  Adresse | Die E-Mail-Adresse des Hauptkontakts. |
   | Beschreibung | (Optional) Beschreibung für die Einrichtung dieser Integration |

1. Konfigurieren Sie die folgenden **[!UICONTROL Variablenzuordnungselemente]**:

   | Element | Beschreibung |
   |---|---|
   | Link-ID | Wählen Sie eine eVar, um Link-IDs in Echtzeit zu erfassen. |
   | Nachrichten-ID | Wählen Sie eine eVar, um Nachrichten-IDs in Echtzeit zu erfassen. |
   | Empfänger-ID | Wählen Sie eine eVar, um Empfänger-IDs in Echtzeit zu erfassen. |
   | Absprünge | Wählen Sie ein numerisches Ereignis aus, um tägliche Absprünge von ContactLab zu erhalten. |
   | Gesendet | Wählen Sie ein numerisches Ereignis aus, um tägliche Sendungen von ContactLab zu erhalten. |
   | Angeklickt | Wählen Sie ein numerisches Ereignis aus, um die tägliche Gesamtzahl der Klicks von ContactLab zu erhalten. |
   | Geöffnet | Wählen Sie ein numerisches Ereignis aus, um die tägliche Gesamtzahl der geöffneten Elemente von ContactLab zu erhalten. |
   | Abo storniert | Wählen Sie ein numerisches Ereignis aus, um die täglichen gekündigten Abonnements von ContactLab zu erhalten. |

1. Aktivieren Sie den Datenzugriff und konfigurieren Sie die Datenerfassung.
   1. Benennen Sie Klassifizierungen nach Bedarf um.
   1. **[!UICONTROL Partnersegmente]** sind Remarketing-Standardsegmente, die in Ihrer Integration enthalten sind.
   1. Wählen Sie unter **[!UICONTROL Ihre Segmente]** benutzerspezifische Segmente aus, die Sie in diese Integration aufnehmen möchten. Sie können weitere benutzerspezifische Segmente im Admin-Bereich erstellen.
   1. Aktivieren Sie unter **[!UICONTROL Zugriffsanforderungen]** das Kontrollkästchen, damit Produktinformationen in täglichen Remarketing-Segmenten nach ContactLab exportiert werden können.
   1. Benennen Sie berechnete Metriken nach Bedarf um.
   1. Konfigurieren Sie, ob Sie IDs durch manuelles Aktualisieren Ihres Analytics-Erfassungscodes oder durch Verwendung der automatisierten Lösung erfassen werden. Wenn Sie **[!UICONTROL Automatisierte Lösung]** auswählen, müssen Sie die Parameter angeben, die in E-Mail-Links zur Übergabe von IDs verwendet werden.
1. Überprüfen Sie alle Konfigurationselemente. Klicken Sie dann auf **[!UICONTROL Jetzt aktivieren]**.

## Überprüfen der Integration {#verifying-the-integration}

Anzeigen der Konfiguration der ContactLab-Integration in der Adobe Experience Cloud

1. Anzeigen des Protokolls zu den Integrationsaktivitäten.
   1. Navigieren Sie in Adobe Experience Cloud zu **[!UICONTROL Support]** > **[!UICONTROL Protokoll zu den Integrationsaktivitäten]**.

      ![](assets/integration_activity_log.png)

   1. Suchen Sie nach Einträgen wie **[!UICONTROL Classification-Daten wurden erfolgreich importiert]**, **[!UICONTROL Metrikdaten wurden erfolgreich importiert]** und **[!UICONTROL Metrikdaten wurden erfolgreich exportiert]**. Diese Einträge sollten innerhalb 1 Tags nach erfolgreicher Bereitstellung angezeigt werden.
1. Zeigen Sie Ihre Berichtsdaten in Adobe Analytics an.
   1. Navigieren Sie zu **[!UICONTROL Benutzerspez. Konversion]** > **[!UICONTROL Benutzerspez. Konversion 1-10]** > **[!UICONTROL Nachrichten-ID-Berichte]**.

      ![](assets/reporting.png)

   1. Suchen Sie nach ContactLab-Berichten. Diese Daten sollten innerhalb von 24–48 Stunden nach erfolgreicher Bereitstellung angezeigt werden.
