---
description: Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenzzeiten und mögliche negative Auswirkungen auf das Gesamtsystem zu minimieren.
title: Erforderliche Vorlaufzeit für Traffic-Zunahme
topic: Admin tools
uuid: aa3fb882-51b0-458f-917b-7c54d5659623
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Erforderliche Vorlaufzeit für Traffic-Zunahme

Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenzzeiten und mögliche negative Auswirkungen auf das Gesamtsystem zu minimieren.

Die Zuordnung von Hardware wird durch Warnhinweise gesteuert, die über die Benutzeroberfläche für Reports &amp; Analytics übermittelt werden.

>[!IMPORTANT] Adobe kann keine Traffic-Änderungsanforderungen für „Platzhalter“ berücksichtigen. Sofern nicht anders angegeben, halten Sie die vorgeschlagene Vorlaufzeit so gut wie möglich ein. Senden Sie wenn möglich auch keinen Warnhinweis zu früh. Siehe [Planen von Traffic-Spitzen](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) oder [Angeben einer dauerhaften Traffic-Zunahme](/help/admin/c-traffic-management/t-traffic-permanent.md).

Verwenden Sie die folgenden Richtlinien, um zu bestimmen, wie lange im Voraus Sie eine Traffic-Warnung senden müssen:

## Vorlaufzeiten für die Hardware-Zuordnung

<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> TÄGLICHE Traffic-Schätzungen (Treffer) </th>
   <th colname="col2" class="entry"> <p>Benötigte Vorlaufzeit (Januar–Oktober) </p> </th>
   <th colname="col3" class="entry"> <p>Benötigte Vorlaufzeit (November–Dezember) </p> </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> Bis zu 1.000.000 </td>
   <td colname="col2"> Keine Vorlaufzeit erforderlich </td>
   <td colname="col3"> Keine Vorlaufzeit erforderlich </td>
  </tr>
  <tr>
   <td colname="col1"> 1.000.000 - 5.000.000 </td>
   <td colname="col2"> Zwei WERKTAGE </td>
   <td colname="col3" morerows="3"> Traffic-Zunahmen für November–Dezember sollten bis zum 1. September eingereicht werden. Dies dient dazu, bei Bedarf Kapazitäten zu erwerben, um den Traffic während der Feiertage zu gewährleisten. </td>
  </tr>
  <tr>
   <td colname="col1"> 5.000.000 - 10.000.000 </td>
   <td colname="col2"> Eine Kalenderwoche </td>
  </tr>
  <tr>
   <td colname="col1"> 10.000.000 - 25.000.000 </td>
   <td colname="col2"> Zwei Kalenderwochen </td>
  </tr>
  <tr>
   <td colname="col1"> <p>über 25.000.000 </p> </td>
   <td colname="col2"> Ein oder mehrere Monate </td>
  </tr>
 </tbody>
</table>

Weitere Aspekte:

* Wenn Sie mehrere Report Suites starten oder erhöhen, die zu den oben aufgeführten Zahlen führen, gilt die Vorlaufzeit als Summe des für jeden von ihnen erwarteten Traffics.
* Halten Sie die folgenden Informationen bereit, um eine Traffic-Änderung zu senden:

   * Die Report Suite-ID
   * Geschätzte Treffer pro Tag
   * Aufschaltdatum

* Client-Warnhinweise sind auch erforderlich, wenn der Traffic abnimmt oder eine Report Suite nicht mehr unterstützt wird.

## Aufhebung der Hardware-Zuordnung aufgrund von nicht realisiertem Traffic

Die Hardware-Zuordnungen bei neuen Konten, Traffic-Spitzen und Traffic-Zunahmen werden aufgehoben, wenn sich die Traffic-Prognose im Client-Warnhinweis nicht binnen vier Wochen ab „Aufschaltdatum“ einstellt. Wenn der Traffic nach wie vor erwartet wird, muss ein neuer Client-Warnhinweis für eine Traffic-Zunahme erstellt werden.
