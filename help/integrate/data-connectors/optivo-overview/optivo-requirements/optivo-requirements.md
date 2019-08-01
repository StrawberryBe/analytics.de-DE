---
description: 'Führen Sie vor dem Start der Data Connectors-Integration die folgenden Anforderungen aus. '
seo-description: 'Führen Sie vor dem Start der Data Connectors-Integration die folgenden Anforderungen aus. '
seo-title: Vor der Aktivierung
title: Vor der Aktivierung
uuid: 45275635-a 80 d -46 c 2-b 9 ad -985 df 5737 bf 2
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Before You Activate{#before-you-activate}

Bevor Sie die Data Connectors-Integration starten, führen Sie die folgenden Anforderungen aus:

## Adobe Analytics Requirements {#section-960e70fd2eae4a1cb88a2e4b53a97313}

* **Report Suite spezifisch:** Wir empfehlen, dass diese Integration Report Suite-spezifisch ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren.
* **Verfügbare und konfigurierte Adobe Analytics-Variablen:** Für diese Integration sind benutzerspezifische Ereignisse und benutzerdefinierte evars erforderlich. See [Adobe Analytics Integration Variables](../../optivo-overview/optivo-requirements/optivo-variables.md#concept-8ebd2bde4a1c4b0aad2987e050ffbbfc).

* **Autorisierter Vertreter:** Es wird empfohlen, dass Ihr Unternehmen bei Aktivierung dieser Integration Gebühren in Übereinstimmung mit Ihrem Servicevertrag mit Adobe, Inc. oder Ihrem Servicevertrag bei einem der vertrauenswürdigen Partner von Adobe erbringt. Durch Aktivierung dieser Integration stellen Sie sicher, dass Sie ein autorisierter Vertreter Ihres Unternehmens sind; und somit beschließt Ihr Unternehmen, die Gebühren, sofern vorhanden, in der oben beschriebenen Servicevereinbarung zu zahlen.
* **Nachrichten-ID:** Die Integration erfordert, dass wir eine Nachrichten-ID in einer Adobe Analytics-Variable (evar) erfassen und speichern. Diese IDs sind erforderlich, um die gesendeten Nachrichten zu identifizieren. Während des Setup-Prozesses müssen Sie eine evar zu diesem Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* ** [!DNL ~Partner~]:** The integration requires that we capture and store a " [!DNL ~Partner~]" within a Adobe Analytics variable (eVar). This ID is an encoded or numeric representation of an email address from the [!DNL ~Partner~] system. This " [!DNL ~Partner~]" is associated with downstream visitor behavior on the site (cart abandons, purchases, etc.) that is pulled into the [!DNL ~Partner~] system and can be leveraged for remarketing purposes. Während des Setup-Prozesses müssen Sie eine evar zu diesem Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Zeitpunkt des Beitrags:** Im Rahmen des Setup-Prozesses erfordert diese Integration eine Zuweisung zu einer evar, die dem Zeitpunkt einer Beitragsaktion entspricht. This is needed to transmit information about a recipient action to [!DNL ~Partner~] after the recipient clicked a link in a mailing.

* **Nach dem Klicken auf Produkt:** Im Rahmen des Setup-Prozesses erfordert diese Integration eine Zuordnung zu einer evar, die dem angebotenen Produkt entspricht, das mit einer Beitragsaktion verknüpft ist. This is needed to transmit information about a recipient action to [!DNL ~Partner~] after the recipient clicked a link in a mailing.

* **Beitragstyp der Aktion:** Im Rahmen des Setup-Prozesses erfordert diese Integration eine Zuweisung zu einer evar, die dem Typ einer Beitragsaktion entspricht. This is needed to transmit information about a recipient action to [!DNL ~Partner~] after the recipient clicked a link in a mailing.

* **Datenschutzeinhaltung:** Sie sollten wissen, dass diese Funktion durch Aktivierung der Empfänger- oder Besucher-ID-Verfolgung personenbezogene Informationen zu Ihren Site-Besuchern nachverfolgen kann. Dies hat Auswirkungen auf Datenschutzbestimmungen, die die Implementierung angemessener Vorgehensweisen durch Ihr Unternehmen erfordern, z. B. die Bereitstellung und Zustimmung Ihrer Site-Besucher.

## Section Title {#section-370f12579a224d509545cba1c28adb22}

