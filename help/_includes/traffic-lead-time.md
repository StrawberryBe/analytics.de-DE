---
description: Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenz sowie mögliche negative Auswirkungen auf das gesamte System zu minimieren.
title: Erforderliche Vorlaufzeit für Traffic-Zunahme
feature: Traffic Management
exl-id: fb428f8d-9dff-43a6-a1e8-1a892cbed7ac
source-git-commit: 55c8337dbeebcc76db367ead15128c095e4d8ce5
workflow-type: ht
source-wordcount: '337'
ht-degree: 100%

---

# Erforderliche Vorlaufzeit für Traffic-Zunahme

## Erforderliche Vorlaufzeit für Traffic-Zunahme

Adobe benötigt eine vorherige Benachrichtigung bei der Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Die Hardware muss vorab zugeordnet werden, um Latenz sowie mögliche negative Auswirkungen auf das gesamte System zu minimieren.

Die Zuordnung von Hardware wird durch Warnhinweise gesteuert, die über die Benutzeroberfläche für Reports &amp; Analytics übermittelt werden.

>[!IMPORTANT]
>
>Adobe kann keine Traffic-Änderungsanfragen für „Platzhalter“ berücksichtigen. Sofern nicht anders angegeben, halten Sie die vorgeschlagene Vorlaufzeit so gut wie möglich ein. Senden Sie wenn möglich auch keinen Warnhinweis zu früh.

Ermitteln Sie anhand der folgenden Richtlinien, wie lange im Voraus Sie einen Verkehrswarnhinweis übermitteln müssen:

### Vorlaufzeiten Hardware-Zuordnung


<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Typ der Traffic-Änderung </th>
   <th colname="col2" class="entry"> Benötigte Vorlaufzeit </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> Neue Kontoeinrichtung </td>
   <td colname="col2"> <ul><li>3 Werktage</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Traffic-Spitze oder plötzlicher permanenter Traffic-Anstieg von bis zu 25 % des durchschnittlichen täglichen Volumens im Vergleich zu den letzten 30 Tagen</td>
   <td colname="col2"> <ul><li>Report Suites mit &lt; 100 Mio. Treffern/Tag: Keine Benachrichtigung erforderlich</li><li>Report Suites mit &gt; 100 Mio Treffern/Tag: 5 Werktage</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Traffic-Spitze oder plötzlicher permanenter Traffic-Anstieg von mehr als 25 % des durchschnittlichen täglichen Volumens im Vergleich zu den letzten 30 Tagen</td>
   <td colname="col2"> <ul><li>5 Werktage</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Feiertagsereignisse Oktober – Dezember </td>
   <td colname="col2"> <ul><li>1 Kalendermonat</li></ul> </td>
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

### Aufhebung der Hardware-Zuordnung aufgrund von nicht realisiertem Traffic

Die Hardware-Zuordnungen bei neuen Konten, Traffic-Spitzen und Traffic-Zunahmen werden aufgehoben, wenn sich die Traffic-Prognose im Client-Warnhinweis nicht binnen vier Wochen ab „Aufschaltdatum“ einstellt. Wenn der Traffic nach wie vor erwartet wird, muss ein neuer Client-Warnhinweis für eine Traffic-Zunahme erstellt werden.
