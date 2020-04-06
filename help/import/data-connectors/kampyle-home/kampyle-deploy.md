---
description: 'null'
title: Bereitstellen der Integration
uuid: ebb385ca-7bfb-4cd3-9ff6-a5f5a52db5c9
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Bereitstellen der Integration {#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Vorgang, bei dem Sie den Adobe Integration Wizard, den Plug-in-Code (JavaScript) und die Integration überprüfen müssen.

## Abschließen des Adobe-Integrationsassistenten {#complete-the-adobe-integration-wizard}

Um die Integration zu aktivieren, führen Sie den Konfigurationsassistenten in der Data Connectors-Oberfläche aus.

1. Melden Sie sich bei Adobe Experience Cloud an.
1. Navigieren Sie zu **[!UICONTROL Data Connectors]**.
1. Starten Sie den Kampyle-Integrationsassistenten.
1. Wählen Sie die gewünschte Report Suite aus. Geben Sie dann einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:
   1. **[!UICONTROL Email address]**: Die E-Mail-Adresse des Hauptkontakts.
   1. **[!UICONTROL Description]** (optional): Beschreibung für diese Integrationseinrichtung.
   1. **[!UICONTROL Kampyle Key]**: Suchen Sie diesen Schlüssel in der Anwendung Kampyle unter **[!UICONTROL Feedback Form]** > **[!UICONTROL Feedback Form Customization]**.
   1. **[!UICONTROL Tracking Server]**: Der Wert des Tracking-Servers, den Sie zur Verfolgung von Adobe Analytics-Daten verwenden.
   1. **[!UICONTROL Tracking Server Secure]**: Wenn sich Ihr Tracking-Server für sicheren/https-Traffic unterscheidet, geben Sie diese Einstellung hier an.
1. Configure the following **[!UICONTROL Variable Mappings]** items:
   1. **[!UICONTROL Kampyle Feedback ID]**: Wählen Sie eine verfügbare eVar-Variable aus Ihrer Report Suite aus
   1. **[!UICONTROL Feedback Grade]**: Wählen Sie ein verfügbares Erfolgserlebnis (Typ &quot;Zähler&quot;) aus Ihrer Report Suite aus.
   1. **[!UICONTROL Feedback Items]**: Wählen Sie ein verfügbares Erfolgserlebnis (Typ &quot;Zähler&quot;) aus Ihrer Report Suite aus.
   1. **[!UICONTROL Feedback with Grade]**: Wählen Sie ein verfügbares Erfolgserlebnis (Typ &quot;Zähler&quot;) aus Ihrer Report Suite aus.
1. Aktivieren Sie das Kästchen, damit das Dashboard für die Kampyle-Integration automatisch für Sie erstellt wird (empfohlen).
1. Review all configuration items and click **[!UICONTROL Activate Now]**.

## Bereitstellen des Integrationskonfigurationsobjekts {#deploy-the-integration-configuration-object}

Stellen Sie nach Abschluss des Integrationsassistenten das Integrationskonfigurationsobjekt für Ihre Webeigenschaft bereit. In vielen Fällen ist es am einfachsten, das Integrationskonfigurationsobjekt in Ihren Adobe Analytics-Bereitstellungscode aufzunehmen.

>[!NOTE] Wenn Sie Adobe Experience Platform Launch verwenden, können Sie das Integrationskonfigurationsobjekt einfach über dieses Tool hinzufügen.

1. Navigate to the **[!UICONTROL Resources]** > **[!UICONTROL Support]** tab of the integration.
1. Download and save the **[!UICONTROL Kampyle Integration Code (JS)]** resource. Der Code sieht in etwa so aus:

   ```
   /* Kampyle:  Integration configuration settings */
     window.k_sc_param = { "version":1.1 }
   ```

1. Stellen Sie den Code mit einer der folgenden Methoden bereit:

   * Adobe Experience Platform Launch verwenden.
   * Stellen Sie den Code für die organisatorische Ressource bereit, die Ihre Adobe Analytics-Bereitstellung verwaltet.

## Überprüfen der Integration {#verify-the-integration}

Überprüfen Sie, ob die Integration Daten erfolgreich übertragen hat, indem Sie einige Prüfungen durchführen.

### Protokoll zu den Integrationsaktivitäten {#section-0472df9180db4f218db5f6040cab07af}

View your Kampyle integration setup within the Adobe Experience Cloud by navigating to **[!UICONTROL Support]** > **[!UICONTROL Integration Activity Log]**. Under the **[!UICONTROL Data In]** tab, you should see entries stating that classification data was successfully imported.

>[!NOTE] Protokolleinträge werden in der Regel innerhalb von 24 Stunden nach erfolgreicher Bereitstellung angezeigt.

![Integrations-Aktivität-Protokoll](assets/integration_activity_log.png)

### Adobe-Berichtsdaten {#section-1ae9f0a5e6bc40988478ff55aefd56ac}

Zeigen Sie Ihre Kampyle-Feedback-Berichte mit Adobe Analytics an, indem Sie innerhalb der entsprechenden Menüstruktur zur Kampyle-Berichterstellung navigieren.

>[!NOTE] Berichtsdaten sollten innerhalb von 24–48 Stunden nach erfolgreicher Bereitstellung angezeigt werden, sofern die integrierten Feedback-Formulare Übermittlungen aktiv empfangen.

![Adobe Berichte-Daten](assets/adobe_reporting_data.png)
