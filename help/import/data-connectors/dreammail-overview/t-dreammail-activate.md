---
description: Richten Sie die Integration mithilfe des Adobe-Konfigurationsassistenten für Data Connectors ein.
title: Aktivieren der Integration
uuid: 9084b691-291d-49f7-9fa4-abda507e060d
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 95%

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
| Integrations-UUID | Geben Sie Ihre Integrations-UUID für DreamMail an. |
| Clientname | Geben Sie Ihren Clientnamen für DreamMail an. |
| Site-Name | Geben Sie Ihren Site-Namen für DreamMail an. |
| Rückmeldungen | Anzahl der E-Mail-Nachrichten, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| Lieferung | Anzahl erfolgreicher Nachrichtenzustellungen. |
| Bereitstellungsfehler | Fehlgeschlagene Nachrichtenzustellungen. |
| HTML wird geöffnet | Anzahl der Besucher, welche die E-Mail-Nachricht geöffnet haben. |
| Ungültige | Anzahl der ungültigen E-Mail-Adressen. |
| Kampagne | Marketing-Kampagnen-ID. |
| Weiterleitungen | Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| E-Mail eVar | Eine E-Mail-Adresse aus dem DreamMail-System. Diese „E-Mail eVar“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft, wird in das DreamMail-System übertragen und kann für Remarketing-Zecke genutzt werden. |
| Spotlight-Ereignis | Ereignis, das in Remarketing-Segmente exportiert werden kann. |
| Spotlight-Käufe | Ereignis, das in Remarketing-Segmente exportiert werden kann. |
| Spotlight-Wert | Umsatzereignis, das in Remarketing-Segmente exportiert werden kann. |
| TotalClicks | Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| Segmente | Diese Integration erstellt die von Partnern definierten Segmente, die im Abschnitt „Partnersegmente“ angezeigt werden. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration aufgenommen werden sollen. |
| Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsberechtigungen. |
| Datenerfassung | Wählen Sie das **JavaScript-Plug-in** aus, wenn Sie das Plug-in „s_code.js“ als Erfassungsmodell für diese Integration nutzen möchten. Wählen Sie **Automatisierte Lösung** aus, wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Kennungen für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen Kennungen an, die für diese Integration verwendet werden:<ul><li>Abfragezeichenfolgenparameter der Nachrichten-ID: Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Landingpage angehängt hat.</li><li>Abfragezeichenfolgenparameter der Empfänger-ID: Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Mail-Partner an die URL der Landingpage anhängt.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Generieren Sie automatisch ein Dashboard und Lesezeichen für die Integration. |
