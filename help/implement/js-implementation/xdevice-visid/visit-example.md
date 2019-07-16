---
description: Beispiel mit einer Reihe von Server-Aufrufen, die bei einer gewöhnlichen Kundeninteraktion gesendet werden.
keywords: Analytics-Implementierung
seo-description: Beispiel mit einer Reihe von Server-Aufrufen, die bei einer gewöhnlichen Kundeninteraktion gesendet werden.
seo-title: Beispielbesuch
solution: Analytics
subtopic: Besuchern
title: Beispielbesuch
topic: Entwickler und Implementierung
uuid: bc 5 f 8 f 56-52 e 3-42 d 8-af 1 a -7 f 5 c 7 b 9496 c 0
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Beispielbesuch

>[!IMPORTANT]
>
>Diese Methode zur Identifizierung von Besuchern auf Gerätegeräten wird nicht mehr empfohlen. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

Beispiel mit einer Reihe von Server-Aufrufen, die bei einer gewöhnlichen Kundeninteraktion gesendet werden.

| Server-Aufruf | Aktion | Besucher-ID-Cookie | Besucher-ID-Variable | Effektive Besucher-ID | Anzahl besuchter Seiten | Besuchsnummer |
|--- |--- |--- |--- |--- |--- |--- |
| 1 | Ein Besucher klickt auf einen Link in einer Marketing-E-Mail und gelangt so von seinem privaten Computer aus auf Ihre Website. Dieser Besucher hat Ihre Website zuvor bereits 7 Mal besucht. | 1 | - | 1 | 1 | 8 |
| 2-8 | Er ruft 7 weitere Seiten auf Ihrer Website auf. | 1 | - | 1 | 2-8 | 8 |
| 9 | Authentifiziert sich auf privatem Computer. | 1 | CID1 | CID1 | 9 <br>This is CID1&#39;s first hit ever, so it takes over and continues on the visitor profile from Visitor ID 1.</br> | 8 |
| 10 | Besucht eine weitere Seite. | 1 | CID1 | CID1 | 10 | 8 |
| 11 | Öffnet Ihre Website auf seinem Laptop im Büro. Dieser Besucher hat Ihre Website zuvor nicht mithilfe dieses Geräts besucht. | 2 | - | 2 | 1 | 1 |
| 12 | Authentifiziert sich auf Laptop. | 2 | CID1 | CID1 | 1 | 9 |
| 13 | Zeigt eine weitere Seite an. | 2 | CID1 | CID1 | 2 | 9 |