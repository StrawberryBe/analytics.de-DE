---
description: Um die Integration zu aktivieren, müssen Sie den Qualtrics-Integrationsassistenten in der Data Connectors-Oberfläche ausfüllen.
seo-description: Um die Integration zu aktivieren, müssen Sie den Qualtrics-Integrationsassistenten in der Data Connectors-Oberfläche ausfüllen.
seo-title: Abschluss des Adobe-Integrationsassistenten
solution: Analytics
subtopic: Qualtrics
title: Abschluss des Adobe-Integrationsassistenten
topic: Data Connectors
uuid: e 065 fba 4-1 fe 1-4 e 25-9 c 45-6 c 52 dc 20 f 81 e
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Completing the Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

Um die Integration zu aktivieren, müssen Sie den Qualtrics-Integrationsassistenten in der Data Connectors-Oberfläche ausfüllen.

1. Navigieren Sie zu Data Connectors und starten Sie den Qualtrics-Integrationsassistenten. ([Data Connectors Hilfe](http://microsite.omniture.com/t2/help/en_US/genesis/)).
1. Wählen Sie die Report Suite aus, die Sie für diese Integration verwenden möchten, und geben Sie einen Namen an.

   Schließen Sie den Integrationsassistenten ab, der die in den folgenden Schritten beschriebenen Informationen enthält. 1. **Wizard Step 1**

   | Email Address | Die primäre Kontakt-E-Mail-Adresse. |
   |---|---|
   | Beschreibung | (Optional) Beschreibung für diese Integration. |
   | Qualtrics Organization ID | [Durchsuchen Ihrer Qualtrics-Organisations-ID](../../qualtrics-overview/qualtrics-org-id.md#task-47ea30d6dcd24893986a5e5b8dcf5e96) |
   | Adobe sitecatalyst Token | [Erstellen Ihres Qualtrics Adobe Analytics Token](../../qualtrics-overview/qualtrics-token.md#task-e32eacbc91614008b84e6b2f0b92d372) |

1. ** Assistent Schritt 2 - Variablenzuordnungen**

   | Qualtrics Response List | Wählen Sie eine verfügbare Listenvariable aus Ihrer Report Suite aus. (Möglicherweise müssen Sie eine neue listvar im Report Suite Manager aktivieren.) |
   |---|---|
   | Qualtrics Response ID | Wählen Sie eine verfügbare evar oder prop aus Ihrer Report Suite aus. (Möglicherweise müssen Sie eine neue listvar im Report Suite Manager aktivieren.) |
   | Tracking-Server | Geben Sie die Tracking-Server (Domäne) an, die Sie zur Verfolgung von Adobe Analytics-Daten verwenden. Use the `trackingServerSecure` tracking server if it differs from your standard tracking server setting. |
   | Qualtrics Survey Submissions | Wählen Sie ein verfügbares Ereignis aus Ihrer Report Suite aus (Sie müssen möglicherweise ein neues Ereignis aus dem Report Suite Manager aktivieren). |

1. **Assistent Schritt 3**: Nichts erforderlich, informativ.

   Schritt 1. ** Assistent Schritt 4 - Exporteinstellungen**

   | eVar | Wählen Sie bis zu fünf Ihrer evars für den Export in Qualtrics aus. |
   |---|---|
   | Ereignis-  | Wählen Sie bis zu fünf Ihrer benutzerspezifischen Ereignisse für den Export in Qualtrics aus. |
   | Props | Wählen Sie bis zu fünf Ihrer Props, die für den Export in Qualtrics verfügbar sein sollen. |
   | Zugriffsanforderungen | Markieren Sie das Kästchen für die Standardmetriken und Dimensionen, die Sie in Qualtrics exportieren möchten. The `visitor_id` is required to allow the export to function properly. |

1. **Assistent Schritt 5**: Überprüfen Sie die Konfiguration und klicken Sie dann auf Jetzt **[!UICONTROL aktivieren]**.
