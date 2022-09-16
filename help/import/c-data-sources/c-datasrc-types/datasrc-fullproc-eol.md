---
title: Ende der Lebensdauer für Full Processing Data Sources
description: Gründe für das Ende der Lebensdauer und Vergleiche zwischen der Bulk Data Insertion-API und Full Processing Data Sources.
feature: Data Sources
exl-id: 24a44b7a-64fd-4a99-975f-4887f4638812
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 100%

---

# Ende der Lebensdauer für Full Processing Data Sources

Für lange Zeit konnten Sie mit Full Processing Data Sources Daten auf Trefferebene an Adobe Analytics übermitteln. Diese Daten wurden auf die gleiche Weise verarbeitet wie Daten, die über unsere JavaScript-Bibliotheken und das SDK für Mobile Apps erhoben wurden. Im Jahr 2020 veröffentlichte Adobe die [Bulk Data Insertion-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md), die dieselben Funktionen wie Full Processing Data Sources ausführt, jedoch mit zusätzlichen Funktionen. Dieses Thema enthält Details zu zusätzlichen Funktionen, die von der Bulk Data Insertion-API bereitgestellt werden, und skizziert Unterschiede in Dateiformaten.

Seit dem 25. März 2021 verhindert Adobe, dass neue Verbindungen mit Full Processing Data Sources erstellt werden. Vorhandene Verbindungen wurden unterstützt, bis der Service am 31. Januar 2022 vollständig eingestellt wurde. Zusätzlich zu unserer Standarddokumentation stellen wir eine exemplarische Vorgehensweise der [Schritte, die zum Übermitteln von Daten über die Bulk Data Insertion-API erforderlich sind](https://adobe.ly/aabdia), bereit.

## Warum haben wir diese Funktion eingestellt?

Die Bulk Data Insertion-API (BDIA) bietet zusätzliche Funktionalität und deckt alle Anwendungsfälle ab, die von der vollständigen Verarbeitung unterstützt wurden. Die bessere Vorgehensweise ist, die Bulk Data Insertion-API zu verwenden.

## Wichtige Unterschiede zwischen Full Processing Data Sources und der Bulk Data Insertion-API

* Bulk Data Insertion ermöglicht die Übermittlung mehrerer Dateien, die parallel verarbeitet werden können. Sie können Besuchergruppen verwenden, um Besucherkontinuität und eVar-Zuordnung sicherzustellen.
* Bulk Data Insertion verfügt über Datenvalidierungs- sowie Fehlerbehandlungsfunktionen, wodurch ein Teil der Verwaltungsarbeit beim Senden von Trefferdaten entfällt.
* Bulk Data Insertion unterstützt mehrere Optionen für Besucher-IDs. Sie können sowohl die Analytics ID als auch die Experience Cloud ID übermitteln (weitere Informationen finden Sie unter [Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de)). Außerdem können Sie Ihre eigene ID als [Startwert für die Generierung einer ECID](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#customer-id-and-experience-cloud-visitor-id-seeds) verwenden.
* Bulk Data Insertion unterstützt Listen- und Kontextdatenvariablen.
* Bulk Data Insertion unterstützt keine Activity Map-Daten.

## Hauptunterschiede in Dateiformat und Inhalt

* Bulk Data Insertion hat einige zusätzliche erforderliche Felder. Einzelheiten finden Sie in der [Dokumentation](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md).
* Um die Besucherkontinuität und -zuordnung sicherzustellen, erfordert das Einfügen von Massendaten, dass Zeilen innerhalb von Dateien in chronologischer Reihenfolge sortiert werden. Weitere Informationen zur dateiübergreifenden Sortierung von Besucheraktivitäten finden Sie unter [Besuchergruppen](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#visitor-groups).
* Bulk Data Insertion erfordert, dass die Dateien im .gzip-Format .csv-komprimiert sind.
* BDIA verwendet „timestamp“ statt „date“.

Weitere Einzelheiten finden Sie im folgenden Vergleich der Feldwerte, die in Bulk Data Insertion (BDIA) und Full Processing Data Sources (FPDS) verfügbar sind.

## Vergleich der in BDIA und FPDS verfügbaren Feldwerte

| BDIA-Variable | Variable für Spalte „Volle Verarbeitung“ | Beschreibung |
| --- | --- | --- |
| aamlh | Nicht unterstützt | Standorthinweis für Adobe Audience Manager. |
| browserHeight | browserHeight | Browser-Höhe in Pixel (z. B. 768) |
| browserWidth | browserWidth | Browser-Breite in Pixel (z. B. 1024) |
| campaign | Kampagne | Konversion-Kampagnen-Trackingcode |
| channel | channel | Kanal-Zeichenfolge (z. B. Sportabteilung) |
| colorDepth | colorDepth | Bildschirmfarbtiefe in Bit (z. B. 24) |
| connectionType | connectionType | Verbindungstyp des Besuchers (LAN oder Modem) |
| contextData.key | Nicht unterstützt | Schlüssel-Wert-Paare werden angegeben, indem der Header &quot;contextData.product&quot; oder &quot;contextData.color&quot; genannt wird. |
| cookiesEnabled | cookiesEnabled | `Y` oder `N`, wenn der Besucher Sitzungscookies von Erstanbietern unterstützt |
| currencyCode | currencyCode | Währungscode für Umsatz (z. B. `USD`) |
| customerID.[customerIDType].authState | Nicht unterstützt | Der authentifizierte Zustand des Besuchers. Unterstützte Werte sind: 0, 1, 2, UNKNOWN, AUTHENTICATED, LOGGED_OUT oder &#39;&#39; (Groß-/Kleinschreibung wird nicht beachtet). Zwei aufeinanderfolgende einfache Anführungszeichen (&#39;&#39;) bewirken, dass der Wert in der Abfragezeichenfolge weggelassen wird, was bei einem Treffer zu 0 übersetzt wird. Bitte beachten Sie, dass die unterstützten authState-Zahlenwerte Folgendes bedeuten: 0 = UNKNOWN, 1 = AUTHENTICATED, 2 = LOGGED_OUT. Der customerIDType kann eine beliebige alphanumerische Zeichenfolge sein, es sollte jedoch zwischen Groß- und Kleinschreibung unterschieden werden. |
| customerID.[customerIDType].id | Nicht unterstützt | Die zu verwendende Kunden-ID. Der customerIDType kann eine beliebige alphanumerische Zeichenfolge sein, es sollte jedoch zwischen Groß- und Kleinschreibung unterschieden werden. |
| customerID.[customerIDType].isMCSeed | Nicht unterstützt | Ob dies der Seed für die Experience Cloud-Besucher-ID ist oder nicht. Unterstützte Werte sind: 0, 1, TRUE, FALSE, &#39;&#39; (Groß-/Kleinschreibung wird nicht beachtet). Die Verwendung von 0, FALSE oder zwei aufeinanderfolgenden einfachen Anführungszeichen (&#39;&#39;) bewirkt, dass der Wert in der Abfragezeichenfolge weggelassen wird. Der customerIDType kann eine beliebige alphanumerische Zeichenfolge sein, es sollte jedoch zwischen Groß- und Kleinschreibung unterschieden werden. |
| eVarN | eVarN, d. h. `<eVar2>`...`<eVar>` | Konversion-eVar-Name. Sie können über bis zu 75 eVars verfügen ( eVar1 - eVar75 ) Sie können den eVar-Namen (eVar12) oder einen Anzeigenamen (Werbekampagne 3) angeben. |
| events | events | [Ereigniszeichenfolge](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html?lang=de#vars), mit derselben Syntax für die Variable s.events formatiert. Zum Beispiel: scAdd,event1,event7 |
| hierN | hierN, d.h. `<hier2>`...`</hier2>` | Hierarchiename. Sie können über bis zu 5 Hierarchien verfügen (  hier1 - hier5 ). Sie können den Standardhierarchienamen (`hier2`) oder einen benutzerfreundlichen Namen (Yankees) festlegen. |
| homePage | homePage | Y oder N, ist die aktuelle Seite die Homepage des Besuchers. |
| ipaddress | Nicht unterstützt | Die IP-Adresse des Besuchers. |
| javaEnabled | javaEnabled | Y oder N, hat der Besucher Java aktiviert. |
| javaScriptVersion | javaScriptVersion | JavaScript-Version (z. B. 1.3). |
| Sprache | Nicht unterstützt | Die unterstützte Sprache des Browsers. Zum Beispiel `en-us`. |
| linkName | linkName | Name des Links. |
| linkType | linkType | Art des Links. Folgende Werte werden unterstützt: `d: Download link`, `e: Exit link`, `o: Custom link`. |
| linkURL | linkURL | HREF des Links. |
| listn Zum Beispiel list2. | Nicht unterstützt | Eine Liste getrennter Werte, die in eine Variable überführt und bei der Berichterstellung als einzelne Zeilenelemente behandelt werden |
| marketingCloudVisitorID | Nicht unterstützt | Experience Cloud ID. Siehe [Besucheridentifizierung](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de#id-service-api) und den Experience Cloud-Besucher-ID-Service |
| Nicht unterstützt | charSet | Der für Ihre Website unterstützte Zeichensatz. Beispiel: UTF-8, ISO-8859-1 usw. |
| Nicht unterstützt | clickAction | Objekt-ID für Besucher-ClickMap (oid). |
| Nicht unterstützt | clickActionType | Objekt-ID-Typ für Besucher-ClickMap (oidt). |
| Nicht unterstützt | clickContext | Seiten-ID für Besucher-ClickMap (pid). |
| Nicht unterstützt | clickContextType | Seiten-ID-Typ für Besucher-ClickMap (pidt). |
| Nicht unterstützt | clickSourceID | Quellenindex für Besucher-ClickMap (oi). |
| Nicht unterstützt | clickTag | Objekt-Tag-Name für Besucher-ClickMap (ot). |
| Nicht unterstützt | scXmlVer | Marketingberichte-XML-Anforderungsversion (z. B. 1.0). |
| Nicht unterstützt | timezone | Zeitzonenversatz des Besuchers zu GMT in Stunden (z. B. -8). |
| pageName | pageName | Name der Seite |
| pageType | pageType | Art der Seite (z. B. &quot;Fehlerseite&quot;). |
| pageURL | pageURL | Seiten-URL (z. B. https://www.example.com/index.html). |
| plugins | plugins | Semikolon-getrennte Liste der Browser-Plug-in-Namen. |
| products | products | Liste aller Produkte auf der Seite. Trennen Sie Produkte mit einem Komma. Zum Beispiel: Sports;Ball;1;5.95,Toys; Top;1:1.99. |
| prop1 – prop75 | propN, d. h. `<prop2>`...`</prop2>` | Zeichenfolge der Eigenschaftsnummer (z. B. Sportabteilung). |
| propN | propN | Eigenschaftswerte für Ihre Eigenschaften. |
| purchaseID | purchaseID | Kauf-ID. |
| referrer | referrer | URL für verweisende Seiten. |
| reportSuiteID | s_account | Gibt die Report Suites an, an die Daten übermittelt werden sollen. Sie sollten mehrere Report Suite-IDs durch ein Komma trennen. |
| resolution | resolution | Bildschirmauflösung (z. B. 1024x768). |
| server | server | Serverzeichenfolge. |
| state | state | Konversion-Status-Zeichenfolge. |
| timestamp | Datum | Verwenden Sie das ISO 8601-Datumsformat YYYY-MM-DDThh:mm:ss±UTC_offset (z. B. 2021-09-01T12:00:00-07:00 ) oder Unix-Zeitformat (die Anzahl der seit dem 1. Januar 1970 verstrichenen Sekunden). |
| trackingServer | Nicht unterstützt | Kann nur über Spaltenkopfzeile geliefert werden. |
| transactionID | Nicht unterstützt | Allgemeiner Wert zur Bündelung von mehrkanaligen Benutzeraktivitäten für Berichtszwecke. Weitere Informationen finden Sie im [Benutzerhandbuch für Data Sources](https://experienceleague.adobe.com/docs/analytics/import/data-sources/datasrc-home.html?lang=de#data-sources). |
| userAgent | Nicht unterstützt | Benutzeragenten-Zeichenfolge |
| visitorID | visitorID | Analytics-ID des Besuchers. Siehe [Besucheridentifizierung](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). |
| zip | zip | Konversion-PLZ. |
