---
description: Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.
seo-description: Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.
seo-title: Integration aktivieren
title: Integration aktivieren
uuid: 9084b691-291d-49f7-9fa4-abda507e060d
translation-type: tm+mt
source-git-commit: a31f25e8a4681cf34525a7994b00580aa3aac15d

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
| Integrations-UUID | Geben Sie Ihre UUID zur Integration von DreamMail an. |
| Kundenname | Geben Sie Ihren DreamMail-Client-Namen an. |
| Site-Name | Geben Sie Ihren DreamMail-Site-Namen an. |
| Rücksendungen | Anzahl der E-Mail-Nachrichten, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| Ausgeliefert | Anzahl erfolgreicher Nachrichtenauslieferungen. |
| Lieferfehler | Fehlgeschlagene Nachrichten. |
| HTML wird geöffnet | Anzahl der Besucher, die die E-Mail-Nachricht geöffnet haben. |
| Ungültiges | Anzahl der ungültigen E-Mail-Adressen. |
| Kampagne | Marketing-Kampagnen-ID. |
| Alongs übermitteln | Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| E-Mail eVar | Eine E-Mail-Adresse aus dem DreamMail-System. Diese "E-Mail-eVar"ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft. , die in das DreamMail-System eingezogen und für Remarketing-Zwecke genutzt werden können. |
| Spotlight-Ereignis | Ereignis, das in Remarketing-Segmente exportiert werden kann. |
| Spotlight-Käufe | Ereignis, das in Remarketing-Segmente exportiert werden kann. |
| Spotlight-Wert | Umsatzereignis, das in Remarketing-Segmente exportiert werden kann. |
| TotalClicks | Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| Segmente | Diese Integration erstellt die von Partnern definierten Segmente, die im Abschnitt Partnersegmente angezeigt werden. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration einbezogen werden sollen. |
|  Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsberechtigungen. |
| Datenerfassung | Wählen Sie das **JavaScript-Plug-in** , wenn Sie das Plug-in s_code.js als Erfassungsmodell für diese Integration verwenden möchten (siehe ). Wählen Sie **Automatisierte Lösung** , wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Bezeichner für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen Bezeichner an, die für diese Integration verwendet werden:<ul><li>Abfragezeichenfolgenparameter der Nachrichten-ID: Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Einstiegsseite angehängt hat.</li><li>Abfragezeichenfolgenparameter der Empfänger-ID: Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Mail-Partner an die URL der Einstiegsseite anhängt.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Generieren Sie automatisch ein Dashboard und Lesezeichen für die Integration. |