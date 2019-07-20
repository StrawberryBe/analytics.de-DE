---
description: Bietet Antworten und Vorschläge zur Fehlerbehebung zu einigen der am häufigsten gestellten Fragen zu Analytics.
keywords: Fehlerbehebung in Analytics
seo-description: Bietet Antworten und Vorschläge zur Fehlerbehebung zu einigen der am häufigsten gestellten Fragen zu Analytics.
seo-title: Häufig gestellte Fragen
title: Häufig gestellte Fragen
uuid: 285 b 0 ea 4-aa 07-4 d 39-a 74 f -37 b 1 d 02 d 19 f 1
translation-type: tm+mt
source-git-commit: fd1e2f1789ed9c8c31c89f0e7b6b7b2dd3ee114d

---


# Häufig gestellte Fragen

Bietet Antworten und Vorschläge zur Fehlerbehebung für einige der häufigsten Analytics-Fragen für Reports &amp; Analysen. For frequently asked implementation questions, see the [FAQ](../../implement/faq.md) in the Implement user guide.

**Mein Konto wurde gesperrt; Wie kann ich das entsperren?**

Wenden Sie sich an einen Administrator innerhalb Ihres Unternehmens, um ein Konto erneut zu aktivieren. See also [Troubleshoot login issues with Adobe Analytics](../../technotes/troubleshoot-login.md) in the Technotes user guide.

**Warum sehe ich einen leeren Bericht, obwohl ich weiß, dass Daten erfasst werden?**

Es gibt mehrere Punkte, um die Fehlerbehebung für Berichtsdaten zu überprüfen:

* Überprüfen Sie die verwendeten Metriken: Einige Berichte enthalten standardmäßig Umsatz in Reports &amp; Analysen. Stellen Sie sicher, dass die angezeigte Metrik für den Bericht relevant ist.
* Überprüfen Sie den Datumsbereich: Datumsbereiche, insbesondere diejenigen, die über die Datenaufbewahrungsrichtlinie Ihres Unternehmens hinausgehen, können keine Daten zurückgeben. Überprüfen Sie, ob der Datumsbereich richtig eingestellt ist.
* Interne URL-Filter überprüfen: Einige Berichte zu Traffic-Quellen funktionieren erst nach der korrekten Definition interner URL-Filter.

**Warum fehlen einige Berichte im Navigationsmenü?**

Berichte, die in einem Menü fehlen, stammen meist aus eingeschränkten Berechtigungen oder Menüanpassungen. Wenden Sie sich an einen Produktadministrator in Ihrem Unternehmen, um sicherzustellen, dass Sie Zugriff auf alle erforderlichen Dimensionen und Metriken haben und dass die Menüstruktur einer Report Suite nicht angepasst wurde.

**Warum werden einige lange Werte abgeschnitten?**

Fast alle Variablen in Adobe Analytics haben eine Zeichenbeschränkung. Der Seitenname hat eine Begrenzung von 100 Zeichen, während benutzerdefinierte Konversionsvariablen (evars) eine Beschränkung von 255 Zeichen haben. Adobe empfiehlt, dass Werte, die Sie an Adobe senden, knapp sind, um abgeschnittene Werte zu vermeiden.

**Warum sehe ich eine größere Verzögerung bei der Berichterstellung?**

Bei der Echtzeit-Berichterstellung stehen einige Traffic-Metrik innerhalb weniger Minuten zur Verfügung; bei Konversionsdaten und anderen verarbeitungsintensiven Daten dauert dies für gewöhnlich 30–90 Minuten. Obwohl die Plattform der Experience Cloud äußerst stabil ist, kann es in einigen wenigen Fällen zu Verzögerungen bei der Berichterstellung kommen. Diese Verzögerung wird als Latenzzeit bezeichnet. See [Latency](../../technotes/latency.md) in the Technotes user guide for more information.

**Warum wird die Geräteversion nicht auf iphones angezeigt?**

Apple-Geräte melden ihre Firmware-Version in der Benutzeragenten-Zeichenfolge, nicht die Geräteversion. Es ist schwierig, die iphone-Geräteversion anhand der für Adobe Analytics verfügbaren Informationen zu bestimmen. See [Comparing iPhone device versions](https://helpx.adobe.com/analytics/kb/comparing-iphone-device-versions.html) in the Analytics KB for more information.

**Warum stimmen die Summen unten in meinem Bericht nicht überein, wenn ich die Werte summiere?**

Dimensionswerte können oft an mehreren Stellen angewendet werden; beispielsweise Besuche, die über Mitternacht oder mehrere Produkte zu einer einzigen Bestellung gehören. Der Dimensionswert wird über alle zutreffenden Zeileneinträge berichtet, wird aber in der Gesamtsumme des Berichts dedupliziert. See [Compare sum of line items to report total](https://helpx.adobe.com/analytics/kb/sum-line-items-different-from-total.html) in the Analytics KB for more information.

**Wie schließe ich Daten aus einer bestimmten IP-Adresse in meiner Report Suite aus?**

Sie können Daten aus internen Website-Aktivitäten, wie Site-Tests und Mitarbeiternutzung, aus Ihren Berichten löschen. Mit dieser Funktion können Sie und Ihre Kollegen Ihre Website besuchen, ohne die Traffic-Daten zu verfälschen. See [Exclude by IP Address](../../admin/admin/exclude-ip.md) in the Admin user guide for more information.

**Kann ich eine Report Suite löschen?**

Das Löschen einer Report Suite ist nicht möglich. Eine Report Suite kann jedoch aus allen Ansichten in Adobe Analytics ausgeblendet werden. Beachten Sie, dass Serveraufrufe, die an eine ausgeblendete Report Suite gesendet werden, weiterhin auf Ihre monatliche Vertragsbeschränkung gezählt werden. See [Hide report suites](../../admin/company/c-hide-report-suites.md) in the Admin user guide for more information.

**Welchen Container sollte ich verwenden, wenn ich Segmentierung verwende? Page view, visit, or visitor?**

Der verwendete Segmentbehälter hängt davon ab, wie weit Sie Daten erfassen möchten. Seitenansichtsbehälter bringen nur Treffer, die Segmentkriterien erfüllen, und nützlich zum Herausfiltern irrelevanter Teile von Besuchen. Besuchebehälter bringen es alle Treffer eines Besuchs, bei denen eine oder mehrere Treffer mit den Segmentkriterien übereinstimmen, und nützlich, um Sitzungen im Allgemeinen anzusehen. Besucherbehälter bringen alle Besuche, bei denen ein Trefferkriterium erfüllt ist, und eignet sich für die Betrachtung von Personen. Sie können als Analyst festlegen, welcher Segmentbehälter am besten verwendet werden sollte. See [Segmentation overview](../../components/c-segmentation/seg-overview.md) in the Components user guide for more information.

**Warum wird mein Segment nicht in Data Warehouse angezeigt?**

Aufgrund der einzigartigen Verarbeitungsarchitektur von Data Warehouse ist die Plattform nicht für die Verarbeitung einiger Arten von Daten optimiert, wie z. B. Pfade. See [Data Warehouse segment compatibility](../../components/c-segmentation/seg-reference/seg-compatibility.md) in the Components user guide for more information.
