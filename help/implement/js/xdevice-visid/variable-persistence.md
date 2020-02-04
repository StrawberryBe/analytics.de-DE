---
description: Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Zuordnung im Verlaufsdatensatz nicht geändert.
keywords: Analytics Implementation
title: Attribution und Persistenz
topic: Developer and implementation
uuid: 5dd706be-83f6-498a-a856-e3c5af995348
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Attribution und Persistenz

> [!IMPORTANT] Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Siehe [Geräteübergreifende Analyse](/help/components/cda/cda-home.md) im Komponenten-Benutzerhandbuch.

Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Zuordnung im Verlaufsdatensatz nicht geändert.

* When the variable `s.visitorID` is set and sent on a hit, Adobe checks for any other visitor profiles that have a matching visitor ID.
* Wenn ein Profil vorhanden ist, wird ab diesem Punkt das bereits im System vorhandene Besucherprofil genutzt, und das vorherige Besucherprofil wird nicht mehr eingesetzt.
* Wenn keine übereinstimmende Besucher-ID gefunden werden kann, wird ein neues Profil erstellt.

Wenn ein nicht authentifizierter Kunde Ihre Site zum ersten Mal besucht, wird diesem Kunden von Adobe Analytics ein Besucherprofil zugewiesen. Bei der Erstellung des neuen Profils endet ein Besuch und ein neuer Besuch beginnt.

## Beispiel 1

Das folgende Beispiel zeigt, wie Daten an Adobe Analytics gesendet werden, wenn sich ein Kunde zum ersten Mal auf dem ersten Gerät authentifiziert:

* `eVar16` hat einen Ablauf von 1 Tag und `evar17` läuft beim Besuch ab.
* Die Spalte `post_visitor_id` stellt das von Adobe Analytics verwaltete Profil dar. Beitragsspalten werden in der Regel in Datenfeeds angezeigt. Siehe [Datenfeeds](/help/export/analytics-data-feed/data-feed-overview.md) im Benutzerhandbuch &quot;Exportieren&quot;.
* Die Spalten `post_evar16` und `post_evar17` zeigen die Persistenz von eVars an.
* `cust_visid` steht für einen in `s.visitorID` festgelegten Wert.
* Jede Zeile ist ein „Treffer“, also eine einzelne Anforderung, die an den Adobe Analytics-Datenerfassungsserver gesendet wird.

![Geräteübergreifendes Beispiel 1](assets/xdevice_first.jpg)

On the first data connection containing a previously unrecognized `s.visitorID` value (`u999` above), a new profile is created. Persistente Werte aus dem vorherigen Profil werden an das neue Profil übertragen.

* eVars, die beim Besuch ablaufen sollen, werden nicht in das authentifizierte Profil kopiert. Beachten Sie, dass der Wert `car` oben nicht beibehalten wird.
* eVars, die nach anderen Kennzahlen ablaufen sollen, werden in das authentifizierte Profil kopiert. Beachten Sie, dass der Wert `apple` beibehalten wird.
* Für die beibehaltenen eVars wird keine Instanzmetrik aufgezeichnet. Bei der Verwendung von geräteübergreifender Besucheridentifizierung können also Berichte erscheinen, bei denen die Metrik für Unique Visits für einen eVar-Wert größer als die Instanzmetrik ist.

> [!NOTE] Wenn ein Benutzer neu auf Ihrer Site ist (noch nie auf diesem Gerät besucht hat) und sich innerhalb von etwa 3 Minuten nach der Ankunft authentifiziert, bleiben keine Werte für das authentifizierte Profil erhalten.

## Beispiel 2

Das folgende Beispiel zeigt, wie Daten an Adobe Analytics gesendet werden, wenn ein Kunde sich auf einem neuen Gerät authentifiziert, nachdem er sich zuvor auf einem anderen Gerät authentifiziert hat.

![Geräteübergreifendes Beispiel 2](assets/xdevice-subsequent.jpg)

Wenn sich der Kunde authentifiziert, werden sie dem vorherigen &quot;authentifizierten&quot;Profil zugeordnet - `2947539300`. Das zu Beginn dieses Besuchs verwendete Profil (`5477766334477`) wird nicht mehr verwendet, und es werden keine Daten aus der Datei beibehalten.

* Geo-Segmentdaten werden auf der Grundlage des ersten Treffers des Besuchs vermerkt und bei einem einzelnen Besuch nicht geändert, wobei es keine Rolle spielt, welches Gerät verwendet wird. Daher werden Geo-Segmentdaten bei einer nachfolgenden Datenverbindung mit einem neuen Gerät im Allgemeinen nicht aufgenommen.
* Technologiespalten, wie Browser, Betriebssystem und Farbtiefe, werden beim ersten Treffer eines Besuchs aufgezeichnet. Wie Geo-Segmentierungswerte werden auch diese nicht in das geheftete Profil kopiert.
* Marketingkanäle überschreiben andere Kanäle bei einer nachfolgenden Datenverbindung, die eine erste Authentifizierung für dieses Gerät enthält.
