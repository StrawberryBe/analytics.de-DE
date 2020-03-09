---
description: Die folgenden Informationen können bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten helfen.
keywords: missing data;slow
subtopic: Current data
title: Datenverfügbarkeit und Latenz
topic: Reports
uuid: 1f0e67e3-6cea-4af8-8b18-7ae9223df7c8
translation-type: tm+mt
source-git-commit: a4a4d9e6e2d3e3ed88b4ef66e9da3b05865a9b79

---


# Datenverfügbarkeit und -latenz in Adobe Analytics

In der Regel werden 2 Stunden nach der Datenerfassung vollständige Daten in Berichten angezeigt. Die folgenden Informationen können bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten helfen.

## Grundlagen der Datenstapelung

Jeder Datenerfassungsserver erfasst und verarbeitet Analyse-Rohdaten und lädt die Batch-Daten dann stündlich zur Berichterstellung hoch. Die Übertragung dauert in der Regel 30 Minuten. Die normale Latenz für Traffic direkt nach dem letzten Hochladen liegt daher bei etwa 90 Minuten (60 Minuten bis zum nächsten Batch-Upload und anschließend 30 Minuten für die Dateiübertragung und die Anzeige). Bei Traffic, der direkt vor dem Hochladen erfolgt, kann die Datenlatenz bis zu 30 Minuten betragen (0 Minuten bis zum nächsten Batch-Upload und 30 Minuten für Dateiübertragung und -anzeige).

Bei Bedarf kann die Adobe-Kundenunterstützung Batch-Daten-Uploads über 30 Minuten (statt stündlich) für Ihre am häufigsten verwendeten Report Suites aktivieren.

## Beitrag zur Latenz

Die Latenz ist eine Verzögerung, die länger als die normalen 2 Stunden dauert, bis die Datenerfassungsserver die Daten vollständig verarbeiten. Die Datenerfassung wird nicht beeinflusst. Daten werden weiterhin für eine funktionierende Implementierung erfasst, unabhängig davon, wie lange eine Report Suite latent ist. Der Schweregrad (wie aktuell die Daten sind) und die Länge (die Zeit, die es dauert, um sie zu beheben) können stark variieren. Er ist normalerweise auf eine einzige Report Suite beschränkt.

Latenzzeiten werden durch eine der folgenden allgemeinen Kategorien verursacht:

* **Unerwartete Traffic-Spitze:** Diese Art von Latenz tritt auf, wenn mehr Daten an eine Report Suite gesendet werden, als vertraglich festgelegt oder erwartet wurde. Dies ist die häufigste Ursache für Latenzzeiten.
* **Normale Hardwareprobleme:** Adobe setzt erstklassige Strategien für die Verwaltung und Überwachung von Rechenzentren, Datenredundanz und Hardwarezuverlässigkeit ein. Die Hardware wird regelmäßig und in Verbindung mit bekanntgegebenen Wartungsfenstern aktualisiert. Die Notwartung von fehlerhaften Hardware kann eine notwendige und vorübergehende Unterbrechung der Datenverarbeitung (nicht der Datenerfassung) erfordern, da Ersatzhardware online verfügbar gemacht wird. Dieser vorübergehende Stillstand bei der Verarbeitung kann zu einer merklichen Latenzzeit führen.
* **Ungewöhnliche Daten:** Unnatürliche Datenmuster wie ungewöhnlich lange Besuche, die von einem Bot oder Crawler verursacht werden, können zeitweise bestimmte Verarbeitungslasten erhöhen, die zu Latenzzeiten führen.

## Funktionen, die von der Latenz abhängen

Einige Funktionen der Adobe Experience Cloud verfügen über eine angeborene Latenzzeit zusätzlich zur standardmäßigen Verarbeitungszeit.

* Für Analytics for Zielgruppe (A4T) ist eine zusätzliche Latenz von 5-10 Minuten erforderlich, damit gesammelte Daten von beiden Plattformen im selben Treffer gespeichert werden können.
* Daten mit Zeitstempel erfordern aufgrund verschiedener Server, auf denen diese Daten verarbeitet werden, zusätzliche Zeit. Treffer mit Zeitstempel, die in Echtzeit oder in der Nähe von Echtzeit empfangen werden, können bis zu 15 Minuten dauern. Treffer mit einem Zeitstempel von gestern können bis zu 2 Stunden dauern. Ältere Treffer können länger dauern und jeden Tag bis zu einer Höchstdauer von etwa 24 Stunden ansteigen.

## Möglichkeiten zur Verringerung oder Verhinderung von Latenzzeiten

Zur Vermeidung von Latenzzeiten oder Verkürzung der Wiederherstellungsdauer bei eingetretener Latenz gibt es mehrere Strategien:

* **Informieren Sie Adobe über erwartete Traffic-Spitzen:** Es ist zwar nicht möglich, jede Traffic-Spitze Ihrer Site vorherzusehen, es kann jedoch vorkommen, dass Sie einen erheblichen Traffic-Anstieg erwarten. Beispiele hierfür sind eine besonders erfolgreiche Urlaubszeit oder kurz nach einem großen Campaign-Push. In diesen Situationen stellt Adobe eine Möglichkeit bereit, wie Ihre Firma uns über erwartete Trafficzunahmen informieren kann, damit wir Ihrer Report Suite zusätzliche Verarbeitungsressourcen zuweisen können. Weitere Informationen zur Benachrichtigung von Adobe über erhöhten Traffic finden Sie unter Traffic-Spitzen [planen](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) im Admin-Benutzerhandbuch.
* **Berücksichtigen Sie beim Aktivieren neuer Funktionen die Verarbeitungslast:** Einige Funktionen sind verarbeitungsintensiver als andere. Je mehr Funktionen für eine Report Suite aktiviert sind, desto schwieriger ist die Wiederherstellung des normalen Betriebs nach dem Auftreten von Latenzzeiten. Beachten Sie beim Aktivieren von Funktionen für eine Report Suite, dass die folgenden Funktionen die zu verarbeitende Datenmenge vergrößern:

   * Implementieren von mehr als 20 Ereignissen auf derselben Seite
   * Komplexe VISTA-Regeln
   * Mehr als 20 Werte in der Variable products
   * Ereignis-Serialisierung

* Enable IAB Bot filtering: [Bot filtering](/help/admin/admin/bot-removal/bot-removal.md) can greatly reduce latency if your report suite is frequented by bots or crawlers. Verwenden Sie die IAB-Botliste, da diese vom [Interactive Advertising Bureau](https://www.iab.net/about_the_iab) aktualisiert und gewartet wird. Ein Benutzer kann seine eigenen Bot-Regeln anpassen, um die vom IAB zu ergänzen.

## Verfahren bei Latenzzeit

Wenn Latenzzeiten auftreten, stellen Sie sicher, dass Adobe die Verarbeitungspipeline proaktiv überwacht und alles in seiner Macht Stehende tut, um die Verarbeitungszeit so schnell wie möglich wieder auf den Normalzustand zurückzusetzen. Viele Latenzprobleme können innerhalb von Stunden behoben werden. Wenn Sie Fragen zu einer bestimmten Report Suite haben, kann sich ein unterstützter Benutzer Ihrer Firma mit der Report-Suite-ID, bei der Latenzzeiten auftreten, an den Kundendienst wenden. Der Adobe-Support-Mitarbeiter kann die Latenzzeit überprüfen und Sie über den Fortschritt und die Behebung des Problems informieren.
