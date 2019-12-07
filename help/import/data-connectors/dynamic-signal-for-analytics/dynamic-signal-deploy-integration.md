---
description: 'null'
title: Bereitstellen der Integration
uuid: 1a0770a7-c61b-4eec-a9b3-983def842ad8
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bereitstellen der Integration{#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der darin besteht, den Adobe Integration Wizard auszufüllen und die Integration zu überprüfen.

## Ausführen des Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

Schritte zum Abschließen des Integrationsassistenten in der Data Connectors-Oberfläche.

1. Navigieren Sie zum Bereich Data Connectors (früher Genesis) in der Adobe Experience Cloud.
1. Starten Sie den Assistenten zur Integration dynamischer Signale.
1. Wählen Sie die gewünschte Report Suite und geben Sie einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:

   | Element | Beschreibung |
   |---|---|
   | E-Mail-Adresse | Die E-Mail-Adresse des Hauptkontakts. |
   | Beschreibung | (Optional) Beschreibung für diese Integration. |
   | Community-ID | Sie können diese ID von Ihrem Kundenbetreuer für dynamische Signale abrufen. |

1. Konfigurieren Sie die folgenden **[!UICONTROL Variablenzuordnungen]** :

   | Element | Beschreibung |
   |---|---|
   | Trackingcode | Wählen Sie eine verfügbare eVar-Variable aus Ihrer Report Suite aus. |

1. Überprüfen Sie die Classifications, die für diese Integration erstellt werden.
1. Markieren Sie das Kontrollkästchen, um das Dashboard zur Integration dynamischer Signale zu erstellen (optional, jedoch dringend empfohlen).
1. Überprüfen Sie alle Konfigurationselemente und klicken Sie auf Jetzt **[!UICONTROL aktivieren]**.
1. **Wichtig**: Nach Abschluss des Assistenten müssen Sie Ihren Kundenbetreuer für dynamische Signale darüber informieren, dass er die Integration auf der VoiceStorm-Plattform aktivieren kann.

## Überprüfen der Integration{#verifying-the-integration}

Schritte zum Anzeigen Ihrer Einrichtung für die dynamische Signal VoiceStorm-Integration in der Adobe Experience Cloud

1. Zeigen Sie Ihre Einrichtung für die dynamische Signalintegration im Integrationsaktivitätsprotokoll an.
   1. Navigieren Sie in der Adobe Experience Cloud zu **[!UICONTROL Support]** &gt; **[!UICONTROL Integrationsaktivitätsprotokoll]** .

      ![](assets/integration_activity_log.png)

   1. Suchen Sie nach Einträgen wie erfolgreich importierten **[!UICONTROL Klassifizierungsdaten]**. Diese Einträge sollten innerhalb von 24 Stunden nach erfolgreicher Bereitstellung angezeigt werden.
1. Überprüfen Sie Ihre Berichte mit dynamischen Signalen in Adobe Analytics mit dem Dashboard, das automatisch mit dem Adobe Integrationsassistenten erstellt wurde (Schritt 7). Alternativ dazu können Sie in der Menüstruktur von Adobe Analytics zur Berichterstellung über dynamische Signale navigieren - siehe die folgenden Screenshots.

   **Hinweis**:Diese Daten sollten innerhalb von 24-48 Stunden nach erfolgreicher Bereitstellung angezeigt werden.

   ![](assets/reporting.png)

   ![](assets/reporting2.png)
