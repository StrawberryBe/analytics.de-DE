---
description: Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.
seo-description: Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.
seo-title: Integration aktivieren
title: Integration aktivieren
uuid: 0 a 5 d 2 d 45-5133-4259-96 ce-c 992 a 1 e 314 ee
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a3310ec57ce4c68539f07e0d294c8175742c49dc

---


# Activate the Integration {#activate-the-integration}

Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.

1. Start [Data Connectors](https://marketing.adobe.com/resources/help/en_US/genesis/c_overview.html) and click **[!UICONTROL + Add New]** to [add a new integration](https://marketing.adobe.com/resources/help/en_US/genesis/t_add_integration.html).
1. In the **[!UICONTROL Show]** list, select **[!UICONTROL By Name]** and drag the [!DNL ~Partner~] integration to an empty plug-in slot.
1. Schließen Sie den Integrationsassistenten mit den Informationen in der folgenden Tabelle ab:

| Feld | Beschreibung |
|--- |--- |
| Report Suite | Die Report Suite, die die Daten aus dieser Integration erhält. |
| Integrationsname | Geben Sie den Integrationsnamen an, den Data Connectors in der aktiven Integrationsliste der Report Suite anzeigt. |
| Konto-ID | Geben Sie Ihre Aprimo-Konto-ID an. |
| Recipient ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Email-Adresse aus dem Aprimo-System. Diese "Empfänger-ID" ist mit dem abgerundeten Besucherverhalten in der Site-Empfänger-ID verknüpft (Warenkorbabbrüche, Käufe usw.). das in das Aprimo-System gezogen wird und für Wiederverkaufszwecke genutzt werden kann. |
| Angeklickt | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die per E-Email angeklickten Daten aus dem E-Email-System speichert. Mit dem Ereignis "Angeklickt" können Sie erkennen, wie viele Besucher auf die E-Email geklickt haben. |
| Nachrichten-ID | (Erforderlich) Speichert die eindeutige Mailingid. |
| Geöffnet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die vom E-Email-System importierten Daten per E-Email speichert. Mit dem Ereignis "Geöffnet" können Sie erkennen, wie viele Besucher die E-Email geöffnet haben. |
| Recipient ID | (Erforderlich) Speichert die Unique Visitor-ID. |
| Gesendet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die per E-Email gesendeten Daten speichert, die aus dem E-Email-System importiert wurden. Im Ereignisereignis können Sie die Anzahl der gesendeten E-Email-Nachrichten anzeigen. |
| Absprünge | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Email-System importierten Gesamt-Absprungdaten speichert. Das Ereignis "Total-Bounces" zeigt die Anzahl der E-Email-Nachrichten an, die aufgrund eines Problems mit der Auslieferung nicht an Empfänger übermittelt wurden. |
| Abonnement | (Pflichtfeld) Geben Sie das Adobe Analytics-Ereignis an, das die vom E-Email-System importierten Daten zum Abonnieren von Abonnements speichert. Mit dem nicht abonnierten Ereignis können Sie die Anzahl der Besucher anzeigen, die die E-Email-Nachricht geöffnet haben, dann aber auf den Link Abonnieren klicken, um zukünftige E-Email-Nachrichten aus Ihrer Organisation abzuwählen. |
| Segmente | Mit dieser Integration werden die im Abschnitt Partner-Segmente angezeigten Partner-definierten Segmente erstellt. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration einbezogen werden sollen. |
| Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsrechte. |
| Datenerfassung | Select **JavaScript Plug-in** if you want to use the s_code.js plug-in as the collection model for this integration. |
Select **Automated Solution** if you want to use an automated collection model for this integration, then specify the unique identifiers used for this integration. Wenn Sie diese Option auswählen, geben Sie die eindeutigen ids für diese Integration an:
<ul><li>Nachrichten-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Nachrichten-ID dar, die durch Ihren E-Email-Partner an die URL der Einstiegsseite angehängt wurde.</li>
<li>Empfänger-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Empfänger-ID an die URL der Einstiegsseite Ihres E-Email-Partners.</li></ul>|
| Dashboard und Lesezeichengenerierung | Automatisch ein Dashboard und Lesezeichen für die Integration erstellen.|
