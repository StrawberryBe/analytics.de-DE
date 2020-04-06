---
description: Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.
title: Zeitstempel optional
topic: Admin tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Zeitstempel optional

Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.

Mit Zeitstempel optional können Sie:

* Mischen Sie Daten mit und ohne Zeitstempel in derselben globalen Report Suite.
* Senden von Daten mit Zeitstempel von einer mobilen App an eine globale Report Suite
* Aktualisieren Sie Apps, um die Offline-Verfolgung zu verwenden, ohne eine neue Report Suite erstellen zu müssen.

>[!IMPORTANT] Wenn Sie &quot;Zeitstempel optional&quot;verwenden, stellen Sie [s.visitorID](/help/implement/vars/config-vars/visitorid.md) nicht für Daten ein, die bereits mit einem Zeitstempel versehen sind. Diese Festlegung kann zu Unordnung in den Daten führen und sich negativ auf Zeitberechnungen (wie Besuchszeitwerte), die Zuordnung (eVar-Persistenz), Besuchsnummer/Besuchsanzahl und Pfadsetzungsberichte auswirken.

>[!NOTE] Mit Zeitstempel versehene Daten werden bis zu 92 Tage gespeichert. Das bedeutet, dass ein Besuch/eine Sitzung 92 Tage lang „offen gehalten“ wird, während jeder zusätzliche Hit – also keine 30 Minuten nach dem vorherigen Hit (in der Hit-Zeit) – noch in denselben Besuch/dieselbe Sitzung einbezogen werden kann. Alle „alten“ Hits, die nicht in Reihenfolge empfangen werden, führen zu „unbekannten“ Ergebnissen, da eine Reihe von Faktoren (Segmentierung, Zuordnung, Ablauf usw.) beeinflussen, ob diese Hits in die Berichterstellung einbezogen werden.

## Neue Report Suites {#section_095A7CFBD280494593B9BEC1592B73A6}

* Wenn eine neue Report Suite aus einer Vorlage erstellt wird, wird standardmäßig &quot;Zeitstempel optional&quot;verwendet.

   (Sie können eine neue Report Suite aus einer Vorlage unter **Admin > Report Suites > Neu erstellen > Report Suite** erstellen.)
* Wenn sie aus einer vorhandenen Report Suite kopiert wird, übernimmt die neue Report Suite die Zeitstempeleinstellung des Originals, einschließlich:

   * **Zeitstempel nicht zulässig** (Einstellung &quot;s.visitorID&quot;wird unterstützt)
   * **Zeitstempel erforderlich** (Einstellung s.visitorID wird nicht unterstützt)
   * **Zeitstempel optional** (Einstellung von s.visitorID unterstützt, jedoch nicht bei Treffern mit Zeitstempel)

## Änderung vorhandener Report Suites in „Zeitstempel optional“ {#section_40BCD3B4639241DEA716F7640ED33E72}

1. Gehen Sie zu **Admin > Report Suites > Einstellungen bearbeiten > Allgemein > Zeitstempelkonfiguration**.
1. Wählen Sie das Feld &quot;Ausgewählte Report Suites in optionale Zeitstempel **konvertieren&quot;** .

   Dadurch wird Ihre Report Suite in &quot;Zeitstempel optional&quot;geändert.

>[!NOTE] Wurde eine Report Suite auf **Zeitstempel optional** festgelegt, müssen Sie sich an die Adobe-Kundenunterstützung wenden, um diese oder andere Einstellungen zu ändern.

