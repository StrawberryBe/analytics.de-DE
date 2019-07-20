---
description: Es gibt mehrere Möglichkeiten, Adobe Analytics zu implementieren.
keywords: Analytics-Implementierung; Implementierungsmethode; dynamisches Tag-Management; dtm; javascript
seo-description: Es gibt mehrere Möglichkeiten, Adobe Analytics zu implementieren.
seo-title: Implementierungsmethode auswählen
solution: Analytics
title: Implementierungsmethode auswählen
topic: Entwickler und Implementierung
uuid: 20 d 3317 f -7 c 63-4421-93 e 0-fff 60 dbd 9 f 87
translation-type: tm+mt
source-git-commit: b1e69abd65f171b804e7f56031e594890bbd27bb

---


# Implementierungsmethode auswählen

Es gibt mehrere Möglichkeiten, Adobe Analytics zu implementieren.

* [!UICONTROL Adobe Experience Platform Launch] (empfohlen)
* [!UICONTROL Dynamic Tag Management]
* JavaScript

## [!UICONTROL Adobe Experience Platform Launch]{#section_AEEA6AFE2C8D4182BC778F08EA171DC8}

[!UICONTROL Experience Platform Launch] ist die nächste Generation von Website-Tag und mobilen SDK-Verwaltungsfunktionen von Adobe. [!UICONTROL Erlebnisplattformstart] bietet Ihnen eine einfache Möglichkeit, alle Analyse-, Marketing- und Anzeigenintegrationen bereitzustellen und zu verwalten, die für relevante Kundenerfahrungen erforderlich sind.

[!UICONTROL Mit der Experience Platform Launch] können Sie ihre eigenen Integrationen mit dem Namen Erweiterungen [!DNL Experience Platform Launch]erstellen und verwalten. These extensions are available to web and mobile [!UICONTROL Experience Platform Launch] customers in an app-store experience, so customers can quickly install, configure, and deploy their integrations.

For more information, see [Getting Started with Experience Platform Launch](https://docs.adobelaunch.com/getting-started).

## [!UICONTROL Dynamic Tag Management] {#section_22E3F3F928894A6A8D77E6953E6CA51C}

[!UICONTROL Das dynamische Tag-Management] automatisiert die für die Implementierung [!DNL Analytics]erforderlichen Details. Geben Sie die erforderlichen Informationen auf einer formularbasierten Oberfläche ein, und das [!DNL Dynamic Tag Management] generiert den Code, den Sie zum Hinzufügen Ihrer Seiten benötigen.
Sie sollten mit javascript vertraut sein und grundlegende Analytics-Terminologie verstehen, wie zum Beispiel

* was [eVars](https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html) sind und wie sie funktionieren;
* wann ein [benutzerdefiniertes Ereignis](../../implement/analytics-terminology-basics/c-props-evars/event-custom.md#concept_CDA3C98C85B24A71B4B5C71F24BF918F) verwendet wird.

Weitere Informationen für den Zugriff auf das Dynamic Tag Management und dessen Verwendung finden Sie unter [Einstieg](https://marketing.adobe.com/resources/help/en_US/dtm/get_started.html) in der Produktdokumentation für das Dynamic Tag Management.

Weitere Informationen finden Sie unter [Implementieren von Analytics mit dynamischem Tag-Management](../../implement/c-implement-with-dtm/dtm-implementation-overview.md).

## JavaScript {#section_55429940D5094B9BB513E526F224D1B4}

Für die JavaScript-Implementierungsmethode müssen Sie die JavaScript-Codes auf Ihren Seiten manuell konfigurieren. Ein großer Teil dieser Arbeit kann vereinfacht werden, wenn Sie den Implementierungsmethoden von Experteneience Platform oder Dynamisches Tag-Management verwenden. Einige Benutzer benötigen jedoch möglicherweise die JavaScript-Methode.

Die JavaScript-Implementierung erfordert:

* umfassende JavaScript-Kenntnisse
* ein solides Verständnis der Konzepte und der Terminologie von Analytics

Weitere Informationen finden Sie unter [Implementieren von Analytics mit javascript](../../implement/js-implementation/javascript-implementation-overview.md).
