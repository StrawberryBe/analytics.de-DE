---
description: Eine umfassende Liste und Beschreibung der Konfigurationsvariablen, HTTP-Header und Datensignale in Aufrufen der serverseitigen Weiterleitung.
title: Daten- und Codereferenz für die serverseitige Weiterleitung
uuid: 3eb3ea0f-a530-448d-bba5-6408b2490dc8
translation-type: tm+mt
source-git-commit: 327fdfd6a6d6bfe1c7bae9825fc8812b5ac7d095
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 100%

---


# Daten- und Codereferenz für die serverseitige Weiterleitung

Eine umfassende Liste und Beschreibung der Konfigurationsvariablen, HTTP-Header und Datensignale in Aufrufen der serverseitigen Weiterleitung.

## Konfigurationsvariablen {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

Parameter mit dem Präfix `d_*` kennzeichnen spezielle Schlüsselwert-Paare auf Systemebene, die von unseren [Datenerfassungsservern](https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/reference/system-components/components-data-collection.html) (DCS) verwendet werden. Siehe auch [Unterstützte Attribute für DCS-API-Aufrufe](https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html).

| Parameter | Beschreibung |
|--- |--- |
| d_rs | (Wird mit veralteter/Tracking-Server-basierter serverseitiger Weiterleitung eingestellt) <br>Auf die Report Suites eingestellt, die mit dem Hit an Analytics übergeben werden. |
| d_dst_filter | (Wird mit Report Suite-basierter serverseitiger Weiterleitung eingestellt) <br>Auf die Report Suite-IDs eingestellt, die mit dem Hit an Analytics weitergeleitet werden. |
| d_dst | Festlegung von d_dst=1<br>, wenn die Anfrage an Analytics erwartet, dass Inhalte über das Ziel an den Client zurückgesendet werden. |
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
| Referrer | Festgelegt auf die Seiten-URL, die an Analytics übergeben oder aus dem Referrer-Header erfasst wurde, der an Analytics übergeben worden ist. |

## Kundendefinierte Signale {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

Parameter mit dem Präfix `c_` kennzeichnen vom Kunden definierte Variablen. Siehe auch [Unterstützte Attribute für DCS-API-Aufrufe](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html).

| Signal | Beschreibung |
|--- |--- |
| c_browserWidth und c_browserHeight | Breite und Höhe des Browser-Fensters. |
| c_campaign | Festgelegt durch s.campaign. |
| c_channel | Festgelegt durch s.channel. |
| c_clientDateTime | Zeitstempel formatiert als TT/MM/JJJ hh:mm:ss W TZ .    TZ ist in Minuten angegeben und stimmt mit der Rückgabe der Methode Date.getTimezoneOffset überein. |
| c_colorDepth | Angabe als 16- oder 32-Bit-Farbe. |
| c_connectionType | Gibt den Verbindungstyp an. Zu den Optionen zählen:<ul><li>modem</li><li>lan</li></ul> |
| c_contextData.* | Beispiele:<ul><li>AppMeasurement: s.contextData</li><li>[&quot;category&quot;] = &quot;news&quot;;</li><li>Signal: c_contextData.category=news</li></ul> |
| c_cookiesEnabled | Gibt an, ob Cookies aktiviert werden können. Zu den Optionen zählen: ja, nein, unbekannt |
| c_currencyCode | Typ der für die Transaktion verwendeten Währung. |
| c_evar# | Benutzerdefinierte eVars |
| c_events | Festgelegt durch s.events. |
| c_hier# | Benutzerdefinierte Hierarchievariablen. |
| c_javaEnabled | Gibt an, ob Java aktiviert werden kann. Zu den Optionen zählen: ja, nein, unbekannt |
| c_javaScriptVersion | Version von Javascript, die von einem Browser unterstützt wird. |
| c_latitude | Numerische Breite |
| c_linkClick | Zu den Optionen gehören: benutzerdefiniert, herunterladen, beenden |
| c_linkCustomName | Der benutzerdefinierte Name (sofern vorhanden), der für den Link bereitgestellt wurde. |
| c_linkDownloadURL | Die URL der Download-Links. |
| c_linkExitURL | Die Exitlink-URL. |
| c_list# | Benutzerdefinierte Listenvariablen. |
| c_longitude | Numerische Länge. |
| c_mediaPlayerType | Für Medienstream-Verfolgungsanfragen. Zu den Optionen zählen:    andere, primetime |
| c_pageName | Der Seitenname (sofern festgelegt). |
| c_pageURL | Die Adresse der Seite in der Adressleiste des Browsers. |
| c_products | Die Produktzeichenfolge (festgelegt durch s.products). |
| c_prop | Benutzerdefinierte Eigenschaften. |
| c_purchaseID | Eine eindeutige ID für den Kauf. |
| c_referrer | Die Seite vor der aktuellen Seite. |
| c_screenResolution | Bildschirmbreite und -höhe (in Pixeln). |
| c_server | Name des Webservers (festgelegt durch s.server). |
| c_state | Geografische Region (festgelegt durch s.state). |
| c_timezone | Zeitversatz (in Stunden). |
| c_transactionID | Eine eindeutige ID für eine Transaktion. |
| c_zip | Postleitzahl (festgelegt durch s.zip). |
