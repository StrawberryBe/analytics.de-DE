---
description: Richten Sie die Integration mithilfe des Adobe-Konfigurationsassistenten für Data Connectors ein.
title: Aktivieren der Integration
uuid: 3b2acdb8-9a1f-4f17-92f2-6a3780a8f626
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 97%

---


# Aktivieren der Integration {#activate-the-integration}

Richten Sie die Integration mithilfe des Adobe-Konfigurationsassistenten für Data Connectors ein.

1. Starten Sie [Data Connectors](https://docs.adobe.com/content/help/en/analytics/import/dataconnectors/getting-started-data-connectors.html) und klicken Sie auf **[!UICONTROL + Neu hinzufügen]**, [um eine neue Integration hinzuzufügen](https://docs.adobe.com/content/help/en/analytics/import/dataconnectors/getting-started-data-connectors.html).
1. Wählen Sie in der Liste **[!UICONTROL Anzeigen]** den Eintrag **[!UICONTROL Nach Name]** aus und ziehen Sie die Integration [!DNL ~Partner~] in einen leeren Plug-in-Slot.
1. Führen Sie den Integrationsassistenten aus. Verwenden Sie dabei die Informationen aus der folgenden Tabelle:

| Feld | Beschreibung |
|--- |--- |
| Report Suite  | Die Report Suite, an welche die Daten aus dieser Integration gesendet werden. |
| Integrationsname | Geben Sie den Integrationsnamen an, den Data Connectors in „Aktive Integrationsliste“ der Report Suite anzeigt. |
| E-Mail-Adresse | Geben Sie eine E-Mail-Adresse an, an welche die Integrationsdaten gesendet werden können. |
| Konto-ID | Dies ist die eindeutige Kennung, die Ihrer Organisation von Ihrem E-Mail-Serviceanbieter zugewiesen wurde. Sie wird verwendet, wenn Sie E-Mail-Kampagnendaten (z. B. Anzahl der versandten, geöffneten, angeklickten Elemente usw.) von Ihrem E-Mail-Serviceanbieter anfordern und Besuchersegmente an ihn senden. |
| Empfänger-ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse des optivo® broadmail-Systems. Diese „Empfänger-ID“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft, wird in das optivo® broadmail-System übertragen und kann für Remarketing-Zwecke genutzt werden. |
| Nachrichten-ID | (Erforderlich) Speichert die eindeutige Versand-ID. Diese Klassifizierungsdimensionen werden vom Data Connectors-Assistenten für die Nachrichten-ID erstellt: <br>a)**Kampagnen**: Kampagnen, die mit der Nachricht verknüpft sind. <br>b)**Kanal**: Der Übertragungskanal, dieser lautet ständig „optivo broadmail“. <br>c)**Ländercode**: Dieses Feld enthält den Ländercode des Herkunftslands des Absenders. Es ist eine Konstante „DE“. <br>d) **Bereitstellungswerkzeug**: Übertragungsmethode, immer „E-Mail“.<br> e) **Nachrichtenname**: Der Name des Mailings, wie er in optivo® broadmail konfiguriert ist. <br>f) **Startdatum**: Zeitstempel des Beginns dieses Mailings. |
| Zeit nach dem Klick | (Erforderlich) Dies ist erforderlich, um Informationen über eine Empfängeraktion an optivo® broadmail zu übermitteln, nachdem der Empfänger auf einen Link in einem Mailing geklickt hat. |
| Nach dem Klick auf Produkt | (Erforderlich) Dies ist erforderlich, um Informationen über eine Empfängeraktion an optivo® broadmail zu übermitteln, nachdem der Empfänger auf einen Link in einem Mailing geklickt hat. |
| Aktion nach dem Klick | (Erforderlich) Dies ist erforderlich, um Informationen über eine Empfängeraktion an optivo® broadmail zu übermitteln, nachdem der Empfänger auf einen Link in einem Mailing geklickt hat. |
| Hard-Bounce | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Mail-System importierten Hard-Bounce-Daten gespeichert werden. Anzahl der E-Mail-Nachrichten, die nicht an Empfänger versendet wurden und als dauerhaft nicht verfügbar angesehen werden. |
| Soft-Bounce | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Mail-System importierten Soft-Bounce-Daten gespeichert werden. Anzahl der E-Mail-Nachrichten, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| Angeklickt | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, mit dem die aus dem E-Mail-System importierten angeklickten E-Mail Daten gespeichert werden. Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| Geöffnet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten, geöffneten E-Mail-Daten speichert. Das Ereignis „Geöffnet“ zeigt die Anzahl der Besucher an, welche die E-Mail geöffnet haben. |
| Gesendet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten, gesendeten E-Mail-Daten speichert. Das Ereignis „Gesendet“ zeigt die Anzahl der gesendeten E-Mail-Nachrichten an. |
| Abo storniert | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten E-Mail-Daten zur Kündigung des Abonnements speichert. Mit dem Ereignis „Abo storniert“ können Sie die Anzahl der Besucher anzeigen, welche die E-Mail-Nachricht geöffnet, aber dann auf den Link „Abonnement kündigen“ geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrer Organisation abzuwählen. |
| Segmente | Aktivieren Sie vorhandene Segmente, die zusammen mit dieser Integration verwendet werden sollen (optional). |
| Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsberechtigungen. |
| Datenerfassung | Wählen Sie das **JavaScript-Plug-in** aus, wenn Sie das Plug-in „s_code.js“ als Erfassungsmodell für diese Integration verwenden möchten. Wählen Sie **Automatisierte Lösung** aus, wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Kennungen für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen Kennungen an, die für diese Integration verwendet werden:<ul><li>Abfragezeichenfolgenparameter der Nachrichten-ID: Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Landingpage angehängt hat.</li><li>Abfragezeichenfolgenparameter der Empfänger-ID: Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Mail-Partner an die URL der Landingpage anhängt.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Generieren Sie automatisch ein Dashboard und Lesezeichen für die Integration. |
