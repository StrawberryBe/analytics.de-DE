---
description: In Analytics wird jede einzelne Besucher-ID als ein Unique Visitor gezählt.
keywords: Analytics-Implementierung
seo-description: In Analytics wird jede einzelne Besucher-ID als ein individueller Besucher gezählt.
seo-title: Besucher
solution: Analytics
subtopic: Besucher
title: Besucher
topic: Entwickler und Implementierung
uuid: 16 cfdb 64-a 3 c 6-4056-97 da -3227 cddcf 1 cd
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Besuchern

>[!IMPORTANT]
>
>Diese Methode zur Identifizierung von Besuchern auf Gerätegeräten wird nicht mehr empfohlen. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

In Analytics wird jede einzelne Besucher-ID als ein Unique Visitor gezählt.

If you look at the [previous table](../../../implement/js-implementation/xdevice-visid/visit-example.md#concept_E3B32B8E539F4FDC8E3FA872328B87BA), this occurred 3 times: at hits 1, 9, and 10. Der Grund dafür ist der, dass bei beiden Server-Aufrufen die gleiche [!UICONTROL Besucher-ID] vorlag, obwohl beide Besuche von unterschiedlichen Geräten aus und im Abstand mehrerer Stunden erfolgten.

Dadurch kann sich die Zahl Unique Visitors erhöhen, wenn die geräteübergreifende Identifizierung aktiviert ist. So kann ein Besucher gleich doppelt gezählt werden: Das erste Mal bei seinem ursprünglichen Besuch, und das zweite Mal nach seiner Authentifizierung.

Wenn ein neuer Besucher Ihre Site anzeigt, wird das Cookie `s_vi`   ausgefüllt und gespeichert. Auf dem Datenerfassungsserver wird ein neues Besucherprofil für diese Besucher-ID erstellt, und die effektive [!UICONTROL Besucher-ID] im Profil wird mit dem Cookie abgeglichen.

Wenn bei aktivierter geräteübergreifender Besucheridentifizierung bei einem späteren Treffer eine [!UICONTROL Besucher-ID]-Variable angegeben ist, (z. B. nach einer Authentifizierung), wird die effektive [!UICONTROL Besucher-ID] so aktualisiert, dass sie mit dem benutzerspezifischen Wert übereinstimmt. Das kann dazu führen, dass sich die effektive [!UICONTROL Besucher-ID] direkt nach der Authentifizierung ändert, sodass dadurch mehrere Besucher gezählt werden.

![](assets/visitors.png)

Nach der anfänglichen Zuordnung verhält sich die Besucherzählung wieder normal, da der Besucher über das [!UICONTROL Besucher-ID]-Cookie zugeordnet wird. Wenn der Besucher später wieder auf Ihre Site zurückkehrt und sich authentifiziert, wird der Besucherzähler nicht hochgezählt, da sich die effektive [!UICONTROL Besucher-ID] nach der Authentifizierung nicht mehr geändert hat.

![](assets/visitors_2.png)

