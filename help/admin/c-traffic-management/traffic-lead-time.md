---
description: Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenz sowie mögliche negative Auswirkungen auf das gesamte System zu minimieren.
title: Erforderliche Vorlaufzeit für Traffic-Zunahme
topic: Admin tools
uuid: aa3fb882-51b0-458f-917b-7c54d5659623
translation-type: tm+mt
source-git-commit: a114bef4679da24d4fd6323a55c9ccf52ac772ed
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 100%

---


# Erforderliche Vorlaufzeit für Traffic-Zunahme

Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenz sowie mögliche negative Auswirkungen auf das gesamte System zu minimieren.

Die Zuordnung von Hardware wird durch Warnhinweise gesteuert, die über die Benutzeroberfläche für Reports &amp; Analytics übermittelt werden.

>[!IMPORTANT]
>
>Adobe kann keine Traffic-Änderungsanforderungen für „Platzhalter“ berücksichtigen. Sofern nicht anders angegeben, halten Sie die vorgeschlagene Vorlaufzeit so gut wie möglich ein. Senden Sie wenn möglich auch keinen Warnhinweis zu früh. Siehe [Planen von Traffic-Spitzen](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) oder [Angeben einer dauerhaften Traffic-Zunahme](/help/admin/c-traffic-management/t-traffic-permanent.md).

Ermitteln Sie anhand der folgenden Richtlinien, wie lange im Voraus Sie einen Verkehrswarnhinweis übermitteln müssen:

## Vorlaufzeiten Hardware-Zuordnung

<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> TÄGLICHE Traffic-Prognose (Treffer) </th>
   <th colname="col2" class="entry"> <p>Benötigte Vorlaufzeit (Januar–Oktober) </p> </th>
   <th colname="col3" class="entry"> <p>Benötigte Vorlaufzeit (November–Dezember) </p> </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> Bis zu 1,000,000 </td>
   <td colname="col2"> Keine Vorlaufzeit notwendig </td>
   <td colname="col3"> Keine Vorlaufzeit notwendig </td>
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

## Aufhebung der Hardware-Zuordnung aufgrund von nicht realisiertem Traffic

Die Hardware-Zuordnungen bei neuen Konten, Traffic-Spitzen und Traffic-Zunahmen werden aufgehoben, wenn sich die Traffic-Prognose im Client-Warnhinweis nicht binnen vier Wochen ab „Aufschaltdatum“ einstellt. Wenn der Traffic nach wie vor erwartet wird, muss ein neuer Client-Warnhinweis für eine Traffic-Zunahme erstellt werden.
