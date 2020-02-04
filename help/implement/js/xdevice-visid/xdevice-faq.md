---
title: Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung
description: Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Häufig gestellte Fragen zur geräteübergreifenden Identifizierung von Besuchern

Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung.

**Was ist der Unterschied zwischen der geräteübergreifenden Besucheridentifizierung und der geräteübergreifenden Analyse?**

Bei der geräteübergreifenden Besucheridentifizierung wird die `visitorID` Variable verwendet, um Geräte mit verschiedenen Einschränkungen zu verbinden. Eine der größten Einschränkungen dieser Identifizierungsmethode besteht darin, dass nicht authentifizierte Treffer isoliert werden, es sei denn, das Gerät wurde bereits erkannt. Diese nicht authentifizierten Treffer können die Zählung Ihrer individuellen Besucher erhöhen.

Geräteübergreifende Analytics ist die neueste geräteübergreifende Besucheridentifizierungsmethode von Adobe. Es verwendet das Experience Cloud ID-Dienst- und Gerätediagramm, um Besuche von verschiedenen Geräten rückwirkend zu verbinden. CDA erfordert die Verwendung der `setCustomerIDs` Funktion, um zu ermitteln, welche Geräte von demselben Besucher verwendet werden.

**Wie behandelt die geräteübergreifende Besucheridentifizierung Segmente?**

Die geräteübergreifende Besucheridentifizierung behandelt Segmente ähnlich wie andere Funktionen. Er prüft jeden einzelnen Treffer, um zu sehen, ob er mit den Segmentkriterien übereinstimmt, und schließt diese Treffer in Ihre Daten ein, wenn sie übereinstimmen. Segmente, die Besuchs- und besucherbasierte Behälter verwenden, betrachten weiterhin die Besucher-ID. Stellen Sie sicher, dass Ihre Implementierung nach Möglichkeit die `visitorID` Variable verwendet, um eindeutige Besucher für die Segmentierung einheitlich zu identifizieren.
