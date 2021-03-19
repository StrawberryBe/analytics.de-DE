---
title: null
description: null
translation-type: tm+mt
source-git-commit: 537b41ee45cfa21bdf2e282fabc43a17fd90e327
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 12%

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

| BDIA, FPDS, Beides | BDIA-Variable | Variable für Spalte „Volle Verarbeitung“ | Beschreibung |
| --- | --- | --- | --- |
| BDIA | aamlh | Nicht unterstützt | Adobe Audience Manager-Positionshinweis. Siehe Gültige ID-Werte in der unten stehenden Tabelle AAM Region. |
| Beide | browserHeight | browserHeight | Browser-Höhe in Pixel (z. B. 768) |
| Beide | browserWidth | browserWidth | Browser-Breite in Pixel (z. B. 1024) |
| Beide | campaign | Kampagne | Konversion-Kampagnen-Trackingcode |
| Beide | channel | Kanal | Kanal-Zeichenfolge (z. B. Sportabteilung) |
| Beide | colorDepth | colorDepth | Bildschirmfarbtiefe in Bit (z. B. 24) |
| Beide | connectionType | connectionType | Verbindungstyp des Besuchers (LAN oder Modem) |
| BDIA | contextData.key | Nicht unterstützt | Schlüsselwertpaare werden in der Kopfzeile &quot;contextData.product&quot;oder &quot;contextData.color&quot;angegeben |
| Beide | cookiesEnabled | cookiesEnabled | `Y` oder  `N` wenn der Besucher Sitzungs-Cookies von Erstanbietern unterstützt |
| Beide | currencyCode | currencyCode | Währungscode des Umsatzes (z. B. `USD`) |
| BDIA | customerID.[customerIDType].authState | Nicht unterstützt | Der authentifizierte Status des Besuchers. Folgende Werte werden unterstützt: 0, 1, 2, UNKNOWN, AUTHENTICATED, LOGGED_OUT oder &#39;&#39; (ohne Unterscheidung zwischen Groß- und Kleinschreibung). Zwei aufeinander folgende einfache Anführungszeichen (&#39;&#39;) führen dazu, dass der Wert in der Abfrage-Zeichenfolge weggelassen wird, was beim Treffer in 0 umgewandelt wird. Bitte beachten Sie, dass die unterstützten numerischen authState-Werte Folgendes bedeuten: 0 = UNKNOWN, 1 = AUTHENTICATED, 2 = LOGGED_OUT. Bei customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, wobei jedoch die Groß-/Kleinschreibung zu beachten ist. |
| BDIA | customerID.[customerIDType].id | Nicht unterstützt | Die zu verwendende Kunden-ID. Bei customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, wobei jedoch die Groß-/Kleinschreibung zu beachten ist. |
| BDIA | customerID.[customerIDType].isMCSeed | Nicht unterstützt | Gibt an, ob dies der Samen für die Marketing Cloud-Besucher-ID ist. Folgende Werte werden unterstützt: 0, 1, TRUE, FALSE, &#39;&#39; (Groß-/Kleinschreibung wird nicht berücksichtigt). Wenn Sie 0, FALSE oder zwei aufeinander folgende einfache Anführungszeichen (&#39;&#39;) verwenden, wird der Wert in der Abfrage-Zeichenfolge weggelassen. Bei customerIDType kann es sich um eine beliebige alphanumerische Zeichenfolge handeln, wobei jedoch die Groß-/Kleinschreibung zu beachten ist. |
