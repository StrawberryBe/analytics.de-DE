---
description: Richten Sie die Integration mithilfe des Adobe-Konfigurationsassistenten für Data Connectors ein.
title: Aktivieren der Integration
uuid: 0a5d2d45-5133-4259-96ce-c992a1e314ee
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 96%

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
| Konto-ID | Geben Sie Ihre Aprimo-Konto-ID ein. |
| Empfänger-ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse des Aprimo-Systems. Diese „Empfänger-ID“ ist mit dem nachgelagerten Besucherverhalten der Site-Empfänger-ID (Warenkorbabbrüche, Käufe usw.) verknüpft, wird in das Aprimo-System übertragen und kann für Remarketing-Zecke genutzt werden. |
| Angeklickt | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, mit dem die vom E-Mail-System importierten per E-Mail angeklickten Daten gespeichert werden. Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| Nachrichten-ID | (Erforderlich) Speichert die eindeutige Versand-ID. |
| Geöffnet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten, geöffneten E-Mail-Daten speichert. Das Ereignis „Geöffnet“ zeigt die Anzahl der Besucher an, welche die E-Mail geöffnet haben. |
| Empfänger-ID | (Erforderlich) Speichert die eindeutige Besucher-ID. |
| Gesendet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten, gesendeten E-Mail-Daten speichert. Das Ereignis „Gesendet“ zeigt die Anzahl der gesendeten E-Mail-Nachrichten an. |
| Absprünge | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Mail-System importierten Daten zu „Rücksendungen insgesamt“ gespeichert werden. Das Ereignis „Rücksendungen insgesamt“ zeigt die Anzahl der E-Mail-Nachrichten an, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| Abo storniert | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten E-Mail-Daten zur Kündigung des Abonnements speichert. Mit dem Ereignis „Abo storniert“ können Sie die Anzahl der Besucher anzeigen, welche die E-Mail-Nachricht geöffnet, aber dann auf den Link „Abonnement kündigen“ geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrer Organisation abzuwählen. |
| Segmente | Diese Integration erstellt die von Partnern definierten Segmente, die im Abschnitt „Partnersegmente“ angezeigt werden. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration aufgenommen werden sollen. |
| Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsberechtigungen. |
| Datenerfassung | Wählen Sie das **JavaScript-Plug-in** aus, wenn Sie das Plug-in „s_code.js“ als Erfassungsmodell für diese Integration verwenden möchten. |
Wählen Sie **Automatisierte Lösung** aus, wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Kennungen für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen Kennungen an, die für diese Integration verwendet werden:
<ul><li>Abfragezeichenfolgenparameter der Nachrichten-ID: Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Landingpage angehängt hat.</li>
<li>Abfragezeichenfolgenparameter der Empfänger-ID: Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Mail-Partner an die URL der Landingpage anhängt.</li></ul> |
|Dashboard- und Lesezeichenerstellung|Generieren Sie automatisch ein Dashboard und Lesezeichen für die Integration.|
