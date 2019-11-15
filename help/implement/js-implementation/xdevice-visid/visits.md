---
description: In Analytics wird jeder Serveraufruf, bei dem die „Anzahl besuchter Seiten“ gleich 1 ist, als ein Besuch gewertet.
keywords: Analytics Implementation
solution: Analytics
subtopic: Visitors
title: Besuche
topic: Developer and implementation
uuid: 3035be8f-6adc-45df-a3f2-5de6d3ed99ce
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Besuche

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie in der [Adobe Experience Cloud Device Co-op-Dokumentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

In Analytics wird jeder Server-Aufruf, bei dem die „Anzahl besuchter Seiten“ gleich 1 ist, als ein Besuch gewertet.

Wenn Sie sich die [vorherige Tabelle](/help/implement/js-implementation/xdevice-visid/visit-example.md) ansehen, ist dies viermal passiert: bei den Treffern 1, 9, 11 und 12. Ähnlich wie bei Besuchern wird auch dieser Wert nach der ersten Zuordnung wieder normal gezählt, da die [!UICONTROL Anzahl besuchter Seiten] aufgrund einer Änderung der effektiven [!UICONTROL Besucher-ID] wieder auf 1 zurückgesetzt wird.
