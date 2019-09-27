---
description: Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.
seo-description: Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.
seo-title: Zeitstempel optional
solution: Analytics
title: Zeitstempel optional
topic: Admin Tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

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
>If you are using Timestamps Optional, then do not set [s.visitorID](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_custom.html) on data that is already timestamped. Diese Festlegung kann zu Unordnung in den Daten führen und sich negativ auf Zeitberechnungen (wie Besuchszeitwerte), die Zuordnung (eVar-Persistenz), Besuchnummer/Besuchsanzahl und Pfadsetzungsberichte auswirken.

>[!NOTE]
>
>Mit Zeitstempel versehene Daten werden bis zu 92 Tage gespeichert. Das bedeutet, dass ein Besuch/eine Sitzung 92 Tage lang "geöffnet"bleibt, während ein zusätzlicher Treffer - also nicht 30 Minuten nach dem vorherigen Treffer (in Trefferzeit) - weiterhin im selben Besuch/derselben Sitzung eingeschlossen werden kann. Any "old" hits that are received out of order will produce "unknown" results, since a number of factors (segmentation, allocation, expiration, etc.) Einfluss darauf, ob diese Treffer in die Berichterstellung einbezogen werden.

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

>[!NOTE]
>
>If a report suite was set to **Timestamps Optional**, to change this to any other setting, please contact Adobe Client Care.

