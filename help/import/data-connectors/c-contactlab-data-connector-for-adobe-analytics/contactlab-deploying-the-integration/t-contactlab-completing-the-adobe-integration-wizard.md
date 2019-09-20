---
description: Schritte zum Abschließen des Integrationsassistenten in der Data Connectors-Oberfläche.
seo-description: Schritte zum Abschließen des Integrationsassistenten in der Data Connectors-Oberfläche.
seo-title: Ausführen des Adobe Integration Wizard
solution: Analytics
title: Ausführen des Adobe Integration Wizard
uuid: a8135be3-fba3-436d-8959-faed40b15088
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Ausführen des Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

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
   | Link-ID | Wählen Sie eine eVar zum Erfassen von Link-IDs in Echtzeit. |
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
