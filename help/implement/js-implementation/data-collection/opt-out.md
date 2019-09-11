---
description: 'null'
keywords: Analytics-Implementierung
seo-description: 'null'
seo-title: Adobe-Ausschlüsse implementieren
solution: Analytics
title: Adobe-Ausschlüsse implementieren
topic: Entwickler und Implementierung
uuid: fc 3 a 411 c -8476-409 d -99 de -5 b 34 ace 5019
translation-type: tm+mt
source-git-commit: b59e232b98c7e180478103ac2939a2c8c64a1407

---


# Adobe-Ausschlüsse implementieren

Einige Besucher Ihrer Website bevorzugen es möglicherweise, dass ihre Browserinformationen nicht von Adobe Experience Cloud-Produkten und -Diensten gesammelt und analysiert und ihnen keine relevanten Inhalte und Werbung bereitgestellt werden. Adobe bietet Ihnen die Möglichkeit, den Besuchern Ihrer Website die Option bereitzustellen, sich von der Datenerfassung durch die folgenden Adobe-Produkte ausschließen zu lassen:

* Adobe Analytics
* Adobe Target
* Adobe Audience Targeted Creative
* Adobe AudienceManager
* Adobe AdLens
* Adobe Experience Manager

## Empfehlungen für Datenschutzrichtlinien {#section_BBDEE21C259842F7881642E31FB3D9B7}

Adobe empfiehlt Ihnen, dass Sie den Besuchern Ihrer Website leicht auffindbare und leicht verständliche Informationen darüber bereitstellen, wie sie sich von der Erfassung von Browserinformationen durch Adobe-Produkte und -Dienste ausschließen lassen können.

Besucher können im [Datenschutzzentrum von Adobe](https://www.adobe.com/privacy.html) mehr darüber erfahren, wie Adobe die Informationen generell verwendet, die im Zusammenhang mit der Bereitstellung unserer Produkte und Dienste für unsere Kunden gesammelt werden. Da Sie jedoch selbst bestimmen, wie Sie unsere Dienste in Ihre Websites implementieren, liegt es in Ihrer Verantwortung, wie Sie die Besucher Ihrer Website darüber informieren, auf welche Weise sie unsere Produkte und Dienste nutzen. Sie sind selbst für die Erstellung Ihrer eigenen Datenschutzrichtlinien verantwortlich sowie für die Einhaltung Ihrer Datenschutzrichtlinien, die Einhaltung Ihres Servicevertrags mit Adobe und die Einhaltung jeglichen geltenden Rechts.

## Opt-outs for Adobe Analytics (including Reports &amp; Analytics, Data Warehouse, Ad Hoc Analysis) {#section_8089B80CDA4043C9BC2DED49E484E8D7}

Adobe offers three types of opt-outs for Adobe Analytics (including [!UICONTROL Reports &amp; Analytics], [!UICONTROL Data Warehouse], [!UICONTROL Ad Hoc Analysis]):

* Wenn Sie Adobe Analytics-Produkte mit Ihrem eigenen Erstanbieter-Cookie implementieren, müssen Sie [Ihren eigenen Ausschluss-Link](../../../implement/js-implementation/data-collection/opt-out-link.md#concept_C2C4F19811A445EF9E9BEAC709B568A9) für Besucher Ihrer Website entwickeln.
* Ihre Kunden haben die Möglichkeit des Ausschlusses mittels der Cookieeinstellungen des Browsers. Lesen Sie hierzu auch [Enable privacy settings for browser cookies](https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/?f=browser_cookie_settings) (in englischer Sprache).

Unabhängig davon, welchen Mechanismus zum Ausschluss von der Datenerfassung Sie verwenden, empfiehlt Adobe, dass Sie die Verfügbarkeit eines solchen Mechanismus in Ihren Datenschutzrichtlinien klar beschreiben und auch anderweitig jegliche gesetzlichen Vorschriften oder empfohlene Best Practices einhalten.
