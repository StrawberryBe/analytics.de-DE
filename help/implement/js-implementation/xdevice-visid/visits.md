---
description: In Analytics wird jeder Server-Aufruf, bei dem die „Anzahl besuchter Seiten“ gleich 1 ist, als ein Besuch gewertet.
keywords: Analytics-Implementierung
seo-description: In Analytics wird jeder Serveraufruf, bei dem die „Anzahl besuchter Seiten“ gleich 1 ist, als ein Besuch gewertet.
seo-title: Besuche
solution: Analytics
subtopic: Besucher
title: Besuche
topic: Entwickler und Implementierung
uuid: 3035be8f-6adc-45df-a3f2-5de6d3ed99ce
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# Besuche

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie in der [Adobe Experience Cloud Device Co-op-Dokumentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

In Analytics wird jeder Server-Aufruf, bei dem die „Anzahl besuchter Seiten“ gleich 1 ist, als ein Besuch gewertet.

Wenn Sie sich die [vorherige Tabelle](/help/implement/js-implementation/xdevice-visid/visit-example.md) ansehen, ist dies viermal passiert: bei den Treffern 1, 9, 11 und 12. Ähnlich wie bei Besuchern wird auch dieser Wert nach der ersten Zuordnung wieder normal gezählt, da die [!UICONTROL Anzahl besuchter Seiten] aufgrund einer Änderung der effektiven [!UICONTROL Besucher-ID] wieder auf 1 zurückgesetzt wird.
