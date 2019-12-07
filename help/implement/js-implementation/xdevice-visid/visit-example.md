---
description: Beispiel mit einer Reihe von Server-Aufrufen, die bei einer gewöhnlichen Kundeninteraktion gesendet werden.
keywords: Analytics Implementation
subtopic: Visitors
title: Beispiel zur geräteübergreifenden Besucheridentifizierung
topic: Developer and implementation
uuid: bc5f8f56-52e3-42d8-af1a-7f5c7b9496c0
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Beispiel zur geräteübergreifenden Besucheridentifizierung

> [!IMPORTANT] Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Siehe [Geräteübergreifende Analyse](/help/components/cda/cda-home.md) im Komponenten-Benutzerhandbuch.

Das folgende Beispiel zeigt, wie die geräteübergreifende Besucheridentifizierung mithilfe eines Beispiels von Serveraufrufen funktioniert, die in einer allgemeinen Kundeninteraktion gesendet werden.

| Server-Aufruf | Aktion | Besucher-ID-Cookie | Besucher-ID-Variable | Effektive Besucher-ID | Anzahl besuchter Seiten | Besuchnummer |
|--- |--- |--- |--- |--- |--- |--- |
| 1 | Ein Besucher klickt auf einen Link in einer Marketing-E-Mail und gelangt so von seinem privaten Computer aus auf Ihre Website. Dieser Besucher hat Ihre Website zuvor bereits 7 Mal besucht. | 1 | - | 1 | 1 | 8 |
| 2-8 | Er ruft 7 weitere Seiten auf Ihrer Website auf. | 1 | - | 1 | 2-8 | 8 |
| 9 | Authentifiziert sich auf privatem Computer. | 1 | CID1 | CID1 | 9 <br>(This is CID1's first hit ever, so it takes over and continues on the visitor profile from Visitor ID 1.) | 8 |
| 10 | Besucht eine weitere Seite. | 1 | CID1 | CID1 | 10 | 8 |
| 11 | Öffnet Ihre Website auf seinem Laptop im Büro. Dieser Besucher hat Ihre Website zuvor nicht mithilfe dieses Geräts besucht. | 2 | - | 2 | 1 | 1 |
| 12 | Authentifiziert sich auf Laptop. | 2 | CID1 | CID1 | 1 | 9 |
| 13 | Zeigt eine weitere Seite an. | 2 | CID1 | CID1 | 2 | 9 |

## Besuchszählung

Analytics zählt einen Besuch jedes Mal, wenn ein Treffer mit einer Besuchsseitenzahl gleich 1 angezeigt wird.

In der obigen Tabelle wurde ein neuer Besuch viermal gezählt: bei Treffern 1, 9, 11 und 12.

## Besucherzählung

In Analytics wird jede einzelne Besucher-ID als ein Unique Visitor gezählt.

In der obigen Tabelle wurde ein neuer Besucher dreimal gezählt: bei Treffern 1, 9 und 10.

Wenn Sie die geräteübergreifende Besucheridentifizierung verwenden, kann sich die Anzahl der Unique Visitors, die Sie sehen, erhöhen. Der Besucher kann bei demselben Besuch zweimal gezählt werden: einmal für den ersten Besuch und erneut, nachdem der Benutzer authentifiziert wurde.

![](assets/visitors.png)

Nach der anfänglichen Zuordnung kehren die Besucherzählungen zur Normalität zurück, da der Besucher über sein Browser-Cookie zugeordnet wird. Wenn der Besucher später wieder auf Ihre Site zurückkehrt und sich authentifiziert, wird der Besucherzähler nicht hochgezählt, da sich die effektive Besucher-ID nach der Authentifizierung nicht mehr geändert hat.

![](assets/visitors_2.png)

Stellen Sie sicher, dass Sie bei der Identifizierung individueller Besucher so konsistent wie möglich sind. Verwenden Sie beispielsweise immer die `visitorID` Variable, wenn der Benutzer authentifiziert ist.
