---
description: In Analytics wird jede einzelne Besucher-ID als ein Unique Visitor gezählt.
keywords: Analytics Implementation
solution: Analytics
subtopic: Visitors
title: Besucher
topic: Developer and implementation
uuid: 16cfdb64-a3c6-4056-97da-3227cddcf1cd
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Besucher

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie in der [Adobe Experience Cloud Device Co-op-Dokumentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

In Analytics wird jede einzelne Besucher-ID als ein Unique Visitor gezählt.

Wenn Sie sich die [vorherige Tabelle](/help/implement/js-implementation/xdevice-visid/visit-example.md) ansehen, ist dies dreimal passiert: bei den Treffern 1, 9 und 10. Der Grund dafür ist der, dass bei beiden Server-Aufrufen die gleiche [!UICONTROL Besucher-ID] vorlag, obwohl beide Besuche von unterschiedlichen Geräten aus und im Abstand mehrerer Stunden erfolgten.

Dadurch kann sich die Zahl Unique Visitors erhöhen, wenn die geräteübergreifende Identifizierung aktiviert ist. So kann ein Besucher gleich doppelt gezählt werden: Das erste Mal bei seinem ursprünglichen Besuch, und das zweite Mal nach seiner Authentifizierung.

Wenn ein neuer Besucher Ihre Site anzeigt, wird das Cookie `s_vi` ausgefüllt und gespeichert. Auf dem Datenerfassungsserver wird ein neues Besucherprofil für diese Besucher-ID erstellt, und die effektive [!UICONTROL Besucher-ID] im Profil wird mit dem Cookie abgeglichen.

Wenn bei aktivierter geräteübergreifender Besucheridentifizierung bei einem späteren Treffer eine [!UICONTROL Besucher-ID]-Variable angegeben ist, (z. B. nach einer Authentifizierung), wird die effektive [!UICONTROL Besucher-ID] so aktualisiert, dass sie mit dem benutzerspezifischen Wert übereinstimmt. Das kann dazu führen, dass sich die effektive [!UICONTROL Besucher-ID] direkt nach der Authentifizierung ändert, sodass dadurch mehrere Besucher gezählt werden.

![](assets/visitors.png)

Nach der anfänglichen Zuordnung verhält sich die Besucherzählung wieder normal, da der Besucher über das [!UICONTROL Besucher-ID]-Cookie zugeordnet wird. Wenn der Besucher später wieder auf Ihre Site zurückkehrt und sich authentifiziert, wird der Besucherzähler nicht hochgezählt, da sich die effektive [!UICONTROL Besucher-ID] nach der Authentifizierung nicht mehr geändert hat.

![](assets/visitors_2.png)

