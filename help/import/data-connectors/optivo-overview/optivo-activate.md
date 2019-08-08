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
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Integration aktivieren{#activate-the-integration}

Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.

1. Starten [Sie Data Connectors](https://marketing.adobe.com/resources/help/en_US/genesis/c_overview.html) und klicken **[!UICONTROL Sie auf + Neu]** hinzufügen, um [eine neue Integration hinzuzufügen](https://marketing.adobe.com/resources/help/en_US/genesis/t_add_integration.html).
1. Wählen Sie in der **[!UICONTROL Liste "Anzeigen"]** die Option **[!UICONTROL " Nach Name]** " aus und ziehen Sie die [!DNL ~Partnerintegration~] in einen leeren Plugin-Slot.
1. Schließen Sie den Integrationsassistenten mit den Informationen in der folgenden Tabelle ab:

| Feld | Beschreibung |
|--- |--- |
| Report Suite | Die Report Suite, die die Daten aus dieser Integration erhält. |
| Integrationsname | Geben Sie den Integrationsnamen an, den Data Connectors in der aktiven Integrationsliste der Report Suite anzeigt. |
| E-Mail-Adresse | Geben Sie eine E-Mail-Adresse an, um integrationsbezogene Informationen zu erhalten. |
| Konto-ID | Dies ist die eindeutige Kennung, die Ihr E-Mail-Serviceanbieter Ihrer Organisation zugewiesen hat. Sie wird verwendet, wenn Sie E-Email-Kampagnendaten anfordern (z. B. # Gesendet, # Geöffnet, # Angeklickt usw.) von und senden Sie Besuchersegmente an Ihren E-Mail-Serviceanbieter. |
| Recipient ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Email-Adresse vom Optivo® Broadmail-System. Diese "Empfänger-ID" ist mit dem nachgeordneten Besucherverhalten auf der Site verknüpft (Warenkorbabbrüche, Käufe usw.). das in das Optivo® Broadmail-System gezogen wird und für Wiederverkaufszwecke genutzt werden kann. |
| Nachrichten-ID | (Erforderlich) Speichert die eindeutige Mailingid. Diese Classification-Dimensionen werden vom Data Connectors-Assistenten für die Nachrichten-ID erstellt: a)**Kampagnen**: Kampagnen, die mit der Nachricht verbunden sind. b)**Kanal**: Der Kanal der Übertragung ist ständig "optivo broadmail" . c)**Ländercode**: Dieses Feld enthält den Ländercode des Ursprungssenders. Es handelt sich um eine Konstante "DE" . d) **Bereitstellungswerkzeug**: Übertragungsmethode, immer "E-Mail" . e) **Nachrichtenname**: Der Name des Postings, der in der optivo® Broadmail konfiguriert ist. f) **Startdatum**: Zeitstempel des Starts dieses Postings. |
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
| Datenerfassung | Wählen Sie **javascript-Plug-in,** wenn Sie das Plug-in s_ code. js als Collection-Modell für diese Integration verwenden möchten. Wählen Sie **Automatisierte Lösung** , wenn Sie ein automatisiertes Collection-Modell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen ids für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen ids für diese Integration an:<ul><li>Nachrichten-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Nachrichten-ID dar, die Ihr E-Email-Partner an die URL der Einstiegsseite angehängt hat.</li><li>Empfänger-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Empfänger-ID an die URL der Einstiegsseite Ihres E-Email-Partners.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Erstellen Sie automatisch ein Dashboard und Lesezeichen für die Integration. |