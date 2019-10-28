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
translation-type: ht
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Besuche

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie in der [Adobe Experience Cloud-Gerätekooperations-Dokumentation](https://marketing.adobe.com/resources/help/de_DE/mcdc/).

In Analytics wird jeder Server-Aufruf, bei dem die „Anzahl besuchter Seiten“ gleich 1 ist, als ein Besuch gewertet.

Wenn Sie sich die [vorherige Tabelle](../../../implement/js-implementation/xdevice-visid/visit-example.md#concept_E3B32B8E539F4FDC8E3FA872328B87BA) ansehen, ist dies viermal passiert: bei den Treffern 1, 9, 11 und 12. Ähnlich wie bei Besuchern wird auch dieser Wert nach der ersten Zuordnung wieder normal gezählt, da die [!UICONTROL Anzahl besuchter Seiten] aufgrund einer Änderung der effektiven [!UICONTROL Besucher-ID] wieder auf 1 zurückgesetzt wird.
