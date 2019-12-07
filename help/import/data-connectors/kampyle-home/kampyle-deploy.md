---
description: 'null'
title: Bereitstellen der Integration
uuid: ebb385ca-7bfb-4cd3-9ff6-a5f5a52db5c9
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

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

1. Stellen Sie den Code mit einer der folgenden Methoden bereit:
| **Sie verwenden Adobe TagManager oder das dynamische Tag-Management.** | Verwenden Sie die Tag-Management-Oberfläche, um den Code hinzuzufügen. ||—|—|| **In allen anderen Fällen** | Stellen Sie den Code an die Organisationsressource weiter, die für die Aktualisierung Ihres Adobe Analytics-Bereitstellungscodes zuständig ist.  |

## Integration überprüfen{#verify-the-integration}

Überprüfen Sie, ob die Integration Daten erfolgreich übertragen hat, indem Sie einige Prüfungen durchführen.

### Protokoll zu den Integrationsaktivitäten {#section-0472df9180db4f218db5f6040cab07af}

Zeigen Sie Ihre Einrichtung für die Kampyle-Integration in der Adobe Experience Cloud an, indem Sie zu **[!UICONTROL Support]** &gt; **[!UICONTROL Integrationsaktivitätsprotokoll]** navigieren. Auf der Registerkarte " **[!UICONTROL Daten in]** "werden Einträge angezeigt, aus denen hervorgeht, dass Klassifizierungsdaten erfolgreich importiert wurden.

> [!NOTE] Protokolleinträge sollten innerhalb von 24 Stunden nach erfolgreicher Bereitstellung angezeigt werden.

![](assets/integration_activity_log.png)

### Adobe-Berichtsdaten {#section-1ae9f0a5e6bc40988478ff55aefd56ac}

Zeigen Sie Ihre Kampyle-Feedback-Berichte mit Adobe Analytics an, indem Sie innerhalb der entsprechenden Menüstruktur zur Kampyle-Berichterstellung navigieren.

> [!NOTE] Berichtsdaten sollten innerhalb von 24-48 Stunden nach erfolgreicher Bereitstellung angezeigt werden, vorausgesetzt, dass das/die integrierte(n) Feedback-Formular(e) aktiv Übermittlungen empfängt.

![](assets/adobe_reporting_data.png)

