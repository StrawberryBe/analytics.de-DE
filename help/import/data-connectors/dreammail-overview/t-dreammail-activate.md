---
description: Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.
seo-description: Verwenden Sie den Adobe Data Connectors-Konfigurationsassistenten, um die Integration einzurichten.
seo-title: Integration aktivieren
title: Integration aktivieren
uuid: 9084 b 691-291 d -49 f 7-9 fa 4-abda 507 e 060 d
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
| Integrations-UUID | Geben Sie die dreammail Integration-UUID an. |
| Kundenname | Geben Sie Ihren dreammail Client-Namen an. |
| Site-Name | Geben Sie den dreammail Site-Namen an. |
| Absprungbacks | Anzahl der E-Mail-Nachrichten, die aufgrund eines Problems mit der Auslieferung nicht an Empfänger übermittelt wurden. |
| Bereitgestellt | Anzahl erfolgreicher Nachrichten. |
| Bereitstellungsfehler | Nicht erfolgreiche Nachrichten. |
| HTML wird geöffnet | Anzahl der Besucher, die die E-Mail-Nachricht geöffnet haben. |
| Ungültig | Anzahl ungültiger E-Mail-Adressen. |
| Kampagne | Marketing-Kampagnen-ID. |
| Altigungen übergeben | Mit dem Ereignis "Angeklickt" können Sie erkennen, wie viele Besucher auf die E-Email geklickt haben. |
| E-Mail eVar | Eine E-Email-Adresse vom dreammail-System. Diese "E-Mail-evar" ist mit dem nachgeordneten Besucherverhalten auf der Site verknüpft (Warenkorbabbrüche, Käufe usw.). das in das dreammail-System gezogen wird und für Wiederverkaufszwecke genutzt werden kann. |
| Spotlight-Ereignis | Ereignis, das in Remarketing-Segmente exportiert werden kann. |
| Spotlight-Käufe | Ereignis, das in Remarketing-Segmente exportiert werden kann. |
| Spotlight-Wert | Umsatzereignis, das in Remarketing-Segmente exportiert werden kann. |
| Totalclicks | Mit dem Ereignis "Angeklickt" können Sie erkennen, wie viele Besucher auf die E-Email geklickt haben. |
| Segmente | Mit dieser Integration werden die im Abschnitt Partner-Segmente angezeigten Partner-definierten Segmente erstellt. Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration einbezogen werden sollen. |
| Zugriffsanforderungen | Aktivieren Sie die empfohlenen Zugriffsrechte. |
| Datenerfassung | Wählen Sie **javascript-Plug-in** , wenn Sie das Plug-in s_ code. js als Erfassungsmodell für diese Integration verwenden möchten (siehe). Wählen Sie **Automatisierte Lösung** , wenn Sie ein automatisiertes Collection-Modell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen ids für diese Integration an. Wenn Sie diese Option auswählen, geben Sie die eindeutigen ids für diese Integration an:<ul><li>Nachrichten-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Nachrichten-ID dar, die durch Ihren E-Email-Partner an die URL der Einstiegsseite angehängt wurde.</li><li>Empfänger-ID Abfragezeichenfolgenparameter: Dieser Wert stellt die Empfänger-ID an die URL der Einstiegsseite Ihres E-Email-Partners.</li></ul> |
| Dashboard- und Lesezeichenerstellung | Erstellen Sie automatisch ein Dashboard und Lesezeichen für die Integration. |