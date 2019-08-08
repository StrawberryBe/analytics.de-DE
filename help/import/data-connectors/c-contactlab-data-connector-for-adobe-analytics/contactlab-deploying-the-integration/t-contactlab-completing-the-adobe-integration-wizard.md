---
description: Schritte zum Abschluss des Integrationsassistenten in der Data Connectors-Oberfläche.
seo-description: Schritte zum Abschluss des Integrationsassistenten in der Data Connectors-Oberfläche.
seo-title: Abschluss des Adobe-Integrationsassistenten
solution: Analytics
title: Abschluss des Adobe-Integrationsassistenten
uuid: a 8135 be 3-fba 3-436 d -8959-faed 40 b 15088
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Abschluss des Adobe-Integrationsassistenten{#completing-the-adobe-integration-wizard}

Schritte zum Abschluss des Integrationsassistenten in der Data Connectors-Oberfläche.

1. Navigieren Sie zum Bereich Data Connectors (ehemals Genesis) innerhalb der Adobe Marketing Cloud.
1. Starten Sie den connectlab-Integrationsassistenten.
1. Wählen Sie die gewünschte Report Suite aus und geben Sie einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:

   | Element | Beschreibung |
   |---|---|
   | E-Mail-Adresse | Die E-Mail-Adresse des primären Kontakts |
   | Beschreibung | (Optional) Beschreibung für diese Integrations-Setup |

1. Konfigurieren Sie die folgenden **[!UICONTROL Variablenzuordnungselemente]** :

   | Element | Beschreibung |
   |---|---|
   | Link-ID | Wählen Sie eine evar zum Erfassen der Link-Ids in Echtzeit. |
   | Nachrichten-ID | Wählen Sie eine evar zum Erfassen der Nachrichten-Ids in Echtzeit. |
   | Recipient ID | Wählen Sie eine evar zum Erfassen der Empfänger-Ids in Echtzeit. |
   | Absprünge | Wählen Sie ein numerisches Ereignis aus, um tägliche Absprünge von Kontakttab zu erhalten. |
   | Gesendet | Wählen Sie ein numerisches Ereignis aus, das täglich von Kontakttab gesendet werden soll. |
   | Angeklickt | Wählen Sie ein numerisches Ereignis aus, um die täglichen Klicks von Kontakttab zu erhalten. |
   | Geöffnet | Wählen Sie ein numerisches Ereignis aus, um die tägliche Gesamtsumme von "contactlab" zu erhalten. |
   | Abonnement | Wählen Sie ein numerisches Ereignis aus, das täglich von Kontakttab abonniert werden soll. |

1. Aktivieren Sie den Datenzugriff und konfigurieren Sie die Datenerfassung.
   1. Benennen Sie Klassifizierungen nach Bedarf um.
   1. **[!UICONTROL Partnersegmente]** sind Standard-Remarketing-Segmente, die in Ihrer Integration enthalten sind.
   1. Wählen Sie unter **[!UICONTROL Ihren Segmenten]** alle benutzerdefinierten Segmente aus, die in diese Integration einbezogen werden sollen. Sie können unter dem Admin-Bedienfeld weitere benutzerdefinierte Segmente erstellen.
   1. Markieren Sie unter **[!UICONTROL Zugriffsanforderungen]** das Kästchen, damit Produktinformationen in täglicher Remarketing-Segmente in kontakttlab exportiert werden können.
   1. Benennen Sie die berechneten Metriken nach Bedarf um.
   1. Konfigurieren Sie, ob Sie die Ids erfassen werden, indem Sie Ihren Analytics-Erfassungscode manuell aktualisieren oder die automatisierte Lösung verwenden. Wenn Sie **[!UICONTROL die automatisierte Lösung]** auswählen, müssen Sie die Parameter einbeziehen, die in E-Email-Links verwendet werden, um die Ids zu übermitteln.
1. Überprüfen Sie alle Konfigurationselemente und klicken **[!UICONTROL Sie auf Jetzt aktivieren]**.
