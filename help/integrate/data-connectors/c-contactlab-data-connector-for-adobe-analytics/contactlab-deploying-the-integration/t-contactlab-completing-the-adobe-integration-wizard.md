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
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Completing the Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

Schritte zum Abschluss des Integrationsassistenten in der Data Connectors-Oberfläche.

1. Navigieren Sie zum Bereich Data Connectors (ehemals Genesis) innerhalb der Adobe Marketing Cloud.
1. Starten Sie den connectlab-Integrationsassistenten.
1. Wählen Sie die gewünschte Report Suite aus und geben Sie einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:

   | Element | Beschreibung |
   |---|---|
   | E-Mail-Adresse | Die E-Mail-Adresse des primären Kontakts |
   | Beschreibung | (Optional) Beschreibung für diese Integrations-Setup |

1. Configure the following **[!UICONTROL Variable Mappings]** items:

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
   1. Under **[!UICONTROL Your Segments]**, select any custom segments that you would like to include in this integration. Sie können unter dem Admin-Bedienfeld weitere benutzerdefinierte Segmente erstellen.
   1. Under **[!UICONTROL Access Requests]**, check the box to allow product information to be exported to ContactLab in daily remarketing segments.
   1. Benennen Sie die berechneten Metriken nach Bedarf um.
   1. Konfigurieren Sie, ob Sie die Ids erfassen werden, indem Sie Ihren Analytics-Erfassungscode manuell aktualisieren oder die automatisierte Lösung verwenden. If you select **[!UICONTROL Automated Solution]**, you must include the parameters that are used in email links to pass ID’s.
1. Review all configuration items and click **[!UICONTROL Activate Now]**.
