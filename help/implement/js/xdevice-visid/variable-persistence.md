---
description: Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Attribution im Verlaufsdatensatz nicht geändert.
keywords: Analytics Implementation
title: Attribution und Persistenz
topic: Developer and implementation
uuid: 5dd706be-83f6-498a-a856-e3c5af995348
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Attribution und Persistenz

>[!IMPORTANT] Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Siehe [Geräteübergreifende Analyse](/help/components/cda/cda-home.md) im Komponentenleitfaden.

Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Attribution im Verlaufsdatensatz nicht geändert.

* Wenn die Variable `s.visitorID` festgelegt ist und bei einem Treffer gesendet wird, sucht Adobe nach allen anderen Besucherprofilen mit einer übereinstimmenden Besucher-ID.
* Wenn ein Profil vorhanden ist, wird ab diesem Zeitpunkt das bereits im System vorhandene Besucher-Profil verwendet und das Profil des vorherigen Besuchers wird nicht mehr verwendet.
* Wenn keine übereinstimmende Besucher-ID gefunden wird, wird ein neues Profil erstellt.

Wenn ein nicht authentifizierter Kunde zum ersten Mal auf Ihre Site gelangt, wird dem Kunden von Adobe Analytics ein Besucher-Profil zugewiesen. Bei der Erstellung des neuen Profils endet ein Besuch und ein neuer Besuch beginnt.

## Beispiel 1

Im folgenden Beispiel wird gezeigt, wie Daten an Adobe Analytics gesendet werden, wenn ein Kunde sich zum ersten Mal mit dem ersten Gerät authentifiziert:

* `eVar16` hat eine Gültigkeit von 1 Tag und `evar17` läuft beim Besuch ab.
* Die Spalte `post_visitor_id` stellt das von Adobe Analytics verwaltete Profil dar. Post-Spalten werden in der Regel in Daten-Feeds angezeigt. Siehe [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) im Exportbenutzerhandbuch.
* Die Spalten `post_evar16` und `post_evar17` zeigen die Persistenz von eVars an.
* `cust_visid` steht für einen in `s.visitorID` festgelegten Wert.
* Jede Zeile ist ein „Treffer“, also eine einzelne Anforderung, die an den Adobe Analytics-Datenerfassungsserver gesendet wird.

![Geräteübergreifendes Beispiel 1](assets/xdevice_first.jpg)

Bei der ersten Datenverbindung mit einem zuvor unbekannten `s.visitorID`-Wert (`u999` oben) wird ein neues Profil erstellt. Beständige Werte aus dem vorherigen Profil werden in das neue Profil übertragen.

* eVars, die beim Besuch ablaufen sollen, werden nicht in das authentifizierte Profil kopiert. Beachten Sie, dass der Wert `car` oben nicht beibehalten wird.
* eVars, die nach anderen Kennzahlen ablaufen sollen, werden in das authentifizierte Profil kopiert. Beachten Sie, dass der Wert `apple` beibehalten wird.
* Für die beibehaltenen eVars wird keine Instanzmetrik aufgezeichnet. Das bedeutet, dass bei der Verwendung der geräteübergreifenden Besucher-Identifizierung Berichte angezeigt werden können, in denen die Metrik &quot;Individuelle Besuche&quot;für eine eVar größer als die Instanzmetrik ist.

>[!NOTE] Wenn ein Benutzer neu auf Ihrer Website ist (Sie noch nie über dieses Gerät besucht hat) und sich innerhalb von ca. drei Minuten nach seiner Ankunft authentifiziert, werden keine Werte in das authentifizierte Profil übernommen.

## Beispiel 2

Im folgenden Beispiel wird gezeigt, wie Daten an Adobe Analytics gesendet werden, wenn ein Kunde sich auf einem neuen Gerät authentifiziert, nachdem er sich zuvor auf einem anderen Gerät authentifiziert hat.

![Geräteübergreifendes Beispiel 2](assets/xdevice-subsequent.jpg)

Wenn sich der Kunde authentifiziert, wird er dem vorherigen „authentifizierten“ Profil zugeordnet – `2947539300`. Das zu Beginn dieses Besuchs verwendete Profil (`5477766334477`) wird nicht mehr verwendet, und es werden keine Daten aus der Datei beibehalten.

* Geo-Segmentdaten werden basierend auf dem ersten Treffer des Besuchs aufgezeichnet und bei einem einzelnen Besuch nicht geändert, unabhängig vom verwendeten Gerät. Das bedeutet, dass bei einer nachfolgenden Datenverbindung auf einem neuen Gerät Geo-Segmentdaten im Allgemeinen nicht einbezogen werden.
* Technologiespalten wie Browser, Betriebssystem und Farbtiefe werden beim ersten Treffer eines Besuchs aufgezeichnet. Wie Geo-Segmentdatenwerte werden auch diese Werte nicht in das authentifizierte Profil kopiert.
* Marketing-Kanäle überschreiben andere Kanäle bei einer nachfolgenden Datenverbindung, die eine erste Authentifizierung für dieses Gerät enthält.
