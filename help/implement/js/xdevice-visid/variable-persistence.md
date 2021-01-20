---
description: Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Attribution im Verlaufsdatensatz nicht geändert.
keywords: Analytics Implementation
title: Attribution und Persistenz
topic: Developer and implementation
uuid: 5dd706be-83f6-498a-a856-e3c5af995348
translation-type: tm+mt
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 98%

---


# Attribution und Persistenz

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Siehe [Geräteübergreifende Analyse](/help/components/cda/overview.md) im Komponenten-Benutzerhandbuch.

Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Attribution im Verlaufsdatensatz nicht geändert.

* Wenn die Variable `s.visitorID` festgelegt ist und bei einem Treffer gesendet wird, sucht Adobe nach allen anderen Besucherprofilen mit einer übereinstimmenden Besucher-ID.
* Wenn ein Profil vorhanden ist, wird ab diesem Punkt das bereits im System vorhandene Besucherprofil genutzt, und das vorherige Besucherprofil wird nicht mehr eingesetzt.
* Wenn keine übereinstimmende Besucher-ID gefunden werden kann, wird ein neues Profil erstellt.

Wenn ein nicht authentifizierter Kunde Ihre Site zum ersten Mal besucht, wird diesem Kunden von Adobe Analytics ein Besucherprofil zugewiesen. Bei der Erstellung des neuen Profils endet ein Besuch und ein neuer Besuch beginnt.

## Beispiel 1

Im folgenden Beispiel wird gezeigt, wie Daten an Adobe Analytics gesendet werden, wenn ein Kunde sich zum ersten Mal mit dem ersten Gerät authentifiziert:

* `eVar16` hat eine Gültigkeit von 1 Tag und `evar17` läuft beim Besuch ab.
* Die Spalte `post_visitor_id` stellt das von Adobe Analytics verwaltete Profil dar. Post-Spalten werden in der Regel in Daten-Feeds angezeigt. Siehe [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) im Exportbenutzerhandbuch.
* Die Spalten `post_evar16` und `post_evar17` zeigen die Persistenz von eVars an.
* `cust_visid` steht für einen in `s.visitorID` festgelegten Wert.
* Jede Zeile ist ein „Treffer“, also eine einzelne Anforderung, die an den Adobe Analytics-Datenerfassungsserver gesendet wird.

![Geräteübergreifendes Beispiel 1](assets/xdevice_first.jpg)

Bei der ersten Datenverbindung mit einem zuvor unbekannten `s.visitorID`-Wert (`u999` oben) wird ein neues Profil erstellt. Persistente Werte aus dem vorherigen Profil werden an das neue Profil übertragen.

* eVars, die beim Besuch ablaufen sollen, werden nicht in das authentifizierte Profil kopiert. Beachten Sie, dass der Wert `car` oben nicht beibehalten wird.
* eVars, die nach anderen Kennzahlen ablaufen sollen, werden in das authentifizierte Profil kopiert. Beachten Sie, dass der Wert `apple` beibehalten wird.
* Für die beibehaltenen eVars wird keine Instanzmetrik aufgezeichnet. Bei der Verwendung von geräteübergreifender Besucheridentifizierung können also Berichte erscheinen, bei denen die Metrik für Unique Visits für einen eVar-Wert größer als die Instanzmetrik ist.

>[!NOTE]
>
>Wenn ein Benutzer neu auf Ihrer Website ist (Sie noch nie über dieses Gerät besucht hat) und sich innerhalb von ca. drei Minuten nach seiner Ankunft authentifiziert, werden keine Werte in das authentifizierte Profil übernommen.

## Beispiel 2

Im folgenden Beispiel wird gezeigt, wie Daten an Adobe Analytics gesendet werden, wenn ein Kunde sich auf einem neuen Gerät authentifiziert, nachdem er sich zuvor auf einem anderen Gerät authentifiziert hat.

![Geräteübergreifendes Beispiel 2](assets/xdevice-subsequent.jpg)

Wenn sich der Kunde authentifiziert, wird er dem vorherigen „authentifizierten“ Profil zugeordnet – `2947539300`. Das zu Beginn dieses Besuchs verwendete Profil (`5477766334477`) wird nicht mehr verwendet, und es werden keine Daten aus der Datei beibehalten.

* Geo-Segmentdaten werden auf der Grundlage des ersten Treffers des Besuchs vermerkt und bei einem einzelnen Besuch nicht geändert, wobei es keine Rolle spielt, welches Gerät verwendet wird. Daher werden Geo-Segmentdaten bei einer nachfolgenden Datenverbindung mit einem neuen Gerät im Allgemeinen nicht aufgenommen.
* Technologiespalten, wie Browser, Betriebssystem und Farbtiefe, werden beim ersten Treffer eines Besuchs aufgezeichnet. Wie Geo-Segmentdatenwerte werden auch diese Werte nicht in das authentifizierte Profil kopiert.
* Marketing-Kanäle überschreiben andere Kanäle bei einer nachfolgenden Datenverbindung, die eine erste Authentifizierung für dieses Gerät enthält.
