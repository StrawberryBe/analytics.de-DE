---
title: Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung
description: Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung
translation-type: tm+mt
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 100%

---


# Häufig gestellte Fragen zur geräteübergreifenden Identifizierung von Besuchern

Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung.

**Was ist der Unterschied zwischen der geräteübergreifenden Besucheridentifizierung und Cross-Device Analytics?**

Bei der geräteübergreifenden Besucheridentifizierung wird die `visitorID`-Variable verwendet, um Geräte miteinander zu verbinden. Dabei gibt es einige wesentliche Einschränkungen. Eine der größten Einschränkungen dieser Identifizierungsmethode besteht darin, dass nicht authentifizierte Treffer isoliert werden, es sei denn, das Gerät wurde bereits erkannt. Diese nicht authentifizierten Treffer können die Unique Visitor-Anzahl überhöhen.

Cross-Device Analytics ist die neueste Methode zur geräteübergreifenden Besucheridentifizierung von Adobe. Sie verwendet den Experience Cloud ID-Dienst und das Gerätediagramm, um Besuche von verschiedenen Geräten rückwirkend zu verbinden. CDA erfordert die Verwendung der `setCustomerIDs`-Funktion, um zu ermitteln, welche Geräte von demselben Besucher verwendet werden.

**Wie behandelt die geräteübergreifende Besucheridentifizierung Segmente?**

Die geräteübergreifende Besucheridentifizierung behandelt Segmente ähnlich wie andere Funktionen. Sie prüft jeden einzelnen Treffer, um zu sehen, ob er mit den Segmentkriterien übereinstimmt, und schließt diese Treffer in Ihre Daten ein, wenn sie übereinstimmen. Segmente, die besuchs- und besucherbasierte Behälter verwenden, betrachten weiterhin die Besucher-ID. Stellen Sie sicher, dass Ihre Implementierung die `visitorID`-Variable wo immer möglich verwendet, um Unique Visitors für die Segmentierung konsistent zu identifizieren.
