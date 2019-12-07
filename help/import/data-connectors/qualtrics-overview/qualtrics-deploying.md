---
description: Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert.
subtopic: Qualtrics
title: Bereitstellen der Integration
topic: Data connectors
uuid: 9bdc233d-63f6-456d-8c26-b5736dfdef09
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bereitstellen der Integration{#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert.

## Ausführen des Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

Zum Aktivieren der Integration müssen Sie den Qualitätssicherungs-Integrationsassistenten in der Data Connectors-Oberfläche ausführen

1. Navigieren Sie zu den Data Connectors und starten Sie den qualitativen Integrationsassistenten.
1. Wählen Sie die Report Suite aus, die Sie für diese Integration verwenden möchten, und geben Sie einen Namen ein.

   Führen Sie den Integrationsassistenten aus und geben Sie die in den folgenden Schritten beschriebenen Informationen ein. 1. Schritt 1 **des Assistenten**

   | Email Address | Die primäre E-Mail-Adresse des Kontakts. |
   |---|---|
   | Beschreibung | (Optional) Beschreibung für diese Integration. |
   | Organisations-ID von Qualtrics | [Suchen der Organisations-ID von Qualtrics](../qualtrics-overview/qualtrics-org-id.md) |
   | Adobe SiteCatalyst-Token | [Generieren Ihres Qualtrics-Adobe Analytics-Tokens](../qualtrics-overview/qualtrics-token.md) |

1. **Assistent: Schritt 2 - Variablenzuordnungen**| Qualtrics Response List| Wählen Sie eine verfügbare Listenvariable aus Ihrer Report Suite. (Möglicherweise müssen Sie eine neue listVar im Report Suite Manager aktivieren.)  ||—|—|| Qualtrics Response ID| Wählen Sie eine verfügbare eVar oder Eigenschaft aus Ihrer Report Suite aus. (Möglicherweise müssen Sie eine neue listVar im Report Suite Manager aktivieren.)  || Tracking-Server|Geben Sie die Einstellung für den Tracking-Server (Domäne) an, die Sie zur Verfolgung von Adobe Analytics-Daten verwenden. Verwenden Sie den `trackingServerSecure` Tracking-Server, wenn er sich von der Einstellung des Standard-Trackingservers unterscheidet.  || Qualtrics Survey Submissions| Wählen Sie ein verfügbares Ereignis aus Ihrer Report Suite aus (unter Umständen müssen Sie ein neues Ereignis im Report Suite Manager aktivieren).  |

1. **Assistent Schritt 3**: Nichts erforderlich, nur informativ.

   Schritt Ergebnis 1. **Assistent Schritt 4: Exporteinstellungen**

   | eVar | Wählen Sie bis zu fünf Ihrer eVars aus, die Sie für den Export in Qualtrics verfügbar machen möchten |
   |---|---|
   | Ereignisse | Wählen Sie bis zu fünf Ihrer benutzerspezifischen Ereignisse aus, die Sie für den Export in Qualtrics verfügbar machen möchten |
   | Props | Wählen Sie bis zu fünf Eigenschaften aus, die Sie für den Export in Qualtrics verfügbar machen möchten |
   | Zugriffsanforderungen | Markieren Sie das Kästchen für eine der Standardmetriken und -dimensionen, die Sie nach Qualtrics exportieren möchten. Die `visitor_id` ist erforderlich, damit der Export ordnungsgemäß funktioniert. |

1. **Assistent Schritt 5**: Überprüfen Sie die Konfiguration und klicken Sie dann auf Jetzt **[!UICONTROL aktivieren]**.

## Integration in die Qualtrics Research Suite aktivieren{#enabling-the-integration-in-qualtrics-research-suite}

Nach Abschluss des Integrationsassistenten müssen Sie die Integration für jede Qualtrics-Umfrage aktivieren, die Sie verbinden möchten.

1. Melden Sie sich bei der Qualtrics Research Suite an.
1. Klicken Sie auf der Registerkarte **[!UICONTROL Meine Umfragen]** auf die Schaltfläche **[!UICONTROL Bearbeiten]** für die Umfrage, die Sie integrieren möchten.
1. Klicken Sie auf das Menü **[!UICONTROL Erweiterte Optionen]** und wählen Sie **[!UICONTROL Adobe Analytics]**. (Wenn diese Option nicht angezeigt wird, fragen Sie Ihren Administrator, ob Sie die erforderlichen Berechtigungen erhalten.)

   ![](assets/advanced_options.png)

1. Wählen Sie die Adobe Analytics-Konfiguration und klicken Sie auf **[!UICONTROL Speichern]**. Wenn keine Konfigurationen verfügbar sind, haben Sie den Adobe Integration Wizard wahrscheinlich noch nicht abgeschlossen.
   1. Das Kontrollkästchen Teilantworten **** einschließen kann verwendet werden, um anzugeben, dass Sie Daten nach Abschluss der einzelnen Teilumfragebildschirme in Adobe Analytics erfassen möchten. Wenn diese Option nicht aktiviert ist, werden die Daten nur für vollständig abgeschlossene Umfragen übertragen.
   1. Das Kontrollkästchen "Zeitstempel **[!UICONTROL mit Beacon]** senden"sollte nur bei der Integration mit einer Report Suite verwendet werden, die für den Empfang von Daten mit Zeitstempel konfiguriert ist (nicht üblich).
   ![](assets/integration_config.png)

## Überprüfen der Integration{#verifying-the-integration}

Nachdem alle Implementierungsschritte abgeschlossen sind, können Sie überprüfen, ob die Integration erfolgreich Daten übertragen hat.

1. **Integrationsaktivitätsprotokoll**: Rufen Sie in der Benutzeroberfläche von Data Connectors die Registerkarte **[!UICONTROL Support]** in der Integration von Qualtrics auf. Unter der Überschrift " **[!UICONTROL Integrationsaktivitätsprotokoll]** "werden Einträge angezeigt, aus denen hervorgeht, dass die Klassifizierungsdaten erfolgreich importiert wurden.

   >[!NOTE]
   >
   >Diese Einträge sollten innerhalb einer Stunde nach erfolgreicher Bereitstellung angezeigt werden.

   ![](assets/verify-1.png)

1. **Berichtsdaten**: Zeigen Sie Ihre Qualtrics-Umfrageberichte mit der Benutzeroberfläche von Marketing Reports &amp; Analysen an, indem Sie in die Qualtrics-Umfrageberichte navigieren (unter **[!UICONTROL Listenvariablen]**).

   >[!NOTE]
   >
   >Diese Daten sollten innerhalb von 24-48 Stunden nach erfolgreicher Bereitstellung angezeigt werden, vorausgesetzt, die integrierte Umfrage erhält aktiv Antworten.

   ![](assets/verify-2.png) ![](assets/verify-3.png)


