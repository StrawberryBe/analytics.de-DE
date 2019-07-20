---
description: Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.
seo-description: Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.
seo-title: Zeitstempel optional
solution: Analytics
title: Zeitstempel optional
topic: Admin Tools
uuid: 0 fa 63658-1 cc 2-4 adc -8 d 51-a 0662 d 0 aa 941
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Zeitstempel optional

Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.

„Zeitstempel optional“ bietet folgende Möglichkeiten:

* Sie können auch Daten mit und Daten ohne Zeitstempel gemeinsam in einer globalen Report Suite verwenden.
* Senden Sie Daten mit Zeitstempel von einer mobilen App an eine globale Report Suite.
* Aktualisieren Sie Apps, um die Offline-Nachverfolgung zu verwenden, ohne eine neue Report Suite erstellen zu müssen.

Unter [Verwendung von „Zeitstempel optional“](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=timestamps-overview) finden Sie Best Practices für die Verwendung von Zeitstempeln in Ihrer Report Suite.

>[!IMPORTANT]
>
>If you are using Timestamps Optional, then do not set [s.visitorID](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_custom) on data that is already timestamped. Diese Festlegung kann zu Unordnung in den Daten führen und sich negativ auf Zeitberechnungen (wie Besuchszeitwerte), die Zuordnung (eVar-Persistenz), Besuchnummer/Besuchsanzahl und Pfadsetzungsberichte auswirken.

>[!NOTE]
>
>Mit Zeitstempel versehene Daten werden bis zu 92 Tage gespeichert.

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

