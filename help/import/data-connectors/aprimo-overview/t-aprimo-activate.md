---
description: Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.
seo-description: Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.
seo-title: Integration aktivieren
title: Integration aktivieren
uuid: 0a5d2d45-5133-4259-96ce-c992a1e314ee
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Integration aktivieren {#activate-the-integration}

Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.

1. Starten Sie [Data Connectors](https://marketing.adobe.com/resources/help/en_US/genesis/c_overview.html) und klicken Sie auf **[!UICONTROL + Neu]** hinzufügen, um eine neue Integration[](https://marketing.adobe.com/resources/help/en_US/genesis/t_add_integration.html)hinzuzufügen.
1. Wählen Sie in der Liste " **[!UICONTROL Anzeigen]** "die Option "Nach Name **[!UICONTROL "und ziehen Sie die]Partnerintegration**[!DNL ~ ~]in einen leeren Steckplatz.
1. Füllen Sie den Integrationsassistenten mit den Informationen in der folgenden Tabelle aus:

| Feld | Beschreibung |
|--- |--- |
| Report Suite | Die Report Suite, an die die Daten aus dieser Integration gesendet werden. |
| Integrationsname | Geben Sie den Integrationsnamen an, den Data Connectors in der Liste Aktive Integration der Report Suite anzeigt. |
| Konto-ID | Geben Sie Ihre Aprimo-Konto-ID ein. |
| Recipient ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse des Aprimo-Systems. Diese "Empfänger-ID"ist mit dem nachgelagerten Besucherverhalten auf der Site-Empfänger-ID (Warenkorbabbrüche, Käufe usw.) verknüpft. die in das Aprimo-System eingezogen werden und für die Wiedervermarktung genutzt werden können. |
| Angeklickt | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, mit dem die vom E-Mail-System importierten per E-Mail angeklickten Daten gespeichert werden. Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| Nachrichten-ID | (Erforderlich) Speichert die eindeutige Mailing-ID. |
| Geöffnet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, mit dem die vom E-Mail-System importierten geöffneten Daten gespeichert werden. Das Ereignis "Geöffnet"zeigt die Anzahl der Besucher an, die die E-Mail geöffnet haben. |
| Recipient ID | (Erforderlich) Speichert die Unique Visitor-ID. |
| Gesendet | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Mail-System importierten E-Mail-Versanddaten gespeichert werden. Das Ereignis "Gesendet"zeigt die Anzahl der gesendeten E-Mail-Nachrichten an. |
| Absprünge | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Mail-System importierten Absprungdaten insgesamt gespeichert werden. Das Ereignis "Absprünge insgesamt"zeigt die Anzahl der E-Mail-Nachrichten an, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| Nicht abonniert | (Erforderlich) Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Mail-System importierten E-Mail-Abonnentendaten gespeichert werden. Mit dem Abmeldung-Ereignis können Sie sehen, wie viele Besucher die E-Mail-Nachricht geöffnet haben, aber dann auf den Link Abmelden geklickt haben, um zukünftige E-Mail-Nachrichten Ihres Unternehmens abzuwählen. |
| Segmente | Diese Integration erstellt die von Partnern definierten Segmente, die im Abschnitt Partnersegmente angezeigt werden. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration einbezogen werden sollen. |
|  Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsberechtigungen. |
| Datenerfassung | Wählen Sie das **JavaScript-Plug-in** , wenn Sie das Plug-in s_code.js als Erfassungsmodell für diese Integration verwenden möchten. |
Wählen Sie **Automatisierte Lösung** , wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Bezeichner für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen Bezeichner an, die für diese Integration verwendet werden:
<ul><li>Abfragezeichenfolgenparameter der Nachrichten-ID: Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Einstiegsseite angehängt hat.</li>
<li>Abfragezeichenfolgenparameter der Empfänger-ID: Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Mail-Partner an die URL der Einstiegsseite anhängt.</li></ul>||Dashboard- und Lesezeichenerstellung|Dashboard und Lesezeichen für die Integration automatisch erstellen.|
