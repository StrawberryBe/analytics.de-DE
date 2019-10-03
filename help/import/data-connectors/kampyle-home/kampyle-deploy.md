---
description: 'null'
seo-description: 'null'
seo-title: Bereitstellen der Integration
solution: Analytics
title: Bereitstellen der Integration
uuid: ebb385ca-7bfb-4cd3-9ff6-a5f5a52db5c9
translation-type: tm+mt
source-git-commit: f326b29bb73fd6e8630957c43dfd89f47b711986

---


# Bereitstellen der Integration{#deploying-the-integration}

Bei der Bereitstellung dieser Integration handelt es sich um einen einfachen Vorgang, bei dem der Adobe Integration-Assistent, die Bereitstellung des Plugin-Codes (javascript) und die Überprüfung der Integration ausgeführt werden.

## Führen Sie den Adobe-Integrationsassistenten aus{#complete-the-adobe-integration-wizard}

Zum Aktivieren der Integration müssen Sie den Konfigurationsassistenten in der Data Connectors-Oberfläche ausführen.

1. Melden Sie sich bei Adobe Experience Cloud an.
1. Navigieren Sie zu **[!UICONTROL Data Connectors]** (früher Genesis).
1. Starten Sie den Kampyle-Integrationsassistenten.
1. Wählen Sie die gewünschte Report Suite aus und geben Sie einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:
   1. **[!UICONTROL E-Mail-Adresse]** - die E-Mail-Adresse des Hauptkontakts.
   1. **[!UICONTROL Beschreibung]** - (optional) Beschreibung für diese Integration.
   1. **[!UICONTROL Kampyle-Schlüssel]** - Suchen Sie diesen Schlüssel in der Kampyle-Anwendung unter **[!UICONTROL Feedback-Formular]** &gt; **[!UICONTROL Feedback-Formularanpassung]**.
   1. **[!UICONTROL Tracking-Server]** - die Einstellung des Trackingservers (Domäne), mit der Sie Adobe Analytics-Daten verfolgen.
   1. **[!UICONTROL Tracking Server Secure]** - Wenn Ihr Tracking-Server für sicheren/https-Traffic unterschiedlich ist, geben Sie diese Einstellung hier an.
1. Konfigurieren Sie die folgenden **[!UICONTROL Variablenzuordnungen]** :
   1. **[!UICONTROL Kampyle-Feedback-ID]** - Wählen Sie eine verfügbare eVar-Variable aus Ihrer Report Suite
   1. **[!UICONTROL Feedback-Bewertung]** - Wählen Sie ein verfügbares Erfolgsereignis (Typ "Zähler") aus Ihrer Report Suite aus.
   1. **[!UICONTROL Feedback-Elemente]** - Wählen Sie ein verfügbares Erfolgsereignis (Typ "Zähler") aus Ihrer Report Suite aus.
   1. **[!UICONTROL Feedback mit Bewertung]** - Wählen Sie ein verfügbares Erfolgsereignis (Typ "Zähler") aus Ihrer Report Suite aus.
1. Markieren Sie das Kästchen, damit das Kampyle Integration Dashboard automatisch für Sie erstellt wird (empfohlen).
1. Überprüfen Sie alle Konfigurationselemente und klicken Sie auf Jetzt **[!UICONTROL aktivieren]**.

## Integrationskonfigurationsobjekt bereitstellen{#deploy-the-integration-configuration-object}

Nach Abschluss des Integrationsassistenten müssen Sie das Integrationskonfigurationsobjekt für Ihre Webeigenschaft bereitstellen.

In vielen Fällen ist es am einfachsten, das Integrationskonfigurationsobjekt in Ihren Adobe Analytics-Bereitstellungscode einzuschließen.

> [!NOTE] Wenn Sie Adobe TagManager oder das dynamische Tag-Management verwenden, um Adobe Analytics bereitzustellen, können Sie das Integrationskonfigurationsobjekt einfach über dieses Tool hinzufügen.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Ressourcen]** &gt; **[!UICONTROL Support]** der Integration.
1. Laden Sie die **[!UICONTROL Kampyle Integration Code (JS)]** -Ressource herunter und speichern Sie sie. Der Code sieht in etwa so aus:

   ```
   /* Kampyle:  Integration configuration settings */
     window.k_sc_param = { "version":1.1 }
   ```

1. Deploy the code using one of the following methods:
| **You use Adobe TagManager or Dynamic Tag Management.** | Use the tag management interface to add the code. ||—|—|| **In allen anderen Fällen** | Stellen Sie den Code an die Organisationsressource weiter, die für die Aktualisierung Ihres Adobe Analytics-Bereitstellungscodes zuständig ist.  |

## Verify the Integration{#verify-the-integration}

Validate that the integration is successfully transferring data by completing a couple of checks.

### Protokoll zu den Integrationsaktivitäten {#section-0472df9180db4f218db5f6040cab07af}

View your Kampyle integration setup within the Adobe Experience Cloud by navigating to Support &gt; Integration Activity Log. ******** Under the Data In tab, you should see entries stating that classification data was successfully imported.****

> [!NOTE] Log entries should appear within 24 hours of successful deployment.

![](assets/integration_activity_log.png)

### Adobe Reporting Data {#section-1ae9f0a5e6bc40988478ff55aefd56ac}

View your Kampyle feedback reports with Adobe Analytics by navigating to the Kampyle reporting within the appropriate menu structure.

> [!NOTE] Reporting data should appear within 24-48 hours of successful deployment, assuming that the integrated feedback form(s) is actively receiving submissions.

![](assets/adobe_reporting_data.png)

