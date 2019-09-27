---
description: Die folgenden Informationen können bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten helfen.
keywords: fehlende Daten; langsam
seo-description: Die folgenden Informationen können bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten helfen.
seo-title: Datenverfügbarkeit und Latenz
solution: Analytics
subtopic: aktuelle Daten
title: Datenverfügbarkeit und Latenz
topic: Berichte
uuid: 1f0e67e3-6cea-4af8-8b18-7ae9223df7c8
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Datenverfügbarkeit und -latenz in Adobe Analytics

In der Regel werden 2 Stunden nach der Datenerfassung vollständige Daten in Berichten angezeigt. Die folgenden Informationen können bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten helfen.

## Grundlagen der Datenstapelung

Jeder Datenerfassungsserver erfasst und verarbeitet Analyse-Rohdaten und lädt die Batch-Daten dann stündlich zur Berichterstellung hoch. Die Übertragung dauert in der Regel 30 Minuten. Die normale Latenz für Traffic direkt nach dem letzten Hochladen liegt daher bei etwa 90 Minuten (60 Minuten bis zum nächsten Batch-Upload und anschließend 30 Minuten für die Dateiübertragung und die Anzeige). Bei Traffic, der direkt vor dem Hochladen erfolgt, kann die Datenlatenz bis zu 30 Minuten betragen (0 Minuten bis zum nächsten Batch-Upload und 30 Minuten für Dateiübertragung und -anzeige).

If needed, Adobe Customer Care can enable 30 minute batched data uploads (instead of hourly) for your most-used report suites.

## Contributors to latency

Latency is a delay that is longer than the typical 2 hours it takes for data collection servers to fully process data. Die Datenerfassung wird nicht beeinflusst. Daten werden weiterhin für eine funktionierende Implementierung erfasst, unabhängig davon, wie lange eine Report Suite latent ist. Its severity (how current the data is) and length (the time it takes to resolve) can vary greatly. Er ist normalerweise auf eine einzige Report Suite beschränkt.

Latenzzeiten werden durch eine der folgenden allgemeinen Kategorien verursacht:

* **** Unerwartete Traffic-Spitze: Diese Art von Latenz tritt auf, wenn mehr Daten an eine Report Suite gesendet werden, als vertraglich festgelegt oder erwartet wurde. Dies ist die häufigste Ursache für Latenzzeiten.
* **** Normale Hardwareprobleme: Adobe setzt erstklassige Strategien für die Verwaltung und Überwachung von Rechenzentren, Datenredundanz und Hardwarezuverlässigkeit ein. Die Hardware wird regelmäßig und in Verbindung mit bekanntgegebenen Wartungsfenstern aktualisiert. Die Notwartung von fehlerhaften Hardware kann eine zeitweilige Unterbrechung der Datenverarbeitung (nicht der Datenerfassung) erfordern, da Ersatzhardware online verfügbar gemacht wird. Dieser vorübergehende Stillstand bei der Verarbeitung kann zu einer merklichen Latenzzeit führen.
* **** Ungewöhnliche Daten: Unnatürliche Datenmuster wie ungewöhnlich lange Besuche, die von einem Bot oder Crawler verursacht werden, können zeitweise bestimmte Verarbeitungslasten erhöhen, die zu Latenzzeiten führen.

## Von Latenz abhängige Funktionen

Some capabilities in the Adobe Experience Cloud come with an innate amount of latency on top of standard processing time.

* Analytics for Target (A4T) requires an additional 5-10 minutes of latency to allow collected data from both platforms to be stored in the same hit.
* Timestamped data requires additional time due to different servers this data is processed on. Timestamped hits received at or near real-time can take up to 15 minutes. Hits received with a timestamp of yesterday can take up to 2 hours. Older hits can take longer, increasing each day up to a cap of approximately 24 hours.

## Möglichkeiten zur Verringerung oder Verhinderung von Latenzzeiten

Zur Vermeidung von Latenzzeiten oder Verkürzung der Wiederherstellungsdauer bei eingetretener Latenz gibt es mehrere Strategien:

* **** Notify Adobe of expected traffic spikes: While it is impossible to anticipate every traffic spike to your site, there may be cases where you are expecting to receive a significant increase in traffic. Examples include a particularly successful holiday period, or shortly after a large campaign push. In diesen Situationen stellt Adobe eine Möglichkeit bereit, wie Ihre Firma uns über erwartete Trafficzunahmen informieren kann, damit wir Ihrer Report Suite zusätzliche Verarbeitungsressourcen zuweisen können. See Schedule a traffic spike in the Admin user guide to learn how to notify Adobe of increased traffic.[](../admin/c-traffic-management/t-traffic-schedule-spike.md)
* **** Berücksichtigen Sie beim Aktivieren neuer Funktionen die Verarbeitungslast: Einige Funktionen sind verarbeitungsintensiver als andere. Je mehr Funktionen für eine Report Suite aktiviert sind, desto schwieriger ist die Wiederherstellung des normalen Betriebs nach dem Auftreten von Latenzzeiten. Beachten Sie beim Aktivieren von Funktionen für eine Report Suite, dass die folgenden Funktionen die zu verarbeitende Datenmenge vergrößern:

   * Implementing more than 20 events on the same page
   * Komplexe VISTA-Regeln
   * Mehr als 20 Werte in der Variable products
   * Ereignis-Serialisierung

* Enable IAB Bot filtering: [Bot filtering](https://marketing.adobe.com/resources/help/en_US/admin/c_bot_rules.html) can greatly reduce latency if your report suite is frequented by bots or crawlers. Verwenden Sie die IAB-Botliste, da diese vom [Interactive Advertising Bureau](https://www.iab.net/about_the_iab) aktualisiert und gewartet wird. A user can customize their own bot rules to complement those from the IAB.

## Verfahren bei Latenzzeit

In cases where latency occurs, rest assured that Adobe proactively monitors the processing pipeline and does everything possible to return processing time back to normal as quickly as possible. Viele Latenzprobleme können innerhalb von Stunden behoben werden. Wenn Sie Fragen zu einer bestimmten Report Suite haben, kann sich ein unterstützter Benutzer Ihrer Firma mit der Report-Suite-ID, bei der Latenzzeiten auftreten, an den Kundendienst wenden. Der Adobe-Support-Mitarbeiter kann die Latenzzeit überprüfen und Sie über den Fortschritt und die Behebung des Problems informieren.
