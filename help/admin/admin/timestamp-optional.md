---
description: Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.
title: Zeitstempel optional
topic: Admin tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Zeitstempel optional

Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.

„Zeitstempel optional“ bietet folgende Möglichkeiten:

* Sie können auch Daten mit und Daten ohne Zeitstempel gemeinsam in einer globalen Report Suite verwenden.
* Senden Sie Daten mit Zeitstempel von einer mobilen App an eine globale Report Suite.
* Aktualisieren Sie Apps, um die Offline-Nachverfolgung zu verwenden, ohne eine neue Report Suite erstellen zu müssen.

Unter [Verwendung von „Zeitstempel optional“](/help/implement/js-implementation/timestamps-overview.md) finden Sie Best Practices für die Verwendung von Zeitstempeln in Ihrer Report Suite.

>[!IMPORTANT]
>
>Wenn Sie „Zeitstempel optional“ verwenden, dürfen Sie für bereits mit einem Zeitstempel versehene Daten [s.visitorID](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_custom.html) nicht festlegen. Diese Festlegung kann zu Unordnung in den Daten führen und sich negativ auf Zeitberechnungen (wie Besuchszeitwerte), die Zuordnung (eVar-Persistenz), Besuchsnummer/Besuchsanzahl und Pfadsetzungsberichte auswirken.

> [!NOTE] Mit Zeitstempel versehene Daten werden bis zu 92 Tage gespeichert. Das bedeutet, dass ein Besuch/eine Sitzung 92 Tage lang „offen gehalten“ wird, während jeder zusätzliche Hit – also keine 30 Minuten nach dem vorherigen Hit (in der Hit-Zeit) – noch in denselben Besuch/dieselbe Sitzung einbezogen werden kann. Alle „alten“ Hits, die nicht in Reihenfolge empfangen werden, führen zu „unbekannten“ Ergebnissen, da eine Reihe von Faktoren (Segmentierung, Zuordnung, Ablauf usw.) beeinflussen, ob diese Hits in die Berichterstellung einbezogen werden.

## Neue Report Suites {#section_095A7CFBD280494593B9BEC1592B73A6}

* Wenn sie aus einer Vorlage erstellt wird, gilt für eine neue Report Suite die Standardeinstellung „Zeitstempel optional“.

   (Sie können eine neue Report Suite über **Admin &gt; Report Suites &gt; Neu erstellen &gt; Report Suite** aus einer Vorlage erstellen.)
* Wenn sie aus einer vorhandenen Report Suite kopiert wird, erbt die neue Report Suite die Zeitstempeleinstellung des Originals, einschließlich:

   * **Keine Zeitstempel zulässig** (Einstellung „s.visitorID“ wird unterstützt)
   * **Zeitstempel erforderlich** (Einstellung „s.visitorID“ wird nicht unterstützt)
   * **Zeitstempel optional** (Einstellung „s.visitorID“ wird unterstützt, aber nicht für Zeitstempeltreffer)

## Änderung vorhandener Report Suites in „Zeitstempel optional“ {#section_40BCD3B4639241DEA716F7640ED33E72}

1. Wechseln Sie zu **Admin &gt; Report Suites &gt; Einstellungen bearbeiten &gt; Allgemein &gt; Zeitstempelkonfiguration**.
1. Aktivieren Sie **Ausgewählte Report Suites in „Zeitstempel optional“ konvertieren**.

   Damit wird die Report Suite in „Zeitstempel optional“ geändert.

> [!NOTE] Wurde eine Report Suite auf **Zeitstempel optional** festgelegt, müssen Sie sich an den Adobe-Kundendienst wenden, um diese oder andere Einstellungen zu ändern.

