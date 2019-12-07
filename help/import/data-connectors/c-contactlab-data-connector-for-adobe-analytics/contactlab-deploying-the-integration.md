---
description: 'null'
title: Bereitstellen der Integration
uuid: df3f24c9-d2e3-489e-b97e-e1af0d5dd1fa
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bereitstellen der Integration{#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert:

## Führen Sie den Adobe-Integrationsassistenten aus{#completing-the-adobe-integration-wizard}

Schritte zum Abschließen des Integrationsassistenten in der Data Connectors-Oberfläche.

1. Navigieren Sie zum Bereich Data Connectors (früher Genesis) in der Adobe Experience Cloud.
1. Starten Sie den Integrationsassistenten von ContactLab.
1. Wählen Sie die gewünschte Report Suite und geben Sie einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:

   | Element | Beschreibung |
   |---|---|
   | E-Mail-Adresse | Die E-Mail-Adresse des Hauptkontakts |
   | Beschreibung | (Optional) Beschreibung für diese Integration |

1. Konfigurieren Sie die folgenden **[!UICONTROL Variablenzuordnungen]** :

   | Element | Beschreibung |
   |---|---|
   | Link-ID | Wählen Sie eine eVar, um Link-IDs in Echtzeit zu erfassen. |
   | Nachrichten-ID | Wählen Sie eine eVar, um Nachrichten-IDs in Echtzeit zu erfassen. |
   | Recipient ID | Wählen Sie eine eVar, um Empfänger-IDs in Echtzeit zu erfassen. |
   | Absprünge | Wählen Sie ein numerisches Ereignis aus, um tägliche Absprünge von ContactLab zu erhalten. |
   | Gesendet | Wählen Sie ein numerisches Ereignis aus, das täglich von ContactLab gesendet werden soll. |
   | Angeklickt | Wählen Sie ein numerisches Ereignis aus, um die täglichen Klicks von ContactLab zu empfangen. |
   | Geöffnet | Wählen Sie ein numerisches Ereignis aus, um die tägliche Gesamtanzahl aus ContactLab zu erhalten. |
   | Nicht abonniert | Wählen Sie ein numerisches Ereignis aus, um tägliche Abmeldung von ContactLab zu erhalten. |

1. Aktivieren Sie den Datenzugriff und konfigurieren Sie die Datenerfassung.
   1. Benennen Sie Klassifizierungen nach Bedarf um.
   1. **[!UICONTROL Partnersegmente]** sind Standard-Remarketing-Segmente, die in Ihrer Integration enthalten sind.
   1. Wählen Sie unter **[!UICONTROL Segmente]** benutzerdefinierte Segmente aus, die Sie in diese Integration einbeziehen möchten. Sie können weitere benutzerdefinierte Segmente im Admin-Bedienfeld erstellen.
   1. Aktivieren Sie unter **[!UICONTROL Zugriffsanforderungen]** das Kontrollkästchen, um den Export von Produktinformationen in tägliche Remarketingsegmente an ContactLab zuzulassen.
   1. Benennen Sie berechnete Metriken nach Bedarf um.
   1. Konfigurieren Sie, ob Sie IDs erfassen, indem Sie Ihren Analytics-Erfassungscode manuell aktualisieren oder die automatisierte Lösung verwenden. Wenn Sie **[!UICONTROL Automatisierte Lösung]** auswählen, müssen Sie die Parameter einbeziehen, die in E-Mail-Links verwendet werden, um IDs zu übermitteln.
1. Überprüfen Sie alle Konfigurationselemente und klicken Sie auf Jetzt **[!UICONTROL aktivieren]**.

## Integration überprüfen{#verifying-the-integration}

Anzeigen der Konfiguration der ContactLab-Integration in der Adobe Experience Cloud

1. Anzeigen des Integrationsaktivitätsprotokolls.
   1. Navigieren Sie in Adobe Experience Cloud zu **[!UICONTROL Support]** &gt; **[!UICONTROL Integrationsaktivitätsprotokoll]**.

      ![](assets/integration_activity_log.png)

   1. Suchen Sie nach Einträgen wie **[!UICONTROL Klassifizierungsdaten, die erfolgreich]** importiert wurden, **[!UICONTROL Metrikdaten erfolgreich]** importiert wurden und **[!UICONTROL Metrikdaten erfolgreich]** exportiert wurden. Diese Einträge sollten innerhalb eines Tages nach erfolgreicher Bereitstellung angezeigt werden.
1. Zeigen Sie Ihre Berichtsdaten in Adobe Analytics an.
   1. Navigieren Sie zu **[!UICONTROL Custom Conversion]** &gt; **[!UICONTROL Custom Conversion 1-10]** &gt; **[!UICONTROL Message ID Reports]**.

      ![](assets/reporting.png)

   1. Suchen Sie nach ContactLab-Berichten. Diese Daten sollten innerhalb von 24-48 Stunden nach erfolgreicher Bereitstellung angezeigt werden.
