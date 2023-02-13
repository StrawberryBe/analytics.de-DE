---
description: Eine umfassende Liste und Beschreibung der Konfigurationsvariablen, HTTP-Header und Datensignale in Aufrufen der serverseitigen Weiterleitung.
title: Daten- und Codereferenz für die Server-seitige Weiterleitung
feature: Server-Side Forwarding
exl-id: 6ab7bbb6-0709-427b-b9fa-a179dbe55fc9
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: ht
source-wordcount: '518'
ht-degree: 100%

---

# Daten- und Codereferenz für die Server-seitige Weiterleitung

Eine umfassende Liste und Beschreibung der Konfigurationsvariablen, HTTP-Header und Datensignale in Aufrufen der serverseitigen Weiterleitung.

## Konfigurationsvariablen {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

Parameter mit dem Präfix `d_*` kennzeichnen spezielle Schlüsselwert-Paare auf Systemebene, die von unseren [Datenerfassungsservern](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/system-components/components-data-collection.html?lang=de) (DCS) verwendet werden. Siehe auch [Unterstützte Attribute für DCS-API-Aufrufe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html?lang=de).

| Parameter | Beschreibung |
|--- |--- |
| `d_rs` | (Wird bei veralteter/Tracking-Server-basierter Server-seitiger Weiterleitung eingestellt) <br>Auf die Report Suites eingestellt, die mit dem Hit an Analytics weitergeleitet werden. |
| `d_dst_filter` | (Wird bei Report Suite-basierter Server-seitiger Weiterleitung eingestellt) <br>Auf die Report Suite-IDs eingestellt, die mit dem Hit an Analytics weitergeleitet werden. |
| `d_dst` | Festlegung von `d_dst=1` <br>, wenn bei der Anfrage an Analytics erwartet wird, dass Inhalte, die das Ziel betreffen, an den Client zurückgesendet werden. |
| `d_mid` | Die an Analytics übergebene Experience Cloud-ID. |

## HTTP-Header {#section_0549705E76004F9585224AEF872066C0}

Diese Header sind Felder und enthalten Informationen wie Aufrufe für Daten und Antworten in einem HTTP-Aufruf.

| HTTP-Header | Beschreibung | h_key, der von Audience Manager akzeptiert wird |
| --- | --- | --- |
| Host | Diese Einstellung wird auf den jeweiligen Hostnamen der Datenerfassung des Clients festgelegt, der in der Hostkonfigurationsdatei von Analytics angegeben ist. Die Anzeige erscheint als `host name .demdex.net`. Siehe [Aufrufe an die demdex-Domain](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=de). | `h_host` |
| User-Agent | Festgelegt auf den an Analytics übergebenen Benutzer-Agent-Header. | `h_user-agent` |
| Accept-Language | Festgelegt auf den an Analytics übergebenen `Accept-Language`-Header. | `h_accept-language` |
| Referrer | Festgelegt auf die Seiten-URL, die an Analytics übergeben oder aus dem `Referer`-Header erfasst wurde, der an Analytics übergeben worden ist. | `h_referer` |
| Referrer | Festgelegt auf die Seiten-URL, die an Analytics übergeben oder aus dem `Referrer`-Header erfasst wurde, der an Analytics übergeben worden ist. | `h_referrer` |
| Datum | Festgelegt auf den an Analytics übergebenen `Date`-Header. | `h_date` |

Zusätzlich wird ein `h_ip`-Signal von der IP des Hosts generiert, der die Anfrage an DCS sendet.

## Kundendefinierte Signale {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

Parameter mit dem Präfix `c_` kennzeichnen vom Kunden definierte Variablen. Siehe auch [Unterstützte Attribute für DCS-API-Aufrufe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html?lang=de).

| Signal | Beschreibung |
| --- |--- |
| `c_browserWidth` und `c_browserHeight` | Breite und Höhe des Browser-Fensters. |
| `c_campaign` | Festgelegt durch `s.campaign`. |
| `c_channel` | Festgelegt durch `s.channel`. |
| `c_clientDateTime` | Zeitstempel formatiert als `dd/mm/yyy hh:mm:ss  W TZ`. `TZ` ist in Minuten angegeben und stimmt mit der Rückgabe der `Date.getTimezoneOffset`-Methode überein. |
| `c_colorDepth` | Angabe als 16- oder 32-Bit-Farbe. |
| `c_connectionType` | Gibt den Verbindungstyp an. Zu den Optionen zählen:<ul><li>modem</li><li>lan</li></ul> |
| `c_contextData.*` | Beispiele:<ul><li>AppMeasurement: `s.contextData`</li><li>[Kategorie] = &quot;news&quot;;</li><li>Signal: `c_contextData.category=news`</li></ul> |
| `c_cookiesEnabled` | Gibt an, ob Cookies aktiviert werden können. Zu den Optionen zählen:  ja, nein, unbekannt |
| `c_currencyCode` | Typ der für die Transaktion verwendeten Währung. |
| `c_evar#` | Benutzerdefinierte eVars |
| `c_events` | Festgelegt durch `s.events`. |
| `c_hier#` | Benutzerdefinierte Hierarchievariablen. |
| `c_javaEnabled` | Gibt an, ob Java aktiviert werden kann. Zu den Optionen zählen:  ja, nein, unbekannt |
| `c_javaScriptVersion` | Version von JavaScript, die von einem Browser unterstützt wird. |
| `c_latitude` | Numerischer Breitengrad |
| `c_linkClick` | Zu den Optionen gehören: benutzerdefiniert, herunterladen, beenden |
| `c_linkCustomName` | Der benutzerdefinierte Name (sofern vorhanden), der für den Link bereitgestellt wurde. |
| `c_linkDownloadURL` | Die URL der Download-Links. |
| `c_linkExitURL` | Die Exitlink-URL. |
| `c_list#` | Benutzerdefinierte Listenvariablen. |
| `c_longitude` | Numerischer Längengrad. |
| `c_mediaPlayerType` | Für Medienstream-Verfolgungsanfragen. Zu den Optionen zählen:      andere, primetime |
| `c_pageName` | Der Seitenname (sofern festgelegt). |
| `c_pageURL` | Die Adresse der Seite in der Adressleiste des Browsers. |
| `c_products` | Die Produktzeichenfolge (festgelegt durch `s.products`). |
| `c_prop` | Benutzerdefinierte Eigenschaften. |
| `c_purchaseID` | Eine eindeutige ID für den Kauf. |
| `c_referrer` | Die Seite vor der aktuellen Seite. |
| `c_screenResolution` | Bildschirmbreite und -höhe (in Pixeln). |
| `c_server` | Name des Webservers (festgelegt durch `s.server`). |
| `c_state` | Geografische Region (festgelegt durch `s.state`) |
| `c_timezone` | Zeitversatz (in Stunden). |
| `c_transactionID` | Eine eindeutige ID für eine Transaktion. |
| `c_zip` | Postleitzahl (festgelegt durch `s.zip`). |
