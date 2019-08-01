---
description: Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.
seo-description: Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.
seo-title: Integration aktivieren
title: Integration aktivieren
uuid: 93 c 59 f 8 e -3 cf 5-44 c 1-9 a 04-22460 af 93 d 5 d
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a3310ec57ce4c68539f07e0d294c8175742c49dc

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
| Angeklickt | Gesamtanzahl der E-Mail-Klicks. |
| Kampagnen-ID | Speichert die eindeutige Nachrichten-ID. Dies wird oft in der Kampagnenvariablen gespeichert. |
| Geöffnet | Gesamtanzahl der E-Mails wird geöffnet. |
| Personenklicks | Anzahl der Personen, die geklickt haben. |
| Verarbeitet | Gesamtanzahl der verarbeiteten E-Mails. |
| Broadlog ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Email-Adresse vom Neolane-System. Diese "Broadlog-ID" ist mit dem abgerundeten Besucherverhalten auf der Site verknüpft (Warenkorb-ID, Käufe usw. des Einkaufswagens). das in das Neolane-System gezogen wird und für Wiederverkaufszwecke genutzt werden kann. |
| Eingeplant | Anzahl der E-Mail-Nachrichten, die für die Auslieferung geplant sind. |
| Gesendet | Anzahl der gesendeten E-Mail-Nachrichten. |
| Absprünge insgesamt | Anzahl der E-Mail-Nachrichten, die aufgrund eines Problems mit der Auslieferung nicht an Empfänger übermittelt wurden. |
| Eindeutige Klicks | Anzahl der eindeutigen Klicks. |
| Eindeutige Öffnung | Anzahl unterschiedlicher Öffnungen. |
| Abonnement | Anzahl der Besucher, die die E-Email-Nachricht geöffnet haben, dann aber auf den Link Abonnieren klicken, um künftige E-Email-Nachrichten aus Ihrem Unternehmen abzuwählen. |
| Segmente | Mit dieser Integration werden die im Abschnitt Partner-Segmente angezeigten Partner-definierten Segmente erstellt. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration einbezogen werden sollen. |
| Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsrechte. |
| Datenerfassung | Select **JavaScript Plug-in** if you want to use the s_code.js plug-in as the collection model for this integration. Select **Automated Solution** if you want to use an automated collection model for this integration, then specify the unique identifiers used for this integration. Wenn Sie diese Option auswählen, geben Sie die eindeutigen ids für diese Integration an: <ul><li>Nachrichten-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Nachrichten-ID dar, die durch Ihren E-Email-Partner an die URL der Einstiegsseite angehängt wurde.</li><li>Empfänger-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Empfänger-ID an die URL der Einstiegsseite Ihres E-Email-Partners.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Erstellen Sie automatisch ein Dashboard und Lesezeichen für die Integration. |