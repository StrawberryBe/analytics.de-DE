---
description: Die folgenden Informationen helfen bei der Behebung von Report Suite-Latenzproblemen in Analytics-Daten.
keywords: fehlende Daten; langsam
seo-description: Die folgenden Informationen helfen bei der Behebung von Report Suite-Latenzproblemen in Analytics-Daten.
seo-title: Datenverfügbarkeit und Latenz
solution: Analytics
subtopic: aktuelle Daten
title: Datenverfügbarkeit und Latenz
topic: 'Berichte    '
uuid: 1 f 0 e 67 e 3-6 cea -4 af 8-8 b 18-7 ae 9223 df 7 c 8
translation-type: tm+mt
source-git-commit: 1fdd14497171dbf5850ec1b1d873a06931d58435

---


# Datenverfügbarkeit und Latenz in Adobe Analytics

In der Regel werden vollständige Daten in Berichten 2 Stunden nach dem Erfassen der Daten angezeigt. Die folgenden Informationen helfen bei der Behebung von Report Suite-Latenzproblemen in Analytics-Daten.

## Datenstapelung

Jeder Datenerfassungsserver erfasst und verarbeitet Analyse-Rohdaten und lädt die Batch-Daten dann stündlich zur Berichterstellung hoch. Die Übertragung dauert in der Regel 30 Minuten. Die normale Latenz für Traffic direkt nach dem letzten Hochladen liegt daher bei etwa 90 Minuten (60 Minuten bis zum nächsten Batch-Upload und anschließend 30 Minuten für die Dateiübertragung und die Anzeige). Bei Traffic, der direkt vor einem Upload erfolgt, kann die Datenlatenz 30 Minuten (0 Minuten bis zum nächsten Batch-Upload, dann 30 Minuten für die Dateiübertragung und Anzeige) betragen.

Bei Bedarf kann der Adobe-Kundendienst 30-minütige Batch-Datenhochladevorgänge (anstatt stündlich) für Ihre am häufigsten verwendeten Report Suites aktivieren.

## Beitrag zur Latenz

Latenzzeiten sind eine Verzögerung, die länger als die normalen 2 Stunden dauert, bis Datenerfassungsserver Daten vollständig verarbeiten. Die Datenerfassung wirkt sich nicht auf die werden dennoch für eine funktionierende Implementierung erfasst, unabhängig davon, wie Latent eine Report Suite ist. Der Schweregrad (wie aktuell die Daten sind) und die Länge (die zur Auflösung benötigte Zeit) kann stark variieren. Sie ist normalerweise auf eine einzelne Report Suite beschränkt.

Latenzzeiten werden durch eine der folgenden allgemeinen Kategorien verursacht:

* **Unerwartete Traffic-Spitze:** Dieser Latenztyp tritt auf, wenn mehr Daten an eine Report Suite gesendet werden, als vertraglich übermittelt oder erwartet wurde. Dies ist die häufigste Ursache für Latenzzeiten.
* **Normale Hardwareprobleme:** Adobe setzt branchenführende Strategien für die Datencenter-Verwaltung und -überwachung, Datenredundanz und Hardwarezuverlässigkeit ein. Die Hardware wird regelmäßig und in Verbindung mit bekanntgegebenen Wartungsfenstern aktualisiert. Die Notfallwartung fehlgeschlagener Hardware kann einen vorübergehenden und vorübergehenden Stopp bei der Datenverarbeitung (nicht in der Datenerfassung) erfordern, da Ersatzhardware online gesendet wird. Dieser vorübergehende Stillstand bei der Verarbeitung kann zu einer merklichen Latenzzeit führen.
* **Anomale Daten:** Unnatürliche Datenmuster, wie ungewöhnlich lange Besuche, die von einem Bot oder Crawler verursacht werden, können bestimmte Verarbeitungslasten vorübergehend erhöhen, was zu Latenzzeiten führt.

## Funktionen, die von Latenzzeiten abhängig sind

Einige Funktionen in Adobe Experience Cloud erhalten eine Innenzeit von Latenzzeiten über der Standardmäßigen Verarbeitungszeit.

* Für Analytics für Target (A 4 T) sind zusätzliche Latenzzeiten von 5 bis 10 Minuten erforderlich, damit die gesammelten Daten beider Plattformen im selben Treffer gespeichert werden können.
* Daten mit Zeitstempel müssen aufgrund von verschiedenen Servern, auf denen diese Daten verarbeitet werden, zusätzliche Zeit benötigen. Treffer mit Zeitstempel, die in Echtzeit oder in Echtzeit empfangen werden, können bis zu 15 Minuten dauern. Treffer, die mit einem Zeitstempel von gestern empfangen wurden, können bis zu 2 Stunden dauern. Ältere Treffer können länger dauern, wobei jeder Tag bis zu ca. 24 Stunden erhöht wird.

## Möglichkeiten zur Vermeidung oder Vermeidung von Latenzzeiten

Zur Vermeidung von Latenzzeiten oder Verkürzung der Wiederherstellungsdauer bei eingetretener Latenz gibt es mehrere Strategien:

* **Informieren Sie Adobe über erwartete Traffic-Spitzen:** Es ist zwar unmöglich, jede Traffic-Spitze Ihrer Site vorherzusagen, es kann jedoch Fälle geben, in denen Sie eine bedeutende Steigerung des Traffics erwarten. Beispiele sind besonders erfolgreiche Feiertage oder kurz nach einem großen Kampagnenpush. In diesen Situationen stellt Adobe eine Möglichkeit bereit, wie Ihre Firma uns über erwartete Trafficzunahmen informieren kann, damit wir Ihrer Report Suite zusätzliche Verarbeitungsressourcen zuweisen können. See [Schedule a traffic spike](../admin/c-traffic-management/t-traffic-schedule-spike.md) in the Admin user guide to learn how to notify Adobe of increased traffic.
* **Berücksichtigen Sie beim Aktivieren neuer Funktionen die Verarbeitungslast:** Einige Funktionen sind verarbeitungsintensiver als andere. Je mehr Funktionen für eine Report Suite aktiviert sind, desto schwieriger ist die Wiederherstellung des normalen Betriebs nach dem Auftreten von Latenzzeiten. Beachten Sie beim Aktivieren von Funktionen für eine Report Suite, dass die folgenden Funktionen die zu verarbeitende Datenmenge vergrößern:

   * Implementieren von mehr als 20 Ereignissen auf derselben Seite
   * Komplexe VISTA-Regeln
   * Mehr als 20 Werte in der Variable products
   * Ereignis-Serialisierung

* Enable IAB Bot filtering: [Bot filtering](https://marketing.adobe.com/resources/help/en_US/admin/index.html?f=c_bot_rules) can greatly reduce latency if your report suite is frequented by bots or crawlers. Verwenden Sie die IAB-Botliste, da diese vom [Interactive Advertising Bureau](https://www.iab.net/about_the_iab) aktualisiert und gewartet wird. Ein Benutzer kann ihre eigenen Bot-Regeln anpassen, um diese mit dem IAB zu ergänzen.

## Verfahren bei Latenzzeit

In Fällen, in denen Latenzzeiten auftreten, können Sie sicher sein, dass Adobe die Verarbeitungspipeline proaktiv überwacht und alles daran setzt, so schnell wie möglich zur normalen Verarbeitung zurückzukehren. Viele Latenzprobleme können innerhalb von Stunden behoben werden. Wenn Sie Fragen zu einer bestimmten Report Suite haben, kann sich ein unterstützter Benutzer Ihrer Firma mit der Report-Suite-ID, bei der Latenzzeiten auftreten, an den Kundendienst wenden. Der Adobe-Support-Mitarbeiter kann die Latenzzeit überprüfen und Sie über den Fortschritt und die Behebung des Problems informieren.
