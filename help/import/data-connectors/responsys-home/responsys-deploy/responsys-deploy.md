---
description: 'null'
title: Bereitstellen der Integration
uuid: 5abf6d49-b05b-4e0f-8d9b-bb02d8f1c84a
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bereitstellen der Integration{#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert:

## Ausführen des Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

Schritte zum Abschließen des Integrationsassistenten in der Data Connectors-Oberfläche.

1. Navigieren Sie zum Bereich Data Connectors (früher Genesis) in der Adobe Experience Cloud.
1. Starten Sie den Integrationsassistenten für Antworten.
1. Wählen Sie die gewünschte Report Suite und geben Sie einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:

   | Element | Beschreibung |
   |---|---|
   | E-Mail-Adresse | Die E-Mail-Adresse des Hauptkontakts |
   | Beschreibung | (Optional) Beschreibung für diese Integration |
   | Konto-ID | Rufen Sie das Support-Team für Antworten unter support@responsys.com ab. |

1. Konfigurieren Sie die folgenden **[!UICONTROL Variablenzuordnungen]** :

   | Element | Beschreibung |
   |---|---|
   | Nachrichten-ID | Wählen Sie eine eVar, um Nachrichten-IDs in Echtzeit zu erfassen. |
   | Recipient ID | Wählen Sie eine eVar, um Empfänger-IDs in Echtzeit zu erfassen. |
   | Absprünge insgesamt | Wählen Sie ein numerisches Ereignis aus, um tägliche Absprünge von Antworten zu erhalten. |
   | E-Mail gesendet | Wählen Sie ein numerisches Ereignis aus, das täglich von Antworten gesendet werden soll. |
   | Angeklickt | Wählen Sie ein numerisches Ereignis aus, um die täglichen Klicks von Antworten zu erhalten. |
   | Geöffnet | Wählen Sie ein numerisches Ereignis aus, um den täglichen Gesamtwert aus Antworten zu erhalten. |
   | Nicht abonniert | Wählen Sie ein numerisches Ereignis aus, um tägliche Abonnements von Antworten zu erhalten. |
   | Ausgeliefert | Wählen Sie ein numerisches Ereignis aus, das täglich von Antworten gesendet werden soll. |

1. Aktivieren Sie den Datenzugriff und konfigurieren Sie die Datenerfassung.
   1. Benennen Sie Klassifizierungen nach Bedarf um.
   1. **[!UICONTROL Partnersegmente]** sind Standard-Remarketing-Segmente, die in Ihrer Integration enthalten sind.
   1. Aktivieren Sie unter **[!UICONTROL Zugriffsanforderungen]** das Kontrollkästchen, um den Export von Produktinformationen in Remarketingsegmente mit täglicher Remarketing in Antworten zuzulassen.
   1. Konfigurieren Sie, ob Sie IDs erfassen, indem Sie Ihren Analytics-Erfassungscode manuell aktualisieren oder die automatisierte Lösung verwenden. Wenn Sie **[!UICONTROL Automatisierte Lösung]** auswählen, müssen Sie die Parameter einbeziehen, die in E-Mail-Links verwendet werden, um IDs zu übermitteln.
1. Überprüfen Sie alle Konfigurationselemente und klicken Sie auf Jetzt **[!UICONTROL aktivieren]**.

## Konfigurieren im System "Antworten"{#configuring-within-the-responsys-system}

Zur Aktivierung der Integration wenden Sie sich an den Support für Antworten.

Nach Abschluss des Integrationsassistenten müssen Sie die Integration in "Antworten"aktivieren.

Wenden Sie sich hierzu an das Supportteam von Responsys unter support@responsys.com.
