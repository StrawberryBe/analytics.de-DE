---
title: Einstellung der Unterstützung für Data Sources mit vollständiger Verarbeitung
description: Gründe für das Ende des Lebenszyklus und Vergleiche zwischen der Bulk Data Insertion API und Data Sources mit vollständiger Verarbeitung.
exl-id: 24a44b7a-64fd-4a99-975f-4887f4638812
source-git-commit: 0b31585f5a928d68083764b80f3a08927b407387
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 30%

---

# Einstellung der Unterstützung für Data Sources mit vollständiger Verarbeitung

Seit mehreren Jahren können Sie mit Data Sources mit vollständiger Verarbeitung Daten auf Trefferebene an Adobe Analytics senden. Diese Daten wurden auf dieselbe Weise verarbeitet wie Daten, die über unsere JavaScript-Bibliotheken und das Mobile App SDK erfasst wurden. Im Jahr 2020 veröffentlichte Adobe die [Bulk Data Insertion API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md), der dieselben Funktionen wie Data Sources mit vollständiger Verarbeitung, jedoch mit zusätzlichen Funktionen ausführt. In diesem Thema werden die zusätzlichen Funktionen der Bulk Data Insertion API erläutert und die Unterschiede in den Dateiformaten erläutert.

Ab dem 25. März 2021 verhinderte Adobe die Erstellung neuer Data Sources-Verbindungen mit vollständiger Verarbeitung . Vorhandene Verbindungen wurden unterstützt, bis der Dienst am 31. Januar 2022 vollständig eingestellt wurde. Zusätzlich zu unserer Standarddokumentation bieten wir eine schrittweise Anleitung für die [Schritte, die zum Senden von Daten über die Bulk Data Insertion API erforderlich sind](https://adobe.ly/aabdia).

## Warum haben wir diese Funktion eingestellt?

Die Bulk Data Insertion API (BDIA) bietet zusätzliche Funktionen und deckt dabei alle Anwendungsfälle ab, die von der vollständigen Verarbeitung unterstützt werden. Sie werden besser mit der Bulk Data Insertion API versorgt.

## Wichtige Unterschiede zwischen Data Sources mit vollständiger Verarbeitung und der Bulk Data Insertion API

* Die Masseneinfügung von Daten ermöglicht die Übermittlung mehrerer Dateien, die parallel verarbeitet werden können. Sie können Besuchergruppen verwenden, um die Besucherkontinuität und eVar sicherzustellen.
* Die Masseneinfügung von Daten verfügt über Datenvalidierungs- und Fehlerbearbeitungsfunktionen, sodass einige administrative Aufgaben beim Senden von Trefferdaten entfernt werden.
* Die Masseneinfügung von Daten unterstützt mehrere Optionen für Besucher-IDs. Sie können sowohl die Analytics-ID als auch die Marketing Cloud-ID senden (siehe [Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) Weitere Informationen). Darüber hinaus können Sie Ihre eigene ID als [Saatgut zur Generierung einer ECID](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#customer-id-and-experience-cloud-visitor-id-seeds).
* Die Masseneinfügung von Daten unterstützt Listen- und Kontextdatenvariablen.
* Die Massendateneinfügung unterstützt keine Activity Map-Daten.

## Wichtige Unterschiede in Dateiformat und Inhalt

* Die Masseneinfügung von Daten enthält einige zusätzliche erforderliche Felder. Siehe [Dokumentation](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) für Details.
* Um die Besucherkontinuität und -zuordnung sicherzustellen, müssen bei der Massendateneinfügung Zeilen in Dateien in chronologischer Reihenfolge sortiert werden. Siehe [Besuchergruppen](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#visitor-groups) , um mehr über die dateiübergreifende Reihenfolge der Besucheraktivität zu erfahren.
* Für die Masseneinfügung von Daten müssen Dateien im .csv-Format komprimiert werden.
* BDIA verwendet &quot;timestamp&quot;anstelle von &quot;date&quot;.

Weitere Informationen finden Sie im folgenden Vergleich der in Bulk Data Insertion (BDIA) und Full Processing Data Sources (FPDS) verfügbaren Feldwerte.

## Vergleich der in BDIA und FPDS verfügbaren Feldwerte

| BDIA-Variable | Variable für Spalte „Volle Verarbeitung“ | Beschreibung |
| --- | --- | --- |
| aamlh | Nicht unterstützt | Adobe Audience Manager-Standorthinweis. |
| browserHeight | browserHeight | Browser-Höhe in Pixel (z. B. 768) |
| browserWidth | browserWidth | Browser-Breite in Pixel (z. B. 1024) |
| campaign | Kampagne | Konversion-Kampagnen-Trackingcode |
| channel | channel | Kanal-Zeichenfolge (z. B. Sportabteilung) |
| colorDepth | colorDepth | Bildschirmfarbtiefe in Bit (z. B. 24) |
| connectionType | connectionType | Verbindungstyp des Besuchers (LAN oder Modem) |
| contextData.key | Nicht unterstützt | Schlüsselwertpaare werden in durch Benennung der Kopfzeile &quot;contextData.product&quot;oder &quot;contextData.color&quot;angegeben. |
| cookiesEnabled | cookiesEnabled | `Y` oder `N` für den Fall, dass der Besucher Sitzungs-Cookies von Erstanbietern unterstützt |
| currencyCode | currencyCode | Währungscode für Umsatz (z. B. `USD`) |
| customerID.[customerIDType].authState | Nicht unterstützt | Der authentifizierte Status des Besuchers. Folgende Werte werden unterstützt: 0, 1, 2, UNBEKANNT, AUTHENTICATED, LOGGED_OUT oder &#39;&#39; (Groß-/Kleinschreibung wird nicht berücksichtigt). Zwei aufeinander folgende einfache Anführungszeichen (&#39;&#39;) führen dazu, dass der Wert in der Abfragezeichenfolge weggelassen wird, was bei einem Treffer in 0 umgewandelt wird. Beachten Sie, dass die unterstützten numerischen authState-Werte Folgendes kennzeichnen: 0 = UNKNOWN, 1 = AUTHENTICATED, 2 = LOGGED_OUT. Beim customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, es sollte jedoch zwischen Groß- und Kleinschreibung unterschieden werden. |
| customerID.[customerIDType].id | Nicht unterstützt | Die zu verwendende Kunden-ID. Beim customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, es sollte jedoch zwischen Groß- und Kleinschreibung unterschieden werden. |
| customerID.[customerIDType].isMCSeed | Nicht unterstützt | Gibt an, ob dies der Test für die Marketing Cloud-Besucher-ID ist. Folgende Werte werden unterstützt: 0, 1, TRUE, FALSE, &#39;&#39; (Groß-/Kleinschreibung wird nicht berücksichtigt). Bei Verwendung von 0, FALSE oder zwei aufeinander folgenden einfachen Anführungszeichen (&#39;&#39;) wird der Wert in der Abfragezeichenfolge weggelassen. Beim customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, es sollte jedoch zwischen Groß- und Kleinschreibung unterschieden werden. |
| eVarN | eVarN, d. h. `<eVar2>`...`<eVar>` | Konversion-eVar-Name. Sie können über bis zu 75 eVars verfügen (  eVar1 - eVar75 ) Sie können den eVar (eVar12) oder einen Anzeigenamen (Anzeigenkampagne 3) angeben. |
| events | events | [Ereigniszeichenfolge](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html?lang=en#vars), formatiert mit derselben Syntax wie die s.events -Variable. Beispiel: scAdd,event1,event7 |
| hierN | hierN, d.h. `<hier2>`...`</hier2>` | Hierarchiename. Sie können über bis zu 5 Hierarchien verfügen (  hier1 - hier5 ). Sie können den Standardhierarchienamen angeben `hier2` oder einen Anzeigenamen (Yankees). |
| homePage | homePage | Y oder N, ist die aktuelle Seite die Homepage des Besuchers. |
| ipaddress | Nicht unterstützt | Die IP-Adresse des Besuchers. |
| javaEnabled | javaEnabled | Y oder N, hat der Besucher Java aktiviert. |
| javaScriptVersion | javaScriptVersion | JavaScript-Version (z. B. 1.3). |
| language | Nicht unterstützt | Die unterstützte Sprache des Browsers. Beispiel: `en-us`. |
| linkName | linkName | Name des Links. |
| linkType | linkType | Art des Links. Folgende Werte werden unterstützt: `d: Download link`, `e: Exit link`, `o: Custom link`. |
| linkURL | linkURL | HREF des Links. |
| list Zum Beispiel list2. | Nicht unterstützt | Eine Liste getrennter Werte, die in eine Variable überführt und bei der Berichterstellung als einzelne Zeilenelemente behandelt werden |
| marketingCloudVisitorID | Nicht unterstützt | Marketing Cloud ID. Siehe [Besucheridentifizierung](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en#id-service-api) und dem Marketing Cloud-Besucher-ID-Dienst |
| Nicht unterstützt | charSet | Der unterstützte Zeichensatz für Ihre Website. Beispiel: UTF-8, ISO-8859-1 usw. |
| Nicht unterstützt | clickAction | Objekt-ID für Besucher-ClickMap (oid). |
| Nicht unterstützt | clickActionType | Objekt-ID-Typ für Besucher-ClickMap (oidt). |
| Nicht unterstützt | clickContext | Seiten-ID für Besucher-ClickMap (pid). |
| Nicht unterstützt | clickContextType | Seiten-ID-Typ für Besucher-ClickMap (pidt). |
| Nicht unterstützt | clickSourceID | Quellenindex für Besucher-ClickMap (oi). |
| Nicht unterstützt | clickTag | Objekt-Tag-Name für Besucher-ClickMap (ot). |
| Nicht unterstützt | scXmlVer | Marketingberichte-XML-Anforderungsversion (z. B. 1.0). |
| Nicht unterstützt | timezone | Zeitzonenversatz des Besuchers zu GMT in Stunden (z. B. -8). |
| pageName | pageName | Name der Seite |
| pageType | pageType | Seitentyp (z. B. &quot;Fehlerseite&quot;). |
| pageURL | pageURL | Seiten-URL (z. B. https://www.example.com/index.html). |
| plugins | plugins | Durch Semikolon getrennte Liste von Browser-Plug-in-Namen. |
| products | products | Liste aller Produkte auf der Seite. Trennen Sie Produkte durch Kommas. Beispiel: Sport;Ball;1;5.95,Spielzeug; Oben;1:1.99. |
| prop1 – prop75 | propN, d. h. `<prop2>`...`</prop2>` | Zeichenfolge &quot;Property#&quot;(z. B. &quot;Sports Section&quot;). |
| propN | propN | Eigenschaftswerte für Ihre Eigenschaften. |
| purchaseID | purchaseID | Kauf-ID. |
| referrer | referrer | URL für verweisende Seiten. |
| reportSuiteID | s_account | Gibt die Report Suites an, an die Daten übermittelt werden sollen. Sie sollten mehrere Report Suite-IDs durch Kommas trennen. |
| resolution | resolution | Bildschirmauflösung (z. B. 1024x768). |
| server | server | Serverzeichenfolge. |
| state | state | Konversion-Status-Zeichenfolge. |
| timestamp | Datum | Verwenden Sie das ISO 8601-Datumsformat YYY-MM-DDThh.:mm:ss±UTC_offset (z. B. 2021-09-01T12):00:00-07:00 ) oder Unix-Zeitformat (die Anzahl der Sekunden, die seit dem 1. Januar 1970 vergangen sind). |
| trackingServer | Nicht unterstützt | Kann nur über die Spaltenüberschrift bereitgestellt werden. |
| transactionID | Nicht unterstützt | Allgemeiner Wert zur Bündelung von mehrkanaligen Benutzeraktivitäten für Berichtszwecke. Weitere Informationen finden Sie unter [Data Sources-Benutzerhandbuch](https://experienceleague.adobe.com/docs/analytics/import/data-sources/datasrc-home.html?lang=en#data-sources). |
| userAgent | Nicht unterstützt | Benutzeragenten-Zeichenfolge |
| visitorID | visitorID | Analytics-ID des Besuchers. Siehe [Besucheridentifizierung](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). |
| zip | zip | Konversion-PLZ. |
