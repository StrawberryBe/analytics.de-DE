---
description: Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Zuordnung im Verlaufsdatensatz nicht geändert.
keywords: Analytics-Implementierung
seo-description: Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Zuordnung im Verlaufsdatensatz nicht geändert.
seo-title: Zuordnung und Persistenz
solution: Analytics
title: Zuordnung und Persistenz
topic: Entwickler und Implementierung
uuid: 5 dd 706 be -83 f 6-498 a-a 856-e 3 c 5 af 995348
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Zuordnung und Persistenz

>[!IMPORTANT]
>
>Diese Methode zur Identifizierung von Besuchern auf Gerätegeräten wird nicht mehr empfohlen. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

Wenn Besucherprofile zusammengeführt werden, nachdem sie zur gleichen Besucher-ID-Variablen zugehörig erkannt wurden, wird die Zuordnung im Verlaufsdatensatz nicht geändert.

* Wenn die Variable `s.visitorID` festgelegt ist und bei einem Treffer gesendet wird, sucht das System nach allen anderen Besucherprofilen mit einer übereinstimmenden Besucher-ID.
* Wenn ein Profil vorhanden ist, wird ab diesem Punkt das bereits im System vorhandene Besucherprofil genutzt, und das vorherige Besucherprofil wird nicht mehr eingesetzt.
* Wenn keine übereinstimmende Besucher-ID gefunden werden kann, wird ein neues Profil erstellt.

Wenn ein nicht authentifizierter Kunde Ihre Site zum ersten Mal besucht, wird diesem Kunden von Adobe Analytics ein Besucherprofil zugewiesen. Wie in [Unique Visitor und Besuchsanzahl](../../../implement/js-implementation/xdevice-visid/xdevice-connecting.md#section_70330AB6724C4E419A4BD0BDD54641AC) dargestellt, wird bei der Authentifizierung ein neues Profil erstellt. Bei der Erstellung des neuen Profils endet ein Besuch und ein neuer Besuch beginnt.

**Bei der ersten Datenverbindung**

Im folgenden Beispiel wird gezeigt, wie Daten an Adobe Analytics gesendet werden, wenn ein Kunde sich zum ersten Mal mit dem ersten Gerät authentifiziert:

* `eVar16` hat einen Ablauf von 1 Tag und `evar17` läuft beim Besuch ab.

* The `post_visitor_id` column represents the profile maintained by Adobe Analytics.
* The `post_evar16` and `post_evar17` columns show shows the persistence of eVars.

* `cust_visid` stellt einen in `s.visitorID`festgelegten Wert dar.

* Jede Zeile ist ein „Treffer“, also eine einzelne Anforderung, die an den Adobe Analytics-Datenerfassungsserver gesendet wird.

![](assets/xdevice_first.jpg)

Bei der ersten Datenverbindung mit einem zuvor unbekannten `s.visitorID`-Wert (`u999` oben) wird das neue Profil erstellt. Persistente Werte aus dem vorherigen Profil werden an das neue Profil übertragen.

* eVars, die beim Besuch ablaufen sollen, werden nicht in das authentifizierte Profil kopiert. Beachten Sie, dass der Wert `car` oben nicht beibehalten wird.
* eVars, die nach anderen Kennzahlen ablaufen sollen, werden in das authentifizierte Profil kopiert. Beachten Sie, dass der Wert `apple` beibehalten wird.
* Für die beibehaltenen eVars wird keine Instanzmetrik aufgezeichnet. Bei der Verwendung von geräteübergreifender Besucheridentifizierung können also Berichte erscheinen, bei denen die Metrik für Unique Visits für einen eVar-Wert größer als die Instanzmetrik ist.

**Bei nachfolgenden Datenverbindungen**

Im folgenden Beispiel wird gezeigt, wie Daten an Adobe Analytics gesendet werden, wenn ein Kunde sich auf einem neuen Gerät authentifiziert, nachdem er sich zuvor auf einem anderen Gerät authentifiziert hat:

![](assets/xdevice-subsequent.jpg)

Bei der Authentifizierung des Kunden wird dessen ID mit dem zuvor „authentifizierten“ Profil verglichen – `2947539300`. Das zu Beginn dieses Besuchs verwendete Profil (`5477766334477`) wird nicht mehr verwendet, und es werden keine Daten aus der Datei beibehalten.

* Geo-Segmentdaten werden auf der Grundlage des ersten Treffers des Besuchs vermerkt und bei einem einzelnen Besuch nicht geändert, wobei es keine Rolle spielt, welches Gerät verwendet wird. Daher werden Geo-Segmentdaten bei einer nachfolgenden Datenverbindung mit einem neuen Gerät im Allgemeinen nicht aufgenommen.
* Technologiespalten, wie Browser, Betriebssystem und Farbtiefe, werden beim ersten Treffer eines Besuchs aufgezeichnet. Wie Geo-Segmentdatenwerte werden auch diese Werte nicht in das authentifizierte Profil kopiert.
* Ein Marketingkanal, wie „Direkt“ oder „Intern“, der normalerweise so eingerichtet wird, dass keine Überschreibung eines anderen Kanals stattfindet, überscheibt andere Kanäle bei einer nachfolgenden Datenverbindung mit einer ersten Authentifizierung für dieses Gerät, wie der in [Unique Visitor und Besuchsanzahl](../../../implement/js-implementation/xdevice-visid/xdevice-connecting.md#section_70330AB6724C4E419A4BD0BDD54641AC) dargestellten ersten Authentifizierung.

**Sonderfälle**

In einigen anderen Fällen werden Daten nicht aus dem nicht authentifizierten Profil in das authentifizierte Profil übernommen.

* Wenn ein Benutzer neu auf Ihrer Site ist (Sie noch nie über dieses Gerät besucht hat) UND dieser Benutzer sich innerhalb von ca. drei Minuten nach seiner Ankunft authentifiziert, werden keine Werte in das authentifizierte Profil übernommen.

