---
description: Eine Vergleichstabelle für die Berichterstellungs-APIs in Analytics. Links verweisen auf die zugehörige Dokumentation.
title: Vergleich der Analytics-Reporting-APIs
uuid: fa533a8e-33c0-42f4-a294-cabee0258c8f
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Vergleich der Analytics-Reporting-APIs

Eine Vergleichstabelle für die Berichterstellungs-APIs in Analytics. Links verweisen auf die zugehörige Dokumentation.

>[!NOTE] Bezüglich der Latenz werden in Analytics für Target (A4T) die Daten für den gleichen Treffer aus Analytics und Target für eine integrierte Berichterstellung miteinander kombiniert. Da Analytics- und Target-Aufrufe zu unterschiedlichen Zeitpunkten stattfinden, werden Treffer vor der Verarbeitung gespeichert, um Daten aus beiden Lösungen zu sammeln. Durch diesen Prozess entsteht für alle Checkpoints eine **zusätzliche Latenz von 7 bis 10 Minuten**.

<table id="table_7AF4FD678D494063ADF459B3CBC3EF3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> API-Typ </th> 
   <th colname="col2" class="entry"> Vollständig verarbeitet </th> 
   <th colname="col3" class="entry"> Echtzeit </th> 
   <th colname="col4" class="entry"> Livestream </th> 
   <th colname="col5" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Beschreibung</b> </td> 
   <td colname="col2"> Vollständig verarbeitete, finale Daten, die für alle Analytics-Schnittstellen zur Verfügung stehen. </td> 
   <td colname="col3"> Teilweise verarbeitete, beschränkte Metriken, die innerhalb von Sekunden nach der Erfassung verfügbar sind. </td> 
   <td colname="col4"> Teilweise verarbeitete Trefferdaten, die innerhalb von Sekunden nach der Erfassung verfügbar sind. </td> 
   <td colname="col5"> Vollständig verarbeitete, finale Daten, die als Grundlage für umfangreiche Datenexporte dienen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://docs.adobe.com/content/help/en/analytics/technotes/latency.html"  > Latenz</a> </p> </td> 
   <td colname="col2"> 30–90 Minuten </td> 
   <td colname="col3"> * Sekunden – 10 Minuten </td> 
   <td colname="col4"> Sekunden – 10 Minuten </td> 
   <td colname="col5"> 90 Minuten + </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Abschluss der Verarbeitung</b> </td> 
   <td colname="col2"> „Voll“ </td> 
   <td colname="col3"> Teilweise </td> 
   <td colname="col4"> Teilweise </td> 
   <td colname="col5"> „Voll“ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="https://docs.adobe.com/content/help/de-DE/analytics/landing/home.html"  > Berichtsschnittstellen</a> </td> 
   <td colname="col2"> Reports &amp; Analytics, Report Builder, API </td> 
   <td colname="col3"> Echtzeitberichte in Reports &amp; Analytics, Report Builder, API </td> 
   <td colname="col4"> Nur API </td> 
   <td colname="col5"> Data Warehouse und API </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Datengranularität</b> </td> 
   <td colname="col2"> Zusammenfassung </td> 
   <td colname="col3"> Zusammenfassung </td> 
   <td colname="col4"> Trefferebene </td> 
   <td colname="col5"> Zusammenfassung </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verarbeitung von Besucherprofilen</b> </td> 
   <td colname="col2"> Ja </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Nein </td> 
   <td colname="col5"> Ja  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Unterstützung von Segmenten</b> </td> 
   <td colname="col2"> Ja </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Nein </td> 
   <td colname="col5"> Ja (jedoch nur mit Data Warehouse kompatible Segmente) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Analytics-SKU</b> </td> 
   <td colname="col2"> Standard+ </td> 
   <td colname="col3"> Standard+ </td> 
   <td colname="col4"> Premium Complete oder Predictive Intelligence </td> 
   <td colname="col5"> Standard+ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Dokumentation</b> </td> 
   <td colname="col2"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-reporting-1-4/get-started%E2%80%8B"  > Web-Services</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-reporting-1-4/real-time"  > Echtzeitberichte</a> </p> </td> 
   <td colname="col4"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-live-stream/overview-1%E2%80%8B"  > Livestream-Übersicht</a> </p> </td> 
   <td colname="col5"> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/export/data-warehouse/data-warehouse.html"  > Data Warehouse</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verwandte Hilfe**

* [Adobe/IO](https://www.adobe.io/) – Eine umfassende Quelle technischer Dokumentation und Tools für die Integration von Adobe-Technologien in Ihre Anwendungen.
* [Data Workbench-Abfrage-API](https://marketing.adobe.com/developer/documentation/data-workbench-query-api/c-ins-qry-api)

