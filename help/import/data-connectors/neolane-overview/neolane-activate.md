---
description: Richten Sie die Integration mithilfe des Adobe-Konfigurationsassistenten für Data Connectors ein.
title: Aktivieren der Integration
uuid: 93c59f8e-3cf5-44c1-9a04-22460af93d5d
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8
workflow-type: tm+mt
source-wordcount: '425'
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
| Angeklickt | Gesamtzahl der E-Mail-Klicks. |
| Kampagnen-ID | Speichert die eindeutige Nachrichten-ID. Dies wird häufig in der Kampagnenvariablen gespeichert. |
| Geöffnet | Gesamtanzahl der geöffneten E-Mails. |
| Personenklicks | Anzahl der Personen, die geklickt haben. |
| Verarbeitet | Gesamtzahl verarbeiteter E-Mails. |
| Broadlog ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse des Neolane-Systems. Diese „Broadlog ID“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Broadlog ID-Abbrüche, Käufe usw.) verknüpft, wird in das Neolane-System übertragen und kann für Remarketing-Zecke genutzt werden. |
| Eingeplant | Anzahl der für den Versand geplanten E-Mail-Nachrichten. |
| Gesendet | Anzahl der gesendeten E-Mail-Nachrichten. |
| Rücksendungen insgesamt | Anzahl der E-Mail-Nachrichten, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| Eindeutige Klicks | Anzahl der einzelnen Klicks. |
| Eindeutig geöffnete Elemente | Anzahl der einzelnen Öffnungen. |
| Abo storniert | Anzahl der Besucher, welche die E-Mail-Nachricht geöffnet, aber dann auf den Link „Abonnement kündigen“ geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrer Organisation abzuwählen. |
| Segmente | Diese Integration erstellt die von Partnern definierten Segmente, die im Abschnitt „Partnersegmente“ angezeigt werden. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration aufgenommen werden sollen. |
| Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsberechtigungen. |
| Datenerfassung | Wählen Sie das **JavaScript-Plug-in** aus, wenn Sie das Plug-in „s_code.js“ als Erfassungsmodell für diese Integration verwenden möchten. Wählen Sie **Automatisierte Lösung** aus, wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Kennungen für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen Kennungen an, die für diese Integration verwendet werden: <ul><li>Abfragezeichenfolgenparameter der Nachrichten-ID: Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Landingpage angehängt hat.</li><li>Abfragezeichenfolgenparameter der Empfänger-ID: Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Mail-Partner an die URL der Landingpage anhängt.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Generieren Sie automatisch ein Dashboard und Lesezeichen für die Integration. |
