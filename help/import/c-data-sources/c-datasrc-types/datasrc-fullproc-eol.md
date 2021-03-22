---
title: Ende der Lebensdauer für Datenquellen mit vollständiger Verarbeitung
description: Gründe für das Ende des Lebenszyklus und Vergleiche zwischen der Bulk Data Insertion API und der Datenquellen für die vollständige Verarbeitung.
translation-type: tm+mt
source-git-commit: 97e60e4c3a593405f92f47e5aa79ece70e0b3d60
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 30%

---


# Ende der Lebensdauer für Datenquellen mit vollständiger Verarbeitung

Seit mehreren Jahren können Sie mit der Datenquellen-Funktion der vollständigen Verarbeitung Daten auf Trefferebene an Adobe Analytics senden. Diese Daten wurden auf dieselbe Weise verarbeitet wie Daten, die über unsere JavaScript-Bibliotheken und das mobile App-SDK erfasst wurden. Im Jahr 2020 veröffentlichte die Adobe die API [Massendateneinfügung](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md), die dieselben Funktionen wie Datenquellen für die vollständige Verarbeitung, jedoch mit zusätzlichen Funktionen ausführt. In diesem Thema werden Einzelheiten zu den zusätzlichen Funktionen der Bulk Data Insertion API und die Unterschiede in den Dateiformaten erläutert.

Ab dem 25. März 2021 verhindert die Adobe die Erstellung neuer Datenquellen mit voller Verarbeitung. Vorhandene Verbindungen werden weiterhin unterstützt, bis der Dienst vollständig veraltet ist. Die Streichung wird 2021 erfolgen, obwohl noch kein bestimmter Termin festgelegt wurde.

## Warum schaffen wir diese Funktion ab?

Die Bulk Data Insertion API (BDIA) bietet zusätzliche Funktionen und deckt gleichzeitig alle Anwendungsfälle ab, die von der vollständigen Verarbeitung unterstützt werden. Wir glauben, dass Sie besser mit der Bulk Data Insertion API versorgt werden können.

## Schlüsselunterschiede zwischen Datenquellen für die vollständige Verarbeitung und der API für die Dateneinfügung für Massendateien

* Das Einfügen von Massendaten ermöglicht die Übermittlung mehrerer Dateien, die parallel verarbeitet werden können. Sie können Besucher-Gruppen verwenden, um Kontinuität und eVar des Besuchers sicherzustellen.
* Die Dateneinfügung umfasst sowohl Datenvalidierung als auch Fehlerbehandlungsfunktionen, wodurch einige der administrativen Schritte zum Übermitteln von Trefferdaten entfernt werden.
* Das Einfügen von Massendaten unterstützt mehrere Optionen für Besucher-IDs. Sie können sowohl die Analytics-ID als auch die Marketing Cloud-ID senden (weitere Informationen finden Sie unter [Identitätsdienst](https://experienceleague.adobe.com/docs/id-service/using/home.html)). Zusätzlich können Sie Ihre eigene ID als [Seed zum Generieren einer ECID](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#customer-id-and-experience-cloud-visitor-id-seeds) verwenden.
* Das Einfügen von Massendaten unterstützt Listen- und Kontextdatenvariablen.
* Die Massendateneinfügung unterstützt keine Activity Map-Daten.

## Wichtige Unterschiede in Dateiformat und Inhalt

* Das Einfügen von Massendaten enthält einige zusätzliche erforderliche Felder. Weitere Informationen finden Sie in der [Dokumentation](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md).
* Zur Gewährleistung der Kontinuität und Zuordnung von Besuchern erfordert die Eingabe von Massendaten, dass Zeilen in Dateien in chronologischer Reihenfolge sortiert werden. Informationen zur Dateireihenfolge der Aktivität der Besucher finden Sie unter [Besucher Groups](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#visitor-groups).
* Für das Einfügen von Massendaten müssen Dateien im .csv-Format im .gzip-Format komprimiert werden.
* BDIA verwendet &quot;timestamp&quot;anstelle von &quot;date&quot;.

Weitere Informationen finden Sie im folgenden Vergleich der in &quot;Bulk Data Insertion&quot;(BDIA) und &quot;Full Processing Data Sources&quot;(FPDS) verfügbaren Feldwerte.

## Vergleich der in BDIA und FPDS verfügbaren Feldwerte

| BDIA-Variable | Variable für Spalte „Volle Verarbeitung“ | Beschreibung |
| --- | --- | --- |
| aamlh | Nicht unterstützt | Adobe Audience Manager-Positionshinweis. |
| browserHeight | browserHeight | Browser-Höhe in Pixel (z. B. 768) |
| browserWidth | browserWidth | Browser-Breite in Pixel (z. B. 1024) |
| campaign | Kampagne | Konversion-Kampagnen-Trackingcode |
| channel | Kanal | Kanal-Zeichenfolge (z. B. Sportabteilung) |
| colorDepth | colorDepth | Bildschirmfarbtiefe in Bit (z. B. 24) |
| connectionType | connectionType | Verbindungstyp des Besuchers (LAN oder Modem) |
| contextData.key | Nicht unterstützt | Schlüsselwertpaare werden in der Kopfzeile &quot;contextData.product&quot;oder &quot;contextData.color&quot;angegeben |
| cookiesEnabled | cookiesEnabled | `Y` oder  `N` wenn der Besucher Sitzungs-Cookies von Erstanbietern unterstützt |
| currencyCode | currencyCode | Währungscode des Umsatzes (z. B. `USD`) |
| customerID.[customerIDType].authState | Nicht unterstützt | Der authentifizierte Status des Besuchers. Folgende Werte werden unterstützt: 0, 1, 2, UNKNOWN, AUTHENTICATED, LOGGED_OUT oder &#39;&#39; (ohne Unterscheidung zwischen Groß- und Kleinschreibung). Zwei aufeinander folgende einfache Anführungszeichen (&#39;&#39;) führen dazu, dass der Wert in der Abfrage-Zeichenfolge weggelassen wird, was beim Treffer in 0 umgewandelt wird. Bitte beachten Sie, dass die unterstützten numerischen authState-Werte Folgendes bedeuten: 0 = UNKNOWN, 1 = AUTHENTICATED, 2 = LOGGED_OUT. Bei customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, wobei jedoch die Groß-/Kleinschreibung zu beachten ist. |
| customerID.[customerIDType].id | Nicht unterstützt | Die zu verwendende Kunden-ID. Bei customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, wobei jedoch die Groß-/Kleinschreibung zu beachten ist. |
| customerID.[customerIDType].isMCSeed | Nicht unterstützt | Gibt an, ob dies der Samen für die Marketing Cloud-Besucher-ID ist. Folgende Werte werden unterstützt: 0, 1, TRUE, FALSE, &#39;&#39; (Groß-/Kleinschreibung wird nicht berücksichtigt). Wenn Sie 0, FALSE oder zwei aufeinander folgende einfache Anführungszeichen (&#39;&#39;) verwenden, wird der Wert in der Abfrage-Zeichenfolge weggelassen. Bei customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, wobei jedoch die Groß-/Kleinschreibung zu beachten ist. |
| eVarN | eVarN, d.h. `<eVar2>`...`<eVar>` | Konversion-eVar-Name. Sie können über bis zu 75 eVars verfügen (  eVar1 - eVar75 ) Sie können den eVar (eVar12) oder einen Anzeigennamen (Kampagne 3) angeben. |
| events | Ereignisse | [Ereignisses-Zeichenfolge](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html?lang=en#vars), die mit derselben Syntax wie die Variable s.Ereignisses formatiert ist. Beispiel: scAdd,Ereignis1,Ereignis7 |
| hierN | hierN, d.h. `<hier2>`...`</hier2>` | Hierarchiename. Sie können über bis zu 5 Hierarchien verfügen (  hier1 - hier5 ). Sie können den standardmäßigen Hierarchienamen `hier2` oder einen benutzerfreundlichen Namen (Yankees) angeben. |
| homePage | homePage | Y oder N, ist die aktuelle Seite die Homepage des Besuchers. |
| ipaddress | Nicht unterstützt | Die IP-Adresse des Besuchers. |
| javaEnabled | javaEnabled | Y oder N, hat der Besucher Java aktiviert. |
| javaScriptVersion | javaScriptVersion | JavaScript-Version (z. B. 1.3). |
| language | Nicht unterstützt | Die unterstützte Sprache des Browsers. Beispiel: `en-us`. |
| linkName | linkName | Name des Links. |
| linkType | linkType | Art des Links. Folgende Werte werden unterstützt: `d: Download link`, `e: Exit link`, `o: Custom link`. |
| linkURL | linkURL | HREF des Links. |
| listn (z. B. Liste2). | Nicht unterstützt | Eine Liste getrennter Werte, die in eine Variable überführt und bei der Berichterstellung als einzelne Zeilenelemente behandelt werden. |
| marketingCloudVisitorID | Nicht unterstützt | Marketing Cloud ID. Siehe [Besucher-ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en#id-service-api) und den Marketing Cloud-Besucher-ID-Dienst. |
| Nicht unterstützt | charSet | Der für Ihre Website unterstützte Zeichensatz. Beispiel: UTF-8, ISO-8859-1 usw. |
| Nicht unterstützt | clickAction | Objekt-ID für Besucher-ClickMap (oid). |
| Nicht unterstützt | clickActionType | Objekt-ID-Typ für Besucher-ClickMap (oidt). |
| Nicht unterstützt | clickContext | Seiten-ID für Besucher-ClickMap (pid). |
| Nicht unterstützt | clickContextType | Seiten-ID-Typ für Besucher-ClickMap (pidt). |
| Nicht unterstützt | clickSourceID | Quellenindex für Besucher-ClickMap (oi). |
| Nicht unterstützt | clickTag | Objekt-Tag-Name für Besucher-ClickMap (ot). |
| Nicht unterstützt | scXmlVer | Marketingberichte-XML-Anforderungsversion (z. B. 1.0). |
| Nicht unterstützt | timezone | Zeitzonenversatz des Besuchers zu GMT in Stunden (z. B. -8). |
| pageName | pageName | Name der Seite. |
| pageType | pageType | Seitentyp (z. B. &quot;Fehlerseite&quot;). |
| pageURL | pageURL | Seiten-URL (z. B. https://www.example.com/index.html). |
| plugins | plugins | Durch Semikolon getrennte Liste von Browser-Plugin-Namen. |
| products | products | Liste aller Produkte auf der Seite. Trennen Sie Produkte durch Kommas. Beispiel: Sport;Ball;1;5.95,Spielzeug; Oben;1:1.99. |
| prop1 – prop75 | propN, d.h. `<prop2>`...`</prop2>` | Zeichenfolge der Eigenschaftsnummer (z. B. Sportbereich). |
| propN | propN | Eigenschaftswerte für Ihre Eigenschaften. |
| purchaseID | purchaseID | Kauf-ID. |
| referrer | Werber | URL für verweisende Seiten. |
| reportSuiteID | s_account | Gibt die Report Suites an, an die Daten übermittelt werden sollen. Sie sollten mehrere Report Suite-IDs durch ein Komma trennen. |
| resolution | resolution | Bildschirmauflösung (z. B. 1024x768). |
| server | server | Serverzeichenfolge. |
| state | state | Konversion-Status-Zeichenfolge. |
| timestamp | Datum | Verwenden Sie das ISO 8601-Datumsformat YYY-MM-DDThh:mm:ss±UTC_offset (z. B. 2021-09-01T12:00:00-07:00 ) oder Unix Time Format (die Anzahl der Sekunden seit dem 1. Januar 197) 0). |
| trackingServer | Nicht unterstützt | Kann nur über die Spaltenüberschrift bereitgestellt werden. |
| transactionID | Nicht unterstützt | Allgemeiner Wert zur Bündelung von mehrkanaligen Benutzeraktivitäten für Berichtszwecke. Weitere Informationen finden Sie im [Datenquellen-Benutzerhandbuch](https://experienceleague.adobe.com/docs/analytics/import/data-sources/datasrc-home.html?lang=en#data-sources). |
| userAgent | Nicht unterstützt | Benutzeragenten-Zeichenfolge |
| visitorID | visitorID | Analytics-ID des Besuchers. Siehe [Besucher-ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). |
| zip | zip | Konversion-PLZ. |
