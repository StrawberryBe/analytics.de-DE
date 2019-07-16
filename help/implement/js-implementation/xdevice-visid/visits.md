---
description: In Analytics wird jeder Server-Aufruf, bei dem die „Anzahl besuchter Seiten“ gleich 1 ist, als ein Besuch gewertet.
keywords: Analytics-Implementierung
seo-description: In Analytics wird jeder Serveraufruf, bei dem die "Anzahl besuchter Seiten" gleich 1 ist, als ein Besuch gewertet.
seo-title: Besuche
solution: Analytics
subtopic: Besuchern
title: Besuchen
topic: Entwickler und Implementierung
uuid: 3035 be 8 f -6 adc -45 df-a 3 f 2-5 de 6 d 3 ed 99 ce
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Besuchen

>[!IMPORTANT]
>
>Diese Methode zur Identifizierung von Besuchern auf Gerätegeräten wird nicht mehr empfohlen. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

In Analytics wird jeder Server-Aufruf, bei dem die „Anzahl besuchter Seiten“ gleich 1 ist, als ein Besuch gewertet.

If you look at the [previous table](../../../implement/js-implementation/xdevice-visid/visit-example.md#concept_E3B32B8E539F4FDC8E3FA872328B87BA), this occurred 4 times: at hits 1, 9, 11, and 12. Ähnlich wie bei Besuchern wird auch dieser Wert nach der ersten Zuordnung wieder normal gezählt, da die [!UICONTROL Anzahl besuchter Seiten] aufgrund einer Änderung der effektiven [!UICONTROL Besucher-ID] wieder auf 1 zurückgesetzt wird.
