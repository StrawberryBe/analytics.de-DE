---
description: Bietet Antworten und Vorschläge zur Fehlerbehebung zu einigen der am häufigsten gestellten Fragen zu Analytics.
keywords: Fehlerbehebung in Analytics
title: Häufig gestellte Fragen
uuid: 285b0ea4-aa07-4d39-a74f-37b1d02d19f1
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 99%

---


# Häufig gestellte Fragen

Bietet Antworten und Vorschläge zur Fehlerbehebung zu einigen der am häufigsten gestellten Analytics-Fragen zu Reports &amp; Analytics. Häufig gestellte Fragen zur Implementierung finden Sie in den [FAQs](/help/implement/faq.md) im Benutzerhandbuch zur Implementierung.

**Mein Konto wurde gesperrt. Wie kann ich es freischalten?**

Wenden Sie sich an einen Administrator in Ihrer Organisation, um Ihr Konto erneut zu aktivieren. Siehe auch [Fehlerbehebung bei Anmeldeproblemen mit Adobe Analytics](/help/technotes/troubleshoot-login.md) im Technotes-Benutzerhandbuch.

**Warum sehe ich einen leeren Bericht, obwohl ich weiß, dass Daten gesammelt werden?**

Zur Fehlerbehebung bei Berichtsdaten müssen Sie mehrere Punkte prüfen:

* Überprüfen Sie die verwendeten Metriken: In einigen Berichten wird standardmäßig „Umsatz“ in Reports &amp; Analytics verwendet. Stellen Sie sicher, dass die angezeigte Metrik für den Bericht relevant ist.
* Überprüfen Sie den Datumsbereich: Datumsbereiche, insbesondere solche, die über die Datenaufbewahrungsrichtlinie Ihrer Organisation hinausgehen, können keine Daten zurückgeben. Vergewissern Sie sich, dass Ihr Datumsbereich korrekt eingestellt ist.
* Prüfen Sie interne URL-Filter: Einige Berichte zu Traffic-Quellen funktionieren erst, nachdem Sie die internen URL-Filter korrekt definiert haben.

**Warum fehlen einige Berichte im Navigationsmenü?**

Berichte, die in einem Menü fehlen, sind meist auf eingeschränkte Berechtigungen oder eine Anpassung des Menüs zurückzuführen. Wenden Sie sich an einen Produktadministrator in Ihrer Organisation, um sicherzustellen, dass Sie Zugriff auf alle erforderlichen Dimensionen und Metriken haben und dass die Menüstruktur einer Report Suite nicht angepasst wurde.

**Warum sind einige lange Werte abgeschnitten?**

Fast alle Variablen in Adobe Analytics haben eine Zeichenbeschränkung. Der Seitenname ist auf 100 Zeichen begrenzt, während benutzerdefinierte Konversionsvariablen (eVars) eine Beschränkung von 255 Zeichen haben. Adobe empfiehlt, dass die an Adobe gesendeten Werte kurz sind, damit sie nicht abgeschnitten werden.

**Warum verzögert sich die Berichterstellung so lange?**

Bei der Echtzeit-Berichterstellung stehen einige Traffic-Metrik innerhalb weniger Minuten zur Verfügung; bei Konversionsdaten und anderen verarbeitungsintensiven Daten dauert dies für gewöhnlich 30–90 Minuten. Obwohl die Plattform der Experience Cloud äußerst stabil ist, kann es in einigen wenigen Fällen zu Verzögerungen bei der Berichterstellung kommen. Diese Verzögerung wird als Latenzzeit bezeichnet. Weitere Informationen finden Sie unter [Latenz](/help/technotes/latency.md) im Technotes-Benutzerhandbuch.

**Warum kann ich die Geräteversion auf iPhones nicht sehen?**

Apple-Geräte melden ihre Firmware-Version in ihrer Benutzeragenten-Zeichenfolge, nicht die Geräteversion. Es ist schwierig, die iPhone-Geräteversion anhand der für Adobe Analytics verfügbaren Informationen zu ermitteln. Weitere Informationen finden Sie unter [Vergleichen von iPhone-Geräteversionen](https://helpx.adobe.com/de/analytics/kb/comparing-iphone-device-versions.html) in der Analytics-KB.

**Warum stimmen die Summen am Ende meines Berichts nicht überein, wenn ich die Werte addiere?**

Dimensionselemente können oft an mehreren Stellen angewendet werden, beispielsweise bei Besuchen, die sich über Mitternacht erstrecken, oder bei mehreren Produkten, die zu einer Bestellung gehören. Das Dimensionselement wird über alle zutreffenden Zeileneinträge hinweg gemeldet, jedoch im Gesamtwert des Berichts dedupliziert. Weitere Informationen finden Sie unter [Vergleichen der Summe der Zeileneinträge mit der Summe im Bericht](https://helpx.adobe.com/de/analytics/kb/sum-line-items-different-from-total.html) in der Analytics-KB.

**Wie kann ich Daten von einer bestimmten IP-Adresse aus meiner Report Suite ausschließen?**

Sie können Daten aus internen Website-Aktivitäten, wie Site-Tests und Mitarbeiternutzung, aus Ihren Berichten löschen. Mit dieser Funktion können Sie und Ihre Kollegen Ihre Website besuchen, ohne die Traffic-Daten zu verfälschen. Weitere Informationen finden Sie unter [Nach IP-Adresse ausschließen](/help/admin/admin/exclude-ip.md) im Admin-Benutzerhandbuch.

**Kann ich eine Report Suite löschen?**

Das Löschen einer Report Suite ist nicht möglich. Eine Report Suite kann jedoch in Adobe Analytics für alle Ansichten ausgeblendet werden. Beachten Sie, dass an eine ausgeblendete Report Suite gesendete Serveraufrufe weiterhin auf Ihre monatliche vertragliche Beschränkung angerechnet werden. Weitere Informationen finden Sie unter [Ausblenden von Report Suites](/help/admin/company/c-hide-report-suites.md) im Admin-Benutzerhandbuch.

**Welchen Container sollte ich für die Segmentierung verwenden? Seitenansicht, Besuch oder Besucher?**

Der verwendete Segmentcontainer hängt davon ab, wie breit die Daten erfasst werden sollen. Seitencontainer berücksichtigen nur Treffer, die Segmentkriterien entsprechen. Dies ist nützlich, um irrelevante Teile von Besuchen herauszufiltern. Besuchscontainer berücksichtigen alle Treffer eines Besuchs, die mit einem oder mehreren Segmentkriterien übereinstimmen. Dies ist für die Betrachtung von Sitzungen im Allgemeinen nützlich. Besuchercontainer berücksichtigen alle Besuche, bei denen ein Treffer mit Segmentkriterien übereinstimmt. Dies ist für die Betrachtung von Personen nützlich. Als Analyst entscheiden Sie selbst, welcher Segmentcontainer am besten für Sie geeignet ist. Weitere Informationen finden Sie in der [Segmentierungsübersicht](/help/components/segmentation/seg-overview.md) im Komponentenleitfaden.

**Warum wird mein Segment nicht in Data Warehouse angezeigt?**

Aufgrund der einzigartigen Verarbeitungsarchitektur von Data Warehouse ist die Plattform nicht für die Verarbeitung bestimmter Datentypen optimiert, wie z. B. Pfade. Weitere Informationen finden Sie unter [Data Warehouse-Segmentkompatibilität](/help/components/segmentation/seg-reference/seg-compatibility.md) im Komponentenleitfaden.
