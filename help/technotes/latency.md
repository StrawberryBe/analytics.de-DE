---
description: Die nachfolgenden Informationen helfen bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten.
keywords: missing data;slow
subtopic: Current data
title: Datenverfügbarkeit und -latenz
topic: Reports
uuid: 1f0e67e3-6cea-4af8-8b18-7ae9223df7c8
translation-type: ht
source-git-commit: a4a4d9e6e2d3e3ed88b4ef66e9da3b05865a9b79
workflow-type: ht
source-wordcount: '803'
ht-degree: 100%

---


# Datenverfügbarkeit und -latenz in Adobe Analytics

Die vollständigen Daten sind im Allgemeinen zwei Stunden nach dem Erfassen der Daten in Berichten verfügbar. Die nachfolgenden Informationen helfen bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten.

## Grundlagen des Daten-Batchings

Jeder Datenerfassungsserver erfasst und verarbeitet Analyse-Rohdaten und lädt die Batch-Daten dann stündlich zur Berichterstellung hoch. Die Übertragung dauert in der Regel 30 Minuten. Die normale Latenz für Traffic direkt nach dem letzten Hochladen liegt daher bei etwa 90 Minuten (60 Minuten bis zum nächsten Batch-Upload und anschließend 30 Minuten für die Dateiübertragung und die Anzeige). Bei Traffic, der direkt vor dem Hochladen anfällt, kann die Datenlatenz auf 30 Minuten sinken (0 Minuten bis zum nächsten Batchupload und anschließend 30 Minuten für die Dateiübertragung und die Anzeige).

Bei Bedarf können Sie bei der Adobe-Kundenunterstützung anfordern, halbstündliche (statt stündliche) Batch-Daten-Uploads für Ihre meistgenutzten Report Suites einzurichten.

## Gründe für Latenz

Latenz ist eine Verzögerung, die länger dauert als die zwei Stunden, die Datenerfassungs-Server normalerweise für die vollständige Verarbeitung der Daten benötigen. Die Datenerfassung wird hierdurch nicht beeinträchtigt. Daten werden weiterhin für eine funktionierende Implementierung erfasst, unabhängig davon, wie hoch die Latenz einer Report Suite ist. Der Schweregrad (wie aktuell die Daten sind) und die Länge (die Zeit, die es dauert, um sie zu beheben) können stark variieren. Meist sind Latenzen nur auf eine einzelne Report Suite beschränkt.

Latenzzeiten werden durch eine der folgenden allgemeinen Kategorien verursacht:

* **Unerwartete Traffic-Spitzen:** Diese Art von Latenz tritt auf, wenn mehr Daten an eine Report Suite gesendet werden als vertraglich festgelegt oder erwartet wurde. Dies ist die häufigste Ursache für Latenzzeiten.
* **Normale Hardwareprobleme:** Adobe setzt branchenführende Strategien für die Rechenzentrumsverwaltung und -überwachung, Datenredundanz und Hardware-Zuverlässigkeit ein. Die Hardware wird regelmäßig und in Verbindung mit bekanntgegebenen Wartungsfenstern aktualisiert. Für außerplanmäßige Wartungsarbeiten an fehlerhafter Hardware kann ein vorübergehender Stopp der Datenverarbeitung (nicht der Datenerfassung) erforderlich sein, wenn Ersatz-Hardware in Betrieb genommen werden muss. Dieser vorübergehende Stillstand bei der Verarbeitung kann zu einer merklichen Latenzzeit führen.
* **Anomale Daten:** Unnatürliche Datenmuster, wie ungewöhnlich lange, von einem Bot oder Crawler verursachte Besuche, können zeitweilig bestimmte Verarbeitungslasten erhöhen, die dann zu Latenz führen.

## Von Latenz abhängige Funktionen

Einige Funktionen von Adobe Experience Cloud verfügen zusätzlich zur standardmäßigen Verarbeitungszeit auch über eine standardmäßige Latenzzeit.

* Für Analytics for Target (A4T) ist eine zusätzliche Latenz von 5 bis 10 Minuten erforderlich, damit gesammelte Daten von beiden Plattformen im selben Treffer gespeichert werden können.
* Daten mit Zeitstempel erfordern aufgrund verschiedener Server, auf denen diese Daten verarbeitet werden, zusätzliche Zeit. Treffer mit Zeitstempel, die (nahezu) in Echtzeit empfangen werden, können bis zu 15 Minuten erfordern. Treffer mit einem Zeitstempel von gestern können bis zu zwei Stunden dauern. Ältere Treffer können länger dauern und jeden Tag bis zu einer Höchstdauer von etwa 24 Stunden ansteigen.

## Möglichkeiten zur Senkung oder Vermeidung von Latenzen

Zur Vermeidung von Latenzzeiten oder Verkürzung der Wiederherstellungsdauer bei eingetretener Latenz gibt es mehrere Strategien:

* **Informieren Sie Adobe über erwartete Traffic-Spitzen:** Es ist zwar nicht möglich, jede Traffic-Spitze Ihrer Site vorherzusehen, es kann jedoch vorkommen, dass Sie einen erheblichen Traffic-Anstieg erwarten. Beispiele sind besonders erfolgreiche Phasen während der Feiertagssaison oder kurz nach dem Start einer großen Kampagne. In diesen Situationen stellt Adobe eine Möglichkeit bereit, wie Ihre Firma uns über erwartete Trafficzunahmen informieren kann, damit wir Ihrer Report Suite zusätzliche Verarbeitungsressourcen zuweisen können. Weitere Informationen zur Benachrichtigung von Adobe über erhöhten Traffic finden Sie unter [Planen von Traffic-Spitzen](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) im Administratorhandbuch.
* **Berücksichtigen Sie beim Aktivieren neuer Funktionen die Verarbeitungslast:** Einige Funktionen sind verarbeitungsintensiver als andere. Je mehr Funktionen für eine Report Suite aktiviert sind, desto schwieriger ist die Wiederherstellung des normalen Betriebs nach dem Auftreten von Latenzzeiten. Beachten Sie beim Aktivieren von Funktionen für eine Report Suite, dass die folgenden Funktionen die zu verarbeitende Datenmenge vergrößern:

   * Implementieren von mehr als 20 Ereignissen auf derselben Seite
   * Komplexe VISTA-Regeln
   * Mehr als 20 Werte in der Variable products
   * Ereignis-Serialisierung

* Aktivieren Sie die IAB-Bot-Filterung: Durch die [Bot-Filterung](/help/admin/admin/bot-removal/bot-removal.md) können Latenzzeiten deutlich reduziert werden, wenn Ihre Report Suite häufig von Bots oder Crawlern besucht wird. Verwenden Sie die IAB-Botliste, da diese vom [Interactive Advertising Bureau](https://www.iab.net/about_the_iab) aktualisiert und gewartet wird. Anwender können in Ergänzung zu den IAB-Regeln eigene Bot-Regeln erstellen.

## Verfahren bei Latenzzeit

Wenn Latenzen auftreten, stellen Sie sicher, dass Adobe die Verarbeitungs-Pipeline proaktiv überwacht und alles unternimmt, um die Verarbeitungszeit so schnell wie möglich wieder auf den Normalzustand zurückzusetzen. Viele Latenzprobleme können innerhalb von Stunden behoben werden. Wenn Sie Fragen zu einer bestimmten Report Suite haben, kann sich ein unterstützter Benutzer Ihrer Firma mit der Report-Suite-ID, bei der Latenzzeiten auftreten, an den Kundendienst wenden. Der Adobe-Support-Mitarbeiter kann die Latenzzeit überprüfen und Sie über den Fortschritt und die Behebung des Problems informieren.
