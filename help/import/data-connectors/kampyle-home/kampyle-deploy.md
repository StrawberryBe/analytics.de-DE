---
description: 'null'
title: Bereitstellen der Integration
uuid: ebb385ca-7bfb-4cd3-9ff6-a5f5a52db5c9
translation-type: ht
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# Bereitstellen der Integration {#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der aus der Fertigstellung des Adobe-Integrationsassistenten, der Bereitstellung des Plug-in-Codes (JavaScript) und der Verifizierung der Integration besteht.

## Abschließen des Adobe-Integrationsassistenten {#complete-the-adobe-integration-wizard}

Zum Aktivieren der Integration müssen Sie den Konfigurationsassistenten auf der Data Connectors-Oberfläche ausführen.

1. Melden Sie sich bei Adobe Experience Cloud an.
1. Navigieren Sie zu **[!UICONTROL Data Connectors]** (früher Genesis).
1. Starten Sie den Kampyle-Integrationsassistenten.
1. Wählen Sie die gewünschte Report Suite aus. Geben Sie dann einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:
   1. **[!UICONTROL E-Mail-Adresse]**: Die E-Mail-Adresse des Hauptkontakts.
   1. **[!UICONTROL Beschreibung]**: (optional) Die Beschreibung für die Einrichtung dieser Integration.
   1. **[!UICONTROL Kampyle-Schlüssel]**: Suchen Sie diesen Schlüssel in der Kampyle-Anwendung unter **[!UICONTROL Feedback-Formular]** > **[!UICONTROL Feedback-Formularanpassung]**.
   1. **[!UICONTROL Tracking-Server]**: Die Einstellung des Tracking-Servers (Domäne), mit der Sie Adobe Analytics-Daten verfolgen.
   1. **[!UICONTROL Sicherer Tracking-Server]**: Wenn Ihr Tracking-Server für sicheren/HTTPS-Traffic unterschiedlich ist, geben Sie diese Einstellung hier an.
1. Konfigurieren Sie die folgenden **[!UICONTROL Variablenzuordnungselemente]**:
   1. **[!UICONTROL Kampyle-Feedback-ID]**: Wählen Sie eine verfügbare eVar-Variable aus Ihrer Report Suite aus.
   1. **[!UICONTROL Feedback-Bewertung]**: Wählen Sie ein verfügbares Erfolgsereignis (Typ „Zähler“) aus Ihrer Report Suite aus.
   1. **[!UICONTROL Feedback-Elemente]**: Wählen Sie ein verfügbares Erfolgsereignis (Typ „Zähler“) aus Ihrer Report Suite aus.
   1. **[!UICONTROL Feedback mit Bewertung]**: Wählen Sie ein verfügbares Erfolgsereignis (Typ „Zähler“) aus Ihrer Report Suite aus.
1. Aktivieren Sie das Kästchen, damit das Dashboard für die Kampyle-Integration automatisch für Sie erstellt wird (empfohlen).
1. Überprüfen Sie alle Konfigurationselemente. Klicken Sie dann auf **[!UICONTROL Jetzt aktivieren]**.

## Bereitstellen des Integrationskonfigurationsobjekts {#deploy-the-integration-configuration-object}

Nach Abschluss des Integrationsassistenten müssen Sie das Integrationskonfigurationsobjekt für Ihre Webeigenschaft bereitstellen.

In vielen Fällen ist es am einfachsten, das Integrationskonfigurationsobjekt in Ihren Adobe Analytics-Bereitstellungscode aufzunehmen.

> [!NOTE] Wenn Sie Adobe TagManager oder Dynamic Tag Management verwenden, um Adobe Analytics bereitzustellen, können Sie das Integrationskonfigurationsobjekt einfach über dieses Tool hinzufügen.

1. Navigieren Sie zur Registerkarte **[!UICONTROL Ressourcen]** > **[!UICONTROL Support]** der Integration.
1. Laden Sie die Ressource **[!UICONTROL Kampyle Integration Code (JS)]** herunter. Speichern Sie diese anschließend. Der Code sieht in etwa so aus:

   ```
   /* Kampyle:  Integration configuration settings */
     window.k_sc_param = { "version":1.1 }
   ```

1. Stellen Sie den Code mit einer der folgenden Methoden bereit:
  **Verwenden Sie Adobe TagManager oder Dynamic Tag Management.** | Verwenden Sie die Tag-Management-Oberfläche, um den Code hinzuzufügen.  |
|---|---|
| **In allen anderen Fällen** | Versenden Sie den Code an die Organisationsressource, die für die Aktualisierung Ihres Adobe Analytics-Bereitstellungscodes zuständig ist. |

## Überprüfen der Integration {#verify-the-integration}

Validieren Sie anhand einiger Prüfungen, ob die Integration erfolgreich Daten überträgt.

### Protokoll zu den Integrationsaktivitäten {#section-0472df9180db4f218db5f6040cab07af}

Zeigen Sie Ihre Einrichtung für die Kampyle-Integration in der Adobe Experience Cloud an. Navigieren Sie dazu zu **[!UICONTROL Support]** > **[!UICONTROL Protokoll zu den Integrationsaktivitäten]**. Auf der Registerkarte **[!UICONTROL Dateneingang]** werden Einträge angezeigt, aus denen hervorgeht, dass Klassifizierungsdaten erfolgreich importiert wurden.

> [!NOTE] Protokolleinträge sollten innerhalb von 24 Stunden nach erfolgreicher Bereitstellung angezeigt werden.

![](assets/integration_activity_log.png)

### Adobe-Berichtsdaten {#section-1ae9f0a5e6bc40988478ff55aefd56ac}

Zeigen Sie Ihre Kampyle-Feedback-Berichte mit Adobe Analytics an, indem Sie innerhalb der entsprechenden Menüstruktur zur Kampyle-Berichterstellung navigieren.

> [!NOTE] Berichtsdaten sollten innerhalb von 24–48 Stunden nach erfolgreicher Bereitstellung angezeigt werden, sofern die integrierten Feedback-Formulare Übermittlungen aktiv empfangen.

![](assets/adobe_reporting_data.png)

