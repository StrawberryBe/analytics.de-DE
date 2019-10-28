---
description: Beispiel mit einer Reihe von Server-Aufrufen, die bei einer gewöhnlichen Kundeninteraktion gesendet werden.
keywords: Analytics-Implementierung
seo-description: Beispiel mit einer Reihe von Server-Aufrufen, die bei einer gewöhnlichen Kundeninteraktion gesendet werden.
seo-title: Beispielbesuch
solution: Analytics
subtopic: Besucher
title: Beispielbesuch
topic: Entwickler und Implementierung
uuid: bc5f8f56-52e3-42d8-af1a-7f5c7b9496c0
translation-type: ht
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Beispielbesuch

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie in der [Adobe Experience Cloud-Gerätekooperations-Dokumentation](https://marketing.adobe.com/resources/help/de_DE/mcdc/).

Beispiel mit einer Reihe von Server-Aufrufen, die bei einer gewöhnlichen Kundeninteraktion gesendet werden.

| Server-Aufruf | Aktion | Besucher-ID-Cookie | Besucher-ID-Variable | Effektive Besucher-ID | Anzahl besuchter Seiten | Besuchnummer |
|--- |--- |--- |--- |--- |--- |--- |
| 1 | Ein Besucher klickt auf einen Link in einer Marketing-E-Mail und gelangt so von seinem privaten Computer aus auf Ihre Website. Dieser Besucher hat Ihre Website zuvor bereits 7 Mal besucht. | 1 | - | 1 | 1 | 8 |
| 2-8 | Er ruft 7 weitere Seiten auf Ihrer Website auf. | 1 | - | 1 | 2-8 | 8 |
| 9 | Authentifiziert sich auf privatem Computer. | 1 | CID1 | CID1 | 9 <br>Dies ist der erste Treffer für CID1, also übernimmt CID1 und wird für das Besucherprofil von Besucher-ID 1 weiterverwendet.</br> | 8 |
| 10 | Besucht eine weitere Seite. | 1 | CID1 | CID1 | 10 | 8 |
| 11 | Öffnet Ihre Website auf seinem Laptop im Büro. Dieser Besucher hat Ihre Website zuvor nicht mithilfe dieses Geräts besucht. | 2 | - | 2 | 1 | 1 |
| 12 | Authentifiziert sich auf Laptop. | 2 | CID1 | CID1 | 1 | 9 |
| 13 | Zeigt eine weitere Seite an. | 2 | CID1 | CID1 | 2 | 9 |