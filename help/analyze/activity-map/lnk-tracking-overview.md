---
description: 'Activity Map verfolgt Links mit einem stabileren Algorithmus, der Folgendes ermöglicht '
title: Zuverlässiges Linktracking
topic: Activity map
uuid: a72b1652-2e69-41c7-8cf2-d39e9c705302
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Zuverlässiges Linktracking

Activity Map verfolgt Links mit einem stabileren Algorithmus, der Folgendes ermöglicht:

* Umfasst die Verfolgung von Seitenregionen, um zu vermeiden, dass derselbe Link auf verschiedenen Geräten verwechselt wird, da der Link an verschiedenen Positionen auf der Seite angezeigt wird;
* Stellt die Eindeutigkeit von Links sicher, d. h., dass unterschiedliche Links aufgrund von Problemen mit der LinkID oder über verschiedene Browsermarken hinweg nicht mit einem Link verwechselt werden können.

Weitere Informationen zur Linktracking in Aktivität Map finden Sie [hier](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md).

## Art der Sammlung von PII-Daten mittels Activity Map-Linktracking {#section_AEE57510D17B4C21A7D49D32D21D67B9}

>[!CAUTION] Beim Aktivieren von Activity Map-Tracking erfassen Sie möglicherweise persönlich identifizierbare Informationen (PII). Diese Daten können alleine oder in Verbindung mit anderen Informationen dazu verwendet werden, eine Einzelperson zu identifizieren, zu kontaktieren oder zu lokalisieren oder eine Einzelperson im Kontext zu identifizieren.

Im Folgenden finden Sie einige Fälle, in denen PII-Daten möglicherweise mit dem Activity Map-Tracking gesammelt werden:

* `Mailto`-Links. Ein Mailto-Link ist ein HTML-Linktyp, der den standardmäßigen E-Mail-Client auf dem Computer für das Senden einer E-Mail aktiviert.
* `User ID`-Links, die in der Kopf-/Fußzeile einer Website angezeigt werden, nachdem sich der Benutzer angemeldet hat.
* Bei Finanzinstituten wird möglicherweise die Kontonummer als Link angezeigt. Beim Klicken darauf wird der Linktext erfasst.
* Auch auf Gesundheitswebsites werden möglicherweise PII in Form von Links angezeigt. Beim Klicken auf diese Links werden der Linktext und damit auch die PII-Daten erfasst.
