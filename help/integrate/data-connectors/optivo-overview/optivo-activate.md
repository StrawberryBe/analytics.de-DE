---
description: Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.
seo-description: Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.
seo-title: Integration aktivieren
title: Integration aktivieren
uuid: 3 b 2 acdb 8-9 a 1 f -4 f 17-92 f 2-6 a 3780 a 8 f 626
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d10546972c03efae1bc365b7391000a40a79b0a4

---


# Activate the Integration{#activate-the-integration}

Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.

1. Start [Data Connectors](https://marketing.adobe.com/resources/help/en_US/genesis/c_overview.html) and click **[!UICONTROL + Add New]** to [add a new integration](https://marketing.adobe.com/resources/help/en_US/genesis/t_add_integration.html).
1. In the **[!UICONTROL Show]** list, select **[!UICONTROL By Name]** and drag the [!DNL ~Partner~] integration to an empty plug-in slot.
1. Schließen Sie den Integrationsassistenten mit den Informationen in der folgenden Tabelle ab:

| Feld | Beschreibung |
|--- |--- |
| Report Suite | Die Report Suite, die die Daten aus dieser Integration erhält. |
| Integrationsname | Geben Sie den Integrationsnamen an, den Data Connectors in der aktiven Integrationsliste der Report Suite anzeigt. |
| E-Mail-Adresse | Geben Sie eine E-Mail-Adresse an, um integrationsbezogene Informationen zu erhalten. |
| Konto-ID | Dies ist die eindeutige Kennung, die Ihr E-Mail-Serviceanbieter Ihrer Organisation zugewiesen hat. Sie wird verwendet, wenn Sie E-Email-Kampagnendaten anfordern (z. B. # Gesendet, # Geöffnet, # Angeklickt usw.) von und senden Sie Besuchersegmente an Ihren E-Mail-Serviceanbieter. |
| Recipient ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Email-Adresse vom Optivo® Broadmail-System. Diese "Empfänger-ID" ist mit dem nachgeordneten Besucherverhalten auf der Site verknüpft (Warenkorbabbrüche, Käufe usw.). das in das Optivo® Broadmail-System gezogen wird und für Wiederverkaufszwecke genutzt werden kann. |
| Nachrichten-ID | (Erforderlich) Speichert die eindeutige Mailingid. These classification dimensions are created by the Data Connectors wizard for the Message ID: a)**Campaigns**: Campaigns associated with the message. b)**Channel**: The channel of transmission, this is constantly "optivo broadmail". c)**Country Code**: This field contains the country code of the origin sender country. Es handelt sich um eine Konstante "DE" . d) **Delivery Tool**: Method of transmission, always "Email". e) **Message Name**: The name of the mailing, as it is configured in optivo® broadmail. f) **Start Date**: Timestamp of the start of this mailing. |
| Beitrag nach dem Klicken | (Erforderlich) Dies ist erforderlich, um Informationen zu einer Empfängeraktion an die optivo® Broadmail zu senden, nachdem der Empfänger auf einen Link in einem Versand geklickt hat. |
| Beitrag auf Produkt | (Erforderlich) Dies ist erforderlich, um Informationen zu einer Empfängeraktion an die optivo® Broadmail zu senden, nachdem der Empfänger auf einen Link in einem Versand geklickt hat. |
| Beitragsaktionen | (Erforderlich) Dies ist erforderlich, um Informationen zu einer Empfängeraktion an die optivo® Broadmail zu senden, nachdem der Empfänger auf einen Link in einem Versand geklickt hat. |
| Hartes Abspringen | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Email-System importierten Hartabsprungdaten speichert. Anzahl der E-Mail-Nachrichten, die nicht an Empfänger übermittelt wurden und dauerhaft nicht bereitstehen. |
| Weiches Abspringen | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Email-System importierten Softbounces-Daten speichert. Anzahl der E-Mail-Nachrichten, die aufgrund eines Problems mit der Auslieferung nicht an Empfänger übermittelt wurden. |
| Angeklickt | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die per E-Email angeklickte Datenimportdatei vom E-Email-System speichert. Mit dem Ereignis "Angeklickt" können Sie erkennen, wie viele Besucher auf die E-Email geklickt haben. |
| Geöffnet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Email-System importierten Daten gespeichert werden. Mit dem Ereignis "Geöffnet" können Sie erkennen, wie viele Besucher die E-Email geöffnet haben. |
| Gesendet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die per E-Email gesendeten Daten speichert, die aus dem E-Email-System importiert wurden. Im Ereignisereignis können Sie die Anzahl der gesendeten E-Email-Nachrichten anzeigen. |
| Abonnement | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die vom E-Email-System importierten Daten zum Abonnieren von Abonnements speichert. Mit dem nicht abonnierten Ereignis können Sie die Anzahl der Besucher anzeigen, die die E-Email-Nachricht geöffnet haben, dann aber auf den Link Abonnieren klicken, um zukünftige E-Email-Nachrichten aus Ihrer Organisation abzuwählen. |
| Segmente | Aktivieren Sie vorhandene Segmente zusammen mit dieser Integration (optional). |
| Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsrechte. |
| Datenerfassung | Select **JavaScript Plug-in** if you want to use the s_code.js plug-in as the collection model for this integration. Select **Automated Solution** if you want to use an automated collection model for this integration, then specify the unique identifiers used for this integration. Wenn Sie diese Option auswählen, geben Sie die eindeutigen ids für diese Integration an:<ul><li>Nachrichten-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Nachrichten-ID dar, die Ihr E-Email-Partner an die URL der Einstiegsseite angehängt hat.</li><li>Empfänger-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Empfänger-ID an die URL der Einstiegsseite Ihres E-Email-Partners.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Erstellen Sie automatisch ein Dashboard und Lesezeichen für die Integration. |