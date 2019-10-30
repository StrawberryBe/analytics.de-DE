---
description: Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.
seo-description: Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.
seo-title: Integration aktivieren
title: Integration aktivieren
uuid: 3b2acdb8-9a1f-4f17-92f2-6a3780a8f626
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Integration aktivieren{#activate-the-integration}

Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.

1. Starten Sie [Data Connectors](https://marketing.adobe.com/resources/help/en_US/genesis/c_overview.html) und klicken Sie auf **[!UICONTROL + Neu]** hinzufügen, um eine neue Integration[](https://marketing.adobe.com/resources/help/en_US/genesis/t_add_integration.html)hinzuzufügen.
1. Wählen Sie in der Liste " **[!UICONTROL Anzeigen]** "die Option "Nach Name **[!UICONTROL "und ziehen Sie die]Partnerintegration**[!DNL ~ ~]in einen leeren Steckplatz.
1. Füllen Sie den Integrationsassistenten mit den Informationen in der folgenden Tabelle aus:

| Feld | Beschreibung |
|--- |--- |
| Report Suite | Die Report Suite, an die die Daten aus dieser Integration gesendet werden. |
| Integrationsname | Geben Sie den Integrationsnamen an, den Data Connectors in der Liste Aktive Integration der Report Suite anzeigt. |
| E-Mail-Adresse | Geben Sie eine E-Mail-Adresse ein, um integrationsbezogene Informationen zu erhalten. |
| Konto-ID | Dies ist die eindeutige Kennung, die Ihrem Unternehmen von Ihrem E-Mail-Serviceanbieter zugewiesen wurde. Es wird bei der Anforderung von E-Mail-Kampagnendaten (z. Anzahl gesendet, # geöffnet, # angeklickt usw.) von Besuchersegmenten an Ihren E-Mail-Serviceanbieter senden und diese senden. |
| Recipient ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse aus dem optivo® Broadmail-System. Diese "Empfänger-ID"ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft. die in das optivo®-Broadmail-System eingebunden werden und für Remarketing genutzt werden können. |
| Nachrichten-ID | (Erforderlich) Speichert die eindeutige Mailing-ID. Diese Classification-Dimensionen werden vom Data Connectors-Assistenten für die Nachrichten-ID erstellt: <br>a)**Kampagnen**: Kampagnen, die mit der Nachricht verknüpft sind. <br>b)**Kanal**: Der Übertragungskanal, dies ist ständig "optivo Broadmail". <br>c)**Ländercode**: Dieses Feld enthält den Ländercode des Ursprungssenderlandes. Es ist eine Konstante "DE". <br>d) **Bereitstellungswerkzeug**: Übertragungsmethode, immer "E-Mail".<br> e) **Nachrichtenname**: Der Name des Mailings, wie er in optivo® Broadmail konfiguriert ist. <br>f) **Startdatum**: Zeitstempel des Beginns dieses Postings. |
| Post-Klickzeit | (Erforderlich) Dies ist erforderlich, um Informationen über eine Empfängeraktion an optivo®-Broadmail zu übermitteln, nachdem der Empfänger auf einen Link in einer Mailing-Anfrage geklickt hat. |
| Post-Click-Produkt | (Erforderlich) Dies ist erforderlich, um Informationen über eine Empfängeraktion an optivo®-Broadmail zu übermitteln, nachdem der Empfänger auf einen Link in einer Mailing-Anfrage geklickt hat. |
| Aktion nach Klick | (Erforderlich) Dies ist erforderlich, um Informationen über eine Empfängeraktion an optivo®-Broadmail zu übermitteln, nachdem der Empfänger auf einen Link in einer Mailing-Anfrage geklickt hat. |
| Hardbottom | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Mail-System importierten Daten auf den Festplatte gespeichert werden. Anzahl der E-Mail-Nachrichten, die nicht an Empfänger gesendet wurden und als dauerhaft nicht verfügbar angesehen werden. |
| Weicher Absprung | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, das die vom E-Mail-System importierten Soft Bounces-Daten speichert. Anzahl der E-Mail-Nachrichten, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| Angeklickt | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, mit dem die per E-Mail gesendeten Daten gespeichert werden. Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| Geöffnet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, mit dem die vom E-Mail-System importierten geöffneten Daten gespeichert werden. Das Ereignis "Geöffnet"zeigt die Anzahl der Besucher an, die die E-Mail geöffnet haben. |
| Gesendet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, mit dem die vom E-Mail-System importierten E-Mail-gesendeten Daten gespeichert werden. Das Ereignis "Gesendet"zeigt die Anzahl der gesendeten E-Mail-Nachrichten an. |
| Nicht abonniert | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, mit dem die vom E-Mail-System importierten E-Mail-Abmeldedaten gespeichert werden. Mit dem Abmeldung-Ereignis können Sie sehen, wie viele Besucher die E-Mail-Nachricht geöffnet haben, aber dann auf den Link Abmelden geklickt haben, um zukünftige E-Mail-Nachrichten Ihres Unternehmens abzuwählen. |
| Segmente | Aktivieren Sie vorhandene Segmente, die zusammen mit dieser Integration verwendet werden sollen (optional). |
|  Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsberechtigungen. |
| Datenerfassung | Wählen Sie das **JavaScript-Plug-in** , wenn Sie das Plug-in s_code.js als Erfassungsmodell für diese Integration verwenden möchten. Wählen Sie **Automatisierte Lösung** , wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Bezeichner für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen Bezeichner an, die für diese Integration verwendet werden:<ul><li>Abfragezeichenfolgenparameter der Nachrichten-ID: Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Einstiegsseite angehängt hat.</li><li>Abfragezeichenfolgenparameter der Empfänger-ID: Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Mail-Partner an die URL der Einstiegsseite anhängt.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Generieren Sie automatisch ein Dashboard und Lesezeichen für die Integration. |