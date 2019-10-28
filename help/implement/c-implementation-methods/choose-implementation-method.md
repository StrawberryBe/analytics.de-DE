---
description: Es gibt mehrere Möglichkeiten, Adobe Analytics zu implementieren.
keywords: Analytics-Implementierung;Implementierungsmethode;Dynamic Tag Management;DTM;JavaScript
seo-description: Es gibt mehrere Möglichkeiten, Adobe Analytics zu implementieren.
seo-title: Implementierungsmethode auswählen
solution: Analytics
title: Implementierungsmethode auswählen
topic: Entwickler und Implementierung
uuid: 20d3317f-7c63-4421-93e0-fff60dbd9f87
translation-type: ht
source-git-commit: b1e69abd65f171b804e7f56031e594890bbd27bb

---


# Implementierungsmethode auswählen

Es gibt mehrere Möglichkeiten, Adobe Analytics zu implementieren.

* [!UICONTROL Adobe Experience Platform Launch] (empfohlen)
* [!UICONTROL Dynamic Tag Management]
* JavaScript

## [!UICONTROL Adobe Experience Platform Launch] {#section_AEEA6AFE2C8D4182BC778F08EA171DC8}

[!UICONTROL Experience Platform Launch] umfasst die nächste Generation von Adobe-Verwaltungsfunktionen für Website-Tags und mobile SDKs. [!UICONTROL Experience Platform Launch] bietet Ihnen eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Integrationen bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerlebnisse erforderlich sind.

Mit [!UICONTROL Experience Platform Launch] kann jeder eigene Integrationen mit [!DNL Experience Platform Launch], auch Erweiterungen genannt, erstellen und verwalten. Diese Erweiterungen stehen Kunden der Web- und Mobile-Version von [!UICONTROL Experience Platform Launch] in einer App-Store-Oberfläche zur Verfügung, sodass sie ihre Integrationen schnell installieren, konfigurieren und bereitstellen können.

Weitere Informationen finden Sie unter [Erste Schritte mit Experience Platform Launch](https://docs.adobelaunch.com/getting-started).

## [!UICONTROL Dynamic Tag Management] {#section_22E3F3F928894A6A8D77E6953E6CA51C}

Das [!UICONTROL Dynamic Tag Management ] automatisiert einen Großteil der Detailarbeit, die zur Implementierung von [!DNL Analytics] erforderlich ist. Geben Sie die erforderlichen Informationen auf einer formularbasierten Oberfläche ein, und das [!DNL Dynamic Tag Management] generiert den Code, den Sie zum Hinzufügen Ihrer Seiten benötigen.
Es ist nützlich, sich mit JavaScript vertraut zu machen und grundlegende Analytics-Terminologie zu verstehen, z. B.

* Was ist ein [eVar](https://marketing.adobe.com/resources/help/de_DE/reference/conversion_var_admin.html) und wie funktioniert es
* Verwenden eines [benutzerspezifischen Ereignisses](../../implement/analytics-terminology-basics/c-props-evars/event-custom.md#concept_CDA3C98C85B24A71B4B5C71F24BF918F)

Informationen zum Zugriff auf Dynamic Tag Management und zum Einrichten und Ausführen finden Sie in der Produktdokumentation für Dynamic Tag Management unter [Erste Schritte](https://marketing.adobe.com/resources/help/de_DE/dtm/get_started.html).

Weitere Informationen finden Sie unter [Implementieren von Analytics mit Dynamic Tag Management](../../implement/c-implement-with-dtm/dtm-implementation-overview.md).

## JavaScript {#section_55429940D5094B9BB513E526F224D1B4}

Für die JavaScript-Implementierungsmethode müssen Sie die JavaScript-Codes auf Ihren Seiten manuell konfigurieren. Ein Großteil dieser Bemühungen kann vereinfacht werden, wenn Sie die Implementierungsmethoden von Experience Platform Launch oder Dynamic Tag Management verwenden. Einige Benutzer benötigen jedoch möglicherweise die JavaScript-Methode.

Die JavaScript-Implementierung erfordert:

* umfassende JavaScript-Kenntnisse
* ein solides Verständnis der Konzepte und der Terminologie von Analytics

Weitere Informationen finden Sie unter [Analytics mit JavaScript implementieren ](../../implement/js-implementation/javascript-implementation-overview.md)
