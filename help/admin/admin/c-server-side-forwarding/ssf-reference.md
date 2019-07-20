---
description: Eine umfassende Liste und Beschreibung der Konfigurationsvariablen, HTTP-Header und Datensignale in Aufrufen der serverseitigen Weiterleitung.
seo-description: Eine umfassende Liste und Beschreibung der Konfigurationsvariablen, HTTP-Header und Datensignale in Aufrufen der serverseitigen Weiterleitung.
seo-title: Serverseitige Weiterleitungsdaten und Code-Referenz
title: Serverseitige Weiterleitungsdaten und Code-Referenz
uuid: 3 eb 3 ea 0 f-a 530-448 d-bba 5-6408 b 2490 dc 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Serverseitige Weiterleitungsdaten und Code-Referenz

Eine umfassende Liste und Beschreibung der Konfigurationsvariablen, HTTP-Header und Datensignale in Aufrufen der serverseitigen Weiterleitung.

## Konfigurationsvariablen {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

Parameters prefixed with `d_*` identify special, system-level key-value pairs used by our [data collection servers](https://marketing.adobe.com/resources/help/en_US/aam/c_compcollect.html) (DCS). Siehe auch [Unterstützte Attribute für DCS-API-Aufrufe](https://marketing.adobe.com/resources/help/en_US/aam/dcs-keys.html).

| Parameter | Beschreibung |
|--- |--- |
| d_rs | (Gets set with legacy/tracking-server-based server-side forwarding) <br>Set to the report suites passed in with the hit to Analytics. |
| d_dst_filter | (Gets set with report-suite-based server-side forwarding)  <br>Set to the report suite IDs passed in with the hit to Analytics. |
| d_dst | Festlegung von d_dst=1<br>, wenn die bei der Analytics-Anfrage Inhalt zu dem Ziel erwartet wird, der an den Client zurückgesendet werden soll. |
| d_mid | Die an Analytics übergebene Experience Cloud ID. |

## HTTP-Header {#section_0549705E76004F9585224AEF872066C0}

Diese Header sind Felder und enthalten Informationen wie Aufrufe für Daten und Antworten in einem HTTP-Aufruf.

<!-- Meike, missing link in table below: "See Understanding Calls to the Demdex Domain" -->

| HTTP-Header | Beschreibung |
|--- |--- |
| Host | Diese Einstellung wird auf den jeweiligen Hostnamen der Datenerfassung des Clients festgelegt, der in der Hostkonfigurationsdatei von Analytics angegeben ist. Die Anzeige erscheint als   `host name .demdex.net` .  Siehe Aufrufe an die Domäne „demdex.net“. |
| User-Agent | Festgelegt auf den an Analytics übergebenen Benutzer-Agent-Header. |
| X-Original-User-Agent | Die Festlegung erfolgt nur dann, wenn von einem dieser Header ein alternativer Benutzer-Agent angegeben wurde: </br>`X-Device-User-Agent\ `  </br>`X-Original-User-Agent\`   </br>`X-OperaMini-Phone-UA\`   </br>`X-Skyfire-Phone\`    </br>`X-Bolt-Phone-UA\` |
| X-Forwarded-For | Festgelegt auf die IP-Adresse des anfragenden Clients. Analytics hat den eingehenden Header `X-Forwarded-For` bereits analysiert und die korrekte zu verwendende IP-Adresse bestimmt. |
| Accept-Language | Festgelegt auf den an Analytics übergebenen `Accept-Language`-Header. |
| Referer | Festgelegt auf die Seiten-URL, die an Analytics übergeben oder aus dem Referer-Header erfasst wurde, der an Analytics übergeben worden ist. |

## Kundendefinierte Signale {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

Parameters prefixed with `c_` identify customer-defined variables. Siehe auch [Unterstützte Attribute für DCS-API-Aufrufe](https://marketing.adobe.com/resources/help/en_US/aam/dcs-keys.html).

| Signal | Beschreibung |
|--- |--- |
| c_browserWidth und c_browserHeight | Breite und Höhe des Browserfensters. |
| c_campaign | Festgelegt durch s.campaign . |
| c_channel | Festgelegt durch s.channel . |
| c_clientDateTime | Zeitstempel als TT/MM/JJJJ-HH: mm: SS W TZ. TZ ist in Minuten angegeben und stimmt mit der Rückgabe der Methode Date.getTimezoneOffset überein. |
| c_colorDepth | Angabe als 16- oder 32-Bit-Farbe. |
| c_connectionType | Gibt den Verbindungstyp an. Zu den Optionen zählen:<ul><li>modem</li><li>lan</li></ul> |
| c_contextData.* | Beispiele:<ul><li>Appmeasurement: s. contextdata</li><li>[" category "] =" news ";</li><li>Signal: c_contextData.category=news</li></ul> |
| c_cookiesEnabled | Gibt an, ob Cookies aktiviert werden können. Zu den Optionen zählen: ja, nein, unbekannt |
| c_currencyCode | Typ der für die Transaktion verwendeten Währung. |
| c_evar# | Benutzerspezifische eVars |
| c_events | Festgelegt durch s.events . |
| c_hier# | Benutzerdefinierte Hierarchievariablen. |
| c_javaEnabled | Gibt an, ob Java aktiviert werden kann. Zu den Optionen zählen: ja, nein, unbekannt |
| c_javaScriptVersion | Version von Javascript, die von einem Browser unterstützt wird. |
| c_latitude | Numerische Breite |
| c_linkClick | Zu den Optionen gehören: benutzerspezifisch, Download-Exit |
| c_linkCustomName | Der benutzerdefinierte Name (sofern vorhanden), der für den Link bereitgestellt wurde. |
| c_linkDownloadURL | Die URL der Download-Links. |
| c_linkExitURL | Die Exitlink-URL. |
| c_list# | Benutzerdefinierte Listenvariablen. |
| c_longitude | Numerische Länge. |
| c_mediaPlayerType | Für Medienstream-Verfolgungsanfragen. Zu den Optionen zählen:  other, primetime |
| c_pageName | Der Seitenname (sofern festgelegt). |
| c_pageURL | Die Adresse der Seite in der Adressleiste des Browsers. |
| c_products | Die Produktzeichenfolge (festgelegt durch s.products ). |
| c_prop | Benutzerdefinierte Eigenschaften. |
| c_purchaseID | Eine eindeutige ID für den Kauf. |
| c_referrer | Die Seite vor der aktuellen Seite. |
| c_screenResolution | Bildschirmbreite und -höhe (in Pixeln). |
| c_server | Name des Webservers (festgelegt durch s.server ). |
| c_state | Geografische Region (festgelegt durch s.state ). |
| c_timezone | Zeitversatz (in Stunden). |
| c_transactionID | Eine eindeutige ID für eine Transaktion. |
| c_zip | Postleitzahl (festgelegt durch s.zip ). |
