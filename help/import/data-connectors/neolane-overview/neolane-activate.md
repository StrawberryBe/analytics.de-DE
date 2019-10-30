---
description: Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.
seo-description: Richten Sie die Integration mithilfe des Adobe Data Connectors-Konfigurationsassistenten ein.
seo-title: Integration aktivieren
title: Integration aktivieren
uuid: 93c59f8e-3cf5-44c1-9a04-22460af93d5d
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
| Angeklickt | Gesamtzahl der E-Mail-Klicks. |
| Kampagnen-ID | Speichert die eindeutige Nachrichten-ID. Dies wird häufig in der Kampagnenvariablen gespeichert. |
| Geöffnet | Gesamtanzahl der geöffneten E-Mails. |
| Personenklicks | Anzahl der Personen, die geklickt haben. |
| verarbeitet | Gesamtzahl verarbeiteter E-Mails. |
| Broadlog ID | Diese ID ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse des Neolane-Systems. Diese "Broadlog-ID"ist mit dem nachgelagerten Besucherverhalten auf der Site verknüpft (Abbruch der Broadlog-ID, Einkäufe usw.) die in das Neolane-System eingebunden werden und für Remarketing-Zwecke genutzt werden können. |
| Eingeplant | Anzahl der für die Auslieferung geplanten E-Mail-Nachrichten. |
| Gesendet | Anzahl der gesendeten E-Mail-Nachrichten. |
| Absprünge insgesamt | Anzahl der E-Mail-Nachrichten, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| Eindeutige Klicks | Anzahl der einzelnen Klicks. |
| Eindeutige Öffnen | Anzahl der einzelnen Schritte. |
| Nicht abonniert | Anzahl der Besucher, die die E-Mail-Nachricht geöffnet, aber dann auf den Link "Abmelden"geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrer Organisation abzuwählen. |
| Segmente | Diese Integration erstellt die von Partnern definierten Segmente, die im Abschnitt Partnersegmente angezeigt werden. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration einbezogen werden sollen. |
|  Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsberechtigungen. |
| Datenerfassung | Wählen Sie das **JavaScript-Plug-in** , wenn Sie das Plug-in s_code.js als Erfassungsmodell für diese Integration verwenden möchten. Wählen Sie **Automatisierte Lösung** , wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Bezeichner für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen Bezeichner an, die für diese Integration verwendet werden: <ul><li>Abfragezeichenfolgenparameter der Nachrichten-ID: Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Einstiegsseite angehängt hat.</li><li>Abfragezeichenfolgenparameter der Empfänger-ID: Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Mail-Partner an die URL der Einstiegsseite anhängt.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Generieren Sie automatisch ein Dashboard und Lesezeichen für die Integration. |
