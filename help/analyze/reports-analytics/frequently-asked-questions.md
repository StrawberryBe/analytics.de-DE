---
description: Bietet Antworten und Vorschläge zur Fehlerbehebung zu einigen der am häufigsten gestellten Fragen zu Analytics.
keywords: Troubleshooting Analytics
title: Häufig gestellte Fragen
uuid: 285b0ea4-aa07-4d39-a74f-37b1d02d19f1
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Häufig gestellte Fragen

Enthält Antworten und Vorschläge zur Fehlerbehebung zu einigen der am häufigsten gestellten Fragen zu Analytics für Reports &amp; Analysen. Häufig gestellte Fragen zur Implementierung finden Sie in den [häufig gestellten Fragen](/help/implement/faq.md) im Implementierungs-Benutzerhandbuch.

**Mein Konto wurde gesperrt. Wie kann ich es freischalten?**

Wenden Sie sich an einen Administrator in Ihrer Organisation, um ein Konto zu reaktivieren. Siehe auch [Fehlerbehebung bei Anmeldeproblemen mit Adobe Analytics](/help/technotes/troubleshoot-login.md) im Technotes-Benutzerhandbuch.

**Warum sehe ich einen leeren Bericht, obwohl ich weiß, dass Daten gesammelt werden?**

Zur Fehlerbehebung bei Berichtsdaten müssen Sie mehrere Punkte prüfen:

* Überprüfen Sie die verwendeten Metriken: In einigen Berichten wird standardmäßig Umsatz in Reports &amp; Analysen verwendet. Stellen Sie sicher, dass die angezeigte Metrik für den Bericht relevant ist.
* Überprüfen Sie den Datumsbereich: Datumsbereiche, insbesondere solche, die über die Datenaufbewahrungsrichtlinie Ihres Unternehmens hinausgehen, können keine Daten zurückgeben. Vergewissern Sie sich, dass Ihr Datumsbereich korrekt eingestellt ist.
* Interne URL-Filter prüfen: Einige Berichte zu Traffic-Quellen funktionieren erst, nachdem Sie die internen URL-Filter korrekt definiert haben.

**Warum fehlen einige Berichte im Navigationsmenü?**

Berichte, die in einem Menü fehlen, stammen meist entweder aus eingeschränkten Berechtigungen oder aus der Menüanpassung. Wenden Sie sich an einen Produktadministrator in Ihrer Organisation, um sicherzustellen, dass Sie Zugriff auf alle erforderlichen Dimensionen und Metriken haben und dass die Menüstruktur einer Report Suite nicht angepasst wurde.

**Warum sind einige lange Werte abgeschnitten?**

Fast alle Variablen in Adobe Analytics haben eine Zeichenbeschränkung. Der Seitenname ist auf 100 Zeichen begrenzt, während benutzerdefinierte Konversionsvariablen (eVars) eine Beschränkung von 255 Zeichen haben. Adobe empfiehlt, dass die an Adobe gesendeten Werte knapp sind, um eine Kürzung zu vermeiden.

**Warum sehe ich eine große Verzögerung bei der Berichterstattung?**

Bei der Echtzeit-Berichterstellung stehen einige Traffic-Metrik innerhalb weniger Minuten zur Verfügung; bei Konversionsdaten und anderen verarbeitungsintensiven Daten dauert dies für gewöhnlich 30–90 Minuten. Obwohl die Plattform der Experience Cloud äußerst stabil ist, kann es in einigen wenigen Fällen zu Verzögerungen bei der Berichterstellung kommen. Diese Verzögerung wird als Latenzzeit bezeichnet. Weitere Informationen finden Sie unter [Latenzzeit](/help/technotes/latency.md) im Technotes-Benutzerhandbuch.

**Warum kann ich die Geräteversion nicht auf iPhones sehen?**

Apple-Geräte melden ihre Firmware-Version in der Benutzeragenten-Zeichenfolge, nicht in der Geräteversion. Es ist schwierig, die iPhone-Geräteversion anhand der Adobe Analytics verfügbaren Informationen zu ermitteln. Weitere Informationen finden Sie unter [Vergleichen von iPhone-Geräteversionen](https://helpx.adobe.com/analytics/kb/comparing-iphone-device-versions.html) in der Analytics-KB.

**Warum stimmen die Summen am Ende meines Berichts nicht überein, wenn ich die Werte zusammenfasse?**

Dimensionswerte können oft an mehreren Stellen angewendet werden. zum Beispiel Besuche, die sich über Mitternacht erstrecken, oder mehrere Produkte, die zu einer Bestellung gehören. Der Dimensionswert wird über alle zutreffenden Zeileneinträge hinweg gemeldet, jedoch im Gesamtwert des Berichts dedupliziert. Weitere Informationen finden Sie unter Summe der Zeilenelemente mit der Gesamtsumme[ in der Analytics-KB ](https://helpx.adobe.com/analytics/kb/sum-line-items-different-from-total.html)vergleichen.

**Wie schließe ich Daten von einer bestimmten IP-Adresse in meiner Report Suite aus?**

Sie können Daten aus internen Website-Aktivitäten, wie Site-Tests und Mitarbeiternutzung, aus Ihren Berichten löschen. Mit dieser Funktion können Sie und Ihre Kollegen Ihre Website besuchen, ohne die Traffic-Daten zu verfälschen. Weitere Informationen finden Sie unter Nach IP-Adresse [ausschließen](/help/admin/admin/exclude-ip.md) im Admin-Benutzerhandbuch.

**Kann ich eine Report Suite löschen?**

Das Löschen einer Report Suite ist nicht möglich. Eine Report Suite kann jedoch in Adobe Analytics für alle Ansichten ausgeblendet werden. Beachten Sie, dass an eine ausgeblendete Report Suite gesendete Serveraufrufe weiterhin auf Ihre monatliche vertragliche Beschränkung angerechnet werden. Weitere Informationen finden Sie unter Report Suites[ ](/help/admin/company/c-hide-report-suites.md)ausblenden im Admin-Benutzerhandbuch.

**Welchen Behälter sollte ich bei Verwendung der Segmentierung verwenden? Seitenansicht, Besuch oder Besucher?**

Der verwendete Segmentbehälter hängt davon ab, wie breit die Daten erfasst werden sollen. Seitenansichtsbehälter bringen nur Treffer ein, die Segmentkriterien entsprechen. Dies ist nützlich, um irrelevante Teile von Besuchen herauszufiltern. Besuchsbehälter bringen alle Treffer eines Besuchs mit Treffern, bei denen ein oder mehrere Segmentkriterien übereinstimmen, die für die Betrachtung von Sitzungen im Allgemeinen nützlich sind. Besucherbehälter bringen alle Besuche mit ein, bei denen ein Treffer mit Segmentkriterien übereinstimmt, die für die Anzeige von Personen nützlich sind. Sie können als Analyst festlegen, welcher Segmentbehälter am besten verwendet werden soll. Weitere Informationen finden Sie unter [Segmentierungsübersicht](/help/components/c-segmentation/seg-overview.md) im Komponenten-Benutzerhandbuch.

**Warum wird mein Segment nicht in Data Warehouse angezeigt?**

Aufgrund der einzigartigen Verarbeitungsarchitektur von Data Warehouse ist die Plattform nicht für die Verarbeitung bestimmter Datentypen optimiert, wie z. B. Pfade. Weitere Informationen finden Sie unter Segmentkompatibilität mit [Data Warehouse](/help/components/c-segmentation/seg-reference/seg-compatibility.md) im Komponenten-Benutzerhandbuch.
