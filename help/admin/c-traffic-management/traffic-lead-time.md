---
description: Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenz sowie mögliche negative Auswirkungen auf das gesamte System zu minimieren.
seo-description: Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenz sowie mögliche negative Auswirkungen auf das gesamte System zu minimieren.
seo-title: Erforderliche Vorlaufzeit für Trafficzuwachs
solution: Analytics
title: Erforderliche Vorlaufzeit für Trafficzuwachs
topic: Admin Tools
uuid: aa3fb882-51b0-458f-917b-7c54d5659623
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Erforderliche Vorlaufzeit für Trafficzuwachs

Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenz sowie mögliche negative Auswirkungen auf das gesamte System zu minimieren.

Die Zuordnung von Hardware wird durch Warnmeldungen gesteuert, die über die Benutzeroberfläche für Reports &amp; Analytics übermittelt werden.

> [!IMPORTANT] Adobe kann Traffic-Änderungsanforderungen für "Platzhalter"nicht aufnehmen. Sofern nichts anderes angegeben ist, halten Sie die vorgeschlagene Vorlaufzeit so genau wie möglich ein, auch wenn Sie keine Warnung zu früh senden. Siehe Traffic-Spitze [planen](../../admin/c-traffic-management/t-traffic-schedule-spike.md) oder [Festlegen einer dauerhaften Traffic-Steigerung](../../admin/c-traffic-management/t-traffic-permanent.md).

Ermitteln Sie anhand der folgenden Richtlinien, wie lange im Voraus Sie einen Verkehrswarnhinweis übermitteln müssen:

## Vorlaufzeiten Hardware-Zuordnung

<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> TÄGLICHE Traffic-Prognose (Treffer) </th>
   <th colname="col2" class="entry"> <p>Benötigte Vorlaufzeit (Januar - Oktober) </p> </th>
   <th colname="col3" class="entry"> <p>Benötigte Vorlaufzeit (November - Dezember) </p> </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> Bis zu 1.000.000 </td>
   <td colname="col2"> Keine Vorlaufzeit notwendig </td>
   <td colname="col3"> Keine Vorlaufzeit notwendig </td>
  </tr>
  <tr>
   <td colname="col1"> 1,000,000 - 5,000,000 </td>
   <td colname="col2"> Zwei WERKTAGE </td>
   <td colname="col3" morerows="3"> Alle für November bis Dezember geplanten Traffic-Steigerungen sollten bis zum 1. September eingereicht werden. Dies dient dazu, bei Bedarf Kapazitäten zu erwerben, um den Datenverkehr während der Feiertage zu gewährleisten. </td>
  </tr>
  <tr>
   <td colname="col1"> 5,000,000 - 10,000,000 </td>
   <td colname="col2"> Eine Kalenderwoche </td>
  </tr>
  <tr>
   <td colname="col1"> 10,000,000 - 25,000,000 </td>
   <td colname="col2"> Zwei Kalenderwochen </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Über 25.000.000 </p> </td>
   <td colname="col2"> Ein Monat bzw. mehrere Monate </td>
  </tr>
 </tbody>
</table>

Was Sie außerdem noch beachten müssen:

* Wenn Sie mehrere Report Suites einrichten oder erweitern, sodass die oben aufgeführten Zahlen erreicht werden, gilt die Vorlaufzeit für den zusammengefassten Traffic für alle diese Report Suites.
* Um eine Traffic-Änderung zu übermitteln, benötigen Sie die folgenden Informationen:

   * Report Suite-ID
   * Geschätzte Trefferanzahl pro Tag
   * Aufschaltdatum

* Client-Warnhinweise werden auch benötigt, wenn der Datenverkehr nachlässt oder eine Report Suite veraltet ist.

## Aufhebung der Hardware-Zuordnung aufgrund von nicht realisiertem Datenverkehr

Hardware für neue Konten, Traffic-Spitzen und Traffic-Steigerungen werden entzogen, wenn der prognostizierte Traffic im Client-Warnhinweis nicht innerhalb von 4 Wochen nach dem "Aufschaltdatum"eintritt. Wenn der Traffic nach wie vor erwartet wird, muss ein neuer Client-Warnhinweis für eine Traffic-Zunahme erstellt werden.
